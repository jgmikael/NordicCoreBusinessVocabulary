# PD A1 — Mapping to WE BUILD PD A1 SHACL + VC example


## Mapping table (with proposed SHACL-aligned labels)

| Excel label | Proposed SHACL-aligned label | Excel value | Mapped SHACL path |
| --- | --- | --- | --- |
| PIN | Insured person — person identifier (national ID) | 140269-9999 | webuild:insuredPerson / ncbv:hasIdentifier / eu-core:notation |
| Gender | Insured person — Gender | male | webuild:insuredPerson / eu-core:gender |
| Familyname(s) | Insured person — Family name | af Hällström | webuild:insuredPerson / eu-core:familyName |
| Forename(s) | Insured person — Given name(s) | John Gustav Mikael | webuild:insuredPerson / eu-core:givenName |
| Surname at birth | Insured person — Birth name (surname at birth) | Hönttöröm | webuild:insuredPerson / eu-core:birthName |
| Forename(s) at birth | Given name(s) at birth | Kusteli |  |
| Date of Birth | Insured person — Date of birth | 14.02.1969 | webuild:insuredPerson / eu-core:dateOfBirth |
| Nationality | Insured person — Citizenship (nationality) | Finnish | webuild:insuredPerson / eu-core:citizenship |
| Place of Birth | Place of birth — eu-core:placeOfBirth |  | webuild:insuredPerson / eu-core:placeOfBirth |
| Town | Place of birth — Geographic name | Helsingfors | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:geographicName |
| Country code | Place of birth — Country (ISO code) | FI | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:adminUnitLevel1 |
| Address | Address |  |  |
| Address in the state of residence | Address in the state of residence |  |  |
| Street, N° | Registered residence — Street and number | Löjgränden 3 B 3 | webuild:insuredPerson / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Registered residence — Post town / city | Esbo | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postName |
| Post code | Registered residence — Postal code | 02170 | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postCode |
| Country code | Registered residence — Country (ISO code) | FI | webuild:insuredPerson / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| Address in the state of stay | Address in the state of stay |  |  |
| Street, N° | Address during posting/stay — Street and number | Abborgatan 7 | webuild:insuredPerson / ncbv:postalAddress / eu-core:thoroughfare |
| Town | Address during posting/stay — Post town / city | Hässelholm | webuild:insuredPerson / ncbv:postalAddress / eu-core:postName |
| Post code | Address during posting/stay — Postal code | 22610 | webuild:insuredPerson / ncbv:postalAddress / eu-core:postCode |
| Country code | Address during posting/stay — Country (ISO code) | SE | webuild:insuredPerson / ncbv:postalAddress / eu-core:adminUnitLevel1 |
| Member state | Member State whose legislation applies — country code | FI | webuild:hasApplicableJurisdiction / eu-core:adminUnitLevel1 |
| Starting date | Applicable legislation period — Start time | 1.3.2026 | webuild:applicablePeriod / eu-core:startTime |
| Ending date | Applicable legislation period — End time | 31.12.2026 | webuild:applicablePeriod / eu-core:endTime |
| Certificate applies for the duration of the activity | Coverage period (applies for duration of contract) | true | webuild:hasCoverage / webuild:applicablePeriod |
| Determination is provisional | Determination type (provisional/final etc.) | true | webuild:hasDetermination / dcterms:type |
| Transitional rules apply | Applicable legislation — Subject to transitional rules (boolean) | false | webuild:isSubjectToTransitionalRules |
| Type of Employment | Employer — Employment / work-relation type | employment | webuild:insuredPerson / webuild:hasWorkRelation / webuild:employmentType |
| Name | Employer — Legal name | Bosses Bullfabrik | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalName |
| EmployerID | Employer — Identifier value (notation) | 5565878054 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Type of ID | Employer — Identifier scheme | Organisationsnummer Sverige | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |
| Address | Address |  |  |
| Street, N° | Employer registered address — Street and number | Rudeboksvägen 1 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Employer registered address — Post town / city | Lund | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |
| Post code | Employer registered address — Postal code | 22655 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |
| Country code | Employer registered address — Country (ISO code) | SE | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| No fixed place of work exists | Work performed at fixed place of activity (Yes/No) |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasFixedPlaceOfActivity (inverse) |
| Country code | Country where work is performed — country code |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:activityCountry / eu-core:adminUnitLevel1 |
| Place of work | Place of work |  |  |
| Company/vessel name | Work host — legal name (company/vessel) | Bosses Bullfabrik | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalName |
| Flag Base Home State | Vessel — flag state (if applicable) |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:usesOperationalAsset / webuild:flagState (vessel only) |
| CompanyID | Place of work — Identifier value (notation) | 5565878054 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Type of ID | Place of work — Identifier scheme | Organisationsnummer Sverige | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |
| Street, N° | Place of work — Street and number | Rudeboksvägen 1 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:thoroughfare |
| Town | Place of work — Post town / city | Lund | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postName |
| Postal Code | Place of work — Postal code | 22655 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postCode |
| Country code | Place of work — Country (ISO code) | SE | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:adminUnitLevel1 |
| Status confirmation | Issuance status (concept/code) |  |  |
| Document ID | PD A1 certificate identifier | 123456789 | dcterms:identifier |
| InstitutionID | Issuing institution — Identifier value (notation) | 0116415-4 | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Institution Name | Issuing institution — Legal name | Finnish Centre for Pensions | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalName |
| Country code | Issuing institution registered address — Country (ISO code) | FI | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| Office fax N° | Office fax number |  |  |
| Office phone N° | Issuing institution contact — eu-core:hasTelephone | +358 29 411 2816 | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasTelephone |
| E-Mail | Issuing institution contact — eu-core:hasEmail | ulkomaanasiat@etk.fi | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasEmail |
| Street, N° | Issuing institution registered address — Street and number | Insurance of Work Abroad | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Issuing institution registered address — Post town / city | Eläketurvakeskus | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |
| Postal Code | Issuing institution registered address — Postal code | FI-00065 | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |
| Country code | Issuing institution registered address — Country (ISO code) | FI | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |


