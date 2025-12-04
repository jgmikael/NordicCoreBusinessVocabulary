# Nordic Core Business Vocabulary (NCBV)

## Table of Contents

- [Classes](#classes)
- [Object Properties](#object-properties)
- [Datatype Properties](#datatype-properties)

## Classes

### Address
**IRI:** `https://iri.suomi.fi/model/ncbv/Address`  
**Description:** An identification of the fixed location of a geographic place.

### Agent
**IRI:** `https://iri.suomi.fi/model/ncbv/Agent`  
**Description:** 

### Amount
**IRI:** `https://iri.suomi.fi/model/ncbv/MonetaryAmount`  
**Description:** see unece:Amount and schema:MonetaryAmount

### Beneficial Owner
**IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwner`  
**Description:** A natural person(s) who ultimately owns or controls the agent.

### Beneficial Owner Role
**IRI:** `https://iri.suomi.fi/model/ncbv/BeneficialOwnerRole`  
**Description:** 

### Code
**IRI:** `https://iri.suomi.fi/model/ncbv/Code`  
**Description:** A generic class for any code values that a specific class can have; in the NCBV the Code class contains code values for legal form, legal status and (economic) activity.  

### Composite Representation Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/CompositeRepresentationRule`  
**Description:** A class that replaces the "Complex Representation Rule" in previous NCBV versions; example of a composite rule for general signatory rights (legal representation): "CEO alone and two board members jointly"

### Contact Point
**IRI:** `https://iri.suomi.fi/model/ncbv/ContactPoint`  
**Description:** Information (e.g. e-mail address, telephone number) of a person or department through which the user can get in touch with. 

### Document
**IRI:** `https://iri.suomi.fi/model/ncbv/Document`  
**Description:** 

### Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/Identifier`  
**Description:** A unique set of characters used to identify the legal entity. 

### Legal Entity
**IRI:** `https://iri.suomi.fi/model/ncbv/LegalEntity`  
**Description:** 

### Legal Resource
**IRI:** `https://iri.suomi.fi/model/ncbv/LegalResource`  
**Description:** 

### Legal Status
**IRI:** `https://iri.suomi.fi/model/ncbv/LegalStatus`  
**Description:** An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.

### Location
**IRI:** `https://iri.suomi.fi/model/ncbv/Location`  
**Description:** 

### Mandate
**IRI:** `https://iri.suomi.fi/model/ncbv/Mandate`  
**Description:** 

### Mandate Transfer
**IRI:** `https://iri.suomi.fi/model/ncbv/MandateTransfer`  
**Description:** A class for documenting the possible transfer (or delegation) of a Mandate from a previous Mandatee to another; example: Mandate is granted by CEO of Company, is delegable, the first Mandatee delegated the Mandate to another Agent who becomes the new Mandatee; the transfer of the Mandate is logged in this class.

### Membership
**IRI:** `https://iri.suomi.fi/model/ncbv/Membership`  
**Description:** The Membership class describes certain types of relationships between agents (persons and legal entities). 

A person can be a member of an association, employed by a company, be a board member in or the CEO of a limited company.

The official definition of Membership can be found here: 
https://www.w3.org/TR/vocab-org/#org:Membership

This technical note does not change the content of the official definition of the Membership class.

Upper class: 
https://www.w3.org/ns/org#Membership

### Membership Based Representation Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/MembershipBasedRepresentationRule`  
**Description:** A class that replaces the previous "Simple Representation Rule" class (partially); example: a mandate granted to "a man on the street", pointing at a certain person as a  Member of the Mandator (Membership in this case could be "mandatee" or similar).

### Object
**IRI:** `https://iri.suomi.fi/model/ncbv/Object`  
**Description:** Example: can be a specific house, car; has an Identifier (car registration number)

### Period of Time
**IRI:** `https://iri.suomi.fi/model/ncbv/PeriodOfTime`  
**Description:** 

### Person
**IRI:** `https://iri.suomi.fi/model/ncbv/Person`  
**Description:** A individual human being who may be dead or alive, but not imaginary.

### Representation Rule (Signatory Rule)
**IRI:** `https://iri.suomi.fi/model/ncbv/RepresentationRule`  
**Description:** A rule that describes who or which agents a mandate is granted to. 

The rule can be used both in the case of legal representation, when a CEO or a board member signs for the agent (company) based on their official role in the company, as well as when a mandate is given to a specific person ("a man on the street") who has no previous affiliation to the mandating agent.

### Restriction
**IRI:** `https://iri.suomi.fi/model/ncbv/Restriction`  
**Description:** 

### Restriction Type
**IRI:** `https://iri.suomi.fi/model/ncbv/RestrictionType`  
**Description:** A class for describing what the value in the Restriction class means; example: Restriction.value: 10000; RestrictionType: Datatype: Decimal or Integer; Unit: SEK, NOK, EUR... Name: Monetary Amount restriction; Description: "The maximum monetary amount to be used with the Mandate (like: "purchasing a car")  

### Role
**IRI:** `https://iri.suomi.fi/model/ncbv/Role`  
**Description:** In the context of Mandates, the Role class 
indicates the Role that the Agent plays in a Membership relationship with a legal entity. 

Upper class: https://www.w3.org/TR/vocab-org/#class-role

Suggested code list for Nordic use cases: http://uri.suomi.fi/codelist/verotus/membershiproletypes

### Role Based Representation Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/RoleBasedRepresentationRule`  
**Description:** A class that replaces (partially) the Simple Representation Rule in previous versions; example: signatory rights rule "CEO alone"

### Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/Rule`  
**Description:** eli:Rule

### Scope
**IRI:** `https://iri.suomi.fi/model/ncbv/Scope`  
**Description:** A class to define what powers the Mandator grants to the Mandatee through the Mandate.

Example: A gives signatory power to B. A grants B the power to buy a car for the company. 

### Share Capital
**IRI:** `https://iri.suomi.fi/model/ncbv/ShareCapital`  
**Description:** Share capital refers to the total amount of capital raised by a legal entity through the issuance of shares to shareholders.

### Source
**IRI:** `https://iri.suomi.fi/model/ncbv/Source`  
**Description:** A class to describe what the powers that are delegated by the Mandator are originally based on;  example: "law", "statutes of company"; "another mandate" etc.

### nc26a0a7b188c463fbda167dec7465ab9b1
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b1`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b100
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b100`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b109
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b109`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b118
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b118`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b123
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b123`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b126
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b126`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b133
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b133`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b142
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b142`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b145
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b145`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b150
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b150`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b16
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b16`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b177
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b177`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b182
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b182`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b187
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b187`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b208
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b208`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b221
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b221`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b226
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b226`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b231
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b231`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b25
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b25`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b32
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b32`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b37
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b37`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b42
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b42`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b49
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b49`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b54
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b54`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b6
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b6`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b79
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b79`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b84
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b84`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b9
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b9`  
**Description:** 

### nc26a0a7b188c463fbda167dec7465ab9b93
**IRI:** `nc26a0a7b188c463fbda167dec7465ab9b93`  
**Description:** 

## Object Properties

### (Has) Geographical Scope/ Has Location / (Has) Geographical Coverage
**IRI:** `https://iri.suomi.fi/model/ncbv/hasGeographicalScope`  
**Description:** The association geographical scope points at a location; this describes the geographic region the mandate is valid.    
**Domain:** —  
**Range:** —

### (Has) Mandator
**IRI:** `https://iri.suomi.fi/model/ncbv/hasMandator`  
**Description:** The Mandator association points always to the "primary mandator", who is the original source of the delegated power.  
**Domain:** —  
**Range:** —

### Activity
**IRI:** `https://iri.suomi.fi/model/ncbv/hasActivity`  
**Description:** An active deed or action carried out by a legal entity  
**Domain:** —  
**Range:** —

### All of
**IRI:** `https://iri.suomi.fi/model/ncbv/allOf`  
**Description:** Constraint property that requires all of the agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Alone
**IRI:** `https://iri.suomi.fi/model/ncbv/alone`  
**Description:** Requires holder of the post to sign alone.  
**Domain:** —  
**Range:** Membership

### And
**IRI:** `https://iri.suomi.fi/model/ncbv/and`  
**Description:**   
**Domain:** —  
**Range:** —

### Applies to Object
**IRI:** `https://iri.suomi.fi/model/ncbv/appliesToObject`  
**Description:**   
**Domain:** —  
**Range:** —

### Beneficial Owners
**IRI:** `https://iri.suomi.fi/model/ncbv/beneficialOwners`  
**Description:** A natural person(s) who ultimately owns or controls the agent.  
**Domain:** —  
**Range:** —

### Consists of Representation Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/consistsOfRepresentationRule`  
**Description:**   
**Domain:** —  
**Range:** —

### Contact Point
**IRI:** `https://iri.suomi.fi/model/ncbv/hasContactPoint`  
**Description:** The main contact information of the resource.  
**Domain:** —  
**Range:** —

### Defines Valid Membership
**IRI:** `https://iri.suomi.fi/model/ncbv/definesValidMembership`  
**Description:** The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.  
**Domain:** —  
**Range:** —

### Defines Valid Role 
**IRI:** `https://iri.suomi.fi/model/ncbv/definesValidRole`  
**Description:** The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or.  
**Domain:** —  
**Range:** —

### Five of
**IRI:** `https://iri.suomi.fi/model/ncbv/fiveOf`  
**Description:** Requires five of the defined agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Four of
**IRI:** `https://iri.suomi.fi/model/ncbv/fourOf`  
**Description:** Requires four of the defined agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Grants Mandate
**IRI:** `https://iri.suomi.fi/model/ncbv/grantsMandate`  
**Description:**   
**Domain:** —  
**Range:** —

### Grants Representation Right
**IRI:** `https://iri.suomi.fi/model/ncbv/grantsRepresentationRight`  
**Description:** The signatory rights that is registered for the legal entity.  
**Domain:** —  
**Range:** —

### Has Code
**IRI:** `https://iri.suomi.fi/model/ncbv/hasCode`  
**Description:**   
**Domain:** —  
**Range:** core#Concept

### Has Duration
**IRI:** `https://iri.suomi.fi/model/ncbv/hasDuration`  
**Description:** The association "has duration" points to "Period of Time"and indicates the validity period of the mandate; like "1.1.2025-31.12.2025"  
**Domain:** —  
**Range:** —

### Has Member
**IRI:** `https://iri.suomi.fi/model/ncbv/hasMember`  
**Description:**   
**Domain:** —  
**Range:** —

### Has Representation Rule
**IRI:** `https://iri.suomi.fi/model/ncbv/hasRepresentationRule`  
**Description:**   
**Domain:** —  
**Range:** —

### Has Restriction
**IRI:** `https://iri.suomi.fi/model/ncbv/hasRestriction`  
**Description:**   
**Domain:** —  
**Range:** —

### Has Scope
**IRI:** `https://iri.suomi.fi/model/ncbv/hasScope`  
**Description:**   
**Domain:** —  
**Range:** —

### Has Source
**IRI:** `https://iri.suomi.fi/model/ncbv/hasSource`  
**Description:**   
**Domain:** —  
**Range:** —

### Held by Legal Entity
**IRI:** `https://iri.suomi.fi/model/ncbv/heldByLegalEntity`  
**Description:** Indicates the legal entity that is holding the post.  
**Domain:** —  
**Range:** —

### Held by Person
**IRI:** `https://iri.suomi.fi/model/ncbv/heldByPerson`  
**Description:** Indicates the person that holds the post.
  
**Domain:** —  
**Range:** —

### Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/hasIdentifier`  
**Description:**   
**Domain:** —  
**Range:** —

### Implements
**IRI:** `https://iri.suomi.fi/model/ncbv/implements`  
**Description:**   
**Domain:** —  
**Range:** —

### Is a Person
**IRI:** `https://iri.suomi.fi/model/ncbv/isPerson`  
**Description:**   
**Domain:** —  
**Range:** Person

### Jointly
**IRI:** `https://iri.suomi.fi/model/ncbv/jointly`  
**Description:**   
**Domain:** —  
**Range:** —

### Legal Form
**IRI:** `https://iri.suomi.fi/model/ncbv/hasLegalForm`  
**Description:** The legal form of a legal entity.  
**Domain:** —  
**Range:** Code

### Legal Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/legalIdentifier`  
**Description:** An identifier that is given to a legal entity at registration.  
**Domain:** —  
**Range:** —

### Legal Status
**IRI:** `https://iri.suomi.fi/model/ncbv/hasLegalStatus`  
**Description:** An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity.  
**Domain:** —  
**Range:** —

### Majority of
**IRI:** `https://iri.suomi.fi/model/ncbv/majorityOf`  
**Description:** Constraint property that requires majority of agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Mandatee
**IRI:** `https://iri.suomi.fi/model/ncbv/mandatee`  
**Description:**   
**Domain:** —  
**Range:** —

### Member
**IRI:** `https://iri.suomi.fi/model/ncbv/member`  
**Description:**   
**Domain:** —  
**Range:** —

### Member Quantifier
**IRI:** `https://iri.suomi.fi/model/ncbv/memberQuantifier`  
**Description:** Specifies a qualitative quantity or proportion of members required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).  
**Domain:** —  
**Range:** core#Concept

### One of
**IRI:** `https://iri.suomi.fi/model/ncbv/oneOf`  
**Description:** Requires one of the defined agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Or
**IRI:** `https://iri.suomi.fi/model/ncbv/or`  
**Description:**   
**Domain:** —  
**Range:** —

### Original Mandate
**IRI:** `https://iri.suomi.fi/model/ncbv/originalMandate`  
**Description:**   
**Domain:** —  
**Range:** —

### Postal Address
**IRI:** `https://iri.suomi.fi/model/ncbv/postalAddress`  
**Description:** The address to which mail can be sent to the legal entity.  
**Domain:** —  
**Range:** —

### Power
**IRI:** `https://iri.suomi.fi/model/ncbv/power`  
**Description:**   
**Domain:** —  
**Range:** —

### Registered Address
**IRI:** `https://iri.suomi.fi/model/ncbv/registeredAddress`  
**Description:** The address to which formal communications can be sent to the legal entity.  
**Domain:** —  
**Range:** —

### Role
**IRI:** `https://iri.suomi.fi/model/ncbv/hasRole`  
**Description:** Indicates the Role that the Agent plays in a Membership relationship with a legal entity.  
**Domain:** —  
**Range:** —

### Role Holder Quantifier
**IRI:** `https://iri.suomi.fi/model/ncbv/roleHolderQuantifier`  
**Description:** Specifies a qualitative quantity or proportion of role holders required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”).  
**Domain:** —  
**Range:** —

### Share Capital
**IRI:** `https://iri.suomi.fi/model/ncbv/hasShareCapital`  
**Description:** The total registered share capital for the legal entity.  
**Domain:** —  
**Range:** —

### Subject
**IRI:** `https://iri.suomi.fi/model/ncbv/subject`  
**Description:**   
**Domain:** —  
**Range:** —

### Three of
**IRI:** `https://iri.suomi.fi/model/ncbv/threeOf`  
**Description:** Requires two of the defined agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Total Capital Amount
**IRI:** `https://iri.suomi.fi/model/ncbv/totalCapitalAmount`  
**Description:** The total capital amount of the Legal Entity's (company's) share capital, expressed in monetary values.  
**Domain:** —  
**Range:** —

