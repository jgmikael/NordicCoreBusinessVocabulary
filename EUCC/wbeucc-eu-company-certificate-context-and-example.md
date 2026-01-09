# WE BUILD – EU Company Certificate (EUCC) JSON-LD material

This Markdown file contains:

1. The **JSON-LD `@context`** file (as generated from the uploaded SHACL/Turtle).
2. A **minimal example W3C Verifiable Credential (VC) payload** that references the context and uses concrete example values.

---

## 1) JSON-LD `@context`

> Note: in production, host this context at a stable HTTPS URL and reference that URL from issued credentials.

```json
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    {
      "@version": 1.1,
      "@protected": true,
      "id": "@id",
      "type": "@type",
      "xsd": "http://www.w3.org/2001/XMLSchema#",
      "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
      "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
      "owl": "http://www.w3.org/2002/07/owl#",
      "skos": "http://www.w3.org/2004/02/skos/core#",
      "dcterms": "http://purl.org/dc/terms/",
      "ncbv": "https://iri.suomi.fi/model/ncbv/0.0.5/",
      "wbeucc": "https://iri.suomi.fi/model/wbeucc/",
      "EUCompanyCertificateCredential": "wbeucc:EUCompanyCertificateCredential",
      "sameAs": {
        "@id": "owl:sameAs",
        "@type": "@id"
      },
      "ShareCapital": "ncbv:ShareCapital",
      "Person": "ncbv:Person",
      "Address": "ncbv:Address",
      "Membership": "ncbv:Membership",
      "CodeClass": "ncbv:CodeClass",
      "RoleBasedRepresentationRule": "ncbv:RoleBasedRepresentationRule",
      "ContactPoint": "ncbv:ContactPoint",
      "RepresentationRule": "ncbv:RepresentationRule",
      "MembershipBasedRepresentationRule": "ncbv:MembershipBasedRepresentationRule",
      "LegalEntity": "ncbv:LegalEntity",
      "LegalStatus": "ncbv:LegalStatus",
      "Identifier": "ncbv:Identifier",
      "MonetaryAmount": "ncbv:MonetaryAmount",
      "Role": "ncbv:Role",
      "adminUnitLevel1": "ncbv:adminUnitLevel1",
      "adminUnitLevel2": "ncbv:adminUnitLevel2",
      "capitalType": {
        "@id": "ncbv:capitalType",
        "@type": "xsd:string"
      },
      "careOf": "ncbv:careOf",
      "codeValue": {
        "@id": "ncbv:codeValue",
        "@type": "xsd:string"
      },
      "contactPage": {
        "@id": "ncbv:contactPage",
        "@type": "xsd:string"
      },
      "currency": {
        "@id": "ncbv:currency",
        "@type": "xsd:string"
      },
      "date": {
        "@id": "ncbv:date",
        "@type": "xsd:date"
      },
      "dateOfBirth": {
        "@id": "ncbv:dateOfBirth",
        "@type": "xsd:date"
      },
      "definesValidMembership": "ncbv:definesValidMembership",
      "definesValidRole": "ncbv:definesValidRole",
      "description": {
        "@id": "ncbv:description",
        "@type": "xsd:string"
      },
      "email": {
        "@id": "ncbv:email",
        "@type": "xsd:string"
      },
      "fullAddress": {
        "@id": "ncbv:fullAddress",
        "@type": "xsd:string"
      },
      "fullName": {
        "@id": "ncbv:fullName",
        "@type": "xsd:string"
      },
      "hasActivity": "ncbv:hasActivity",
      "hasCode": "ncbv:hasCode",
      "hasContactPoint": "ncbv:hasContactPoint",
      "hasIdentifier": "ncbv:hasIdentifier",
      "hasLegalForm": "ncbv:hasLegalForm",
      "hasLegalStatus": "ncbv:hasLegalStatus",
      "hasRepresentationRule": "ncbv:hasRepresentationRule",
      "hasRole": "ncbv:hasRole",
      "hasShareCapital": "ncbv:hasShareCapital",
      "legalIdentifier": "ncbv:legalIdentifier",
      "legalName": {
        "@id": "ncbv:legalName",
        "@type": "xsd:string"
      },
      "locatorDesignator": "ncbv:locatorDesignator",
      "locatorName": "ncbv:locatorName",
      "member": "ncbv:member",
      "memberQuantifier": {
        "@id": "ncbv:memberQuantifier",
        "@type": "@id"
      },
      "minimumNumberOfMembers": "ncbv:minimumNumberOfMembers",
      "minimumNumberOfRoleHolders": {
        "@id": "ncbv:minimumNumberOfRoleHolders",
        "@type": "xsd:integer"
      },
      "name": {
        "@id": "ncbv:name",
        "@type": "xsd:string"
      },
      "notation": {
        "@id": "ncbv:notation",
        "@type": "xsd:string"
      },
      "postCode": {
        "@id": "ncbv:postCode",
        "@type": "xsd:string"
      },
      "postName": "ncbv:postName",
      "postOfficeBox": "ncbv:postOfficeBox",
      "postalAddress": "ncbv:postalAddress",
      "registeredAddress": "ncbv:registeredAddress",
      "registrationDate": {
        "@id": "ncbv:registrationDate",
        "@type": "xsd:date"
      },
      "roleHolderQuantifier": {
        "@id": "ncbv:roleHolderQuantifier",
        "@type": "@id"
      },
      "schemaAgency": {
        "@id": "ncbv:schemaAgency",
        "@type": "xsd:string"
      },
      "schemeName": {
        "@id": "ncbv:schemeName",
        "@type": "xsd:string"
      },
      "thoroughfare": {
        "@id": "ncbv:thoroughfare",
        "@type": "xsd:string"
      },
      "topObjectProperty": "http://www.w3.org/2002/07/owl#topObjectProperty",
      "totalCapitalAmount": "ncbv:totalCapitalAmount",
      "value": {
        "@id": "ncbv:value",
        "@type": "xsd:decimal"
      }
    }
  ]
}
```

