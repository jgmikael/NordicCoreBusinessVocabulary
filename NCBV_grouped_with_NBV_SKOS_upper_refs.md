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
- **Upper Class:** isa2core:Address

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-4`<br>address<br>*an identification of the fixed location of a geographic place* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Admin Unit Level 1<br>*The uppermost administrative unit for the address, almost always a country.*<br>`https://iri.suomi.fi/model/ncbv/adminUnitLevel1`<br>Upper Property: isa2core:adminUnitLevel1 | Literal | — |
| Admin Unit Level 2<br>*The name of a secondary level/region of the address, usually a county, state or other such area that typically encompasses several localities.*<br>`https://iri.suomi.fi/model/ncbv/adminUnitLevel2`<br>Upper Property: isa2core:adminUnitLevel2 | Literal | — |
| Care of<br>*Used when an address is at the address of another person or legal entity.
*<br>`https://iri.suomi.fi/model/ncbv/careOf`<br>Upper Property: owl:topDataProperty | Literal | — |
| Full Address<br>*The complete address written as a string.*<br>`https://iri.suomi.fi/model/ncbv/fullAddress`<br>Upper Property: isa2core:fullAddress | Literal | — |
| Locator Designator<br>*A number or a sequence of characters that uniquely identifies the locator within the relevant scope.*<br>`https://iri.suomi.fi/model/ncbv/locatorDesignator`<br>Upper Property: isa2core:locatorDesignator | Literal | — |
| Locator Name<br>*Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building.*<br>`https://iri.suomi.fi/model/ncbv/locatorName`<br>Upper Property: isa2core:locatorName | Literal | — |
| Post Code<br>*The code created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.*<br>`https://iri.suomi.fi/model/ncbv/postCode`<br>Upper Property: owl:topDataProperty | Literal | — |
| Post Name<br>*A name created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.*<br>`https://iri.suomi.fi/model/ncbv/postName`<br>Upper Property: owl:topDataProperty | Literal | — |
| Post Office Box<br>*A location designator for a postal delivery point at a post office, usually a number.*<br>`https://iri.suomi.fi/model/ncbv/postOfficeBox`<br>Upper Property: isa2core:poBox | Literal | — |
| Thoroughfare<br>*The name of a passage or way through from one location to another.*<br>`https://iri.suomi.fi/model/ncbv/thoroughfare`<br>Upper Property: isa2core:thoroughfare | Literal | — |

### Agent

- **IRI:** `https://iri.suomi.fi/model/ncbv/Agent`
- **Description:** —
- **Upper Class:** isa2core:Agent

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-41`<br>agent<br>*an entity that is able to carry out actions* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Grants Mandate<br>`https://iri.suomi.fi/model/ncbv/grantsMandate`<br>Upper Property: owl:topObjectProperty | Mandate | — |
| Has Member<br>`https://iri.suomi.fi/model/ncbv/hasMember`<br>Upper Property: owl:topObjectProperty | Membership | — |

### Amount

- **IRI:** `https://iri.suomi.fi/model/ncbv/MonetaryAmount`
- **Description:** see unece:Amount and schema:MonetaryAmount
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-85`<br>monetary amount<br>*TBD* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Currency<br>*The currency in which the monetary amount is expressed. ISO 4217 currency format, e.g. "EUR".*<br>`https://iri.suomi.fi/model/ncbv/currency`<br>Upper Property: owl:topDataProperty | Literal | — |
| Value<br>`https://iri.suomi.fi/model/ncbv/value`<br>Upper Property: isa2core:value | Literal | — |

