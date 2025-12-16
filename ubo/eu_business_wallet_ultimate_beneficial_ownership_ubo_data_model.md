# EU Business Wallet – Ultimate Beneficial Ownership (UBO) Data Model

*Non‑expert, user‑friendly overview*

This document explains, in plain language, the **data model behind an “Ultimate Beneficial Ownership (UBO) attestation”** intended for use with **EU Business Wallets**.  

It is designed to be:
- understandable for **policy makers, register experts, product owners and developers**, not only semantic‑web specialists;
- aligned with **EU beneficial ownership register (BORIS) practices**;
- **grounded in the Nordic Core Business Vocabulary (NCBV)** as the semantic foundation;
- explicit about **what already exists in NCBV** and **what needs to be added** to fully cover UBO information needs.

The document ends with a **complete plain‑JSON example** that illustrates how all parts fit together in practice.

---

## 1. What is a UBO attestation in an EU Business Wallet context?

A **UBO attestation** is a **digitally signed statement** issued by a trusted authority (typically a business register) that answers the question:

> *“Who ultimately owns or controls this company, and on what basis?”*

In an EU Business Wallet, such an attestation should:
- identify the **company** (legal entity);
- list one or more **beneficial owners** (always natural persons);
- describe the **nature and extent of their ownership or control**;
- indicate **whether ownership/control is direct or indirect**;
- provide **dates, provenance, and verification context**;
- be suitable for **selective disclosure** (only show what the relying party needs).

---

## 2. Conceptual model (high level)

At a conceptual level, the model follows a simple and intuitive pattern:

1. **Legal Entity**  
   The company or other legal entity that is subject to UBO transparency obligations.

2. **Person**  
   A natural person who is an ultimate beneficial owner.

3. **Beneficial Ownership Relationship**  
   A relationship that links a person to the legal entity and explains *how* and *to what extent* the person owns or controls it.

This mirrors how UBO information is understood in EU legislation and business‑register practice, and is consistent with BORIS and Open Ownership thinking — but implemented here using **NCBV concepts**.

---

## 3. Existing NCBV classes and properties (reused as‑is)

The following elements **already exist in the Nordic Core Business Vocabulary (NCBV)** and are reused directly.  
In NCBV they are defined in OWL with largely literal‑typed properties; precise datatypes and constraints are expected to be defined later in **SHACL shapes**.

### 3.1 Core classes

#### `ncbv:LegalEntity`
Represents the company or other legal entity whose beneficial owners are being declared.

Typical meaning in this context:
- the subject of the UBO attestation;
- identified by national registration number, LEI, VAT number, etc.

---

#### `ncbv:Person`
Represents a natural person.

In a UBO context:
- every ultimate beneficial owner is a `Person`;
- identification details are attached to this person node.

---

#### `ncbv:BeneficialOwner`
Represents the **beneficial ownership relationship**.

This is a crucial design choice:  
NCBV models beneficial ownership **as a relationship object**, not just as a direct link between a company and a person.

---

### 3.2 Core NCBV properties used for UBO

The following NCBV properties are central and reused without redefining their meaning:

- `ncbv:beneficialOwners`  
  *Links a legal entity to one or more beneficial ownership relationship objects.*

- `ncbv:isPerson`  
  *Links a `ncbv:BeneficialOwner` relationship to the `ncbv:Person` who is the beneficial owner.*

- `ncbv:interestType`  
  *Describes the type of interest (e.g. ownership, control, voting rights).*

- `ncbv:interestControl`  
  *Describes the extent or form of control (e.g. percentage, appointment rights).*

- `ncbv:interestDirectOrIndirect`  
  *Indicates whether the interest is direct or indirect.*

- `ncbv:startDate` / `ncbv:endDate`  
  *Temporal validity of the beneficial ownership relationship.*

These properties are intentionally literal‑based in NCBV; SHACL shapes will later restrict allowed values, formats, and code lists.

---

## 4. Additional classes and properties proposed for NCBV (UBO coverage gaps)

While NCBV provides a solid semantic core, **real‑world UBO use cases and BORIS‑style exchanges require additional structure**.  
The following elements are **not currently present in NCBV** and are proposed as extensions or companion vocabularies.

### 4.1 Attestation‑level concepts

**Proposed additions:**

- `UBOAttestation` (class)
  - Represents a complete beneficial ownership statement issued by an authority.
  - Allows versioning, issuance dates, expiry, and revocation handling.

- `issuer`, `issuanceDate`, `effectiveDate`, `asOfDate`, `expiryDate`
  - Required to assess trust, timeliness, and legal relevance of the data.

---

