# PD A1 — Mapping to WE BUILD PD A1 SHACL + VC example (reassessed 2.4 and 2.5)

## Mapping table

| Excel label | Example value | Mapped SHACL path |
| --- | --- | --- |
| PIN | 140269-9999 | webuild:insuredPerson / ncbv:hasIdentifier / eu-core:notation |
| Gender | male | webuild:insuredPerson / eu-core:gender |
| Familyname(s) | af Hällström | webuild:insuredPerson / eu-core:familyName |
| Forename(s) | John Gustav Mikael | webuild:insuredPerson / eu-core:givenName |
| Surname at birth | Hönttöröm | webuild:insuredPerson / eu-core:birthName |
| Forename(s) at birth | Kusteli |  |
| Date of Birth | 14.02.1969 | webuild:insuredPerson / eu-core:dateOfBirth |
| Nationality | Finnish | webuild:insuredPerson / eu-core:citizenship |
| Place of Birth |  | webuild:insuredPerson / eu-core:placeOfBirth |
| Town | Helsingfors | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:geographicName |
| Country code | FI | webuild:insuredPerson / eu-core:placeOfBirth / eu-core:adminUnitLevel1 |
| Address |  |  |
| Address in the state of residence |  |  |
| Street, N° | Löjgränden 3 B 3 | webuild:insuredPerson / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Esbo | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postName |
| Post code | 02170 | webuild:insuredPerson / eu-core:registeredAddress / eu-core:postCode |
| Country code | FI | webuild:insuredPerson / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| Address in the state of stay |  |  |
| Street, N° | Abborgatan 7 | webuild:insuredPerson / ncbv:postalAddress / eu-core:thoroughfare |
| Town | Hässelholm | webuild:insuredPerson / ncbv:postalAddress / eu-core:postName |
| Post code | 22610 | webuild:insuredPerson / ncbv:postalAddress / eu-core:postCode |
| Country code | SE | webuild:insuredPerson / ncbv:postalAddress / eu-core:adminUnitLevel1 |
| Member state | FI | webuild:hasApplicableJurisdiction / eu-core:adminUnitLevel1 |
| Starting date | 1.3.2026 | webuild:applicablePeriod / eu-core:startTime |
| Ending date | 31.12.2026 | webuild:applicablePeriod / eu-core:endTime |
| Certificate applies for the duration of the activity | true | webuild:hasCoverage / webuild:applicablePeriod |
| Determination is provisional | true | webuild:hasDetermination / dcterms:type |
| Transitional rules apply | false | webuild:isSubjectToTransitionalRules |
| Type of Employment | employment | webuild:insuredPerson / webuild:hasWorkRelation / webuild:employmentType |
| Name | Bosses Bullfabrik | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalName |
| EmployerID | 5565878054 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Type of ID | Organisationsnummer Sverige | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |
| Address |  |  |
| Street, N° | Rudeboksvägen 1 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Lund | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |
| Post code | 22655 | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |
| Country code | SE | webuild:insuredPerson / webuild:hasWorkRelation / webuild:hasEmployer / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| No fixed place of work exists |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasFixedPlaceOfActivity (inverse) |
| Country code |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:activityCountry / eu-core:adminUnitLevel1 |
| Place of work |  |  |
| Company/vessel name | Bosses Bullfabrik | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalName |
| Flag Base Home State |  | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:usesOperationalAsset / webuild:flagState (vessel only) |
| CompanyID | 5565878054 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Type of ID | Organisationsnummer Sverige | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:workHost / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:schemeName |
| Street, N° | Rudeboksvägen 1 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:thoroughfare |
| Town | Lund | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postName |
| Postal Code | 22655 | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:postCode |
| Country code | SE | webuild:insuredPerson / webuild:hasWorkRelation / ncbv:hasActivity / webuild:hasPlaceOfActivity / webuild:hasAddress / eu-core:adminUnitLevel1 |
| Status confirmation |  |  |
| Document ID | 123456789 | dcterms:identifier |
| InstitutionID | 0116415-4 | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalidentifier / eu-core:notation |
| Institution Name | Finnish Centre for Pensions | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:legalName |
| Country code | FI | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |
| Office fax N° |  |  |
| Office phone N° | +358 29 411 2816 | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasTelephone |
| E-Mail | ulkomaanasiat@etk.fi | webuild:issuingInstitution / ncbv:hasContactPoint / eu-core:hasEmail |
| Street, N° | Insurance of Work Abroad | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:thoroughfare |
| Town | Eläketurvakeskus | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postName |
| Postal Code | FI-00065 | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:postCode |
| Country code | FI | webuild:issuingInstitution / webuild:isLegalEntity / eu-core:registeredAddress / eu-core:adminUnitLevel1 |


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
  "id": "urn:uuid:9b6acbcf-19be-4a6f-ab78-071dc2e2d475",
  "type": [
    "VerifiableCredential"
  ],
  "issuer": "did:web:ela.example.fi",
  "validFrom": "2026-03-01T00:00:00Z",
  "validUntil": "2026-12-31T00:00:00Z",
  "credentialSubject": {
    "id": "urn:uuid:079fb09f-c021-40b2-949e-2dcc70b8444f",
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
    "webuild:hasDetermination": [
      {
        "type": "webpda1:Determination",
        "dcterms:type": "true"
      }
    ]
  }
}
```
