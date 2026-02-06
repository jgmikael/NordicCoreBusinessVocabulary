# PD A1 — Mapping from example values to WE BUILD PD A1 SHACL + VC example

This file is generated **only** from:

- `PD A1 example.xlsx` (example values)

- `WE BUILD PD A1 (4).ttl` (SHACL shapes)


No additional values were invented. Where a field is required by SHACL but missing in the values sheet, the VC example will be **incomplete w.r.t. SHACL conformance**.


---

## Mapping table

| Code | Excel label | Example value | Mapped SHACL targetClass | Mapped SHACL path | Notes |
| --- | --- | --- | --- | --- | --- |
| 1 | Subject |  |  |  | Section header No value provided in values sheet. |
| 1.1 | PIN | 140269-9999 | eu-core:Person | webuild:insuredPerson / ncbv:hasIdentifier / eu-core:notation |  |
| 1.2 | Gender | male | eu-core:Person | webuild:insuredPerson / eu-core:gender |  |
| 1.3 | Familyname(s) | af Hällström | eu-core:Person | webuild:insuredPerson / eu-core:familyName |  |
| 1.4 | Forename(s) | John Gustav Mikael | eu-core:Person | webuild:insuredPerson / eu-core:givenName |  |
| 1.5 | Surname at birth | Hönttöröm | eu-core:Person | webuild:insuredPerson / eu-core:birthName |  |
| 1.6 | Forename(s) at birth | Kusteli |  |  | No dedicated property in current SHACL for forename(s) at birth (would require additional modelling). |
| 1.7 | Date of Birth | 14.02.1969 | eu-core:Person | webuild:insuredPerson / eu-core:dateOfBirth |  |
| 1.8 | Nationality | Finnish | eu-core:Person | webuild:insuredPerson / eu-core:citizenship |  |
| 1.9 | Place of Birth |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 1.9.1 | Town | Helsingfors | eu-core:Location | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:geographicName |  |
| 1.9.2 | Country code | FI | eu-core:Location | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:adminUnitLevel1 |  |
| 1.10 | Address |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 1.10.1 | Address in the state of residence |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 1.10.1.1 | Street, N° | Löjgränden 3 B 3 | eu-core:Address | webuild:insuredPerson / eu-core:registeredAddress / eu-core:thoroughfare |  |
| 1.10.1.2 | Town | Esbo | eu-core:Address | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postName |  |
| 1.10.1.3 | Post code | 02170 | eu-core:Address | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postCode |  |
| 1.10.1.4 | Country code | FI | eu-core:Address | webuild:insuredPerson / eu-core:registeredAddress / eu-core:adminUnitLevel1 |  |
| 1.10.2 | Address in the state of stay |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 1.10.2.1 | Street, N° | Abborgatan 7 | eu-core:Address | webuild:insuredPerson / ncbv:postalAddress / eu-core:thoroughfare |  |
| 1.10.2.2 | Town | Hässelholm | eu-core:Address | webuild:insuredPerson / ncbv:postalAddress / eu-core:postName |  |
| 1.10.2.3 | Post code | 22610 | eu-core:Address | webuild:insuredPerson / ncbv:postalAddress / eu-core:postCode |  |
| 1.10.2.4 | Country code | SE | eu-core:Address | webuild:insuredPerson / ncbv:postalAddress / eu-core:adminUnitLevel1 |  |
| 2 | Member state legislation which applies |  |  |  | Section header No value provided in values sheet. |
| 2.1 | Member state | FI | webuild:PDA1Certificate | webuild:hasApplicableJurisdiction / eu-core:adminUnitLevel1 |  |
| 2.2 | Starting date | 1.3.2026 | webuild:PDA1Certificate | webuild:applicablePeriod / eu-core:startTime |  |
| 2.3 | Ending date | 31.12.2026 | webuild:PDA1Certificate | webuild:applicablePeriod / eu-core:endTime |  |
| 2.4 | Certificate applies for the duration of the activity | true |  |  | No matching property found in uploaded SHACL. |
| 2.5 | Determination is provisional | true |  |  | No matching property found in uploaded SHACL. |
| 2.6 | Transitional rules apply | false | webuild:PDA1Certificate | webuild:isSubjectToTransitionalRules |  |
| 3 | Details of Employer(s)/Self-employment |  |  |  | Section header No value provided in values sheet. |
| 3.1 | Type of Employment | employment | webuild:Employment | webuild:insuredPerson / webuild:hasWorkRelation / webuild:employmentType |  |
| 3.2 | Name | Bosses Bullfabrik | eu-core:LegalEntity | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalName |  |
| 3.3 | EmployerID | 5565878054 | eu-core:Identifier | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |  |
| 3.4 | Type of ID | Organisationsnummer Sverige | eu-core:Identifier | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |  |
| 3.5 | Address |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 3.5.1 | Street, N° | Rudeboksvägen 1 | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |  |
| 3.5.2 | Town | Lund | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |  |
| 3.5.3 | Post code | 22655 | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |  |
| 3.5.4 | Country code | SE | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |  |
| 4 | Place(s) of work |  |  |  | Section header No value provided in values sheet. |
| 4.1 | No fixed place of work exists |  | webuild:Activity | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasFixedPlaceOfActivity (inverted from "No fixed place") | No value provided in values sheet. |
| 4.1.1 | Country code |  | webuild:Activity | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:activityCountry / eu-core:adminUnitLevel1 | No value provided in values sheet. |
| 4.2 | Place of work |  |  |  | No suitable mapping found in uploaded SHACL. No value provided in values sheet. |
| 4.2.1 | Company/vessel name | Bosses Bullfabrik | eu-core:LegalEntity | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalName |  |
| 4.2.2 | Flag Base Home State |  |  |  | Vessel/flag-state scenario; SHACL supports via webuild:OperationalAsset/webuild:flagState but no value provided. No value provided in values sheet. |
| 4.2.3 | CompanyID | 5565878054 | eu-core:Identifier | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |  |
| 4.2.4 | Type of ID | Organisationsnummer Sverige | eu-core:Identifier | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |  |
| 4.2.5 | Street, N° | Rudeboksvägen 1 | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:thoroughfare |  |
| 4.2.6 | Town | Lund | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postName |  |
| 4.2.7 | Postal Code | 22655 | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postCode |  |
| 4.2.8 | Country code | SE | eu-core:Address | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:adminUnitLevel1 |  |
| 5 | Status confirmation |  |  |  | Section header No value provided in values sheet. |
| 5.1 | Status confirmation |  |  |  | No matching property found in uploaded SHACL (status confirmation not modelled). No value provided in values sheet. |
| 6 | Unique Number of Issued Document (Credential) |  |  |  | Section header No value provided in values sheet. |
| 6.1 | Document ID | 123456789 | webuild:PDA1Certificate | dcterms:identifier |  |
| 7 | Competent Institution |  |  |  | Section header No value provided in values sheet. |
| 7.1 | InstitutionID | 0116415-4 | eu-core:Identifier | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |  |
| 7.2 | Institution Name | Finnish Centre for Pensions | eu-core:LegalEntity | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalName |  |
| 7.3 | Country code | FI | eu-core:Address | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |  |
| 7.4 | Office fax N° |  |  |  | SHACL ContactPoint has email/telephone; no fax-specific property; fax value missing anyway. No value provided in values sheet. |
| 7.5 | Office phone N° | +358 29 411 2816 | eu-core:ContactPoint | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasTelephone |  |
| 7.6 | E-Mail | ulkomaanasiat@etk.fi | eu-core:ContactPoint | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasEmail |  |
| 7.7 | Street, N° | Insurance of Work Abroad | eu-core:Address | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |  |
| 7.8 | Town | Eläketurvakeskus | eu-core:Address | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |  |
| 7.9 | Postal Code | FI-00065 | eu-core:Address | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |  |
| 7.10 | Country code | FI | eu-core:Address | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |  |


---

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
  "id": "urn:uuid:0703bb19-fbbb-4214-9911-9e160c6bc8cd",
  "type": [
    "VerifiableCredential"
  ],
  "issuer": "did:web:ela.example.fi",
  "validFrom": "2026-03-01T00:00:00Z",
  "validUntil": "2026-12-31T00:00:00Z",
  "credentialSubject": {
    "id": "urn:uuid:7420988a-d899-47b3-b255-97b2a3d0737e",
    "type": "webuild:PDA1Certificate",
    "dcterms:identifier": "123456789",
    "webuild:applicablePeriod": {
      "type": "webpda1:PeriodOfTime",
      "eu-core:startTime": "2026-03-01T00:00:00Z",
      "eu-core:endTime": "2026-12-31T00:00:00Z"
    },
    "webuild:isSubjectToTransitionalRules": false,
    "webuild:hasApplicableJurisdiction": [
      {
        "type": "webpda1:Location",
        "eu-core:adminUnitLevel1": "FI"
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
