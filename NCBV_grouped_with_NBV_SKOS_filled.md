# Nordic Core Business Vocabulary (NCBV)

This documentation is generated from two Turtle files:

- **NCBV ontology** (OWL)
- **NBV / Nordic Core Business Terminology** (SKOS)

All content is derived directly from those files. SKOS `prefLabel` and `definition` values are resolved from the NBV terminology for each linked concept.

## Contents

- [Classes and their properties](#classes-and-their-properties)
- [Ungrouped properties](#ungrouped-properties)

## Classes and their properties

### Address

- **IRI:** `https://iri.suomi.fi/model/ncbv/Address`
- **Description:** An identification of the fixed location of a geographic place.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-4` | address | an identification of the fixed location of a geographic place |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Admin Unit Level 1 | `https://iri.suomi.fi/model/ncbv/adminUnitLevel1` | Literal | The uppermost administrative unit for the address, almost always a country. | — | — | — |
| Admin Unit Level 2 | `https://iri.suomi.fi/model/ncbv/adminUnitLevel2` | Literal | The name of a secondary level/region of the address, usually a county, state or other such area that typically encompasses several localities. | — | — | — |
| Care of | `https://iri.suomi.fi/model/ncbv/careOf` | Literal | Used when an address is at the address of another person or legal entity.
 | — | — | — |
| Full Address | `https://iri.suomi.fi/model/ncbv/fullAddress` | Literal | The complete address written as a string. | — | — | — |
| Locator Designator | `https://iri.suomi.fi/model/ncbv/locatorDesignator` | Literal | A number or a sequence of characters that uniquely identifies the locator within the relevant scope. | — | — | — |
| Locator Name | `https://iri.suomi.fi/model/ncbv/locatorName` | Literal | Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building. | — | — | — |
| Post Code | `https://iri.suomi.fi/model/ncbv/postCode` | Literal | The code created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points. | — | — | — |
| Post Name | `https://iri.suomi.fi/model/ncbv/postName` | Literal | A name created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points. | — | — | — |
| Post Office Box | `https://iri.suomi.fi/model/ncbv/postOfficeBox` | Literal | A location designator for a postal delivery point at a post office, usually a number. | — | — | — |
| Thoroughfare | `https://iri.suomi.fi/model/ncbv/thoroughfare` | Literal | The name of a passage or way through from one location to another. | — | — | — |

### Agent

- **IRI:** `https://iri.suomi.fi/model/ncbv/Agent`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-41` | agent | an entity that is able to carry out actions |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Grants Mandate | `https://iri.suomi.fi/model/ncbv/grantsMandate` | Mandate | — | — | — | — |
| Has Member | `https://iri.suomi.fi/model/ncbv/hasMember` | Membership | — | — | — | — |

### Amount

- **IRI:** `https://iri.suomi.fi/model/ncbv/MonetaryAmount`
- **Description:** see unece:Amount and schema:MonetaryAmount

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-85` | monetary amount | TBD |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Currency | `https://iri.suomi.fi/model/ncbv/currency` | Literal | The currency in which the monetary amount is expressed. ISO 4217 currency format, e.g. "EUR". | — | — | — |
| Value | `https://iri.suomi.fi/model/ncbv/value` | Literal | — | — | — | — |

### Beneficial Owner

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwner`
- **Description:** A natural person(s) who ultimately owns or controls the agent.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-3002` | beneficial owner | a person or persons who ultimately owns or controls an agent |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Is a Person | `https://iri.suomi.fi/model/ncbv/isPerson` | Person | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Interest Control | `https://iri.suomi.fi/model/ncbv/interestControl` | Literal | Extent of the control. 25%, 25-50%, 50%, 50-75%, 75%, 100% | — | — | — |
| Interest Direct Or Indirect | `https://iri.suomi.fi/model/ncbv/interestDirectOrIndirect` | Literal | How directly the interest is exercised by the interested party. The value MUST be 'indirect' if intermediate entities or agents are known to exist, and MUST be 'direct' if such intermediaries are known not to exist. Otherwise the value MUST be 'unknown'. | — | — | — |
| Interest Type | `https://iri.suomi.fi/model/ncbv/interestType` | Literal | The type of interest held by a Natural person in an agent. In Sweden this is free text but can have enum like: shareholding, votingRights, appointmentOfBoard, otherInfluenceOrControl, ,seniorManagingOfficial, settlor, trustee, protector, beneficiaryOfLegalArrangement, rightsToSurplusAssetsOnDissolution, rightsToProfitOrIncome, rightsGrantedByContract, conditionalRightsGrantedByContract, controlViaCompanyRulesOrArticles, controlByLegalFramework, boardMember, boardChair, unknownInterest, unpublishedInterest, enjoymentAndUseOfAssets, rightToProfitOrIncomeFromAssets | — | — | — |

### Beneficial Owner Role

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwnerRole`
- **Description:** —

### Code

- **IRI:** `https://iri.suomi.fi/model/ncbv/Code`
- **Description:** A generic class for any code values that a specific class can have; in the NCBV the Code class contains code values for legal form, legal status and (economic) activity.  

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Code | `https://iri.suomi.fi/model/ncbv/codeValue` | Literal | The actual code value from a selected code list. | — | — | — |
| Identifier | `https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | The identifier of a mandate is used to separate different mandates from each other, making it unique. | — | — | — |
| Name | `https://iri.suomi.fi/model/ncbv/name` | Literal | A word or a combination of characters by which an entity/agent/thing is designated, called, or known. | `https://iri.suomi.fi/terminology/nbvoc/concept-18` | name | a word or a combination of characters by which an agent is designated, called, or known |
| Sequence | `https://iri.suomi.fi/model/ncbv/sequence` | Literal | An indicator for the order of a series of values; "1, 2, 3..." | — | — | — |

### Composite Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/CompositeRepresentationRule`
- **Description:** A class that replaces the "Complex Representation Rule" in previous NCBV versions; example of a composite rule for general signatory rights (legal representation): "CEO alone and two board members jointly"

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-82` | composite representation rule | a representation rule that consist of two or more role or membership based representation rules |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| And | `https://iri.suomi.fi/model/ncbv/and` | Representation Rule (Signatory Rule) | — | — | — | — |
| Or | `https://iri.suomi.fi/model/ncbv/or` | Representation Rule (Signatory Rule) | — | — | — | — |

### Contact Point

- **IRI:** `https://iri.suomi.fi/model/ncbv/ContactPoint`
- **Description:** Information (e.g. e-mail address, telephone number) of a person or department through which the user can get in touch with. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6044` | contact point | information through which one can get in touch with a person or a legal entity |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Contact Page | `https://iri.suomi.fi/model/ncbv/contactPage` | Literal | A web page that could be used to reach out the Contact Point. | — | — | — |
| Has Email | `https://iri.suomi.fi/model/ncbv/email` | Literal | An electronic address through which the Contact Point can be contacted.

Equivalent with schema:email | — | — | — |
| Has Telephone | `https://iri.suomi.fi/model/ncbv/hasTelephone` | Literal | — | — | — | — |

### Document

- **IRI:** `https://iri.suomi.fi/model/ncbv/Document`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-93` | document | TBD |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Title | `https://iri.suomi.fi/model/ncbv/title` | Literal | — | — | — | — |

### Identifier

- **IRI:** `https://iri.suomi.fi/model/ncbv/Identifier`
- **Description:** A unique set of characters used to identify the legal entity. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-7` | identifier | a structured reference that identifies an entity |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Date of Issue | `https://iri.suomi.fi/model/ncbv/dateOfIssue` | Literal | The date on which the something was issued; in this context for instance a Mandate or an Identifier. | — | — | — |
| Identifier | `https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | The identifier of a mandate is used to separate different mandates from each other, making it unique. | — | — | — |
| Notation | `https://iri.suomi.fi/model/ncbv/notation` | Literal | A string of characters to uniquely identify a concept. | — | — | — |
| Schema Agency | `https://iri.suomi.fi/model/ncbv/schemaAgency` | Literal | The name of the agency that issued the identifier. | — | — | — |
| Scheme Name | `https://iri.suomi.fi/model/ncbv/schemeName` | Literal | Name of the scheme used to construct the identifier. | — | — | — |
| Scheme URI | `https://iri.suomi.fi/model/ncbv/schemeURI` | Literal | URI of the scheme used to construct the identifier. | — | — | — |

### Legal Entity

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalEntity`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6006` | legal entity | a formal organization that is involved in economic activity |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Activity | `https://iri.suomi.fi/model/ncbv/hasActivity` | Code | An active deed or action carried out by a legal entity | — | — | — |
| Beneficial Owners | `https://iri.suomi.fi/model/ncbv/beneficialOwners` | Beneficial Owner | A natural person(s) who ultimately owns or controls the agent. | — | — | — |
| Contact Point | `https://iri.suomi.fi/model/ncbv/hasContactPoint` | Contact Point | The main contact information of the resource. | — | — | — |
| Identifier | `https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — | — |
| Legal Form | `https://iri.suomi.fi/model/ncbv/hasLegalForm` | Code | The legal form of a legal entity. | `https://iri.suomi.fi/terminology/nbvoc/concept-16` | legal form | a legal structure according to national legislation |
| Legal Identifier | `https://iri.suomi.fi/model/ncbv/legalIdentifier` | Identifier | An identifier that is given to a legal entity at registration. | — | — | — |
| Legal Status | `https://iri.suomi.fi/model/ncbv/hasLegalStatus` | Legal Status | An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity. | `https://iri.suomi.fi/terminology/nbvoc/concept-23` | legal status | an indication of whether a registration authority has registered some extraordinary proceedings for the legal entity |
| Postal Address | `https://iri.suomi.fi/model/ncbv/postalAddress` | Address | The address to which mail can be sent to the legal entity. | — | — | — |
| Registered Address | `https://iri.suomi.fi/model/ncbv/registeredAddress` | Address | The address to which formal communications can be sent to the legal entity. | — | — | — |
| Share Capital | `https://iri.suomi.fi/model/ncbv/hasShareCapital` | Share Capital | The total registered share capital for the legal entity. | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Alternative Name | `https://iri.suomi.fi/model/ncbv/alternativeName` | Literal | Any other registered name by which a legal entity is known. | — | — | — |
| Legal Name | `https://iri.suomi.fi/model/ncbv/legalName` | Literal | — | `https://iri.suomi.fi/terminology/nbvoc/concept-105` | legal name | a name under which the legal entity is registered |
| Registration Date | `https://iri.suomi.fi/model/ncbv/registrationDate` | Literal | The date when a public authority has registered the legal entity. | `https://iri.suomi.fi/terminology/nbvoc/concept-22` | registration date | The date when a public authority has registered the registered organisation |

### Legal Resource

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalResource`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-90` | legal resource | TBD |

### Legal Status

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalStatus`
- **Description:** An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-23` | legal status | an indication of whether a registration authority has registered some extraordinary proceedings for the legal entity |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Has Code | `https://iri.suomi.fi/model/ncbv/hasCode` | Code | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Date | `https://iri.suomi.fi/model/ncbv/date` | Literal | The date when the legal status was registered. | — | — | — |

### Location

- **IRI:** `https://iri.suomi.fi/model/ncbv/Location`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-86` | location | TBD |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Geographic Identifier | `https://iri.suomi.fi/model/ncbv/geographicIdentifier` | Literal | — | — | — | — |
| Geographic Name | `https://iri.suomi.fi/model/ncbv/geographicName` | Literal | A recognizable name for a place, like "Eiffel Tower" or "Madrid".  | — | — | — |

### Mandate

- **IRI:** `https://iri.suomi.fi/model/ncbv/Mandate`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-75` | mandate | the terms under which a mandator grants or delegates authority or power to a mandatee |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| (Has) Geographical Scope/ Has Location / (Has) Geographical Coverage | `https://iri.suomi.fi/model/ncbv/hasGeographicalScope` | Location | The association geographical scope points at a location; this describes the geographic region the mandate is valid.   | — | — | — |
| (Has) Mandator | `https://iri.suomi.fi/model/ncbv/hasMandator` | Agent | The Mandator association points always to the "primary mandator", who is the original source of the delegated power. | `https://iri.suomi.fi/terminology/nbvoc/concept-76` | mandator | an agent that grants authority to another agent to act on its behalf |
| Has Duration | `https://iri.suomi.fi/model/ncbv/hasDuration` | Period of Time | The association "has duration" points to "Period of Time"and indicates the validity period of the mandate; like "1.1.2025-31.12.2025" | — | — | — |
| Has Representation Rule | `https://iri.suomi.fi/model/ncbv/hasRepresentationRule` | Representation Rule (Signatory Rule) | — | — | — | — |
| Has Restriction | `https://iri.suomi.fi/model/ncbv/hasRestriction` | Restriction | — | — | — | — |
| Has Scope | `https://iri.suomi.fi/model/ncbv/hasScope` | Scope | — | — | — | — |
| Has Source | `https://iri.suomi.fi/model/ncbv/hasSource` | Source | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Date of Issue | `https://iri.suomi.fi/model/ncbv/dateOfIssue` | Literal | The date on which the something was issued; in this context for instance a Mandate or an Identifier. | — | — | — |
| Delegable | `https://iri.suomi.fi/model/ncbv/delegable` | Literal | An indicator of whether the Mandate can be delegated or not. | `https://iri.suomi.fi/terminology/nbvoc/concept-79` | delegable | capable of being delegated |
| Identifier | `https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | The identifier of a mandate is used to separate different mandates from each other, making it unique. | — | — | — |
| Modified | `https://iri.suomi.fi/model/ncbv/modified` | Literal | The date of the last update of something like a Mandate.

upper attribute
http://purl.org/dc/terms/modified


dcterms:modified | — | — | — |
| Status | `https://iri.suomi.fi/model/ncbv/status` | Literal | A mandate's status can be for instance: active, withdrawn/inactive > Tore checks values 

Upper attribute: adms:status | — | — | — |

### Mandate Transfer

- **IRI:** `https://iri.suomi.fi/model/ncbv/MandateTransfer`
- **Description:** A class for documenting the possible transfer (or delegation) of a Mandate from a previous Mandatee to another; example: Mandate is granted by CEO of Company, is delegable, the first Mandatee delegated the Mandate to another Agent who becomes the new Mandatee; the transfer of the Mandate is logged in this class.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-89` | mandate transfer | TBD |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Mandatee | `https://iri.suomi.fi/model/ncbv/mandatee` | Agent | — | — | — | — |
| Original Mandate | `https://iri.suomi.fi/model/ncbv/originalMandate` | Mandate | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Date | `https://iri.suomi.fi/model/ncbv/date` | Literal | The date when the legal status was registered. | — | — | — |
| Identifier | `https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | The identifier of a mandate is used to separate different mandates from each other, making it unique. | — | — | — |

### Membership

- **IRI:** `https://iri.suomi.fi/model/ncbv/Membership`
- **Description:** The Membership class describes certain types of relationships between agents (persons and legal entities). 

A person can be a member of an association, employed by a company, be a board member in or the CEO of a limited company.

The official definition of Membership can be found here: 
https://www.w3.org/TR/vocab-org/#org:Membership

This technical note does not change the content of the official definition of the Membership class.

Upper class: 
https://www.w3.org/ns/org#Membership

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-78` | membership | a structured way to represent an agent's participation in an other agent (usually an organization) |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Member | `https://iri.suomi.fi/model/ncbv/member` | Agent | — | — | — | — |
| Role | `https://iri.suomi.fi/model/ncbv/hasRole` | Role | Indicates the Role that the Agent plays in a Membership relationship with a legal entity. | — | — | — |

### Membership Based Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/MembershipBasedRepresentationRule`
- **Description:** A class that replaces the previous "Simple Representation Rule" class (partially); example: a mandate granted to "a man on the street", pointing at a certain person as a  Member of the Mandator (Membership in this case could be "mandatee" or similar).

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-84` | membership based representation rule | a representation rule where the rule is based on the membership relation between agents |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Defines Valid Membership | `https://iri.suomi.fi/model/ncbv/definesValidMembership` | Membership | The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or. | — | — | — |
| Member Quantifier | `https://iri.suomi.fi/model/ncbv/memberQuantifier` | Concept | Specifies a qualitative quantity or proportion of members required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”). | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Minimum Number of Members | `https://iri.suomi.fi/model/ncbv/minimumNumberOfMembers` | Literal | The number of members required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5... | — | — | — |

### Object

- **IRI:** `https://iri.suomi.fi/model/ncbv/Object`
- **Description:** Example: can be a specific house, car; has an Identifier (car registration number)

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-87` | object | TBD |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Identifier | `https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — | — |
| Type | `https://iri.suomi.fi/model/ncbv/type` | Concept | — | — | — | — |

### Period of Time

- **IRI:** `https://iri.suomi.fi/model/ncbv/PeriodOfTime`
- **Description:** —

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| End Date | `https://iri.suomi.fi/model/ncbv/endDate` | Literal | — | — | — | — |
| Start Date | `https://iri.suomi.fi/model/ncbv/startDate` | Literal | — | — | — | — |

### Person

- **IRI:** `https://iri.suomi.fi/model/ncbv/Person`
- **Description:** A individual human being who may be dead or alive, but not imaginary.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6005` | person | an individual human being who may be dead or alive, but not imaginary |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Identifier | `https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Date Of Birth | `https://iri.suomi.fi/model/ncbv/dateOfBirth` | Literal | The point in time on which the Person was born. Persons can be registered with a membership in a legal entity whithout a identifier being a national registration number. | `https://iri.suomi.fi/terminology/nbvoc/concept-6013` | date of birth | a point in time on which a person was born |
| Full Name | `https://iri.suomi.fi/model/ncbv/fullName` | Literal | The complete name of the Person as one string. | `https://iri.suomi.fi/terminology/nbvoc/concept-6012` | full name | the complete name of the Person as one string. |

### Representation Rule (Signatory Rule)

- **IRI:** `https://iri.suomi.fi/model/ncbv/RepresentationRule`
- **Description:** A rule that describes who or which agents a mandate is granted to. 

The rule can be used both in the case of legal representation, when a CEO or a board member signs for the agent (company) based on their official role in the company, as well as when a mandate is given to a specific person ("a man on the street") who has no previous affiliation to the mandating agent.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6011` | representation rule | a rule that defines which agent(s) can act on behalf of another agent |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Description | `https://iri.suomi.fi/model/ncbv/description` | Literal | An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
 | — | — | — |
| Sequence | `https://iri.suomi.fi/model/ncbv/sequence` | Literal | An indicator for the order of a series of values; "1, 2, 3..." | — | — | — |

### Restriction

- **IRI:** `https://iri.suomi.fi/model/ncbv/Restriction`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-88` | restriction | TBD |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | `https://iri.suomi.fi/model/ncbv/type` | Restriction Type | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Value | `https://iri.suomi.fi/model/ncbv/value` | Literal | — | — | — | — |

### Restriction Type

- **IRI:** `https://iri.suomi.fi/model/ncbv/RestrictionType`
- **Description:** A class for describing what the value in the Restriction class means; example: Restriction.value: 10000; RestrictionType: Datatype: Decimal or Integer; Unit: SEK, NOK, EUR... Name: Monetary Amount restriction; Description: "The maximum monetary amount to be used with the Mandate (like: "purchasing a car")  

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Datatype | `https://iri.suomi.fi/model/ncbv/datatype` | Literal | — | — | — | — |
| Description | `https://iri.suomi.fi/model/ncbv/description` | Literal | An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
 | — | — | — |
| Identifier | `https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | The identifier of a mandate is used to separate different mandates from each other, making it unique. | — | — | — |
| Unit | `https://iri.suomi.fi/model/ncbv/unit` | Literal | — | — | — | — |

### Role

- **IRI:** `https://iri.suomi.fi/model/ncbv/Role`
- **Description:** In the context of Mandates, the Role class 
indicates the Role that the Agent plays in a Membership relationship with a legal entity. 

Upper class: https://www.w3.org/TR/vocab-org/#class-role

Suggested code list for Nordic use cases: http://uri.suomi.fi/codelist/verotus/membershiproletypes

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6004` | role | a defined position or function that an agent holds within another agent |

### Role Based Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/RoleBasedRepresentationRule`
- **Description:** A class that replaces (partially) the Simple Representation Rule in previous versions; example: signatory rights rule "CEO alone"

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-83` | role based representation rule | a representation rule where the rule is based on the roles in an agent (company) |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Defines Valid Role  | `https://iri.suomi.fi/model/ncbv/definesValidRole` | Role | The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or. | — | — | — |
| Role Holder Quantifier | `https://iri.suomi.fi/model/ncbv/roleHolderQuantifier` | Concept | Specifies a qualitative quantity or proportion of role holders required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”). | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Minimum Number of Role Holders | `https://iri.suomi.fi/model/ncbv/minimumNumberOfRoleHolders` | Literal | The number of role holders required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5... | — | — | — |

### Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/Rule`
- **Description:** eli:Rule

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Implements | `https://iri.suomi.fi/model/ncbv/implements` | Legal Resource | — | — | — | — |

### Scope

- **IRI:** `https://iri.suomi.fi/model/ncbv/Scope`
- **Description:** A class to define what powers the Mandator grants to the Mandatee through the Mandate.

Example: A gives signatory power to B. A grants B the power to buy a car for the company. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-92` | scope | TBD |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Applies to Object | `https://iri.suomi.fi/model/ncbv/appliesToObject` | Object | — | — | — | — |
| Power | `https://iri.suomi.fi/model/ncbv/power` | Concept | — | — | — | — |

### Share Capital

- **IRI:** `https://iri.suomi.fi/model/ncbv/ShareCapital`
- **Description:** Share capital refers to the total amount of capital raised by a legal entity through the issuance of shares to shareholders.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6040` | share capital | the total amount of capital raised by a legal entity through the issuance of shares to shareholders |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Total Capital Amount | `https://iri.suomi.fi/model/ncbv/totalCapitalAmount` | Amount | The total capital amount of the Legal Entity's (company's) share capital, expressed in monetary values. | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Capital Type | `https://iri.suomi.fi/model/ncbv/capitalType` | Literal | Values expressed in a separate code list, could contain the following: 

