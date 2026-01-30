# VAT‑ID Attestation (Chapter 1.4) – Non‑expert description + technical schema references

This document explains, in plain language, what the **VAT‑ID Attestation** contains (based on **Chapter 1.4 / Table 1** of the specification), and how those “standalone attributes” are implemented as **Classes and Properties** in the **SHACL Shape**.

It is intended for:
- **Policy / rulebook writers** who need a clear description of the attestation content
- **Wallet / verifier implementers** who need a practical schema reference
- **SD‑JWT VC implementers** who need a machine‑readable definition to validate and selectively disclose claims

---

## 1. What is a VAT‑ID Attestation (in one paragraph)?

A **VAT‑ID Attestation** is a digital proof issued by an authentic source (typically a **Tax Administration**) that confirms:

1) **Which VAT‑ID** belongs to a business (or to an administrative unit of the business)  
2) **When the VAT‑ID is/was valid** (validity period)

The attestation is meant to remove the need for manual checks (e.g., looking up VAT numbers in VIES or requesting paper certificates), because the relying party can trust the attested data as coming from an authentic source.

---

## 2. Conceptual model (simple explanation)

The **VAT‑ID** is registered by a **Tax Administration** for an **Administrative Unit** of an **Economic Operator** (the business).

- One **Economic Operator** (business) can have **multiple Administrative Units**
- One **Administrative Unit** can have **one VAT‑ID**
- One **Economic Operator** can therefore have **multiple VAT‑ID attestations**

This specification focuses on **one VAT‑ID attestation = one Administrative Unit record**.

---

## 3. Attribute groups (from Chapter 1.4)

Chapter 1.4 defines the attributes in a structured way:

1) **Administrative Unit Object** (main subject of the attestation)  
2) **Economic Operator** (the legal entity / sole trader the VAT‑ID belongs to)  
3) **Validity Period object** (start date + optional end date)  
4) **Address object** (optional address fields)  
5) **Economic Activity Type** (optional classification codes such as NACE)

> **Note on “mandatory”:** Mandatory means the *issuer must ensure it exists in the attestation*.  
> It does not automatically mean the relying party must request it, or that the holder must always disclose it.

---

## 4. Mapping: Word “attributes” → SHACL Classes and Properties

This section tells you how the Word‑based attribute list is implemented in the SHACL Shape.

### 4.1 Administrative Unit Object (main content)

| Chapter 1.4 Attribute | Meaning (non‑expert) | Optionality | SHACL Node / Property (implementation) |
|---|---|---:|---|
| `VAT_ID` | The full VAT number including country prefix (e.g., `FI09427182`) | [1..1] | **AdministrativeUnit** → `hasIdentifier` → **Identifier.notation** |
| `Administrative_Unit_Name` | Human readable name of the VAT registration record | [1..1] | **AdministrativeUnit** → `name` *(string)* |
| `Administrative_Unit_Type` | What kind of unit this is (VAT registration type/level) | [1..1] | **AdministrativeUnit** → `level` *(string)* |
| `Administrative_Unit_Address` | Address from the VAT authentic source | [0..1] | **AdministrativeUnit** → `registeredAddress` → **Address** |
| `Validity_Area_Limitation` | Country where VAT‑ID may be used (omit if no limitation) | [0..n] | **AdministrativeUnit** → `geographicIdentifier` *(ISO 3166‑1 code list)* |
| `Validity_Period` | One or more time periods when VAT‑ID was valid | [1..n] | **AdministrativeUnit** → `validityPeriod` → **PeriodOfTime** |
| `Economic_Activity_Type` | Optional activity classifications (e.g., NACE code) | [0..n] | **AdministrativeUnit** → `hasActivity` → **EconomicActivityType** |
| `Economic_Operator` | Reference to the business that owns this VAT‑ID | [1..1] | **AdministrativeUnit** → `subOrganizationOf` → **LegalEntity** |
| `Issuer` | Authentic source of VAT‑ID (NOT the VC issuer) | [1..1] | **Not in credentialSubject schema** (see section 5) |

---

### 4.2 Economic Operator (Legal Entity / Sole Trader)

| Chapter 1.4 Attribute | Meaning | Optionality | SHACL Node / Property |
|---|---|---:|---|
| `EUID` | Legal entity identifier (BRIS style) | [0..1] | **LegalEntity** → `legalIdentifier` → **Identifier.notation** |
| `PID` | Person identifier for sole traders | [0..1] | **LegalEntity** → `pid` *(string)* or a Person identifier node |
| `Economic_Operator_Name` | Name of the legal entity / sole trader | [0..1] | **LegalEntity** → `legalName` *(string)* |

---

### 4.3 Validity Period object

| Chapter 1.4 Attribute | Meaning | Optionality | SHACL Node / Property |
|---|---|---:|---|
| `VAT_ID_start_date` | VAT registration start date | [1..1] | **PeriodOfTime** → `startDate` *(xsd:date)* |
| `VAT_ID_end_date` | VAT registration end date (omit if unknown) | [0..1] | **PeriodOfTime** → `endDate` *(xsd:date)* |

---