### Beneficial Owner

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwner`
- **Description:** A natural person(s) who ultimately owns or controls the agent.
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-3002`<br>beneficial owner<br>*a person or persons who ultimately owns or controls an agent* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Is a Person<br>`https://iri.suomi.fi/model/ncbv/isPerson`<br>Upper Property: owl:topObjectProperty | Person | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Interest Control<br>*Extent of the control. 25%, 25-50%, 50%, 50-75%, 75%, 100%*<br>`https://iri.suomi.fi/model/ncbv/interestControl`<br>Upper Property: owl:topDataProperty | Literal | — |
| Interest Direct Or Indirect<br>*How directly the interest is exercised by the interested party. The value MUST be 'indirect' if intermediate entities or agents are known to exist, and MUST be 'direct' if such intermediaries are known not to exist. Otherwise the value MUST be 'unknown'.*<br>`https://iri.suomi.fi/model/ncbv/interestDirectOrIndirect`<br>Upper Property: owl:topDataProperty | Literal | — |
| Interest Type<br>*The type of interest held by a Natural person in an agent. In Sweden this is free text but can have enum like: shareholding, votingRights, appointmentOfBoard, otherInfluenceOrControl, ,seniorManagingOfficial, settlor, trustee, protector, beneficiaryOfLegalArrangement, rightsToSurplusAssetsOnDissolution, rightsToProfitOrIncome, rightsGrantedByContract, conditionalRightsGrantedByContract, controlViaCompanyRulesOrArticles, controlByLegalFramework, boardMember, boardChair, unknownInterest, unpublishedInterest, enjoymentAndUseOfAssets, rightToProfitOrIncomeFromAssets*<br>`https://iri.suomi.fi/model/ncbv/interestType`<br>Upper Property: owl:topDataProperty | Literal | — |

### Beneficial Owner Role

- **IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwnerRole`
- **Description:** —
- **Upper Class:** ncbv:Role

### Code

- **IRI:** `https://iri.suomi.fi/model/ncbv/Code`
- **Description:** A generic class for any code values that a specific class can have; in the NCBV the Code class contains code values for legal form, legal status and (economic) activity.  
- **Upper Class:** skos:Concept

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Code<br>*The actual code value from a selected code list.*<br>`https://iri.suomi.fi/model/ncbv/codeValue`<br>Upper Property: skos:notation | Literal | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue`<br>Upper Property: dct:identifier | Literal | — |
| Name<br>*A word or a combination of characters by which an entity/agent/thing is designated, called, or known.*<br>`https://iri.suomi.fi/model/ncbv/name`<br>Upper Property: name, skos:prefLabel | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-18`<br>name<br>*a word or a combination of characters by which an agent is designated, called, or known* |
| Sequence<br>*An indicator for the order of a series of values; "1, 2, 3..."*<br>`https://iri.suomi.fi/model/ncbv/sequence`<br>Upper Property: owl:topDataProperty | Literal | — |

### Composite Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/CompositeRepresentationRule`
- **Description:** A class that replaces the "Complex Representation Rule" in previous NCBV versions; example of a composite rule for general signatory rights (legal representation): "CEO alone and two board members jointly"
- **Upper Class:** ncbv:RepresentationRule

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-82`<br>composite representation rule<br>*a representation rule that consist of two or more role or membership based representation rules* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| And<br>`https://iri.suomi.fi/model/ncbv/and`<br>Upper Property: owl:topObjectProperty | Representation Rule (Signatory Rule) | — |
| Or<br>`https://iri.suomi.fi/model/ncbv/or`<br>Upper Property: owl:topObjectProperty | Representation Rule (Signatory Rule) | — |

### Contact Point

- **IRI:** `https://iri.suomi.fi/model/ncbv/ContactPoint`
- **Description:** Information (e.g. e-mail address, telephone number) of a person or department through which the user can get in touch with. 
- **Upper Class:** ContactPoint

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6044`<br>contact point<br>*information through which one can get in touch with a person or a legal entity* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Contact Page<br>*A web page that could be used to reach out the Contact Point.*<br>`https://iri.suomi.fi/model/ncbv/contactPage`<br>Upper Property: owl:topDataProperty | Literal | — |
| Has Email<br>*An electronic address through which the Contact Point can be contacted.

Equivalent with schema:email*<br>`https://iri.suomi.fi/model/ncbv/email`<br>Upper Property: email | Literal | — |
| Has Telephone<br>`https://iri.suomi.fi/model/ncbv/hasTelephone`<br>Upper Property: telephone | Literal | — |

### Document

- **IRI:** `https://iri.suomi.fi/model/ncbv/Document`
- **Description:** —
- **Upper Class:** ncbv:Source, Document

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-93`<br>document<br>*TBD* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Title<br>`https://iri.suomi.fi/model/ncbv/title`<br>Upper Property: title | Literal | — |

