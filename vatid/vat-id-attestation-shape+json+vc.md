# VAT ID Attestation – Data Model (from SHACL)

This document explains, in plain terms, the data model defined by the uploaded SHACL Shapes for a VAT ID attestation intended for use in an eIDAS 2.0 EU Business Wallet (EBW) context.

The SHACL file defines a small set of reusable “building blocks” (classes) and their data fields (properties). Each property below includes its IRI (the technical identifier) in parentheses.

## Economic Operator

- **Shape IRI:** `https://iri.suomi.fi/model/webvatid/LegalEntity`

- **What it represents:** Instances of `https://iri.suomi.fi/model/ncbv/0.0.7/LegalEntity`


### Properties

- **legalIdentifier** (`https://iri.suomi.fi/model/ncbv/0.0.7/legalIdentifier`): Required; Single value; Links to: Identifier.

- **Administrative Unit** (`http://www.w3.org/2002/07/owl#topObjectProperty`): Optional; Repeatable; Links to: AdministrativeUnit.

- **legalName** (`https://iri.suomi.fi/model/ncbv/0.0.7/legalName`): Required; Single value; Value type: string.



## Administrative Unit

- **Shape IRI:** `https://iri.suomi.fi/model/webvatid/AdministrativeUnit`

- **What it represents:** Instances of `https://iri.suomi.fi/model/eu-core/AdministrativeUnit`


### Properties

- **hasIdentifier** (`https://iri.suomi.fi/model/ncbv/0.0.7/hasIdentifier`): Required; Single value; Links to: Identifier.

- **validityPeriod** (`https://iri.suomi.fi/model/eu-core/validityPeriod`): Required; Single value; Links to: PeriodOfTime.

- **registeredAddress** (`https://iri.suomi.fi/model/ncbv/0.0.7/registeredAddress`): Required; Single value; Links to: Address.



## Identifier

- **Shape IRI:** `https://iri.suomi.fi/model/webvatid/Identifier`

- **What it represents:** Instances of `https://iri.suomi.fi/model/ncbv/0.0.7/Identifier`


### Properties

- **notation** (`https://iri.suomi.fi/model/ncbv/0.0.7/notation`): Optional; Repeatable; Value type: string.

- **schemeName** (`https://iri.suomi.fi/model/ncbv/0.0.7/schemeName`): Optional; Repeatable; Value type: string.

- **schemaAgency** (`https://iri.suomi.fi/model/ncbv/0.0.7/schemaAgency`): Optional; Repeatable; Value type: string.

- **dateOfIssue** (`https://iri.suomi.fi/model/ncbv/0.0.7/dateOfIssue`): Optional; Repeatable; Value type: date.



## Address

- **Shape IRI:** `https://iri.suomi.fi/model/webvatid/Address`

- **What it represents:** Instances of `https://iri.suomi.fi/model/ncbv/0.0.7/Address`


### Properties

- **adminUnitLevel2** (`https://iri.suomi.fi/model/ncbv/0.0.7/adminUnitLevel2`): Optional; Repeatable; Value type: string.

- **postName** (`https://iri.suomi.fi/model/ncbv/0.0.7/postName`): Optional; Repeatable; Value type: string.

- **postCode** (`https://iri.suomi.fi/model/ncbv/0.0.7/postCode`): Optional; Repeatable; Value type: string.

- **locatorName** (`https://iri.suomi.fi/model/ncbv/0.0.7/locatorName`): Optional; Repeatable; Value type: string.

- **locatorDesignator** (`https://iri.suomi.fi/model/ncbv/0.0.7/locatorDesignator`): Optional; Repeatable; Value type: string.

- **fullAddress** (`https://iri.suomi.fi/model/ncbv/0.0.7/fullAddress`): Optional; Repeatable; Value type: string.

- **careOf** (`https://iri.suomi.fi/model/ncbv/0.0.7/careOf`): Optional; Repeatable; Value type: string.

- **adminUnitLevel1** (`https://iri.suomi.fi/model/ncbv/0.0.7/adminUnitLevel1`): Optional; Repeatable; Value type: string.

- **thoroughfare** (`https://iri.suomi.fi/model/ncbv/0.0.7/thoroughfare`): Optional; Repeatable; Value type: string.

- **postOfficeBox** (`https://iri.suomi.fi/model/ncbv/0.0.7/postOfficeBox`): Optional; Repeatable; Value type: string.



## Period of Time