## Generated W3C Verifiable Credential example (JSON)

```json
{
  "@context": [
    "https://www.w3.org/ns/credentials/v2",
    {
      "dcterms": "http://purl.org/dc/terms/",
      "skos": "http://www.w3.org/2004/02/skos/core#",
      "eu-core": "https://iri.suomi.fi/model/eu-core/",
      "ncbv": "https://iri.suomi.fi/model/ncbv/0.0.7/",
      "webuild": "https://iri.suomi.fi/model/webuild/",
      "webpda1": "https://iri.suomi.fi/model/webpda1/",
      "id": "@id",
      "type": "@type"
    }
  ],
  "id": "urn:uuid:76c1b2d2-166c-4002-87d1-c22124c31cf1",
  "type": [
    "VerifiableCredential"
  ],
  "issuer": "did:web:ela.example.fi",
  "validFrom": "2026-03-01T00:00:00Z",
  "validUntil": "2026-12-31T00:00:00Z",
  "credentialSubject": {
    "id": "urn:uuid:4f793df9-1938-4502-a6e5-967db7395348",
    "type": "webuild:PDA1Certificate",
    "dcterms:identifier": "123456789",
    "webuild:applicablePeriod": {
      "type": "webpda1:PeriodOfTime",
      "eu-core:startTime": "2026-03-01T00:00:00Z",
      "eu-core:endTime": "2026-12-31T00:00:00Z"
    },
    "webuild:hasApplicableJurisdiction": [
      {
        "type": "webpda1:Location",
        "eu-core:adminUnitLevel1": "FI"
      }
    ],
    "webuild:isSubjectToTransitionalRules": false,
    "webuild:hasCoverage": [
      {
        "type": "webpda1:Coverage",
        "webuild:applicablePeriod": {
          "type": "webpda1:PeriodOfTime",
          "eu-core:startTime": "2026-03-01T00:00:00Z",
          "eu-core:endTime": "2026-12-31T00:00:00Z"
        }
      }
    ],
    "webuild:hasDetermination": [
      {
        "type": "webpda1:Determination",
        "dcterms:type": "true"
      }
    ],
    "webuild:issuingInstitution": [
      {
        "type": "webpda1:Agent",
        "webuild:isLegalEntity": {
          "type": "webpda1:LegalEntity",
          "eu-core:legalName": "Finnish Centre for Pensions",
          "eu-core:legalidentifier": {
            "type": "webpda1:Identifier",
            "eu-core:notation": "0116415-4"
          },
          "eu-core:registeredAddress": {
            "type": "webpda1:Address",
            "eu-core:thoroughfare": "Insurance of Work Abroad",
            "eu-core:postName": "Eläketurvakeskus",
            "eu-core:postCode": "FI-00065",
            "eu-core:adminUnitLevel1": "FI"
          }
        },
        "ncbv:hasContactPoint": [
          {
            "type": "webpda1:ContactPoint",
            "eu-core:hasEmail": "ulkomaanasiat@etk.fi",
            "eu-core:hasTelephone": "+358 29 411 2816"
          }
        ]
      }
    ],
    "webuild:insuredPerson": {
      "type": "webpda1:Person",
      "ncbv:hasIdentifier": [
        {
          "type": "webpda1:Identifier",
          "eu-core:notation": "140269-9999"
        }
      ],
      "eu-core:gender": "male",
      "eu-core:familyName": "af Hällström",
      "eu-core:givenName": [
        "John Gustav Mikael"
      ],
      "eu-core:birthName": "Hönttöröm",
      "eu-core:dateOfBirth": "1969-02-14",
      "eu-core:citizenship": [
        "Finnish"
      ],
      "eu-core:placeOfBirth": [
        {
          "type": "webpda1:Location",
          "eu-core:geographicName": "Helsingfors",
          "eu-core:adminUnitLevel1": "FI"
        }
      ],
      "eu-core:registeredAddress": {
        "type": "webpda1:Address",
        "eu-core:thoroughfare": "Löjgränden 3 B 3",
        "eu-core:postName": "Esbo",
        "eu-core:postCode": "02170",
        "eu-core:adminUnitLevel1": "FI"
      },
      "ncbv:postalAddress": [
        {
          "type": "webpda1:Address",
          "eu-core:thoroughfare": "Abborgatan 7",
          "eu-core:postName": "Hässelholm",
          "eu-core:postCode": "22610",
          "eu-core:adminUnitLevel1": "SE"
        }
      ],
      "webuild:hasWorkRelation": [
        {
          "type": "webpda1:Employment",
          "webuild:employmentType": "employment",
          "webuild:hasEmployer": [
            {
              "type": "webpda1:Agent",
              "webuild:isLegalEntity": {
                "type": "webpda1:LegalEntity",
                "eu-core:legalName": "Bosses Bullfabrik",
                "eu-core:legalidentifier": {
                  "type": "webpda1:Identifier",
                  "eu-core:notation": "5565878054",
                  "eu-core:schemeName": "Organisationsnummer Sverige"
                },
                "eu-core:registeredAddress": {
                  "type": "webpda1:Address",
                  "eu-core:thoroughfare": "Rudeboksvägen 1",
                  "eu-core:postName": "Lund",
                  "eu-core:postCode": "22655",
                  "eu-core:adminUnitLevel1": "SE"
                }
              }
            }
          ],
          "ncbv:hasActivity": [
            {
              "type": "webpda1:Activity",
              "webuild:hasPlaceOfActivity": [
                {
                  "type": "webpda1:Location",
                  "webuild:hasAddress": {
                    "type": "webpda1:Address",
                    "eu-core:thoroughfare": "Rudeboksvägen 1",
                    "eu-core:postName": "Lund",
                    "eu-core:postCode": "22655",
                    "eu-core:adminUnitLevel1": "SE"
                  },
                  "webuild:workHost": {
                    "type": "webpda1:Agent",
                    "webuild:isLegalEntity": {
                      "type": "webpda1:LegalEntity",
                      "eu-core:legalName": "Bosses Bullfabrik",
                      "eu-core:legalidentifier": {
                        "type": "webpda1:Identifier",
                        "eu-core:notation": "5565878054",
                        "eu-core:schemeName": "Organisationsnummer Sverige"
                      }
                    }
                  }
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
```



## Notes on elements not represented in the VC

- Rows with an **empty “Mapped SHACL path”** cannot be represented without extending the SHACL/Vocabulary.

- Some SHACL paths end in `skos:Concept` (e.g., `dcterms:type` for Determination). If your Excel values are booleans/strings, SHACL-conformant instances typically need a concept URI/code.