### Identifier

- **IRI:** `https://iri.suomi.fi/model/ncbv/Identifier`
- **Description:** A unique set of characters used to identify the legal entity. 
- **Upper Class:** isa2core:Identifier

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-7`<br>identifier<br>*a structured reference that identifies an entity* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Date of Issue<br>*The date on which the something was issued; in this context for instance a Mandate or an Identifier.*<br>`https://iri.suomi.fi/model/ncbv/dateOfIssue`<br>Upper Property: isa2core:dateOfIssue | Literal | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue`<br>Upper Property: dct:identifier | Literal | — |
| Notation<br>*A string of characters to uniquely identify a concept.*<br>`https://iri.suomi.fi/model/ncbv/notation`<br>Upper Property: skos:notation | Literal | — |
| Schema Agency<br>*The name of the agency that issued the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemaAgency`<br>Upper Property: isa2core:issuingAuthorityName | Literal | — |
| Scheme Name<br>*Name of the scheme used to construct the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemeName`<br>Upper Property: isa2core:schemeName | Literal | — |
| Scheme URI<br>*URI of the scheme used to construct the identifier.*<br>`https://iri.suomi.fi/model/ncbv/schemeURI`<br>Upper Property: owl:topDataProperty | Literal | — |

### Legal Entity

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalEntity`
- **Description:** —
- **Upper Class:** isa2core:LegalEntity, ncbv:Agent

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6006`<br>legal entity<br>*a formal organization that is involved in economic activity* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Activity<br>*An active deed or action carried out by a legal entity*<br>`https://iri.suomi.fi/model/ncbv/hasActivity`<br>Upper Property: isa2core:companyActivity | Code | — |
| Beneficial Owners<br>*A natural person(s) who ultimately owns or controls the agent.*<br>`https://iri.suomi.fi/model/ncbv/beneficialOwners`<br>Upper Property: owl:topObjectProperty | Beneficial Owner | — |
| Contact Point<br>*The main contact information of the resource.*<br>`https://iri.suomi.fi/model/ncbv/hasContactPoint`<br>Upper Property: isa2core:contactPoint_, contactPoint | Contact Point | — |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier`<br>Upper Property: owl:topObjectProperty | Identifier | — |
| Legal Form<br>*The legal form of a legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasLegalForm`<br>Upper Property: owl:topObjectProperty | Code | `https://iri.suomi.fi/terminology/nbvoc/concept-16`<br>legal form<br>*a legal structure according to national legislation* |
| Legal Identifier<br>*An identifier that is given to a legal entity at registration.*<br>`https://iri.suomi.fi/model/ncbv/legalIdentifier`<br>Upper Property: isa2core:legalidentifier | Identifier | — |
| Legal Status<br>*An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasLegalStatus`<br>Upper Property: isa2core:companyStatus | Legal Status | `https://iri.suomi.fi/terminology/nbvoc/concept-23`<br>legal status<br>*an indication of whether a registration authority has registered some extraordinary proceedings for the legal entity* |
| Postal Address<br>*The address to which mail can be sent to the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/postalAddress`<br>Upper Property: isa2core:address_ | Address | — |
| Registered Address<br>*The address to which formal communications can be sent to the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/registeredAddress`<br>Upper Property: isa2core:registeredAddress | Address | — |
| Share Capital<br>*The total registered share capital for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasShareCapital`<br>Upper Property: owl:topObjectProperty | Share Capital | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Alternative Name<br>*Any other registered name by which a legal entity is known.*<br>`https://iri.suomi.fi/model/ncbv/alternativeName`<br>Upper Property: owl:topDataProperty | Literal | — |
| Legal Name<br>`https://iri.suomi.fi/model/ncbv/legalName`<br>Upper Property: isa2core:legalName | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-105`<br>legal name<br>*a name under which the legal entity is registered* |
| Registration Date<br>*The date when a public authority has registered the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/registrationDate`<br>Upper Property: registrationDate | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-22`<br>registration date<br>*The date when a public authority has registered the registered organisation* |

### Legal Resource

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalResource`
- **Description:** —
- **Upper Class:** ncbv:Source

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-90`<br>legal resource<br>*TBD* |

### Legal Status

- **IRI:** `https://iri.suomi.fi/model/ncbv/LegalStatus`
- **Description:** An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-23`<br>legal status<br>*an indication of whether a registration authority has registered some extraordinary proceedings for the legal entity* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Has Code<br>`https://iri.suomi.fi/model/ncbv/hasCode`<br>Upper Property: owl:topObjectProperty | Code | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Date<br>*The date when the legal status was registered.*<br>`https://iri.suomi.fi/model/ncbv/date`<br>Upper Property: owl:topDataProperty | Literal | — |