- **Shape IRI:** `https://iri.suomi.fi/model/webvatid/PeriodOfTime`

- **What it represents:** Instances of `https://iri.suomi.fi/model/ncbv/0.0.7/PeriodOfTime`


### Properties

- **startDate** (`https://iri.suomi.fi/model/ncbv/0.0.7/startDate`): Required; Single value; Value type: date.

- **endDate** (`https://iri.suomi.fi/model/ncbv/0.0.7/endDate`): Required; Single value; Value type: date.



## Technical notes and observed issues

- The property shape `https://iri.suomi.fi/model/webvatid/hasAdministrativeUnit` is labelled “Administrative Unit”, but its `sh:path` is `owl:topObjectProperty` (`http://www.w3.org/2002/07/owl#topObjectProperty`). In practice, for JSON-LD/VC issuance you typically want a concrete predicate IRI (for example `https://iri.suomi.fi/model/webvatid/hasAdministrativeUnit`) rather than `owl:topObjectProperty`.

- The property shape `https://iri.suomi.fi/model/webvatid/level` (path `https://iri.suomi.fi/model/eu-core/level`) is defined in the file but is not referenced by any NodeShape via `sh:property`, so it currently has no effect on validation.


---

# JSON artefacts for implementation

## JSON-LD @context (for W3C VC issuance)

```json
{
  "@context": [
    "https://www.w3.org/ns/credentials/v2",
    {
      "@version": 1.1,
      "id": "@id",
      "type": "@type",
      "webvatid": "https://iri.suomi.fi/model/webvatid/",
      "ncbv": "https://iri.suomi.fi/model/ncbv/0.0.7/",
      "eucore": "https://iri.suomi.fi/model/eu-core/",
      "xsd": "http://www.w3.org/2001/XMLSchema#",
      "owl": "http://www.w3.org/2002/07/owl#",
      "Address": "https://iri.suomi.fi/model/webvatid/Address",
      "AdministrativeUnit": "https://iri.suomi.fi/model/webvatid/AdministrativeUnit",
      "Identifier": "https://iri.suomi.fi/model/webvatid/Identifier",
      "LegalEntity": "https://iri.suomi.fi/model/webvatid/LegalEntity",
      "PeriodOfTime": "https://iri.suomi.fi/model/webvatid/PeriodOfTime",
      "adminUnitLevel1": "https://iri.suomi.fi/model/webvatid/adminUnitLevel1",
      "adminUnitLevel2": "https://iri.suomi.fi/model/webvatid/adminUnitLevel2",
      "careOf": "https://iri.suomi.fi/model/webvatid/careOf",
      "dateOfIssue": "https://iri.suomi.fi/model/webvatid/dateOfIssue",
      "endDate": "https://iri.suomi.fi/model/webvatid/endDate",
      "fullAddress": "https://iri.suomi.fi/model/webvatid/fullAddress",
      "hasAdministrativeUnit": "https://iri.suomi.fi/model/webvatid/hasAdministrativeUnit",
      "hasIdentifier": "https://iri.suomi.fi/model/webvatid/hasIdentifier",
      "legalIdentifier": "https://iri.suomi.fi/model/webvatid/legalIdentifier",
      "legalName": "https://iri.suomi.fi/model/webvatid/legalName",
      "level": "https://iri.suomi.fi/model/webvatid/level",
      "locatorDesignator": "https://iri.suomi.fi/model/webvatid/locatorDesignator",
      "locatorName": "https://iri.suomi.fi/model/webvatid/locatorName",
      "notation": "https://iri.suomi.fi/model/webvatid/notation",
      "postCode": "https://iri.suomi.fi/model/webvatid/postCode",
      "postName": "https://iri.suomi.fi/model/webvatid/postName",
      "postOfficeBox": "https://iri.suomi.fi/model/webvatid/postOfficeBox",
      "registeredAddress": "https://iri.suomi.fi/model/webvatid/registeredAddress",
      "schemaAgency": "https://iri.suomi.fi/model/webvatid/schemaAgency",
      "schemeName": "https://iri.suomi.fi/model/webvatid/schemeName",
      "startDate": "https://iri.suomi.fi/model/webvatid/startDate",
      "thoroughfare": "https://iri.suomi.fi/model/webvatid/thoroughfare",
      "validityPeriod": "https://iri.suomi.fi/model/webvatid/validityPeriod"
    }
  ]
}
```

