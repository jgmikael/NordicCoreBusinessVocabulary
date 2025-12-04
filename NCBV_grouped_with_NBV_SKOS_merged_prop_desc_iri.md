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

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Admin Unit Level 1<br>*The uppermost administrative unit for the address, almost always a country.*<br>`https://iri.suomi.fi/model/ncbv/adminUnitLevel1` | Literal | — | — | — |
| Admin Unit Level 2<br>*The name of a secondary level/region of the address, usually a county, state or other such area that typically encompasses several localities.*<br>`https://iri.suomi.fi/model/ncbv/adminUnitLevel2` | Literal | — | — | — |
| Care of<br>*Used when an address is at the address of another person or legal entity.
*<br>`https://iri.suomi.fi/model/ncbv/careOf` | Literal | — | — | — |
| Full Address<br>*The complete address written as a string.*<br>`https://iri.suomi.fi/model/ncbv/fullAddress` | Literal | — | — | — |
| Locator Designator<br>*A number or a sequence of characters that uniquely identifies the locator within the relevant scope.*<br>`https://iri.suomi.fi/model/ncbv/locatorDesignator` | Literal | — | — | — |
| Locator Name<br>*Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building.*<br>`https://iri.suomi.fi/model/ncbv/locatorName` | Literal | — | — | — |
| Post Code<br>*The code created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.*<br>`https://iri.suomi.fi/model/ncbv/postCode` | Literal | — | — | — |
| Post Name<br>*A name created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.*<br>`https://iri.suomi.fi/model/ncbv/postName` | Literal | — | — | — |
| Post Office Box<br>*A location designator for a postal delivery point at a post office, usually a number.*<br>`https://iri.suomi.fi/model/ncbv/postOfficeBox` | Literal | — | — | — |
| Thoroughfare<br>*The name of a passage or way through from one location to another.*<br>`https://iri.suomi.fi/model/ncbv/thoroughfare` | Literal | — | — | — |

### Agent

- **IRI:** `https://iri.suomi.fi/model/ncbv/Agent`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-41` | agent | an entity that is able to carry out actions |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Grants Mandate<br>`https://iri.suomi.fi/model/ncbv/grantsMandate` | Mandate | — | — | — |
| Has Member<br>`https://iri.suomi.fi/model/ncbv/hasMember` | Membership | — | — | — |

### Amount

- **IRI:** `https://iri.suomi.fi/model/ncbv/MonetaryAmount`
- **Description:** see unece:Amount and schema:MonetaryAmount

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-85` | monetary amount | TBD |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Currency<br>*The currency in which the monetary amount is expressed. ISO 4217 currency format, e.g. "EUR".*<br>`https://iri.suomi.fi/model/ncbv/currency` | Literal | — | — | — |
| Value<br>`https://iri.suomi.fi/model/ncbv/value` | Literal | — | — | — |

### Beneficial Owner

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwner`
- **Description:** A natural person(s) who ultimately owns or controls the agent.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-3002` | beneficial owner | a person or persons who ultimately owns or controls an agent |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Is a Person<br>`https://iri.suomi.fi/model/ncbv/isPerson` | Person | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Interest Control<br>*Extent of the control. 25%, 25-50%, 50%, 50-75%, 75%, 100%*<br>`https://iri.suomi.fi/model/ncbv/interestControl` | Literal | — | — | — |
| Interest Direct Or Indirect<br>*How directly the interest is exercised by the interested party. The value MUST be 'indirect' if intermediate entities or agents are known to exist, and MUST be 'direct' if such intermediaries are known not to exist. Otherwise the value MUST be 'unknown'.*<br>`https://iri.suomi.fi/model/ncbv/interestDirectOrIndirect` | Literal | — | — | — |
| Interest Type<br>*The type of interest held by a Natural person in an agent. In Sweden this is free text but can have enum like: shareholding, votingRights, appointmentOfBoard, otherInfluenceOrControl, ,seniorManagingOfficial, settlor, trustee, protector, beneficiaryOfLegalArrangement, rightsToSurplusAssetsOnDissolution, rightsToProfitOrIncome, rightsGrantedByContract, conditionalRightsGrantedByContract, controlViaCompanyRulesOrArticles, controlByLegalFramework, boardMember, boardChair, unknownInterest, unpublishedInterest, enjoymentAndUseOfAssets, rightToProfitOrIncomeFromAssets*<br>`https://iri.suomi.fi/model/ncbv/interestType` | Literal | — | — | — |