### Location

- **IRI:** `https://iri.suomi.fi/model/ncbv/Location`
- **Description:** —
- **Upper Class:** isa2core:Location

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-86`<br>location<br>*TBD* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Geographic Identifier<br>`https://iri.suomi.fi/model/ncbv/geographicIdentifier`<br>Upper Property: isa2core:geographicIdentifier | Literal | — |
| Geographic Name<br>*A recognizable name for a place, like "Eiffel Tower" or "Madrid". *<br>`https://iri.suomi.fi/model/ncbv/geographicName`<br>Upper Property: isa2core:geographicName | Literal | — |

### Mandate

- **IRI:** `https://iri.suomi.fi/model/ncbv/Mandate`
- **Description:** —
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-75`<br>mandate<br>*the terms under which a mandator grants or delegates authority or power to a mandatee* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| (Has) Geographical Scope/ Has Location / (Has) Geographical Coverage<br>*The association geographical scope points at a location; this describes the geographic region the mandate is valid.  *<br>`https://iri.suomi.fi/model/ncbv/hasGeographicalScope`<br>Upper Property: dct:spatial | Location | — |
| (Has) Mandator<br>*The Mandator association points always to the "primary mandator", who is the original source of the delegated power.*<br>`https://iri.suomi.fi/model/ncbv/hasMandator`<br>Upper Property: owl:topObjectProperty | Agent | `https://iri.suomi.fi/terminology/nbvoc/concept-76`<br>mandator<br>*an agent that grants authority to another agent to act on its behalf* |
| Has Duration<br>*The association "has duration" points to "Period of Time"and indicates the validity period of the mandate; like "1.1.2025-31.12.2025"*<br>`https://iri.suomi.fi/model/ncbv/hasDuration`<br>Upper Property: owl:topObjectProperty | Period of Time | — |
| Has Representation Rule<br>`https://iri.suomi.fi/model/ncbv/hasRepresentationRule`<br>Upper Property: owl:topObjectProperty | Representation Rule (Signatory Rule) | — |
| Has Restriction<br>`https://iri.suomi.fi/model/ncbv/hasRestriction`<br>Upper Property: owl:topObjectProperty | Restriction | — |
| Has Scope<br>`https://iri.suomi.fi/model/ncbv/hasScope`<br>Upper Property: owl:topObjectProperty | Scope | — |
| Has Source<br>`https://iri.suomi.fi/model/ncbv/hasSource`<br>Upper Property: owl:topObjectProperty | Source | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Date of Issue<br>*The date on which the something was issued; in this context for instance a Mandate or an Identifier.*<br>`https://iri.suomi.fi/model/ncbv/dateOfIssue`<br>Upper Property: isa2core:dateOfIssue | Literal | — |
| Delegable<br>*An indicator of whether the Mandate can be delegated or not.*<br>`https://iri.suomi.fi/model/ncbv/delegable`<br>Upper Property: owl:topDataProperty | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-79`<br>delegable<br>*capable of being delegated* |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue`<br>Upper Property: dct:identifier | Literal | — |
| Modified<br>*The date of the last update of something like a Mandate.

upper attribute
http://purl.org/dc/terms/modified


dcterms:modified*<br>`https://iri.suomi.fi/model/ncbv/modified`<br>Upper Property: owl:topDataProperty | Literal | — |
| Status<br>*A mandate's status can be for instance: active, withdrawn/inactive > Tore checks values 

Upper attribute: adms:status*<br>`https://iri.suomi.fi/model/ncbv/status`<br>Upper Property: owl:topDataProperty | Literal | — |

