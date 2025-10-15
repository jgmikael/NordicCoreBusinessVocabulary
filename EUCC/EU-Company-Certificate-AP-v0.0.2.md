# EU Company Certificate Application Profile (based on NCBV Ontology)

**Status:** Draft • **Version:** 0.0.2 • **Date:** 2025-10-15

## 1. Scope and Purpose

This document describes the **EU Company Certificate (EUCC) Application Profile** and its conformance with the **Nordic Core Business Vocabulary (NCBV)** Ontology (v0.0.5). It includes an explanatory overview, a fact-based cross-check between the EUCC and NCBV, and an updated **W3C Verifiable Credential** example aligned with the NCBV 0.0.5 ontology.

### Legal baseline
The EU Company Certificate is defined in **Directive (EU) 2025/25**, Article **16b**, which requires Member States to issue a harmonised EU-wide company certificate that provides legal proof of incorporation and registration facts for limited liability companies and partnerships.

## 2. Explanatory Overview

### 2.1 Objective
The **EU Company Certificate (EUCC)** ensures that essential company information—such as legal name, form, identifiers, registration data, representatives, object, and share capital—is represented in a structured, semantically interoperable, and verifiable format suitable for digital exchange across the EU.

### 2.2 Relationship to NCBV
The **NCBV Ontology** provides canonical classes and properties for describing business entities and their identifiers, activities, representation, and ownership. The EUCC Application Profile builds on NCBV to ensure semantic interoperability and compliance with Article 16b of the Directive.

### 2.3 Data content according to Article 16b
The EUCC must include the following (factual list from Directive (EU) 2025/25, Article 16b):
- Name of the company and any alternative name(s)
- Legal form and legal status
- EUID (European Unique Identifier)
- Registered office and correspondence address
- Member State of registration and registration number
- Date of registration and, if applicable, date of termination
- Subscribed share capital (where applicable)
- Representation rule(s) and authorised representatives
- Company object and NACE activity code
- Duration (if limited)
- Website and contact details
- Date of issue

## 3. Updated Example: W3C Verifiable Credential (NCBV-aligned)

This example expresses an EUCC instance as a **W3C Verifiable Credential**, aligned with **NCBV 0.0.5** classes and properties and adjusted according to the official directive. The credential uses `did:example:FI-BR:PRH` as issuer and includes an EUID identifier with the corrected format `FIFPRO-1234567-8`.

```json
{
  "@context": [
    "https://www.w3.org/ns/credentials/v2",
    {
      "ncbv": "https://iri.suomi.fi/model/ncbv/"
    }
  ],
  "type": [
    "VerifiableCredential"
  ],
  "issuer": "did:example:FI-BR:PRH",
  "validFrom": "2025-10-14T12:00:00Z",
  "credentialSubject": {
    "@type": "ncbv:LegalEntity",
    "ncbv:legalName": "Acme Oy",
    "ncbv:alternativeName": "Acme Ltd",
    "ncbv:hasIdentifier": [
      {
        "@type": "ncbv:Identifier",
        "ncbv:identifierValue": "FI-1234567-8",
        "ncbv:schemeName": "Business ID",
        "ncbv:schemaAgency": "PRH (FI)"
      },
      {
        "@type": "ncbv:Identifier",
        "ncbv:identifierValue": "FIFPRO-1234567-8",
        "ncbv:schemeName": "EUID"
      }
    ],
    "ncbv:registeredAddress": {
      "@type": "ncbv:Address",
      "ncbv:thoroughfare": "Mannerheimintie 10",
      "ncbv:postCode": "00100",
      "ncbv:postName": "Helsinki",
      "ncbv:adminUnitLevel1": "Uusimaa",
      "ncbv:adminUnitLevel2": "FI",
      "ncbv:fullAddress": "Mannerheimintie 10, 00100 Helsinki, Finland"
    },
    "ncbv:registrationDate": "2010-06-30",
    "ncbv:hasLegalForm": {
      "@type": "ncbv:Code",
      "ncbv:codeValue": "OY",
      "ncbv:codeName": "Osakeyhti\u00f6 (Private Limited Company)"
    },
    "ncbv:hasActivity": {
      "@type": "ncbv:Code",
      "ncbv:codeValue": "62.01",
      "ncbv:codeName": "Computer programming activities"
    },
    "ncbv:hasShareCapital": {
      "@type": "ncbv:ShareCapital",
      "ncbv:value": 25000,
      "ncbv:currency": "EUR",
      "ncbv:capitalType": "subscribed"
    },
    "ncbv:status": "economically active",
    "ncbv:contactPage": "https://www.acme.fi",
    "ncbv:email": "info@acme.fi",
    "ncbv:hasRepresentationRule": {
      "@type": "ncbv:RepresentationRule",
      "ncbv:minimumNumberOfRoleHolders": 1,
      "ncbv:hasRole": [
        {
          "@type": "ncbv:Role",
          "ncbv:heldByPerson": {
            "@type": "ncbv:Person",
            "ncbv:fullName": "Laura Laine",
            "ncbv:dateOfBirth": "1981-03-12"
          }
        },
        {
          "@type": "ncbv:Role",
          "ncbv:heldByPerson": {
            "@type": "ncbv:Person",
            "ncbv:fullName": "Mikko Miettinen",
            "ncbv:dateOfBirth": "1979-11-02"
          }
        }
      ]
    }
  },
  "proof": {
    "type": "DataIntegrityProof",
    "created": "2025-10-14T12:00:00Z",
    "cryptosuite": "eddsa-2022",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "did:example:FI-BR:PRH#keys-1",
    "proofValue": "zExampleSignature"
  }
}
```

## 4. Observations on Alignment (Facts)

- The uploaded EUCC JSON-LD follows the structural intent of NCBV but previously used a versioned namespace (`/ncbv/0.0.5/`), which does **not exist** in the NCBV ontology. The actual IRIs use the unversioned namespace `https://iri.suomi.fi/model/ncbv/`.
- Properties such as `ncbv:hasIdentifier`, `ncbv:registeredAddress`, `ncbv:hasLegalForm`, `ncbv:hasActivity`, `ncbv:hasShareCapital`, and `ncbv:hasRepresentationRule` are confirmed to exist in the NCBV 0.0.5 ontology.
- Identifiers, including EUID, are correctly modelled as instances of `ncbv:Identifier`.
- Representation is aligned with `ncbv:RepresentationRule` and `ncbv:Role` with `ncbv:heldByPerson`.
- The ontology supports both `ncbv:dateOfBirth` and `ncbv:registrationDate` datatype properties required by Article 16b.

## 5. Provenance

- Application Profile (EUCC): `WE BUILD EU Company Certificate.ttl`
- JSON-LD instance: `WE BUILD EU Company Certificate (1).jsonld`
- Ontology: `Nordic Core Business Vocabulary (v0.0.5)`
- Legal baseline: Directive (EU) 2025/25, Article 16b

## 6. Next Steps (Non-normative)

1. Define SHACL shapes to constrain and validate the EUCC structure according to NCBV.
2. Register the profile and its namespace at `https://iri.suomi.fi/model/wbeucc/`.
3. Publish human-readable documentation in Markdown (GitHub Pages) and machine-readable Turtle/JSON-LD formats.
4. Align with BRIS and EU Business Wallet specifications to enable cross-border digital issuance.

---

**Authoring context:** Prepared for WE BUILD LSP WP4 (Semantics Group)  
**Contact:** semantic-interoperability@webuild.eu  
**Version control:** This Markdown documentation is generated directly from the uploaded Turtle and JSON-LD artefacts.