### Transfer of Mandate
**IRI:** `https://iri.suomi.fi/model/ncbv/transferOfMandate`  
**Description:**   
**Domain:** —  
**Range:** —

### Two of
**IRI:** `https://iri.suomi.fi/model/ncbv/twoOf`  
**Description:** Requires two of the defined agents holding a post to sign.  
**Domain:** —  
**Range:** —

### Type
**IRI:** `https://iri.suomi.fi/model/ncbv/type`  
**Description:**   
**Domain:** —  
**Range:** —

## Datatype Properties

### Admin Unit Level 1
**IRI:** `https://iri.suomi.fi/model/ncbv/adminUnitLevel1`  
**Description:** The uppermost administrative unit for the address, almost always a country.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Admin Unit Level 2
**IRI:** `https://iri.suomi.fi/model/ncbv/adminUnitLevel2`  
**Description:** The name of a secondary level/region of the address, usually a county, state or other such area that typically encompasses several localities.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Alternative Name
**IRI:** `https://iri.suomi.fi/model/ncbv/alternativeName`  
**Description:** Any other registered name by which a legal entity is known.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Amount
**IRI:** `https://iri.suomi.fi/model/ncbv/amount`  
**Description:** The amount of money.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Capital Type
**IRI:** `https://iri.suomi.fi/model/ncbv/capitalType`  
**Description:** Values expressed in a separate code list, could contain the following: 

