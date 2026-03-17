# Posted Worker Notification (PWN) – SHACL Data Model Overview

This document provides an easy‑to‑understand description of the **WE BUILD Posted Worker Notification (PWN)** data model expressed as a SHACL Shape. 
It is structured according to the logical parts of the original attestation form and maps each section to:

- The relevant **SHACL NodeShapes and PropertyShapes** in the PWN model
- The corresponding **original attestation data elements** listed in the Excel mapping table (first tab)

The purpose of this document is to support implementers and domain experts in understanding how the semantic model corresponds to the traditional form‑based structure.

## 1. Overall Structure of the SHACL Model

The SHACL model is centered on the node **`webpwn:PostedWorkerNotification`**, which aggregates all core parts of the attestation.

The following NodeShapes structure the model logically:

- `webpwn:Address`
- `webpwn:Agent`
- `webpwn:ContactPoint`
- `webpwn:Country`
- `webpwn:Employment`
- `webpwn:Identifier`
- `webpwn:Jurisdiction`
- `webpwn:LegalEntity`
- `webpwn:Location`
- `webpwn:Occupation`
- `webpwn:Participation`
- `webpwn:PeriodOfTime`
- `webpwn:Person`
- `webpwn:PostedWorkerNotification`
- `webpwn:PublicOrganization`
- `webpwn:SocialSecurityDetermination`
- `webpwn:WorkActivity`
- `webpwn:WorkAssignment`

## 1. Subject

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:Person`
- Supporting nodes: `webpwn:Address`, `webpwn:Country`, `webpwn:Occupation`, `webpwn:Identifier`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 1.1 PIN | Personal Identification Number/ ID number |
| 1.2 Gender |  |
| 1.3 Familyname(s) |  |
| 1.4 Forename(s) |  |
| 1.5 Surname at birth |  |
| 1.6 Forename(s) at birth |  |
| 1.7 Date of Birth |  |
| 1.8 Nationality |  |
| 1.9 Job Title in Home Country |  |
| 1.9 Place of Birth |  |
| 1.9.1 Town |  |
| 1.9.2 Country code |  |
| 1.10 Address |  |
| 1.10.1 Address in the state of residence |  |
| 1.10.1.1 Street, N° |  |
| 1.10.1.2 Town |  |
| 1.10.1.3 Post code |  |
| 1.10.1.4 Country code |  |
| 1.10.2 Address in the state of stay |  |
| 1.10.2.1 Street, N° |  |
| 1.10.2.2 Town |  |
| 1.10.2.3 Post code |  |
| 1.10.2.4 Country code |  |

## 2. Assignment related information

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:Employment`, `webpwn:WorkAssignment`, `webpwn:PeriodOfTime`
- Supporting nodes: `webpwn:Jurisdiction`, `webpwn:SocialSecurityDetermination`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 2.1 Home Member state |  |
| 2.2 Starting date |  |
| 2.3 Ending date |  |
| 2.4 Certificate applies for the duration of the activity |  |
| 2.5 Determination is provisional |  |
| 2.6 Transitional rules apply |  |

## 3. Details of Employer(s)/Self-employment

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:LegalEntity`, `webpwn:Identifier`, `webpwn:Address`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 3.1 Type of Employment (Temporary?) |  |
| 3.2 Name |  |
| 3.3 EmployerID |  |
| 3.4 Type of ID |  |
| 3.5 Address |  |
| 3.5.1 Street, N° |  |
| 3.5.2 Town |  |
| 3.5.3 Post code |  |
| 3.5.4 Country code |  |

## 4. Place(s) of work

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:Location`, `webpwn:WorkActivity`, `webpwn:LegalEntity`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 4.1 No fixed place of work exists |  |
| 4.1.1 Country code |  |
| 4.2 Place of work |  |
| 4.2.1 Company/vessel name |  |
| 4.2.2 Flag Base Home State |  |
| 4.2.3 CompanyID |  |
| 4.2.4 Type of ID  |  |
| 4.2.5 Street, N° |  |
| 4.2.6 Town |  |
| 4.2.7 Postal Code |  |
| 4.2.8 Country code |  |

## 5. Status confirmation

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:SocialSecurityDetermination`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 5.1 Status confirmation |  |

## 6. Unique Number of Issued Document (Credential)

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:PostedWorkerNotification`, `webpwn:Identifier`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 6.1 Document ID |  |

## 7. Competent Institution

### Description
This section corresponds directly to the logical block in the original attestation.

### Mapping to SHACL Model (Conceptual)
- NodeShape: `webpwn:PublicOrganization`, `webpwn:ContactPoint`, `webpwn:Address`

### Mapping to Original Attestation Data Elements

| Original Data Element | Description |
|---|---|
| 7.1 InstitutionID |  |
| 7.2 Institution Name |  |
| 7.3 Country code |  |
| 7.4 Office fax N° |  |
| 7.5 Office phone N° |  |
| 7.6 E-Mail |  |
| 7.7 Street, N° |  |
| 7.8 Town |  |
| 7.9 Postal Code |  |
| 7.10 Country code |  |
| Details of Home Employer(s)/Self-employment |  |
| Company (name / full commercial firm name) |  |
| Industry Sector (NACE) |  |
| Construction Sector (Yes/No) |  |
| VAT identification number |  |
| Address Line 1 |  |
| Address Line 2 |  |
| Postal code (company headquarters) |  |
| City (company headquarters) |  |
| Municipality |  |
| State |  |
| Country (company headquarters) |  |
| Phone number |  |
| Email Address |  |
| Administrative Represenative |  |
| Last Name |  |
| First Name |  |
| Telephone Number |  |
| Email Address |  |
| Address Line 1 |  |
| Address Line 2 |  |
| Postal code  |  |
| City  |  |
| Municipality |  |
| State |  |
| Country  |  |
| Social Represenative |  |
| Last Name |  |
| First Name |  |
| Telephone Number |  |
| Email Address |  |
| Address Line 1 |  |
| Address Line 2 |  |
| Postal code  |  |
| City  |  |
| Municipality |  |
| State |  |
| Country  |  |
| Host Company |  |
| Company (name / full commercial firm name) |  |
| Email address |  |
| Telephone Number |  |
| Industry Sector |  |
| VAT identification number |  |
| Address Line 1 |  |
| Address Line 2 |  |
| Postal code (company headquarters) |  |
| City (company headquarters) |  |
| Municipality |  |
| State |  |
| Country (company headquarters) |  |
| Employee |  |
| Job Duties (Activities abroad) |  |