### Mandate Transfer

- **IRI:** `https://iri.suomi.fi/model/ncbv/MandateTransfer`
- **Description:** A class for documenting the possible transfer (or delegation) of a Mandate from a previous Mandatee to another; example: Mandate is granted by CEO of Company, is delegable, the first Mandatee delegated the Mandate to another Agent who becomes the new Mandatee; the transfer of the Mandate is logged in this class.
- **Upper Class:** ncbv:Source

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-89`<br>mandate transfer<br>*TBD* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Mandatee<br>`https://iri.suomi.fi/model/ncbv/mandatee`<br>Upper Property: owl:topObjectProperty | Agent | — |
| Original Mandate<br>`https://iri.suomi.fi/model/ncbv/originalMandate`<br>Upper Property: owl:topObjectProperty | Mandate | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Date<br>*The date when the legal status was registered.*<br>`https://iri.suomi.fi/model/ncbv/date`<br>Upper Property: owl:topDataProperty | Literal | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue`<br>Upper Property: dct:identifier | Literal | — |

### Membership

- **IRI:** `https://iri.suomi.fi/model/ncbv/Membership`
- **Description:** The Membership class describes certain types of relationships between agents (persons and legal entities). 

A person can be a member of an association, employed by a company, be a board member in or the CEO of a limited company.

The official definition of Membership can be found here: 
https://www.w3.org/TR/vocab-org/#org:Membership

This technical note does not change the content of the official definition of the Membership class.

Upper class: 
https://www.w3.org/ns/org#Membership
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-78`<br>membership<br>*a structured way to represent an agent's participation in an other agent (usually an organization)* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Member<br>`https://iri.suomi.fi/model/ncbv/member`<br>Upper Property: owl:topObjectProperty | Agent | — |
| Role<br>*Indicates the Role that the Agent plays in a Membership relationship with a legal entity.*<br>`https://iri.suomi.fi/model/ncbv/hasRole`<br>Upper Property: role | Role | — |

### Membership Based Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/MembershipBasedRepresentationRule`
- **Description:** A class that replaces the previous "Simple Representation Rule" class (partially); example: a mandate granted to "a man on the street", pointing at a certain person as a  Member of the Mandator (Membership in this case could be "mandatee" or similar).
- **Upper Class:** ncbv:RepresentationRule

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-84`<br>membership based representation rule<br>*a representation rule where the rule is based on the membership relation between agents* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Defines Valid Membership<br>*The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.*<br>`https://iri.suomi.fi/model/ncbv/definesValidMembership`<br>Upper Property: owl:topObjectProperty | Membership | — |
| Member Quantifier<br>*Specifies a qualitative quantity or proportion of members required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).*<br>`https://iri.suomi.fi/model/ncbv/memberQuantifier`<br>Upper Property: owl:topObjectProperty | Concept | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Minimum Number of Members<br>*The number of members required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...*<br>`https://iri.suomi.fi/model/ncbv/minimumNumberOfMembers`<br>Upper Property: owl:topDataProperty | Literal | — |

### Object

- **IRI:** `https://iri.suomi.fi/model/ncbv/Object`
- **Description:** Example: can be a specific house, car; has an Identifier (car registration number)
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-87`<br>object<br>*TBD* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier`<br>Upper Property: owl:topObjectProperty | Identifier | — |
| Type<br>`https://iri.suomi.fi/model/ncbv/type`<br>Upper Property: owl:topObjectProperty | Concept | — |

### Period of Time

- **IRI:** `https://iri.suomi.fi/model/ncbv/PeriodOfTime`
- **Description:** —
- **Upper Class:** dct:PeriodOfTime

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| End Date<br>`https://iri.suomi.fi/model/ncbv/endDate`<br>Upper Property: owl:topDataProperty | Literal | — |
| Start Date<br>`https://iri.suomi.fi/model/ncbv/startDate`<br>Upper Property: owl:topDataProperty | Literal | — |

### Person