Capital Type	Description
Authorized Share Capital	Maximum capital a company is legally allowed to issue, as stated in its statutes

Issued Share Capital	Capital corresponding to the total number of shares that have actually been issued

Subscribed Share Capital	Part of issued capital that investors have agreed to purchase

Paid-up Share Capital	Subscribed capital for which the company has received payment

Called-up Share Capital	Subscribed capital where payment has been requested (called), but not necessarily received

Unpaid Capital	Portion of called-up capital still owed by shareholders

Nominal / Par Value	The base value assigned to each share; may also be relevant at share type level

Equity vs Debt hybrid	Some instruments may qualify as equity under certain laws but be treated as debt elsewhere  
**Domain:** —  
**Range:** rdf-schema#Literal

### Care of
**IRI:** `https://iri.suomi.fi/model/ncbv/careOf`  
**Description:** Used when an address is at the address of another person or legal entity.
  
**Domain:** —  
**Range:** rdf-schema#Literal

### Code
**IRI:** `https://iri.suomi.fi/model/ncbv/codeValue`  
**Description:** The actual code value from a selected code list.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Code Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/codeIdentifier`  
**Description:** An identifier for the code, can be of any format like an URI or just alphanumeric.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Code name
**IRI:** `https://iri.suomi.fi/model/ncbv/codeName`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Contact Page
**IRI:** `https://iri.suomi.fi/model/ncbv/contactPage`  
**Description:** A web page that could be used to reach out the Contact Point.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Currency
**IRI:** `https://iri.suomi.fi/model/ncbv/currency`  
**Description:** The currency in which the monetary amount is expressed. ISO 4217 currency format, e.g. "EUR".  
**Domain:** —  
**Range:** rdf-schema#Literal

