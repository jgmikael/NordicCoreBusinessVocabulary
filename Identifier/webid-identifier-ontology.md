# 🧩 WEBID Ontology — Class: `webid:Identifier`

**Namespace:** [`https://iri.suomi.fi/model/webid/`](https://iri.suomi.fi/model/webid/)  
**Ontology Type:** OWL Ontology (RDF/XML or TTL serialisation)  
**Purpose:** A reusable model for representing and describing **identifiers**, their assignment, issuing authority, scheme, validity, and resolution mechanics.

---

## 📘 Overview

The `webid:Identifier` class represents an identifiable string, code, or URI assigned to an entity or object within a given scheme or namespace.

It captures not only the *notation* (literal identifier value) but also related metadata such as the **scheme**, **issuer**, **assignment date**, **validity period**, and optional resolution instructions (method, resolver, dereferencing parameters).

The ontology aligns conceptually with [ADMS:Identifier](https://www.w3.org/TR/vocab-adms/#identifier) and is designed to be specialized by **SHACL Shapes** for concrete identifier types (e.g., EUID, LEI, VAT, EORI, Y-tunnus).

---

## 🧠 Class Definition

| Element | Value |
|----------|--------|
| **IRI** | [`https://iri.suomi.fi/model/webid/Identifier`](https://iri.suomi.fi/model/webid/Identifier) |
| **Type** | `owl:Class` |
| **Label** | **Identifier** |
| **Comment** | “A node representing an assigned identifier with potential metadata such as issuing authority, scheme, validity, and resolver information.” |
| **Intended Alignment** | `adms:Identifier` (not asserted in the ontology yet, but noted as intended equivalent or subclass) |

---

## 🏗️ Object Properties

| Property | Range | Description |
|-----------|--------|-------------|
| **`webid:issuer`** | `webid:Agent` | The agent (organization, register, or person) that **assigns or issues** the identifier. |
| **`webid:owner`** | `webid:Agent` | The current **holder or owner** of the identifier. |
| **`webid:scheme`** | `xsd:anyURI` *(or resource)* | Reference to the **identifier scheme** or namespace (e.g., EUID, LEI, VAT, etc.). |
| **`webid:resolver`** | `xsd:anyURI` *(or resource)* | A **resolver service** endpoint capable of resolving the identifier into information. |
| **`webid:status`** | `skos:Concept` | Indicates **lifecycle status** such as “active,” “retired,” or “superseded.” |
| **`webid:privacyPosture`** | `skos:Concept` | Describes **privacy level** (e.g., “public,” “restricted,” “confidential”). |
| **`webid:validityPeriod`** | `webid:PeriodOfTime` | The **interval of validity** of the identifier. *(Range placeholder — not yet explicitly defined in the RDF.)* |

---

## 🧩 Datatype Properties

| Property | Datatype | Description |
|-----------|-----------|-------------|
| **`webid:notation`** | `xsd:string` | The **literal identifier value**, such as “FI-PRH.1000000-4” or “5493001KJTIIGC8Y1R12.” |
| **`webid:uri`** | `xsd:anyURI` | A **concrete URI** representation of the identifier, often resolvable or dereferenceable. |
| **`webid:method`** | `xsd:string` | A **resolution or derivation method**, e.g. a DID method (`did:web`, `did:key`, `gleif`). |
| **`webid:dereferencingParameter`** | `xsd:string` | Optional **parameter** (query or fragment) used in dereferencing. |
| **`webid:assignmentDate`** | `xsd:dateTime` | The **date/time when the identifier was assigned**. Semantically aligned with `dct:issued`. |
| **`webid:validFrom`** | `xsd:dateTime` | Start of validity (alternative to `validityPeriod`). |
| **`webid:validThrough`** | `xsd:dateTime` | End of validity (alternative to `validityPeriod`). |

---

## ⏳ Period of Time (supporting class)

| Element | Value |
|----------|--------|
| **IRI** | [`https://iri.suomi.fi/model/webid/PeriodOfTime`](https://iri.suomi.fi/model/webid/PeriodOfTime) |
| **Type** | `owl:Class` |
| **Label** | Period of Time |
| **Description** | Represents the **interval** of validity or activity, consisting of a `startDate` and `endDate`. |

| Property | Datatype | Description |
|-----------|-----------|-------------|
| `webid:startDate` | `xsd:dateTime` | Start of the interval. |
| `webid:endDate` | `xsd:dateTime` | End of the interval. |

---

## 🧭 Ontological Design Notes

- The OWL model intentionally defines **all possible elements**, but **none are mandatory**.  
  → **Obligations and cardinalities are introduced in SHACL**, not in OWL.  
  This keeps the ontology reusable and non-conflicting across domains.

- The **Identifier** class may be specialized via SHACL Shapes such as:
  - `EUIDIdentifierShape` (for EU Company Identifier)
  - `LEIIdentifierShape` (for Legal Entity Identifier)
  - `VATIdentifierShape`, `EORIIdentifierShape`, `YtunnusIdentifierShape`

- The model’s separation between **Issuer**, **Owner**, and **Scheme** allows both public and private identifiers to be handled consistently (even those without resolvers).

---

## 🔗 Alignment and External References

| Concept | Reference |
|----------|------------|
| `adms:Identifier` | [W3C ADMS Vocabulary](https://www.w3.org/TR/vocab-adms/#identifier) |
| `dct:issued` | [Dublin Core Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) |
| `skos:Concept` | [W3C SKOS](https://www.w3.org/TR/skos-reference/) |
| `time:ProperInterval` *(alternative)* | [OWL-Time Ontology](https://www.w3.org/TR/owl-time/) |

---

## 📋 Example Instance (Turtle)

```turtle
@prefix webid: <https://iri.suomi.fi/model/webid/> .
@prefix xsd:   <http://www.w3.org/2001/XMLSchema#> .

ex:FI-PRH.1000000-4
  a webid:Identifier ;
  webid:notation "FI-PRH.1000000-4" ;
  webid:scheme <https://example.org/scheme/euid> ;
  webid:issuer <https://prh.fi> ;
  webid:owner <https://acme.example.org> ;
  webid:assignmentDate "2020-05-12T00:00:00Z"^^xsd:dateTime ;
  webid:uri <https://example.org/resolve/euid/FI-PRH.1000000-4> ;
  webid:status <https://example.org/concept/status/active> ;
  webid:validityPeriod [
      a webid:PeriodOfTime ;
      webid:startDate "2020-05-12T00:00:00Z"^^xsd:dateTime ;
      webid:endDate "2030-05-11T23:59:59Z"^^xsd:dateTime
  ] .
```

---

## 🧩 Visualization

```text
Identifier
 ├── notation : xsd:string
 ├── scheme : xsd:anyURI
 ├── uri : xsd:anyURI
 ├── issuer : Agent
 ├── owner : Agent
 ├── assignmentDate : xsd:dateTime
 ├── status : skos:Concept
 ├── privacyPosture : skos:Concept
 ├── resolver : xsd:anyURI
 ├── method : xsd:string
 ├── dereferencingParameter : xsd:string
 └── validityPeriod : PeriodOfTime
       ├── startDate : xsd:dateTime
       └── endDate   : xsd:dateTime
```

---

## 📄 Metadata

| Field | Value |
|--------|--------|
| **Ontology IRI** | `https://iri.suomi.fi/model/webid/` |
| **Prefix** | `webid:` |
| **Defined By** | Digital and Semantic Interoperability Model (Finland / EU Business Wallet context) |
| **Created** | 2025-10-13 |
| **Status** | Draft, version 0.1 |
| **License** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| **Editor / Contributor** | *Mikael af Hällström (Nordic Business Vocabulary / WE BUILD WP4)* |

---

## 🧾 Notes for Implementers

- Use this ontology as the **upper layer** of your identifier modeling stack.  
  Domain-specific SHACL profiles can enforce:
  - notation format (regex)
  - issuer pattern
  - valid scheme references
  - cardinalities (1..1 or 0..1)

- Ideal for use in:
  - **EUDI Wallet / EU Business Wallet** credentials
  - **Digital Product Passports**
  - **Trade document identifiers** (as per KTDDE)
  - **Public registers** (PRH, BRIS, GLEIF, Vero, Tulli)

---

*End of document*