## JSON Schema (plain JSON; derived from SHACL)

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://iri.suomi.fi/model/webvatid/schema/vat-id-attestation.json",
  "title": "VAT ID Attestation (derived from SHACL)",
  "type": "object",
  "additionalProperties": false,
  "properties": {
    "legalEntity": {
      "$ref": "#/$defs/LegalEntity"
    },
    "validityPeriod": {
      "$ref": "#/$defs/PeriodOfTime"
    }
  },
  "required": [
    "legalEntity"
  ],
  "$defs": {
    "Identifier": {
      "type": "object",
      "additionalProperties": false,
      "properties": {
        "content": {
          "type": "string",
          "minLength": 1
        },
        "schemeIdentifier": {
          "type": "string"
        },
        "schemeName": {
          "type": "string"
        }
      },
      "required": [
        "content",
        "schemeIdentifier",
        "schemeName"
      ],
      "examples": [
        {
          "content": "FI12345678",
          "schemeIdentifier": "VAT",
          "schemeName": "EU VAT Identification Number"
        }
      ]
    },
    "AdministrativeUnit": {
      "type": "object",
      "additionalProperties": false,
      "properties": {
        "level": {
          "type": "string"
        },
        "name": {
          "type": "string",
          "minLength": 1
        }
      },
      "required": [
        "name"
      ],
      "examples": [
        {
          "level": "NUTS2",
          "name": "Helsinki-Uusimaa"
        }
      ]
    },
    "Address": {
      "type": "object",
      "additionalProperties": false,
      "properties": {
        "fullAddress": {
          "type": "string",
          "minLength": 1
        },
        "hasAdministrativeUnit": {
          "$ref": "#/$defs/AdministrativeUnit"
        }
      },
      "required": [
        "fullAddress"
      ],
      "examples": [
        {
          "fullAddress": "Esimerkkikatu 1, 00100 Helsinki, Finland",
          "hasAdministrativeUnit": {
            "level": "Municipality",
            "name": "Helsinki"
          }
        }
      ]
    },
    "LegalEntity": {
      "type": "object",
      "additionalProperties": false,
      "properties": {
        "registeredName": {
          "type": "string"
        },
        "legalName": {
          "type": "string",
          "minLength": 1
        },
        "legalEntityIdentifier": {
          "$ref": "#/$defs/Identifier"
        },
        "address": {
          "$ref": "#/$defs/Address"
        },
        "hasAdministrativeUnit": {
          "$ref": "#/$defs/AdministrativeUnit"
        }
      },
      "required": [
        "legalName",
        "legalEntityIdentifier",
        "address"
      ],
      "examples": [
        {
          "registeredName": "Example Oy",
          "legalName": "Example Oy",
          "legalEntityIdentifier": {
            "content": "FI12345678",
            "schemeIdentifier": "VAT",
            "schemeName": "EU VAT Identification Number"
          },
          "address": {
            "fullAddress": "Esimerkkikatu 1, 00100 Helsinki, Finland",
            "hasAdministrativeUnit": {
              "level": "Municipality",
              "name": "Helsinki"
            }
          },
          "hasAdministrativeUnit": {
            "level": "Country",
            "name": "Finland"
          }
        }
      ]
    },
    "PeriodOfTime": {
      "type": "object",
      "additionalProperties": false,
      "properties": {
        "startDate": {
          "type": "string",
          "format": "date"
        },
        "endDate": {
          "type": "string",
          "format": "date"
        }
      },
      "examples": [
        {
          "startDate": "2026-01-01",
          "endDate": "2027-01-01"
        }
      ]
    }
  },
  "examples": [
    {
      "legalEntity": {
        "registeredName": "Example Oy",
        "legalName": "Example Oy",
        "legalEntityIdentifier": {
          "content": "FI12345678",
          "schemeIdentifier": "VAT",
          "schemeName": "EU VAT Identification Number"
        },
        "address": {
          "fullAddress": "Esimerkkikatu 1, 00100 Helsinki, Finland",
          "hasAdministrativeUnit": {
            "level": "Municipality",
            "name": "Helsinki"
          }
        },
        "hasAdministrativeUnit": {
          "level": "Country",
          "name": "Finland"
        }
      },
      "validityPeriod": {
        "startDate": "2026-01-01",
        "endDate": "2027-01-01"
      }
    }
  ]
}
```

## Example W3C Verifiable Credential (populated)

```json
{
  "@context": [
    "https://www.w3.org/ns/credentials/v2",
    {
      "@version": 1.1,
      "id": "@id",
      "type": "@type",
      "webvatid": "https://iri.suomi.fi/model/webvatid/",
      "ncbv": "https://iri.suomi.fi/model/ncbv/0.0.7/",
      "eucore": "https://iri.suomi.fi/model/eu-core/",
      "xsd": "http://www.w3.org/2001/XMLSchema#",
      "owl": "http://www.w3.org/2002/07/owl#",
      "Address": "https://iri.suomi.fi/model/webvatid/Address",
      "AdministrativeUnit": "https://iri.suomi.fi/model/webvatid/AdministrativeUnit",
      "Identifier": "https://iri.suomi.fi/model/webvatid/Identifier",
      "LegalEntity": "https://iri.suomi.fi/model/webvatid/LegalEntity",
      "PeriodOfTime": "https://iri.suomi.fi/model/webvatid/PeriodOfTime",
      "adminUnitLevel1": "https://iri.suomi.fi/model/webvatid/adminUnitLevel1",
      "adminUnitLevel2": "https://iri.suomi.fi/model/webvatid/adminUnitLevel2",
      "careOf": "https://iri.suomi.fi/model/webvatid/careOf",
      "dateOfIssue": "https://iri.suomi.fi/model/webvatid/dateOfIssue",
      "endDate": "https://iri.suomi.fi/model/webvatid/endDate",
      "fullAddress": "https://iri.suomi.fi/model/webvatid/fullAddress",
      "hasAdministrativeUnit": "https://iri.suomi.fi/model/webvatid/hasAdministrativeUnit",
      "hasIdentifier": "https://iri.suomi.fi/model/webvatid/hasIdentifier",
      "legalIdentifier": "https://iri.suomi.fi/model/webvatid/legalIdentifier",
      "legalName": "https://iri.suomi.fi/model/webvatid/legalName",
      "level": "https://iri.suomi.fi/model/webvatid/level",
      "locatorDesignator": "https://iri.suomi.fi/model/webvatid/locatorDesignator",
      "locatorName": "https://iri.suomi.fi/model/webvatid/locatorName",
      "notation": "https://iri.suomi.fi/model/webvatid/notation",
      "postCode": "https://iri.suomi.fi/model/webvatid/postCode",
      "postName": "https://iri.suomi.fi/model/webvatid/postName",
      "postOfficeBox": "https://iri.suomi.fi/model/webvatid/postOfficeBox",
      "registeredAddress": "https://iri.suomi.fi/model/webvatid/registeredAddress",
      "schemaAgency": "https://iri.suomi.fi/model/webvatid/schemaAgency",
      "schemeName": "https://iri.suomi.fi/model/webvatid/schemeName",
      "startDate": "https://iri.suomi.fi/model/webvatid/startDate",
      "thoroughfare": "https://iri.suomi.fi/model/webvatid/thoroughfare",
      "validityPeriod": "https://iri.suomi.fi/model/webvatid/validityPeriod"
    }
  ],
  "id": "urn:uuid:2fb5b4f8-7e3f-4b85-9a9b-0d9b2a4b1d4e",
  "type": [
    "VerifiableCredential",
    "VATIDAttestation"
  ],
  "issuer": "did:web:example.fi",
  "validFrom": "2026-01-21T00:00:00Z",
  "credentialSubject": {
    "id": "did:lei:5493001KJTIIGC8Y1R12",
    "legalName": "Example Oy",
    "registeredName": "Example Oy",
    "legalEntityIdentifier": {
      "content": "FI12345678",
      "schemeIdentifier": "VAT",
      "schemeName": "EU VAT Identification Number"
    },
    "address": {
      "fullAddress": "Esimerkkikatu 1, 00100 Helsinki, Finland",
      "hasAdministrativeUnit": {
        "level": "Municipality",
        "name": "Helsinki"
      }
    },
    "hasAdministrativeUnit": {
      "level": "Country",
      "name": "Finland"
    }
  },
  "credentialStatus": {
    "id": "https://example.fi/status/vat-id/2fb5b4f8-7e3f-4b85-9a9b-0d9b2a4b1d4e",
    "type": "StatusList2021Entry",
    "statusPurpose": "revocation",
    "statusListIndex": "12345",
    "statusListCredential": "https://example.fi/status/vat-id/statuslist2021.json"
  }
}
```