Capital Type	Description
Authorized Share Capital	Maximum capital a company is legally allowed to issue, as stated in its statutes

Issued Share Capital	Capital corresponding to the total number of shares that have actually been issued

Subscribed Share Capital	Part of issued capital that investors have agreed to purchase

Paid-up Share Capital	Subscribed capital for which the company has received payment

Called-up Share Capital	Subscribed capital where payment has been requested (called), but not necessarily received

Unpaid Capital	Portion of called-up capital still owed by shareholders

Nominal / Par Value	The base value assigned to each share; may also be relevant at share type level

Equity vs Debt hybrid	Some instruments may qualify as equity under certain laws but be treated as debt elsewhere | — | — | — |
| Number of Shares | `https://iri.suomi.fi/model/ncbv/numberOfShares` | Literal | The total number of individual shares associated with the specified share capital value.

This count represents the share units issued, authorized, subscribed, or paid-up, depending on the type of capital being described (capitalType). | — | — | — |

### Source

- **IRI:** `https://iri.suomi.fi/model/ncbv/Source`
- **Description:** A class to describe what the powers that are delegated by the Mandator are originally based on;  example: "law", "statutes of company"; "another mandate" etc.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-91` | source | TBD |

#### Object properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | `https://iri.suomi.fi/model/ncbv/type` | Concept | — | — | — | — |