### Beneficial Owner Role

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwnerRole`
- **Description:** —

### Code

- **IRI:** `https://iri.suomi.fi/model/ncbv/Code`
- **Description:** A generic class for any code values that a specific class can have; in the NCBV the Code class contains code values for legal form, legal status and (economic) activity.  

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Code<br>*The actual code value from a selected code list.*<br>`https://iri.suomi.fi/model/ncbv/codeValue` | Literal | — | — | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | — | — | — |
| Name<br>*A word or a combination of characters by which an entity/agent/thing is designated, called, or known.*<br>`https://iri.suomi.fi/model/ncbv/name` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-18` | name | a word or a combination of characters by which an agent is designated, called, or known |
| Sequence<br>*An indicator for the order of a series of values; "1, 2, 3..."*<br>`https://iri.suomi.fi/model/ncbv/sequence` | Literal | — | — | — |

### Composite Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/CompositeRepresentationRule`
- **Description:** A class that replaces the "Complex Representation Rule" in previous NCBV versions; example of a composite rule for general signatory rights (legal representation): "CEO alone and two board members jointly"

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-82` | composite representation rule | a representation rule that consist of two or more role or membership based representation rules |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| And<br>`https://iri.suomi.fi/model/ncbv/and` | Representation Rule (Signatory Rule) | — | — | — |
| Or<br>`https://iri.suomi.fi/model/ncbv/or` | Representation Rule (Signatory Rule) | — | — | — |

### Contact Point

- **IRI:** `https://iri.suomi.fi/model/ncbv/ContactPoint`
- **Description:** Information (e.g. e-mail address, telephone number) of a person or department through which the user can get in touch with. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6044` | contact point | information through which one can get in touch with a person or a legal entity |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Contact Page<br>*A web page that could be used to reach out the Contact Point.*<br>`https://iri.suomi.fi/model/ncbv/contactPage` | Literal | — | — | — |
| Has Email<br>*An electronic address through which the Contact Point can be contacted.

Equivalent with schema:email*<br>`https://iri.suomi.fi/model/ncbv/email` | Literal | — | — | — |
| Has Telephone<br>`https://iri.suomi.fi/model/ncbv/hasTelephone` | Literal | — | — | — |

### Document

- **IRI:** `https://iri.suomi.fi/model/ncbv/Document`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-93` | document | TBD |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Title<br>`https://iri.suomi.fi/model/ncbv/title` | Literal | — | — | — |

### Identifier

