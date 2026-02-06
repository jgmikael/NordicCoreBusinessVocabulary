# PD A1 Certificate — Human-readable view + VC example

This Markdown file contains:

1. A **full-coverage human-readable table** using the **Excel labels** as the primary labels and the **W3C / vocabulary paths** alongside.

2. A **W3C VC JSON(-LD-ish) example** generated to follow the **WE BUILD PD A1 SHACL** (non-vessel scenario; **no flag-state / vessel properties**).


---

## Human-readable table (Excel labels + W3C paths + values)

| Code | Excel label | W3C / vocabulary path | Value |
| --- | --- | --- | --- |
| 1 | Subject |  |  |
| 1 | 1 PIN |  | 140269-9999 |
| 1 | 2 Gender |  | male |
| 1 | 3 Familyname(s) |  | af Hällström |
| 1 | 4 Forename(s) |  | John Gustav Mikael |
| 1 | 5 Surname at birth |  | Hönttöröm |
| 1 | 6 Forename(s) at birth |  | Kusteli |
| 1 | 7 Date of Birth |  | 14.02.1969 |
| 1 | 8 Nationality |  | Finnish |
| 1 | 9 Place of Birth |  |  |
| 1.9 | 1 Town | webuild:insuredPerson / eu-core:placeOfBirth | Helsingfors |
| 1.9 | 2 Country code | webuild:insuredPerson / eu-core:placeOfBirth | FI |
| 1 | 10 Address |  |  |
| 1.10 | 1 Address in the state of residence | webuild:insuredPerson / eu-core:registeredAddress | Keilaranta 13, 02150 Espoo, FI |
| 1.10.1 | 1 Street, N° | webuild:insuredPerson / eu-core:registeredAddress | Löjgränden 3 B 3 |
| 1.10.1 | 2 Town | webuild:insuredPerson / eu-core:registeredAddress | Esbo |
| 1.10.1 | 3 Post code | webuild:insuredPerson / eu-core:registeredAddress | 02170 |
| 1.10.1 | 4 Country code | webuild:insuredPerson / eu-core:registeredAddress | FI |
| 1.10 | 2 Address in the state of stay | webuild:insuredPerson / eu-core:registeredAddress | Keilaranta 13, 02150 Espoo, FI |
| 1.10.2 | 1 Street, N° | webuild:insuredPerson / ncbv:postalAddress | Abborgatan 7 |
| 1.10.2 | 2 Town | webuild:insuredPerson / ncbv:postalAddress | Hässelholm |
| 1.10.2 | 3 Post code | webuild:insuredPerson / ncbv:postalAddress | 22610 |
| 1.10.2 | 4 Country code | webuild:insuredPerson / ncbv:postalAddress | SE |
| 2 | Member state legislation which applies |  |  |
| 2 | 1 Member state |  | FI |
| 2 | 2 Starting date |  | 1.3.2026 |
| 2 | 3 Ending date |  | 31.12.2026 |
| 2 | 4 Certificate applies for the duration of the activity |  | true |
| 2 | 5 Determination is provisional |  | true |
| 2 | 6 Transitional rules apply |  | false |
| 3 | Details of Employer(s)/Self-employment |  |  |
| 3 | 1 Type of Employment |  | employment |
| 3 | 2 Name |  | Bosses Bullfabrik |
| 3 | 3 EmployerID |  | 5565878054 |
| 3 | 4 Type of ID |  | Organisationsnummer Sverige |
| 3 | 5 Address |  |  |
| 3.5 | 1 Street, N° | webuild:insuredPerson / webuild:hasWorkRelation[0] / webuild:hasEmployer[0] / webuild:isLegalEntity / eu-core:registeredAddress | Rudeboksvägen 1 |
| 3.5 | 2 Town | webuild:insuredPerson / webuild:hasWorkRelation[0] / webuild:hasEmployer[0] / webuild:isLegalEntity / eu-core:registeredAddress | Lund |
| 3.5 | 3 Post code | webuild:insuredPerson / webuild:hasWorkRelation[0] / webuild:hasEmployer[0] / webuild:isLegalEntity / eu-core:registeredAddress | 22655 |
| 3.5 | 4 Country code | webuild:insuredPerson / webuild:hasWorkRelation[0] / webuild:hasEmployer[0] / webuild:isLegalEntity / eu-core:registeredAddress | SE |
| 4 | Place(s) of work |  |  |
| 4 | 1 No fixed place of work exists |  |  |
| 4.1 | 1 Country code | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasFixedPlaceOfActivity | true |
| 4 | 2 Place of work |  |  |
| 4.2 | 1 Company/vessel name | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | Bosses Bullfabrik |
| 4.2 | 2 Flag Base Home State | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] |  |
| 4.2 | 3 CompanyID | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | 5565878054 |
| 4.2 | 4 Type of ID | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | Organisationsnummer Sverige |
| 4.2 | 5 Street, N° | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | Rudeboksvägen 1 |
| 4.2 | 6 Town | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | Lund |
| 4.2 | 7 Postal Code | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | 22655 |
| 4.2 | 8 Country code | webuild:insuredPerson / webuild:hasWorkRelation[0] / ncbv:hasActivity[0] / webuild:hasPlaceOfActivity[0] | SE |
| 5 | Status confirmation |  |  |
| 5 | 1 Status confirmation |  |  |
| 6 | Unique Number of Issued Document (Credential) |  |  |
| 6 | 1 Document ID |  | 123456789 |
| 7 | Competent Institution |  |  |
| 7 | 1 InstitutionID |  | 0116415-4 |
| 7 | 2 Institution Name |  | Finnish Centre for Pensions |
| 7 | 3 Country code |  | FI |
| 7 | 4 Office fax N° |  |  |
| 7 | 5 Office phone N° |  | +358 29 411 2816 |
| 7 | 6 E-Mail |  | ulkomaanasiat@etk.fi |
| 7 | 7 Street, N° |  | Insurance of Work Abroad |
| 7 | 8 Town |  | Eläketurvakeskus |
| 7 | 9 Postal Code |  | FI-00065 |
| 7 | 10 Country code |  | FI |