#### Datatype properties

| Property | IRI | Value type(s) in this class | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- | --- |
| Description | `https://iri.suomi.fi/model/ncbv/description` | Literal | An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
 | — | — | — |

## Ungrouped properties

These properties are declared in the NCBV ontology but are not used in any explicit OWL restriction for the NCBV classes in this Turtle file.

### Object properties without explicit class association

| Property | IRI | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- |
| All of | `https://iri.suomi.fi/model/ncbv/allOf` | Constraint property that requires all of the agents holding a post to sign. | — | — | — |
| Alone | `https://iri.suomi.fi/model/ncbv/alone` | Requires holder of the post to sign alone. | — | — | — |
| Consists of Representation Rule | `https://iri.suomi.fi/model/ncbv/consistsOfRepresentationRule` | — | — | — | — |
| Five of | `https://iri.suomi.fi/model/ncbv/fiveOf` | Requires five of the defined agents holding a post to sign. | — | — | — |
| Four of | `https://iri.suomi.fi/model/ncbv/fourOf` | Requires four of the defined agents holding a post to sign. | — | — | — |
| Grants Representation Right | `https://iri.suomi.fi/model/ncbv/grantsRepresentationRight` | The signatory rights that is registered for the legal entity. | — | — | — |
| Held by Legal Entity | `https://iri.suomi.fi/model/ncbv/heldByLegalEntity` | Indicates the legal entity that is holding the post. | — | — | — |
| Held by Person | `https://iri.suomi.fi/model/ncbv/heldByPerson` | Indicates the person that holds the post.
 | — | — | — |