### 4.2 Entity profile details (beyond bare identity)

**Proposed additions:**

- `EntityProfile`
  - Legal name
  - Register name and authority
  - Jurisdiction
  - Legal form
  - Entity status (active, dissolved, etc.)

These elements are commonly exchanged via BORIS and are needed to make sense of a UBO record outside the issuing country.

---

### 4.3 Person identification and screening

**Proposed additions:**

- `IdentificationDocument`
  - Document type (passport, ID card)
  - Issuing country

- `PersonAddress` (with address type: residential / service)

- `PEPAndSanctionsScreening`
  - PEP status
  - Sanctions status
  - Screening timestamp and provider

These are not part of the *core* NCBV model but are often required by obliged entities relying on UBO information.

---

### 4.4 Detailed interest description

**Proposed additions:**

- `interestDetails`
  - Nature of interest (shareholding, voting rights, appointment rights, other control)
  - Extent of interest (percentage, description, confidence)
  - Acquisition event

This complements the existing NCBV literal properties and aligns with how beneficial interests are described in EU registers.

---

### 4.5 Indirect ownership chains

**Proposed additions:**

- `IntermediaryEntity`
  - Used when ownership/control is indirect
  - Captures holding companies or other intermediate entities

This allows the model to truly represent *ultimate* beneficial ownership, not only immediate relationships.

---

### 4.6 Filing, evidence, and verification

**Proposed additions:**

- `RegisterFiling`
  - Filing reference
  - Filing date
  - Declarant role and capacity

- `EvidenceDocument`
  - Hash‑based reference to supporting documents

- `VerificationStatus`
  - Recorded / verified / partially verified
  - Verification method and timestamp

These elements are essential to assess **data quality and legal reliability**, especially in cross‑border reuse.

---

## 5. How this fits BORIS and EU practice (in simple terms)

From a non‑technical perspective:

- **NCBV provides the shared vocabulary** for *what* things are (company, person, beneficial owner, interest).
- **BORIS defines how national registers exchange those things** across borders.
- **EU Business Wallets define how those things are presented and shared** between companies, authorities, and obliged entities.

This UBO data model sits exactly at that intersection.

---

## 6. Complete plain‑JSON example

The following example shows a **full UBO attestation** using:
- NCBV classes and properties for the core semantics;
- additional proposed elements for completeness and real‑world usability.

```json
{
  "attestationType": "UBOAttestation",
  "attestationVersion": "1.0",
  "attestationId": "urn:uuid:2f5e4b7e-7a7a-4c9e-9fcb-1f9c3a98b3a1",

  "issuer": {
    "issuerName": "Finnish Trade Register / PRH",
    "issuerCountry": "FI",
    "issuerAuthorityType": "BusinessRegister",
    "issuerDid": "did:web:prh.fi"
  },

  "issuance": {
    "issuanceDateTime": "2025-12-16T07:10:00Z",
    "asOfDateTime": "2025-12-15T23:59:59Z",
    "expiryDateTime": "2026-03-16T23:59:59Z"
  },

  "credentialSubject": {
    "ncbv:LegalEntity": {
      "id": "did:ebw:company:FI:1234567-8",

      "entityProfile": {
        "legalName": "Example Timber Export Oy",
        "nationalRegistrationNumber": "1234567-8",
        "registerName": "Finnish Trade Register",
        "jurisdiction": "FI"
      },

      "ncbv:beneficialOwners": [
        {
          "type": "ncbv:BeneficialOwner",

          "ncbv:isPerson": {
            "personId": "did:ebw:person:FI:ubo:001",
            "fullName": "Anna Example",
            "dateOfBirth": "1980-06-12",
            "nationality": "FI"
          },

          "ncbv:interestType": "ownership",
          "ncbv:interestControl": "40%",
          "ncbv:interestDirectOrIndirect": "indirect",

          "interestDetails": {
            "interestNature": ["shareholding", "votingRights"],
            "interestExtent": "40%",
            "startDate": "2022-01-10"
          }
        }
      ]
    }
  }
}
```

*(The JSON example is intentionally verbose to be illustrative; real wallet presentations would use selective disclosure.)*

---

## 7. Summary for non‑experts

- You do **not** need to understand OWL, RDF, or SHACL to use this model.
- Think in terms of:
  - **Company** → **Person(s)** → **Ownership / Control explanation**.
- NCBV already covers the **core meaning**.
- A small, well‑defined set of **extensions** is needed to support UBO obligations, BORIS exchange, and EU Business Wallet usage.

This makes the model both **legally grounded** and **future‑proof** for digital, cross‑border business processes.