### Datatype
**IRI:** `https://iri.suomi.fi/model/ncbv/datatype`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Date
**IRI:** `https://iri.suomi.fi/model/ncbv/date`  
**Description:** The date when the legal status was registered.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Date Of Birth
**IRI:** `https://iri.suomi.fi/model/ncbv/dateOfBirth`  
**Description:** The point in time on which the Person was born. Persons can be registered with a membership in a legal entity whithout a identifier being a national registration number.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Date of Issue
**IRI:** `https://iri.suomi.fi/model/ncbv/dateOfIssue`  
**Description:** The date on which the something was issued; in this context for instance a Mandate or an Identifier.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Delegable
**IRI:** `https://iri.suomi.fi/model/ncbv/delegable`  
**Description:** An indicator of whether the Mandate can be delegated or not.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Description
**IRI:** `https://iri.suomi.fi/model/ncbv/description`  
**Description:** An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
  
**Domain:** —  
**Range:** rdf-schema#Literal

### End Date
**IRI:** `https://iri.suomi.fi/model/ncbv/endDate`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Full Address
**IRI:** `https://iri.suomi.fi/model/ncbv/fullAddress`  
**Description:** The complete address written as a string.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Full Name
**IRI:** `https://iri.suomi.fi/model/ncbv/fullName`  
**Description:** The complete name of the Person as one string.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Geographic Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/geographicIdentifier`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Geographic Name
**IRI:** `https://iri.suomi.fi/model/ncbv/geographicName`  
**Description:** A recognizable name for a place, like "Eiffel Tower" or "Madrid".   
**Domain:** —  
**Range:** rdf-schema#Literal