- **IRI:** `https://iri.suomi.fi/model/ncbv/Person`
- **Description:** A individual human being who may be dead or alive, but not imaginary.
- **Upper Class:** ncbv:Agent, isa2core:Person, Person

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6005`<br>person<br>*an individual human being who may be dead or alive, but not imaginary* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Identifier<br>`https://iri.suomi.fi/model/ncbv/hasIdentifier`<br>Upper Property: owl:topObjectProperty | Identifier | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Date Of Birth<br>*The point in time on which the Person was born. Persons can be registered with a membership in a legal entity whithout a identifier being a national registration number.*<br>`https://iri.suomi.fi/model/ncbv/dateOfBirth`<br>Upper Property: birthDate | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-6013`<br>date of birth<br>*a point in time on which a person was born* |
| Full Name<br>*The complete name of the Person as one string.*<br>`https://iri.suomi.fi/model/ncbv/fullName`<br>Upper Property: name | Literal | `https://iri.suomi.fi/terminology/nbvoc/concept-6012`<br>full name<br>*the complete name of the Person as one string.* |

### Representation Rule (Signatory Rule)

- **IRI:** `https://iri.suomi.fi/model/ncbv/RepresentationRule`
- **Description:** A rule that describes who or which agents a mandate is granted to. 

The rule can be used both in the case of legal representation, when a CEO or a board member signs for the agent (company) based on their official role in the company, as well as when a mandate is given to a specific person ("a man on the street") who has no previous affiliation to the mandating agent.
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6011`<br>representation rule<br>*a rule that defines which agent(s) can act on behalf of another agent* |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description`<br>Upper Property: isa2core:description | Literal | — |
| Sequence<br>*An indicator for the order of a series of values; "1, 2, 3..."*<br>`https://iri.suomi.fi/model/ncbv/sequence`<br>Upper Property: owl:topDataProperty | Literal | — |

### Restriction

- **IRI:** `https://iri.suomi.fi/model/ncbv/Restriction`
- **Description:** —
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-88`<br>restriction<br>*TBD* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Type<br>`https://iri.suomi.fi/model/ncbv/type`<br>Upper Property: owl:topObjectProperty | Restriction Type | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Value<br>`https://iri.suomi.fi/model/ncbv/value`<br>Upper Property: isa2core:value | Literal | — |

### Restriction Type

- **IRI:** `https://iri.suomi.fi/model/ncbv/RestrictionType`
- **Description:** A class for describing what the value in the Restriction class means; example: Restriction.value: 10000; RestrictionType: Datatype: Decimal or Integer; Unit: SEK, NOK, EUR... Name: Monetary Amount restriction; Description: "The maximum monetary amount to be used with the Mandate (like: "purchasing a car")  
- **Upper Class:** owl:Thing

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Datatype<br>`https://iri.suomi.fi/model/ncbv/datatype`<br>Upper Property: owl:topDataProperty | Literal | — |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description`<br>Upper Property: isa2core:description | Literal | — |
| Identifier<br>*The identifier of a mandate is used to separate different mandates from each other, making it unique.*<br>`https://iri.suomi.fi/model/ncbv/identifierValue`<br>Upper Property: dct:identifier | Literal | — |
| Unit<br>`https://iri.suomi.fi/model/ncbv/unit`<br>Upper Property: owl:topDataProperty | Literal | — |

### Role

- **IRI:** `https://iri.suomi.fi/model/ncbv/Role`
- **Description:** In the context of Mandates, the Role class 
indicates the Role that the Agent plays in a Membership relationship with a legal entity. 

Upper class: https://www.w3.org/TR/vocab-org/#class-role

Suggested code list for Nordic use cases: http://uri.suomi.fi/codelist/verotus/membershiproletypes
- **Upper Class:** skos:Concept

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6004`<br>role<br>*a defined position or function that an agent holds within another agent* |

### Role Based Representation Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/RoleBasedRepresentationRule`
- **Description:** A class that replaces (partially) the Simple Representation Rule in previous versions; example: signatory rights rule "CEO alone"
- **Upper Class:** ncbv:RepresentationRule

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-83`<br>role based representation rule<br>*a representation rule where the rule is based on the roles in an agent (company)* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Defines Valid Role <br>*The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.*<br>`https://iri.suomi.fi/model/ncbv/definesValidRole`<br>Upper Property: owl:topObjectProperty | Role | — |
| Role Holder Quantifier<br>*Specifies a qualitative quantity or proportion of role holders required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).*<br>`https://iri.suomi.fi/model/ncbv/roleHolderQuantifier`<br>Upper Property: owl:topObjectProperty | Concept | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Minimum Number of Role Holders<br>*The number of role holders required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...*<br>`https://iri.suomi.fi/model/ncbv/minimumNumberOfRoleHolders`<br>Upper Property: owl:topDataProperty | Literal | — |

