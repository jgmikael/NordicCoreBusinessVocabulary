# 🧩 WEBID Ontology — Class: `webid:Identifier`

**Namespace:** [`https://iri.suomi.fi/model/webid/`](https://iri.suomi.fi/model/webid/)  
**Ontology Type:** OWL Ontology (Turtle serialization)  
**Purpose:** A reusable, extensible model for representing and describing **identifiers**, their assignment, scheme, issuer, validity, and resolution mechanisms.

---

## 📘 Overview

The `webid:Identifier` class represents an identifiable string, code, or URI assigned to an entity or object within a given scheme or namespace.

It captures not only the literal identifier value (`webid:notation`) but also metadata such as the **scheme**, **issuer**, **assignment date**, **validity**, and optional **resolver** information.

The ontology aligns conceptually with [ADMS:Identifier](https://www.w3.org/TR/vocab-adms/#identifier) and follows the principle that the OWL model defines *all possible elements*, while **SHACL Shapes** specialize and restrict actual usage (e.g., LEI, EUID, VAT, EORI, Y-tunnus).

---

## 🧠 Class Definition

| Element | Value |
|----------|--------|
| **IRI** | [`https://iri.suomi.fi/model/webid/Identifier`](https://iri.suomi.fi/model/webid/Identifier) |
| **Type** | `owl:Class` |
| **Label** | **Identifier** |
| **Comment** | “A node representing an assigned identifier and associated metadata such as issuing authority, scheme, validity, and resolver information.” |
| **Alignment** | Intentionally compatible with `adms:Identifier` |

---

## 🏗️ Object Properties

| Property | Range | Description |
|-----------|--------|-------------|
| **`webid:issuer`** | `webid:Agent` | The agent (organization, register, or person) that **assigns or issues** the identifier. |
| **`webid:owner`** | `webid:Agent` | The **holder or owner** of the identifier. |
| **`webid:scheme`** | `rdfs:Resource` | The **identifier scheme or namespace** (e.g., EUID, LEI, VAT). Declared as an object property to allow linking to a resource representing the scheme (for example, `webid:IdentifierScheme`). |
| **`webid:resolver`** | `rdfs:Resource` | The **resolver endpoint or service** that can dereference the identifier. Modeled as an object property for extensibility. |
| **`webid:status`** | `skos:Concept` | Indicates **lifecycle status** such as “active,” “retired,” or “superseded.” |
| **`webid:privacyPosture`** | `skos:Concept` | Describes **privacy level** (e.g., “public,” “restricted,” “confidential”). |
| **`webid:validityPeriod`** | `webid:PeriodOfTime` | The **interval of validity** for the identifier. |

---

### ⚙️ Modeling Note on `scheme` and `resolver`

- Both are defined as **`owl:ObjectProperty`** with **range `rdfs:Resource`**, reflecting a flexible design: they may point to either a resolvable IRI or a resource node describing the scheme or resolver service.  
- In practice, most implementations use **URI literals** (`xsd:anyURI`) in JSON-LD or VC data.  
- To support these cases, parallel convenience properties such as `webid:schemeUri` and `webid:resolverUri` *(DatatypeProperties)* may be introduced, with SHACL `sh:or` allowing either usage.

---

## 🧩 Datatype Properties

| Property | Datatype | Description |
|-----------|-----------|-------------|
| **`webid:notation`** | `xsd:string` | The **literal identifier value**, such as “FI-PRH.1000000-4” or “5493001KJTIIGC8Y1R12.” |
| **`webid:uri`** | `xsd:anyURI` | A **URI form** of the identifier itself, if resolvable. |
| **`webid:method`** | `xsd:string` | A **resolution or derivation method**, such as a DID method (`did:web`, `gleif`). |
| **`webid:dereferencingParameter`** | `xsd:string` | Optional **parameter** (query or fragment) used in dereferencing. |
| **`webid:assignmentDate`** | `xsd:dateTime` | The **date/time when the identifier was assigned**; semantically aligned with `dct:issued`. |
| **`webid:validFrom`** | `xsd:dateTime` | Start of validity (optional shortcut to `validityPeriod.startDate`). |
| **`webid:validThrough`** | `xsd:dateTime` | End of validity (optional shortcut to `validityPeriod.endDate`). |

---

## ⏳ Supporting Class: `webid:PeriodOfTime`

| Element | Value |
|----------|--------|
| **IRI** | [`https://iri.suomi.fi/model/webid/PeriodOfTime`](https://iri.suomi.fi/model/webid/PeriodOfTime) |
| **Type** | `owl:Class` |
| **Label** | Period of Time |
| **Description** | Represents a **time interval** with a `startDate` and an `endDate`. |

| Property | Datatype | Description |
|-----------|-----------|-------------|
| `webid:startDate` | `xsd:dateTime` | Start of the interval. |
| `webid:endDate` | `xsd:dateTime` | End of the interval. |

---

## 🧭 Ontological Design Notes

- The ontology defines **all potential properties** but none are mandatory.  
  *Obligations, formats, and cardinalities are specified in SHACL Shapes.*
- `rdfs:Resource` range on certain properties (e.g., `scheme`, `resolver`) provides extensibility for future modeling of `webid:IdentifierScheme` and `webid:ResolverService` classes.
- Designed for use across multiple identifier ecosystems (EUID, LEI, VAT, EORI, Y-tunnus).

---

## 🔗 Alignment and External References

| Concept | Reference |
|----------|------------|
| `adms:Identifier` | [W3C ADMS Vocabulary](https://www.w3.org/TR/vocab-adms/#identifier) |
| `dct:issued` | [Dublin Core Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) |
| `skos:Concept` | [W3C SKOS](https://www.w3.org/TR/skos-reference/) |
| `time:ProperInterval` | [OWL-Time Ontology](https://www.w3.org/TR/owl-time/) |

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
  ] ;
  webid:resolver <https://example.org/resolver/bris> .
```

---

## 🧩 Visualization

```text
Identifier
 ├── notation : xsd:string
 ├── scheme : rdfs:Resource (IRI or resource node)
 ├── uri : xsd:anyURI
 ├── issuer : Agent
 ├── owner : Agent
 ├── assignmentDate : xsd:dateTime
 ├── status : skos:Concept
 ├── privacyPosture : skos:Concept
 ├── resolver : rdfs:Resource (IRI or resource node)
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
| **Status** | Draft, version 0.2 |
| **License** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| **Editor / Contributor** | *Mikael af Hällström (Nordic Business Vocabulary / WE BUILD WP4)* |

---

## 🧾 Notes for Implementers

- Use this ontology as the **upper-layer semantic model** for identifiers.  
- Concrete profiles (EUID, LEI, VAT, etc.) should define SHACL Shapes enforcing:
  - pattern restrictions for `notation`
  - mandatory presence of `scheme` and `issuer`
  - value constraints for `status`
  - temporal consistency for `validityPeriod`
- In **JSON-LD or Verifiable Credential contexts**, `scheme` and `resolver` may be serialized as plain URI strings while remaining valid IRIs under JSON-LD semantics.

---

*End of document*
