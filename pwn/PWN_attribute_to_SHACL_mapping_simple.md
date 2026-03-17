# PWN attribute to SHACL mapping

| attribute | SHACL property | SHACL class (node) | SHACL Range |
|---|---|---|---|
| `1.1 PIN` | `webpwn:hasIdentifier` | `webpwn:Person` | `webpwn:Identifier` |
| `1.2 Gender` | `webpwn:gender` | `webpwn:Person` | `xsd:string` |
| `1.3 Familyname(s)` | `webpwn:familyName` | `webpwn:Person` | `xsd:string` |
| `1.4 Forename(s)` | `webpwn:givenName` | `webpwn:Person` | `xsd:string` |
| `1.5 Surname at birth` | `webpwn:birthName` | `webpwn:Person` | `xsd:string` |
| `1.6 Forename(s) at birth` | `webpwn:birthName` | `webpwn:Person` | `xsd:string` |
| `1.7 Date of Birth` | `webpwn:dateOfBirth` | `webpwn:Person` | `xsd:date` |
| `1.8 Nationality` | `webpwn:citizenship` | `webpwn:Person` | `webpwn:Jurisdiction` |
| `1.9 Job Title in Home Country` | `webpwn:hasOccupation` | `webpwn:Person` | `webpwn:Occupation` |
| `1.9 Place of Birth` | `webpwn:placeOfBirth` | `webpwn:Person` | `webpwn:Location` |
| `1.9.1 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `1.9.2 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `1.10 Address` | `webpwn:domicile` | `webpwn:Person` | `webpwn:Address` |
| `1.10.1 Address in the state of residence` | `webpwn:domicile` | `webpwn:Person` | `webpwn:Address` |
| `1.10.1.1 Street, N°` | `webpwn:thoroughfare` | `webpwn:Address` | `xsd:string` |
| `1.10.1.1 Street, N°` | `webpwn:locatorDesignator` | `webpwn:Address` | `xsd:string` |
| `1.10.1.2 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `1.10.1.3 Post code` | `webpwn:postCode` | `webpwn:Address` | `xsd:string` |
| `1.10.1.4 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `1.10.2 Address in the state of stay` | `webpwn:hasTemporaryStayAddress` | `webpwn:Person` | `webpwn:Address` |
| `1.10.2.1 Street, N°` | `webpwn:thoroughfare` | `webpwn:Address` | `xsd:string` |
| `1.10.2.1 Street, N°` | `webpwn:locatorDesignator` | `webpwn:Address` | `xsd:string` |
| `1.10.2.2 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `1.10.2.3 Post code` | `webpwn:postCode` | `webpwn:Address` | `xsd:string` |
| `1.10.2.4 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `2.1 Home Member state` | `webpwn:hasApplicableJurisdiction` | `webpwn:WorkAssignment` | `webpwn:Jurisdiction` |
| `2.2 Starting date` | `webpwn:startTime` | `webpwn:PeriodOfTime` | `xsd:date` |
| `2.3 Ending date` | `webpwn:endTime` | `webpwn:PeriodOfTime` | `xsd:date` |
| `2.4 Certificate applies for the duration of the activity` | `webpwn:fullPeriodCoverageIndicator` | `webpwn:SocialSecurityDetermination` | `xsd:boolean` |
| `2.5 Determination is provisional` | `webpwn:isProvisionalDetermination` | `webpwn:SocialSecurityDetermination` | `xsd:boolean` |
| `2.6 Transitional rules apply` | `webpwn:isSubjectToTransitionalRules` | `webpwn:SocialSecurityDetermination` | `xsd:boolean` |
| `3.1 Type of Employment (Temporary?)` | `webpwn:employmentType` | `webpwn:Employment` | `skos:Concept` |
| `3.2 Name` | `webpwn:legalName` | `webpwn:LegalEntity` | `xsd:string` |
| `3.3 EmployerID` | `webpwn:legalidentifier` | `webpwn:LegalEntity` | `webpwn:Identifier` |
| `3.4 Type of ID` | `webpwn:schemeName` | `webpwn:Identifier` | `xsd:string` |
| `3.5 Address` | `webpwn:registeredAddress` | `webpwn:LegalEntity` | `webpwn:Address` |
| `3.5.1 Street, N°` | `webpwn:thoroughfare` | `webpwn:Address` | `xsd:string` |
| `3.5.1 Street, N°` | `webpwn:locatorDesignator` | `webpwn:Address` | `xsd:string` |
| `3.5.2 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `3.5.3 Post code` | `webpwn:postCode` | `webpwn:Address` | `xsd:string` |
| `3.5.4 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `4.1 No fixed place of work exists` | `webpwn:noFixedPlaceOfWork` | `webpwn:WorkAssignment` | `xsd:boolean` |
| `4.1.1 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `4.2 Place of work` | `webpwn:hasWorkLocation` | `webpwn:WorkAssignment` | `webpwn:Location` |
| `4.2.1 Company/vessel name` | `webpwn:vesselName` | `webpwn:WorkAssignment` | `xsd:string` |
| `4.2.1 Company/vessel name` | `webpwn:legalName` | `webpwn:LegalEntity` | `xsd:string` |
| `4.2.2 Flag Base Home State` | `webpwn:flagStateCode` | `webpwn:WorkAssignment` | `xsd:string` |
| `4.2.3 CompanyID` | `webpwn:legalidentifier` | `webpwn:LegalEntity` | `webpwn:Identifier` |
| `4.2.4 Type of ID` | `—` | `—` | `—` |
| `4.2.5 Street, N°` | `webpwn:thoroughfare` | `webpwn:Address` | `xsd:string` |
| `4.2.5 Street, N°` | `webpwn:locatorDesignator` | `webpwn:Address` | `xsd:string` |
| `4.2.6 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `4.2.7 Postal Code` | `webpwn:postCode` | `webpwn:Address` | `xsd:string` |
| `4.2.8 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `5.1 Status confirmation` | `webpwn:confirmationStatus` | `webpwn:PostedWorkerNotification` | `skos:Concept` |
| `6.1 Document ID` | `webpwn:hasIdentifier` | `webpwn:PostedWorkerNotification` | `webpwn:Identifier` |
| `6.1 Document ID` | `webpwn:notation` | `webpwn:Identifier` | `xsd:string` |
| `7.1 InstitutionID` | `webpwn:legalidentifier` | `webpwn:PublicOrganization` | `webpwn:Identifier` |
| `7.2 Institution Name` | `webpwn:legalName` | `webpwn:PublicOrganization` | `xsd:string` |
| `7.2 Institution Name` | `webpwn:preferredLabel` | `webpwn:PublicOrganization` | `xsd:string` |
| `7.3 Country code` | `webpwn:hasApplicableJurisdiction` | `webpwn:PublicOrganization` | `webpwn:Jurisdiction` |
| `7.4 Office fax N°` | `—` | `—` | `—` |
| `7.5 Office phone N°` | `webpwn:hasTelephone` | `webpwn:ContactPoint` | `xsd:string` |
| `7.6 E-Mail` | `webpwn:hasEmail` | `webpwn:ContactPoint` | `xsd:string` |
| `7.7 Street, N°` | `webpwn:thoroughfare` | `webpwn:Address` | `xsd:string` |
| `7.7 Street, N°` | `webpwn:locatorDesignator` | `webpwn:Address` | `xsd:string` |
| `7.8 Town` | `webpwn:postName` | `webpwn:Address` | `xsd:string` |
| `7.9 Postal Code` | `webpwn:postCode` | `webpwn:Address` | `xsd:string` |
| `7.10 Country code` | `webpwn:hasCountry` | `webpwn:Address` | `webpwn:Country` |
| `Details of Home Employer(s)/Self-employment` | `—` | `—` | `—` |
| `Company (name / full commercial firm name)` | `—` | `—` | `—` |
| `Industry Sector (NACE)` | `—` | `—` | `—` |
| `Construction Sector (Yes/No)` | `—` | `—` | `—` |
| `VAT identification number` | `—` | `—` | `—` |
| `Address Line 1` | `—` | `—` | `—` |
| `Address Line 2` | `—` | `—` | `—` |
| `Postal code (company headquarters)` | `—` | `—` | `—` |
| `City (company headquarters)` | `—` | `—` | `—` |
| `Municipality` | `—` | `—` | `—` |
| `State` | `—` | `—` | `—` |
| `Country (company headquarters)` | `—` | `—` | `—` |
| `Phone number` | `—` | `—` | `—` |
| `Email Address` | `—` | `—` | `—` |
| `Administrative Represenative` | `—` | `—` | `—` |
| `Last Name` | `—` | `—` | `—` |
| `First Name` | `—` | `—` | `—` |
| `Telephone Number` | `—` | `—` | `—` |
| `Email Address` | `—` | `—` | `—` |
| `Address Line 1` | `—` | `—` | `—` |
| `Address Line 2` | `—` | `—` | `—` |
| `Postal code` | `—` | `—` | `—` |
| `City` | `—` | `—` | `—` |
| `Municipality` | `—` | `—` | `—` |
| `State` | `—` | `—` | `—` |
| `Country` | `—` | `—` | `—` |
| `Social Represenative` | `—` | `—` | `—` |
| `Last Name` | `—` | `—` | `—` |
| `First Name` | `—` | `—` | `—` |
| `Telephone Number` | `—` | `—` | `—` |
| `Email Address` | `—` | `—` | `—` |
| `Address Line 1` | `—` | `—` | `—` |
| `Address Line 2` | `—` | `—` | `—` |
| `Postal code` | `—` | `—` | `—` |
| `City` | `—` | `—` | `—` |
| `Municipality` | `—` | `—` | `—` |
| `State` | `—` | `—` | `—` |
| `Country` | `—` | `—` | `—` |
| `Host Company` | `—` | `—` | `—` |
| `Company (name / full commercial firm name)` | `—` | `—` | `—` |
| `Email address` | `—` | `—` | `—` |
| `Telephone Number` | `—` | `—` | `—` |
| `Industry Sector` | `—` | `—` | `—` |
| `VAT identification number` | `—` | `—` | `—` |
| `Address Line 1` | `—` | `—` | `—` |
| `Address Line 2` | `—` | `—` | `—` |
| `Postal code (company headquarters)` | `—` | `—` | `—` |
| `City (company headquarters)` | `—` | `—` | `—` |
| `Municipality` | `—` | `—` | `—` |
| `State` | `—` | `—` | `—` |
| `Country (company headquarters)` | `—` | `—` | `—` |
| `Employee` | `—` | `—` | `—` |
| `Job Duties (Activities abroad)` | `—` | `—` | `—` |