### Has Email
**IRI:** `https://iri.suomi.fi/model/ncbv/email`  
**Description:** An electronic address through which the Contact Point can be contacted.

Equivalent with schema:email  
**Domain:** —  
**Range:** rdf-schema#Literal

### Has Telephone
**IRI:** `https://iri.suomi.fi/model/ncbv/hasTelephone`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Identifier
**IRI:** `https://iri.suomi.fi/model/ncbv/identifierValue`  
**Description:** The identifier of a mandate is used to separate different mandates from each other, making it unique.  
**Domain:** —  
**Range:** rdf-schema#Literal

### In Classification
**IRI:** `https://iri.suomi.fi/model/ncbv/inClassification`  
**Description:** NACE codes are published in scheme http://publications.europa.eu/resource/authority/ux2/nace2/nace2. Description in text for all NACE codes in all EU languages can be found there.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Interest Control
**IRI:** `https://iri.suomi.fi/model/ncbv/interestControl`  
**Description:** Extent of the control. 25%, 25-50%, 50%, 50-75%, 75%, 100%  
**Domain:** —  
**Range:** rdf-schema#Literal

### Interest Direct Or Indirect
**IRI:** `https://iri.suomi.fi/model/ncbv/interestDirectOrIndirect`  
**Description:** How directly the interest is exercised by the interested party. The value MUST be 'indirect' if intermediate entities or agents are known to exist, and MUST be 'direct' if such intermediaries are known not to exist. Otherwise the value MUST be 'unknown'.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Interest Type
**IRI:** `https://iri.suomi.fi/model/ncbv/interestType`  
**Description:** The type of interest held by a Natural person in an agent. In Sweden this is free text but can have enum like: shareholding, votingRights, appointmentOfBoard, otherInfluenceOrControl, ,seniorManagingOfficial, settlor, trustee, protector, beneficiaryOfLegalArrangement, rightsToSurplusAssetsOnDissolution, rightsToProfitOrIncome, rightsGrantedByContract, conditionalRightsGrantedByContract, controlViaCompanyRulesOrArticles, controlByLegalFramework, boardMember, boardChair, unknownInterest, unpublishedInterest, enjoymentAndUseOfAssets, rightToProfitOrIncomeFromAssets  
**Domain:** —  
**Range:** rdf-schema#Literal