### 4.4 Address object

Address fields use the Core Location vocabulary pattern.

| Chapter 1.4 Attribute | Optionality | SHACL Node / Property |
|---|---:|---|
| `po_box` | [0..1] | **Address** → `poBox` |
| `thoroughfare` | [0..1] | **Address** → `thoroughfare` |
| `location_designator` | [0..1] | **Address** → `locatorDesignator` |
| `post_code` | [0..1] | **Address** → `postCode` |
| `post_name` | [0..1] | **Address** → `postName` |
| `admin_unit_L1` | [0..1] | **Address** → `adminUnitLevel1` |
| `admin_unit_L2` | [0..1] | **Address** → `adminUnitLevel2` |

---

### 4.5 Economic Activity Type object

| Chapter 1.4 Attribute | Meaning | Optionality | SHACL Node / Property |
|---|---|---:|---|
| `Economic_Activity_Type_Nomenclature` | Which code system is used (e.g. `NACE`) | [1..1] | **EconomicActivityType** → `nomenclature` *(string)* |
| `Economic_Activity_Type_ID` | The classification code (e.g. `2822`) | [1..1] | **EconomicActivityType** → `codeValue` *(string)* |
| `Economic_Activity_Type_Description` | Human readable description | [0..1] | **EconomicActivityType** → `description` *(langString or object)* |

---

## 5. Important note: “Issuer” vs “Credential issuer”

Chapter 1.4 includes an **Issuer Object**, meaning:

> the authentic source of the VAT‑ID (Tax Administration)

However, for verifiable credential implementations (especially SD‑JWT VC), it is important to distinguish:

### 5.1 Credential issuer (technical signing entity)
This is represented in the **SD‑JWT/JWT envelope**, for example:
- `iss` (JWT issuer)
- `iat` (issuance time)
- `exp` (expiration, optional)

### 5.2 Authentic source of the VAT‑ID (domain meaning)
This is part of the *business meaning*, but for your modelling direction it should **not be inside `credentialSubject`**.

Recommended approaches:
- Put authentic-source references in **credential metadata** (outside subject)
- Or reference a separate “source authority attestation”

✅ Outcome: your **credential subject schema remains clean** and only carries *VAT‑ID facts*, while “who signed it” stays in the envelope.

---

## 6. Code lists (from Chapter 1.4)

These lists constrain how values should look:

- **EUID**: BRIS structure (country + register identifier + registration number + optional verification digit)
- **VAT‑ID**: ISO 3166‑1 country code + national VAT number, **no spaces, no hyphens**
- **Validity area limitation**: ISO 3166‑1 country code
- **Language**: ISO 639‑1 code

---

## 7. Integrity rules (from Chapter 1.4)

These are the main consistency rules:

- `VAT_ID_end_date` MUST be >= `VAT_ID_start_date`
- Validity periods MUST NOT overlap
- Validity periods older than 5 years SHOULD be omitted
- VAT‑ID must have at least one validity period
- If there is a NACE equivalent, nomenclature MUST be NACE
- Economic Activity Type Description SHOULD be provided in as many languages as possible

> These rules are often **issuer-side validation rules**.  
> Some can also be expressed as SHACL constraints (especially start/end date ordering).

---

## 8. What technical implementers can download (formats)

To support both semantic modelling and SD‑JWT implementations, the VAT‑ID Attestation schema can be distributed in multiple formats:

### 8.1 For semantic implementers (Linked Data / SHACL)
- **SHACL Shape (Turtle)** – primary normative schema for RDF-based modelling  
- **OWL vocabulary (Turtle)** – the reusable business vocabulary

### 8.2 For JSON / SD‑JWT implementers
- **JSON Schema** – a direct validation schema for claim sets used in SD‑JWT payloads
- **Example JSON instance** – test vector for implementers
- **SD‑JWT VC test vector** – example credential + example disclosures + example KB-JWT

### 8.3 For rulebooks and human review
- This **Markdown** description
- A one-page “attestation profile” summary (claim list + mandatory/optional)

---

## 9. Minimal SD‑JWT VC claim mapping (informative)

Even though the SHACL/JSON Schema focuses on the **subject data**, an SD‑JWT VC also has envelope claims:

### 9.1 JWT / SD‑JWT envelope (outside subject schema)
- `iss` (issuer DID/URI)
- `iat` (issued at)
- `exp` (optional)
- `vct` (credential type identifier)
- `cnf` (holder key binding, if used)
- `_sd_alg`, `_sd` (selective disclosure mechanics)

### 9.2 Subject claims (validated by the SHACL/JSON schema)
- `legalEntity` object  
- `administrativeUnit` object  
- VAT identifier + validity periods + optional address and activity types

---

## 10. Short example (human‑readable)

**Business:** Konecranes Oyj  
**VAT‑ID:** FI09427182  
**Valid from:** 2010‑01‑01  
**Valid in:** Finland (FI)  
**Address (optional):** Keilaranta 13 B, Espoo  
**Activity (optional):** NACE 2822

A relying party can accept the VAT‑ID Attestation as proof of VAT registration without separately checking VIES.

---

**End of document**