- **IRI:** `https://iri.suomi.fi/model/ncbv/Identifier`
- **Description:** A unique set of characters used to identify the legal entity. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-7` | identifier | a structured reference that identifies an entity |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Date of Issue<br>*The date on which the something was issued; in this context for instance a Mandate or an Identifier.*<br>`https://iri.suomi.fi/model/ncbv/dateOfIssue` | Literal | — | — | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | — | — | — |
| Notation<br>*A string of characters to uniquely identify a concept.*<br>`https://iri.suomi.fi/model/ncbv/notation` | Literal | — | — | — |
| Schema Agency<br>*The name of the agency that issued the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemaAgency` | Literal | — | — | — |
| Scheme Name<br>*Name of the scheme used to construct the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemeName` | Literal | — | — | — |
| Scheme URI<br>*URI of the scheme used to construct the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemeURI` | Literal | — | — | — |

### Legal Entity

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalEntity`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6006` | legal entity | a formal organization that is involved in economic activity |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Activity<br>*An active deed or action carried out by a legal entity*<br>`https://iri.suomi.fi/model/ncbv/hasActivity` | Code | — | — | — |
| Beneficial Owners<br>*A natural person(s) who ultimately owns or controls the agent.*<br>`https://iri.suomi.fi/model/ncbv/beneficialOwners` | Beneficial Owner | — | — | — |
| Contact Point<br>*The main contact information of the resource.*<br>`https://iri.suomi.fi/model/ncbv/hasContactPoint` | Contact Point | — | — | — |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — |
| Legal Form<br>*The legal form of a legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasLegalForm` | Code | `https://iri.suomi.fi/terminology/nbvoc/concept-16` | legal form | a legal structure according to national legislation |
| Legal Identifier<br>*An identifier that is given to a legal entity at registration.*<br>`https://iri.suomi.fi/model/ncbv/legalIdentifier` | Identifier | — | — | — |
| Legal Status<br>*An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasLegalStatus` | Legal Status | `https://iri.suomi.fi/terminology/nbvoc/concept-23` | legal status | an indication of whether a registration authority has registered some extraordinary proceedings for the legal entity |
| Postal Address<br>*The address to which mail can be sent to the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/postalAddress` | Address | — | — | — |
| Registered Address<br>*The address to which formal communications can be sent to the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/registeredAddress` | Address | — | — | — |
| Share Capital<br>*The total registered share capital for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasShareCapital` | Share Capital | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Alternative Name<br>*Any other registered name by which a legal entity is known.*<br>`https://iri.suomi.fi/model/ncbv/alternativeName` | Literal | — | — | — |
| Legal Name<br>`https://iri.suomi.fi/model/ncbv/legalName` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-105` | legal name | a name under which the legal entity is registered |
| Registration Date<br>*The date when a public authority has registered the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/registrationDate` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-22` | registration date | The date when a public authority has registered the registered organisation |

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

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Has Code<br>`https://iri.suomi.fi/model/ncbv/hasCode` | Code | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Date<br>*The date when the legal status was registered.*<br>`https://iri.suomi.fi/model/ncbv/date` | Literal | — | — | — |

### Location

- **IRI:** `https://iri.suomi.fi/model/ncbv/Location`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-86` | location | TBD |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Geographic Identifier<br>`https://iri.suomi.fi/model/ncbv/geographicIdentifier` | Literal | — | — | — |
| Geographic Name<br>*A recognizable name for a place, like "Eiffel Tower" or "Madrid". *<br>`https://iri.suomi.fi/model/ncbv/geographicName` | Literal | — | — | — |

### Mandate

- **IRI:** `https://iri.suomi.fi/model/ncbv/Mandate`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-75` | mandate | the terms under which a mandator grants or delegates authority or power to a mandatee |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| (Has) Geographical Scope/ Has Location / (Has) Geographical Coverage<br>*The association geographical scope points at a location; this describes the geographic region the mandate is valid.  *<br>`https://iri.suomi.fi/model/ncbv/hasGeographicalScope` | Location | — | — | — |
| (Has) Mandator<br>*The Mandator association points always to the "primary mandator", who is the original source of the delegated power.*<br>`https://iri.suomi.fi/model/ncbv/hasMandator` | Agent | `https://iri.suomi.fi/terminology/nbvoc/concept-76` | mandator | an agent that grants authority to another agent to act on its behalf |
| Has Duration<br>*The association "has duration" points to "Period of Time"and indicates the validity period of the mandate; like "1.1.2025-31.12.2025"*<br>`https://iri.suomi.fi/model/ncbv/hasDuration` | Period of Time | — | — | — |
| Has Representation Rule<br>`https://iri.suomi.fi/model/ncbv/hasRepresentationRule` | Representation Rule (Signatory Rule) | — | — | — |
| Has Restriction<br>`https://iri.suomi.fi/model/ncbv/hasRestriction` | Restriction | — | — | — |
| Has Scope<br>`https://iri.suomi.fi/model/ncbv/hasScope` | Scope | — | — | — |
| Has Source<br>`https://iri.suomi.fi/model/ncbv/hasSource` | Source | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Date of Issue<br>*The date on which the something was issued; in this context for instance a Mandate or an Identifier.*<br>`https://iri.suomi.fi/model/ncbv/dateOfIssue` | Literal | — | — | — |
| Delegable<br>*An indicator of whether the Mandate can be delegated or not.*<br>`https://iri.suomi.fi/model/ncbv/delegable` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-79` | delegable | capable of being delegated |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | — | — | — |
| Modified<br>*The date of the last update of something like a Mandate.

upper attribute
http://purl.org/dc/terms/modified


dcterms:modified*<br>`https://iri.suomi.fi/model/ncbv/modified` | Literal | — | — | — |
| Status<br>*A mandate's status can be for instance: active, withdrawn/inactive > Tore checks values 