---

## VC example (JSON)

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
  "id": "urn:uuid:0d65edbe-0051-49a2-b812-120a5c1cb81c",
  "type": [
    "VerifiableCredential"
  ],
  "issuer": "did:web:ela.example.fi",
  "validFrom": "2026-02-05T00:00:00Z",
  "validUntil": "2027-02-04T23:59:59Z",
  "credentialSubject": {
    "id": "urn:uuid:8fcb9851-213d-4943-bb8e-a5b1f66ca167",
    "type": "webuild:PDA1Certificate",
    "dcterms:identifier": "FI-ELA-A1-2026-000012345",
    "webuild:applicablePeriod": {
      "type": "webpda1:PeriodOfTime",
      "eu-core:startTime": "2026-02-05T00:00:00Z",
      "eu-core:endTime": "2027-02-04T23:59:59Z"
    },
    "webuild:insuredPerson": {
      "type": "webpda1:Person",
      "ncbv:hasIdentifier": [
        {
          "type": "webpda1:Identifier",
          "eu-core:notation": "010190-123X",
          "eu-core:schemeName": "PersonalID"
        }
      ],
      "eu-core:gender": "male",
      "eu-core:familyName": "Meikäläinen",
      "eu-core:givenName": [
        "Matti"
      ],
      "eu-core:birthName": "Meikäläinen",
      "eu-core:dateOfBirth": "1990-01-01",
      "eu-core:citizenship": [
        "https://publications.europa.eu/resource/authority/country/FIN"
      ],
      "eu-core:registeredAddress": {
        "type": "webpda1:Address",
        "eu-core:thoroughfare": "Keilaranta 13",
        "eu-core:postName": "Espoo",
        "eu-core:postCode": "02150",
        "eu-core:adminUnitLevel1": "FI",
        "eu-core:fullAddress": "Keilaranta 13, 02150 Espoo, FI"
      },
      "eu-core:placeOfBirth": [
        {
          "type": "webpda1:Location",
          "eu-core:adminUnitLevel1": "FI",
          "eu-core:geographicName": "Turku"
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
                "eu-core:legalName": "Konecranes Finland Oy",
                "eu-core:legalidentifier": {
                  "type": "webpda1:Identifier",
                  "eu-core:notation": "FI12345678",
                  "eu-core:schemeName": "BusinessID"
                },
                "eu-core:registeredAddress": {
                  "type": "webpda1:Address",
                  "eu-core:thoroughfare": "Keilaranta 13",
                  "eu-core:postName": "Espoo",
                  "eu-core:postCode": "02150",
                  "eu-core:adminUnitLevel1": "FI",
                  "eu-core:fullAddress": "Keilaranta 13, 02150 Espoo, FI"
                }
              }
            }
          ],
          "ncbv:hasActivity": [
            {
              "type": "webpda1:Activity",
              "webuild:hasFixedPlaceOfActivity": true,
              "webuild:activityCountry": [
                {
                  "type": "webpda1:Location",
                  "eu-core:adminUnitLevel1": "SE"
                }
              ],
              "webuild:hasPlaceOfActivity": [
                {
                  "type": "webpda1:Location"
                }
              ]
            }
          ]
        }
      ]
    },
    "webuild:isSubjectToTransitionalRules": false,
    "webuild:issuingInstitution": [
      {
        "type": "webpda1:Agent",
        "webuild:isLegalEntity": {
          "type": "webpda1:LegalEntity",
          "eu-core:legalName": "Finnish Centre for Pensions",
          "eu-core:legalidentifier": {
            "type": "webpda1:Identifier",
            "eu-core:notation": "FI-ETK-0001",
            "eu-core:schemeName": "InstitutionID"
          },
          "eu-core:registeredAddress": {
            "type": "webpda1:Address",
            "eu-core:thoroughfare": "",
            "eu-core:postName": "",
            "eu-core:postCode": "",
            "eu-core:adminUnitLevel1": "FI",
            "eu-core:fullAddress": ",  , FI"
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
    "webuild:certificateAppliesForDurationOfContract": true,
    "webuild:determinationIsProvisional": false,
    "webuild:statusConfirmation": "01",
    "webuild:hasApplicableJurisdiction": [
      {
        "type": "webpda1:Location",
        "eu-core:adminUnitLevel1": "FI"
      }
    ],
    "webuild:hasCoverage": [
      {
        "type": "webpda1:Coverage",
        "webuild:applicablePeriod": {
          "type": "webpda1:PeriodOfTime",
          "eu-core:startTime": "2026-02-05T00:00:00Z",
          "eu-core:endTime": "2027-02-04T23:59:59Z"
        },
        "webuild:coverageScope": {
          "type": "webpda1:Jurisdiction",
          "eu-core:id": "https://publications.europa.eu/resource/authority/country/FIN",
          "eu-core:name": "Member State legislation"
        },
        "webuild:coverageValidityBasis": "https://example.eu/concept/coverageValidityBasis/statutory"
      }
    ],
    "webuild:hasDetermination": [
      {
        "type": "webpda1:Determination",
        "dcterms:type": "https://example.eu/concept/determinationType/posting"
      }
    ]
  }
}
```