---

## 2) Minimal example VC payload

> Note: This is an illustrative example. Replace `issuer`, identifiers, and code-list IRIs with authoritative values in your deployment.

```json
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://example.com/contexts/wbeucc-eu-company-certificate-context.jsonld"
  ],
  "id": "urn:uuid:6c6d6b6a-1b2c-4d5e-9f10-112233445566",
  "type": [
    "VerifiableCredential",
    "EUCompanyCertificateCredential"
  ],
  "issuer": "did:web:prh.fi",
  "issuanceDate": "2026-01-09T10:00:00Z",
  "credentialSubject": {
    "id": "did:lei:743700O9HROPFJ8P9B42",
    "type": "LegalEntity",
    "legalName": "Nordic Timber Export Oy",
    "registeredAddress": {
      "type": "Address",
      "thoroughfare": "Mannerheimintie 10",
      "postCode": "00100",
      "postName": "Helsinki",
      "adminUnitLevel1": "Uusimaa",
      "adminUnitLevel2": "Helsinki",
      "fullAddress": "Mannerheimintie 10, 00100 Helsinki, Finland"
    },
    "hasIdentifier": [
      {
        "type": "Identifier",
        "schemeName": "FI:BusinessID",
        "codeValue": "1234567-8"
      },
      {
        "type": "Identifier",
        "schemeName": "LEI",
        "codeValue": "743700O9HROPFJ8P9B42"
      }
    ],
    "legalIdentifier": {
      "type": "Identifier",
      "schemeName": "FI:BusinessID",
      "codeValue": "1234567-8"
    },
    "hasLegalForm": {
      "id": "https://example.com/codelists/legal-forms/FI/OY"
    },
    "hasLegalStatus": {
      "id": "https://example.com/codelists/legal-status/active"
    },
    "hasShareCapital": {
      "type": "ShareCapital",
      "capitalType": "SHARE_CAPITAL",
      "totalCapitalAmount": {
        "type": "MonetaryAmount",
        "value": 250000.0,
        "currency": "EUR"
      }
    },
    "hasRepresentationRule": [
      {
        "type": "RoleBasedRepresentationRule",
        "description": "The CEO may represent the company alone; two board members jointly may also represent the company.",
        "definesValidRole": {
          "type": "Role",
          "hasCode": {
            "type": "Identifier",
            "schemeName": "FI:RoleCode",
            "codeValue": "CEO"
          }
        }
      }
    ]
  }
}
```