Upper attribute: adms:status*<br>`https://iri.suomi.fi/model/ncbv/status` | Literal | — | — | — |

### Mandate Transfer

- **IRI:** `https://iri.suomi.fi/model/ncbv/MandateTransfer`
- **Description:** A class for documenting the possible transfer (or delegation) of a Mandate from a previous Mandatee to another; example: Mandate is granted by CEO of Company, is delegable, the first Mandatee delegated the Mandate to another Agent who becomes the new Mandatee; the transfer of the Mandate is logged in this class.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-89` | mandate transfer | TBD |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Mandatee<br>`https://iri.suomi.fi/model/ncbv/mandatee` | Agent | — | — | — |
| Original Mandate<br>`https://iri.suomi.fi/model/ncbv/originalMandate` | Mandate | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Date<br>*The date when the legal status was registered.*<br>`https://iri.suomi.fi/model/ncbv/date` | Literal | — | — | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | — | — | — |

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

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Member<br>`https://iri.suomi.fi/model/ncbv/member` | Agent | — | — | — |
| Role<br>*Indicates the Role that the Agent plays in a Membership relationship with a legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasRole` | Role | — | — | — |

### Membership Based Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/MembershipBasedRepresentationRule`
- **Description:** A class that replaces the previous "Simple Representation Rule" class (partially); example: a mandate granted to "a man on the street", pointing at a certain person as a  Member of the Mandator (Membership in this case could be "mandatee" or similar).

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-84` | membership based representation rule | a representation rule where the rule is based on the membership relation between agents |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Defines Valid Membership<br>*The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.*<br>`https://iri.suomi.fi/model/ncbv/definesValidMembership` | Membership | — | — | — |
| Member Quantifier<br>*Specifies a qualitative quantity or proportion of members required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).*<br>`https://iri.suomi.fi/model/ncbv/memberQuantifier` | Concept | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Minimum Number of Members<br>*The number of members required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...*<br>`https://iri.suomi.fi/model/ncbv/minimumNumberOfMembers` | Literal | — | — | — |

### Object

- **IRI:** `https://iri.suomi.fi/model/ncbv/Object`
- **Description:** Example: can be a specific house, car; has an Identifier (car registration number)

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-87` | object | TBD |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — |
| Type<br>`https://iri.suomi.fi/model/ncbv/type` | Concept | — | — | — |

### Period of Time

- **IRI:** `https://iri.suomi.fi/model/ncbv/PeriodOfTime`
- **Description:** —

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| End Date<br>`https://iri.suomi.fi/model/ncbv/endDate` | Literal | — | — | — |
| Start Date<br>`https://iri.suomi.fi/model/ncbv/startDate` | Literal | — | — | — |

### Person

- **IRI:** `https://iri.suomi.fi/model/ncbv/Person`
- **Description:** A individual human being who may be dead or alive, but not imaginary.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6005` | person | an individual human being who may be dead or alive, but not imaginary |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier` | Identifier | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Date Of Birth<br>*The point in time on which the Person was born. Persons can be registered with a membership in a legal entity whithout a identifier being a national registration number.*<br>`https://iri.suomi.fi/model/ncbv/dateOfBirth` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-6013` | date of birth | a point in time on which a person was born |
| Full Name<br>*The complete name of the Person as one string.*<br>`https://iri.suomi.fi/model/ncbv/fullName` | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-6012` | full name | the complete name of the Person as one string. |

### Representation Rule (Signatory Rule)

- **IRI:** `https://iri.suomi.fi/model/ncbv/RepresentationRule`
- **Description:** A rule that describes who or which agents a mandate is granted to. 