### Rule

- **IRI:** `https://iri.suomi.fi/model/ncbv/Rule`
- **Description:** eli:Rule
- **Upper Class:** ncbv:Source

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Implements<br>`https://iri.suomi.fi/model/ncbv/implements`<br>Upper Property: isa2core:implements | Legal Resource | — |

### Scope

- **IRI:** `https://iri.suomi.fi/model/ncbv/Scope`
- **Description:** A class to define what powers the Mandator grants to the Mandatee through the Mandate.

Example: A gives signatory power to B. A grants B the power to buy a car for the company. 
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-92`<br>scope<br>*TBD* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Applies to Object<br>`https://iri.suomi.fi/model/ncbv/appliesToObject`<br>Upper Property: owl:topObjectProperty | Object | — |
| Power<br>`https://iri.suomi.fi/model/ncbv/power`<br>Upper Property: owl:topObjectProperty | Concept | — |

### Share Capital

- **IRI:** `https://iri.suomi.fi/model/ncbv/ShareCapital`
- **Description:** Share capital refers to the total amount of capital raised by a legal entity through the issuance of shares to shareholders.
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-6040`<br>share capital<br>*the total amount of capital raised by a legal entity through the issuance of shares to shareholders* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Total Capital Amount<br>*The total capital amount of the Legal Entity's (company's) share capital, expressed in monetary values.*<br>`https://iri.suomi.fi/model/ncbv/totalCapitalAmount`<br>Upper Property: owl:topObjectProperty | Amount | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Capital Type<br>*Values expressed in a separate code list, could contain the following: 

Capital Type	Description
Authorized Share Capital	Maximum capital a company is legally allowed to issue, as stated in its statutes

Issued Share Capital	Capital corresponding to the total number of shares that have actually been issued

Subscribed Share Capital	Part of issued capital that investors have agreed to purchase

Paid-up Share Capital	Subscribed capital for which the company has received payment

Called-up Share Capital	Subscribed capital where payment has been requested (called), but not necessarily received

Unpaid Capital	Portion of called-up capital still owed by shareholders

Nominal / Par Value	The base value assigned to each share; may also be relevant at share type level

Equity vs Debt hybrid	Some instruments may qualify as equity under certain laws but be treated as debt elsewhere*<br>`https://iri.suomi.fi/model/ncbv/capitalType`<br>Upper Property: owl:topDataProperty | Literal | — |
| Number of Shares<br>*The total number of individual shares associated with the specified share capital value.

This count represents the share units issued, authorized, subscribed, or paid-up, depending on the type of capital being described (capitalType).*<br>`https://iri.suomi.fi/model/ncbv/numberOfShares`<br>Upper Property: owl:topDataProperty | Literal | — |

### Source

- **IRI:** `https://iri.suomi.fi/model/ncbv/Source`
- **Description:** A class to describe what the powers that are delegated by the Mandator are originally based on;  example: "law", "statutes of company"; "another mandate" etc.
- **Upper Class:** owl:Thing

#### NBV linkage

| NBV / SKOS |
| --- |
| `https://iri.suomi.fi/terminology/nbvoc/concept-91`<br>source<br>*TBD* |

#### Object properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Type<br>`https://iri.suomi.fi/model/ncbv/type`<br>Upper Property: owl:topObjectProperty | Concept | — |

#### Datatype properties

| Property / Description / IRI / Upper Property | Value type(s) in this class | NBV / SKOS |
| --- | --- | --- |
| Description<br>*An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
*<br>`https://iri.suomi.fi/model/ncbv/description`<br>Upper Property: isa2core:description | Literal | — |

## Ungrouped properties