### Legal Name
**IRI:** `https://iri.suomi.fi/model/ncbv/legalName`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Locator Designator
**IRI:** `https://iri.suomi.fi/model/ncbv/locatorDesignator`  
**Description:** A number or a sequence of characters that uniquely identifies the locator within the relevant scope.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Locator Name
**IRI:** `https://iri.suomi.fi/model/ncbv/locatorName`  
**Description:** Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Minimum Number of Members
**IRI:** `https://iri.suomi.fi/model/ncbv/minimumNumberOfMembers`  
**Description:** The number of members required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...  
**Domain:** —  
**Range:** rdf-schema#Literal

### Minimum Number of Role Holders
**IRI:** `https://iri.suomi.fi/model/ncbv/minimumNumberOfRoleHolders`  
**Description:** The number of role holders required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5...  
**Domain:** —  
**Range:** rdf-schema#Literal

### Modified
**IRI:** `https://iri.suomi.fi/model/ncbv/modified`  
**Description:** The date of the last update of something like a Mandate.

upper attribute
http://purl.org/dc/terms/modified


dcterms:modified  
**Domain:** —  
**Range:** rdf-schema#Literal

### Name
**IRI:** `https://iri.suomi.fi/model/ncbv/name`  
**Description:** A word or a combination of characters by which an entity/agent/thing is designated, called, or known.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Notation
**IRI:** `https://iri.suomi.fi/model/ncbv/notation`  
**Description:** A string of characters to uniquely identify a concept.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Number of Shares
**IRI:** `https://iri.suomi.fi/model/ncbv/numberOfShares`  
**Description:** The total number of individual shares associated with the specified share capital value.