The rule can be used both in the case of legal representation, when a CEO or a board member signs for the agent (company) based on their official role in the company, as well as when a mandate is given to a specific person ("a man on the street") who has no previous affiliation to the mandating agent.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6011` | representation rule | a rule that defines which agent(s) can act on behalf of another agent |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description` | Literal | — | — | — |
| Sequence<br>*An indicator for the order of a series of values; "1, 2, 3..."*<br>`https://iri.suomi.fi/model/ncbv/sequence` | Literal | — | — | — |

### Restriction

- **IRI:** `https://iri.suomi.fi/model/ncbv/Restriction`
- **Description:** —

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-88` | restriction | TBD |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Type<br>`https://iri.suomi.fi/model/ncbv/type` | Restriction Type | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Value<br>`https://iri.suomi.fi/model/ncbv/value` | Literal | — | — | — |

### Restriction Type

- **IRI:** `https://iri.suomi.fi/model/ncbv/RestrictionType`
- **Description:** A class for describing what the value in the Restriction class means; example: Restriction.value: 10000; RestrictionType: Datatype: Decimal or Integer; Unit: SEK, NOK, EUR... Name: Monetary Amount restriction; Description: "The maximum monetary amount to be used with the Mandate (like: "purchasing a car")  

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Datatype<br>`https://iri.suomi.fi/model/ncbv/datatype` | Literal | — | — | — |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description` | Literal | — | — | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue` | Literal | — | — | — |
| Unit<br>`https://iri.suomi.fi/model/ncbv/unit` | Literal | — | — | — |

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

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Defines Valid Role <br>*The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.*<br>`https://iri.suomi.fi/model/ncbv/definesValidRole` | Role | — | — | — |
| Role Holder Quantifier<br>*Specifies a qualitative quantity or proportion of role holders required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).*<br>`https://iri.suomi.fi/model/ncbv/roleHolderQuantifier` | Concept | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Minimum Number of Role Holders<br>*The number of role holders required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...*<br>`https://iri.suomi.fi/model/ncbv/minimumNumberOfRoleHolders` | Literal | — | — | — |

### Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/Rule`
- **Description:** eli:Rule

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Implements<br>`https://iri.suomi.fi/model/ncbv/implements` | Legal Resource | — | — | — |

### Scope

- **IRI:** `https://iri.suomi.fi/model/ncbv/Scope`
- **Description:** A class to define what powers the Mandator grants to the Mandatee through the Mandate.

Example: A gives signatory power to B. A grants B the power to buy a car for the company. 

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-92` | scope | TBD |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Applies to Object<br>`https://iri.suomi.fi/model/ncbv/appliesToObject` | Object | — | — | — |
| Power<br>`https://iri.suomi.fi/model/ncbv/power` | Concept | — | — | — |

### Share Capital

- **IRI:** `https://iri.suomi.fi/model/ncbv/ShareCapital`
- **Description:** Share capital refers to the total amount of capital raised by a legal entity through the issuance of shares to shareholders.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6040` | share capital | the total amount of capital raised by a legal entity through the issuance of shares to shareholders |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Total Capital Amount<br>*The total capital amount of the Legal Entity's (company's) share capital, expressed in monetary values.*<br>`https://iri.suomi.fi/model/ncbv/totalCapitalAmount` | Amount | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Capital Type<br>*Values expressed in a separate code list, could contain the following: 

Capital Type	Description
Authorized Share Capital	Maximum capital a company is legally allowed to issue, as stated in its statutes

Issued Share Capital	Capital corresponding to the total number of shares that have actually been issued

Subscribed Share Capital	Part of issued capital that investors have agreed to purchase

Paid-up Share Capital	Subscribed capital for which the company has received payment

Called-up Share Capital	Subscribed capital where payment has been requested (called), but not necessarily received

Unpaid Capital	Portion of called-up capital still owed by shareholders

Nominal / Par Value	The base value assigned to each share; may also be relevant at share type level

Equity vs Debt hybrid	Some instruments may qualify as equity under certain laws but be treated as debt elsewhere*<br>`https://iri.suomi.fi/model/ncbv/capitalType` | Literal | — | — | — |
| Number of Shares<br>*The total number of individual shares associated with the specified share capital value.