These properties are declared in the NCBV ontology but are not used in any explicit OWL restriction for the NCBV classes in this Turtle file.

### Object properties without explicit class association

| Property / Description / IRI / Upper Property | NBV / SKOS |
| --- | --- |
| All of<br>*Constraint property that requires all of the agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/allOf`<br>Upper Property: ncbv:jointly | — |
| Alone<br>*Requires holder of the post to sign alone.*<br>`https://iri.suomi.fi/model/ncbv/alone`<br>Upper Property: owl:topObjectProperty | — |
| Consists of Representation Rule<br>`https://iri.suomi.fi/model/ncbv/consistsOfRepresentationRule`<br>Upper Property: owl:topObjectProperty | — |
| Five of<br>*Requires five of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/fiveOf`<br>Upper Property: owl:topObjectProperty | — |
| Four of<br>*Requires four of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/fourOf`<br>Upper Property: owl:topObjectProperty | — |
| Grants Representation Right<br>*The signatory rights that is registered for the legal entity.*<br>`https://iri.suomi.fi/model/ncbv/grantsRepresentationRight`<br>Upper Property: owl:topObjectProperty | — |
| Held by Legal Entity<br>*Indicates the legal entity that is holding the post.*<br>`https://iri.suomi.fi/model/ncbv/heldByLegalEntity`<br>Upper Property: owl:topObjectProperty | — |
| Held by Person<br>*Indicates the person that holds the post.
*<br>`https://iri.suomi.fi/model/ncbv/heldByPerson`<br>Upper Property: owl:topObjectProperty | — |
| Jointly<br>`https://iri.suomi.fi/model/ncbv/jointly`<br>Upper Property: owl:topObjectProperty | — |
| Majority of<br>*Constraint property that requires majority of agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/majorityOf`<br>Upper Property: owl:topObjectProperty | — |
| One of<br>*Requires one of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/oneOf`<br>Upper Property: owl:topObjectProperty | — |
| Subject<br>`https://iri.suomi.fi/model/ncbv/subject`<br>Upper Property: subject | — |
| Three of<br>*Requires two of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/threeOf`<br>Upper Property: owl:topObjectProperty | — |
| Transfer of Mandate<br>`https://iri.suomi.fi/model/ncbv/transferOfMandate`<br>Upper Property: owl:topObjectProperty | — |
| Two of<br>*Requires two of the defined agents holding a post to sign.*<br>`https://iri.suomi.fi/model/ncbv/twoOf`<br>Upper Property: owl:topObjectProperty | — |

### Datatype properties without explicit class association

| Property / Description / IRI / Upper Property | NBV / SKOS |
| --- | --- |
| Amount<br>*The amount of money.*<br>`https://iri.suomi.fi/model/ncbv/amount`<br>Upper Property: owl:topDataProperty | — |
| Code Identifier<br>*An identifier for the code, can be of any format like an URI or just alphanumeric.*<br>`https://iri.suomi.fi/model/ncbv/codeIdentifier`<br>Upper Property: dct:identifier | — |
| Code name<br>`https://iri.suomi.fi/model/ncbv/codeName`<br>Upper Property: skos:prefLabel | — |
| In Classification<br>*NACE codes are published in scheme http://publications.europa.eu/resource/authority/ux2/nace2/nace2. Description in text for all NACE codes in all EU languages can be found there.*<br>`https://iri.suomi.fi/model/ncbv/inClassification`<br>Upper Property: owl:topDataProperty | — |
| Object Type<br>`https://iri.suomi.fi/model/ncbv/objectType`<br>Upper Property: owl:topDataProperty | — |
| Preferred Label<br>*The preferred label attribute is used to name the actual scope of the Mandate; example: "Car Purchase"; "Filing a Declaration (of some type)"; or using a specific national eService (mandates given in the Swedish Mina Ombud or the Finnish Suomi.fi eAuthorizations).  *<br>`https://iri.suomi.fi/model/ncbv/prefLabel`<br>Upper Property: skos:prefLabel | — |
| Reference<br>*Reference to the description of the NACE code.*<br>`https://iri.suomi.fi/model/ncbv/reference`<br>Upper Property: owl:topDataProperty | — |