This count represents the share units issued, authorized, subscribed, or paid-up, depending on the type of capital being described (capitalType).  
**Domain:** —  
**Range:** rdf-schema#Literal

### Object Type
**IRI:** `https://iri.suomi.fi/model/ncbv/objectType`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Post Code
**IRI:** `https://iri.suomi.fi/model/ncbv/postCode`  
**Description:** The code created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Post Name
**IRI:** `https://iri.suomi.fi/model/ncbv/postName`  
**Description:** A name created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Post Office Box
**IRI:** `https://iri.suomi.fi/model/ncbv/postOfficeBox`  
**Description:** A location designator for a postal delivery point at a post office, usually a number.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Preferred Label
**IRI:** `https://iri.suomi.fi/model/ncbv/prefLabel`  
**Description:** The preferred label attribute is used to name the actual scope of the Mandate; example: "Car Purchase"; "Filing a Declaration (of some type)"; or using a specific national eService (mandates given in the Swedish Mina Ombud or the Finnish Suomi.fi eAuthorizations).    
**Domain:** —  
**Range:** rdf-schema#Literal

### Reference
**IRI:** `https://iri.suomi.fi/model/ncbv/reference`  
**Description:** Reference to the description of the NACE code.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Registration Date
**IRI:** `https://iri.suomi.fi/model/ncbv/registrationDate`  
**Description:** The date when a public authority has registered the legal entity.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Schema Agency
**IRI:** `https://iri.suomi.fi/model/ncbv/schemaAgency`  
**Description:** The name of the agency that issued the identifier.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Scheme Name
**IRI:** `https://iri.suomi.fi/model/ncbv/schemeName`  
**Description:** Name of the scheme used to construct the identifier.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Scheme URI
**IRI:** `https://iri.suomi.fi/model/ncbv/schemeURI`  
**Description:** URI of the scheme used to construct the identifier.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Sequence
**IRI:** `https://iri.suomi.fi/model/ncbv/sequence`  
**Description:** An indicator for the order of a series of values; "1, 2, 3..."  
**Domain:** —  
**Range:** rdf-schema#Literal

### Start Date
**IRI:** `https://iri.suomi.fi/model/ncbv/startDate`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Status
**IRI:** `https://iri.suomi.fi/model/ncbv/status`  
**Description:** A mandate's status can be for instance: active, withdrawn/inactive > Tore checks values 

Upper attribute: adms:status  
**Domain:** —  
**Range:** rdf-schema#Literal

### Thoroughfare
**IRI:** `https://iri.suomi.fi/model/ncbv/thoroughfare`  
**Description:** The name of a passage or way through from one location to another.  
**Domain:** —  
**Range:** rdf-schema#Literal

### Title
**IRI:** `https://iri.suomi.fi/model/ncbv/title`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Unit
**IRI:** `https://iri.suomi.fi/model/ncbv/unit`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal

### Value
**IRI:** `https://iri.suomi.fi/model/ncbv/value`  
**Description:**   
**Domain:** —  
**Range:** rdf-schema#Literal