This count represents the share units issued, authorized, subscribed, or paid-up, depending on the type of capital being described (capitalType).*<br>`https://iri.suomi.fi/model/ncbv/numberOfShares` | Literal | — | — | — |

### Source

- **IRI:** `https://iri.suomi.fi/model/ncbv/Source`
- **Description:** A class to describe what the powers that are delegated by the Mandator are originally based on;  example: "law", "statutes of company"; "another mandate" etc.

#### NBV linkage

| NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-91` | source | TBD |

#### Object properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Type<br>`https://iri.suomi.fi/model/ncbv/type` | Concept | — | — | — |

#### Datatype properties

| Property / Description / IRI | Value type(s) in this class | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- | --- |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description` | Literal | — | — | — |

## Ungrouped properties

These properties are declared in the NCBV ontology but are not used in any explicit OWL restriction for the NCBV classes in this Turtle file.

### Object properties without explicit class association

| Property / Description / IRI | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- |
| All of<br>*Constraint property that requires all of the agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/allOf` | — | — | — |
| Alone<br>*Requires holder of the post to sign alone.*<br>`https://iri.suomi.fi/model/ncbv/alone` | — | — | — |
| Consists of Representation Rule<br>`https://iri.suomi.fi/model/ncbv/consistsOfRepresentationRule` | — | — | — |
| Five of<br>*Requires five of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/fiveOf` | — | — | — |
| Four of<br>*Requires four of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/fourOf` | — | — | — |
| Grants Representation Right<br>*The signatory rights that is registered for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/grantsRepresentationRight` | — | — | — |
| Held by Legal Entity<br>*Indicates the legal entity that is holding the post.*<br>`https://iri.suomi.fi/model/ncbv/heldByLegalEntity` | — | — | — |
| Held by Person<br>*Indicates the person that holds the post.
*<br>`https://iri.suomi.fi/model/ncbv/heldByPerson` | — | — | — |
| Jointly<br>`https://iri.suomi.fi/model/ncbv/jointly` | — | — | — |
| Majority of<br>*Constraint property that requires majority of agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/majorityOf` | — | — | — |
| One of<br>*Requires one of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/oneOf` | — | — | — |
| Subject<br>`https://iri.suomi.fi/model/ncbv/subject` | — | — | — |
| Three of<br>*Requires two of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/threeOf` | — | — | — |
| Transfer of Mandate<br>`https://iri.suomi.fi/model/ncbv/transferOfMandate` | — | — | — |
| Two of<br>*Requires two of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/twoOf` | — | — | — |

### Datatype properties without explicit class association

| Property / Description / IRI | NBV URI | SKOS prefLabel (en) | SKOS definition (en) |
| --- | --- | --- | --- |
| Amount<br>*The amount of money.*<br>`https://iri.suomi.fi/model/ncbv/amount` | — | — | — |
| Code Identifier<br>*An identifier for the code, can be of any format like an URI or just alphanumeric.*<br>`https://iri.suomi.fi/model/ncbv/codeIdentifier` | — | — | — |
| Code name<br>`https://iri.suomi.fi/model/ncbv/codeName` | — | — | — |
| In Classification<br>*NACE codes are published in scheme http://publications.europa.eu/resource/authority/ux2/nace2/nace2. Description in text for all NACE codes in all EU languages can be found there.*<br>`https://iri.suomi.fi/model/ncbv/inClassification` | — | — | — |
| Object Type<br>`https://iri.suomi.fi/model/ncbv/objectType` | — | — | — |
| Preferred Label<br>*The preferred label attribute is used to name the actual scope of the Mandate; example: "Car Purchase"; "Filing a Declaration (of some type)"; or using a specific national eService (mandates given in the Swedish Mina Ombud or the Finnish Suomi.fi eAuthorizations).  *<br>`https://iri.suomi.fi/model/ncbv/prefLabel` | — | — | — |
| Reference<br>*Reference to the description of the NACE code.*<br>`https://iri.suomi.fi/model/ncbv/reference` | — | — | — |