| Jointly | `https://iri.suomi.fi/model/ncbv/jointly` | — | — | — | — |
| Majority of | `https://iri.suomi.fi/model/ncbv/majorityOf` | Constraint property that requires majority of agents holding a post to sign. | — | — | — |
| One of | `https://iri.suomi.fi/model/ncbv/oneOf` | Requires one of the defined agents holding a post to sign. | — | — | — |
| Subject | `https://iri.suomi.fi/model/ncbv/subject` | — | — | — | — |
| Three of | `https://iri.suomi.fi/model/ncbv/threeOf` | Requires two of the defined agents holding a post to sign. | — | — | — |
| Transfer of Mandate | `https://iri.suomi.fi/model/ncbv/transferOfMandate` | — | — | — | — |
| Two of | `https://iri.suomi.fi/model/ncbv/twoOf` | Requires two of the defined agents holding a post to sign. | — | — | — |

### Datatype properties without explicit class association

| Property | IRI | Description | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- | --- |
| Amount | `https://iri.suomi.fi/model/ncbv/amount` | The amount of money. | — | — | — |
| Code Identifier | `https://iri.suomi.fi/model/ncbv/codeIdentifier` | An identifier for the code, can be of any format like an URI or just alphanumeric. | — | — | — |
| Code name | `https://iri.suomi.fi/model/ncbv/codeName` | — | — | — | — |
| In Classification | `https://iri.suomi.fi/model/ncbv/inClassification` | NACE codes are published in scheme http://publications.europa.eu/resource/authority/ux2/nace2/nace2. Description in text for all NACE codes in all EU languages can be found there. | — | — | — |
| Object Type | `https://iri.suomi.fi/model/ncbv/objectType` | — | — | — | — |
| Preferred Label | `https://iri.suomi.fi/model/ncbv/prefLabel` | The preferred label attribute is used to name the actual scope of the Mandate; example: "Car Purchase"; "Filing a Declaration (of some type)"; or using a specific national eService (mandates given in the Swedish Mina Ombud or the Finnish Suomi.fi eAuthorizations).   | — | — | — |
| Reference | `https://iri.suomi.fi/model/ncbv/reference` | Reference to the description of the NACE code. | — | — | — |
