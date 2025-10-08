# Nordisk — Ontology Documentation

_Generated: 2025-10-08 16:10:49_

## Ontology Overview

| Field | Value |
|---|---|
| **Ontology IRI** | `https://iri.suomi.fi/model/ncbv/` |
| **Version IRI** | `https://iri.suomi.fi/model/ncbv/0.0.5/` |
| **Version** | `0.0.5` |
| **Description** | The common Nordic data vocabulary for business information, initiated by the Nordic Smart Government & Business 4.0 program in 2022-24, further developed and maintained by the Nordic Data Quality and Semantics working group (2025-). |
| **Modified** | `2025-03-25T12:24:35.299000+00:00` |

## Namespaces

| Prefix | Namespace |
|---|---|
| `xml` | `http://www.w3.org/XML/1998/namespace` |
| `rdf` | `http://www.w3.org/1999/02/22-rdf-syntax-ns#` |
| `rdfs` | `http://www.w3.org/2000/01/rdf-schema#` |
| `xsd` | `http://www.w3.org/2001/XMLSchema#` |
| `m8g` | `http://data.europa.eu/m8g/` |
| `ncbv` | `https://iri.suomi.fi/model/ncbv/` |
| `dct` | `http://purl.org/dc/terms/` |
| `busdoc` | `https://iri.suomi.fi/model/busdoc/1.0.1/` |
| `owl` | `http://www.w3.org/2002/07/owl#` |
| `isa2core` | `https://iri.suomi.fi/model/isa2core/1.0.0/` |
| `http` | `http://www.w3.org/2011/http#` |
| `suomi-meta` | `https://iri.suomi.fi/model/suomi-meta/` |
| `skos` | `http://www.w3.org/2004/02/skos/core#` |
| `en16931-1` | `https://iri.suomi.fi/model/en16931-1/` |
| `geo` | `http://www.opengis.net/ont/geosparql#` |
| `sh` | `http://www.w3.org/ns/shacl#` |
| `dcap` | `http://purl.org/ws-mmi-dc/terms/` |
| `foaf` | `http://xmlns.com/foaf/0.1/` |

## Contents

- [Classes](#classes)
- [Object Properties](#object-properties)
- [Datatype Properties](#datatype-properties)

## Classes

**Alphabetical index**: [Address](#address) · [Agent](#agent) · [Amount](#amount) · [Beneficial Owner](#beneficial-owner) · [Beneficial Owner Role](#beneficial-owner-role) · [Code](#code) · [Composite Representation Rule](#composite-representation-rule) · [Contact Point](#contact-point) · [Document](#document) · [Identifier](#identifier) · [Legal Entity](#legal-entity) · [Legal Resource](#legal-resource) · [Legal Status](#legal-status) · [Location](#location) · [Mandate](#mandate) · [Mandate Transfer](#mandate-transfer) · [Membership](#membership) · [Membership Based Representation Rule](#membership-based-representation-rule) · [Object](#object) · [Period of Time](#period-of-time) · [Person](#person) · [Representation Rule (Signatory Rule)](#representation-rule-signatory-rule) · [Restriction](#restriction) · [Restriction Type](#restriction-type) · [Role](#role) · [Role Based Representation Rule](#role-based-representation-rule) · [Rule](#rule) · [Scope](#scope) · [Share Capital](#share-capital) · [Source](#source)
### [Complex Representation Rule] not in use

<a id="complex-representation-rule-not-in-use"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/ComplexRepresentationRule` |
| **Description** | A complex rule needs to be broken down into two or more representation rules.

An example: the complex rule "CEO alone or two board members jointly" is broken down into the representation rule "CEO alone" and the rule "two board members jointly" |
| **SubClass Of** | `owl:Thing` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### [Simple Representation Rule] not in use  

<a id="simple-representation-rule-not-in-use"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/SimpleRepresentationRule` |
| **Description** | A simple representation rule indicates which agent(s) have the power to represent another agent. 

This is accomplished by referring to one or several memberships or roles.

Some examples: 
"Kevin and Jim can sign jointly" is a rule that points at two memberships that are held by persons.   

"CEO and two board members sign jointly" is a rule that points at two roles that can exist without a relationship to any persons holding these roles.
  |
| **SubClass Of** | `owl:Thing` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Address

<a id="address"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Address` |
| **Description** | An identification of the fixed location of a geographic place. |
| **SubClass Of** | `isa2core:Address` |
| **Equivalent To** | `<Nc4aa53df62764fe5bb144e1209a8a36c>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Agent

<a id="agent"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Agent` |
| **SubClass Of** | `isa2core:Agent` |
| **Equivalent To** | `<Ndd14b3e79e9947ad8b051acefd3d55d3>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Amount

<a id="amount"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/MonetaryAmount` |
| **Description** | see unece:Amount and schema:MonetaryAmount |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<Nab68c7a58bdf4289b0a822750b6dd8f0>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Beneficial Owner

<a id="beneficial-owner"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/BeneficialOwner` |
| **Description** | A natural person(s) who ultimately owns or controls the agent. |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N5014b2418f17436db2a10782788c0aa4>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Beneficial Owner Role

<a id="beneficial-owner-role"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/BeneficialOwnerRole` |
| **SubClass Of** | `ncbv:Role` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Code

<a id="code"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Code` |
| **Description** | A generic class for any code values that a specific class can have; in the NCBV the Code class contains code values for legal form, legal status and (economic) activity.   |
| **SubClass Of** | `skos:Concept` |
| **Equivalent To** | `<Nc57bfc07f2464731bed5be33b20c7df3>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Composite Representation Rule

<a id="composite-representation-rule"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/CompositeRepresentationRule` |
| **Description** | A class that replaces the "Complex Representation Rule" in previous NCBV versions; example of a composite rule for general signatory rights (legal representation): "CEO alone and two board members jointly" |
| **SubClass Of** | `ncbv:RepresentationRule` |
| **Equivalent To** | `<N2d2f49aabaf249d58778b5ff10e28fa9>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Contact Point

<a id="contact-point"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/ContactPoint` |
| **Description** | Information (e.g. e-mail address, telephone number) of a person or department through which the user can get in touch with.  |
| **SubClass Of** | `m8g:ContactPoint` |
| **Equivalent To** | `<N5884864e46cf46edba1b042f06ca9f1d>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Document

<a id="document"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Document` |
| **SubClass Of** | `ncbv:Source`, `foaf:Document` |
| **Equivalent To** | `<Nb0f2173d9c39440596a3b48dddd53eac>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Identifier

<a id="identifier"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Identifier` |
| **Description** | A unique set of characters used to identify the legal entity.  |
| **SubClass Of** | `isa2core:Identifier` |
| **Equivalent To** | `<N372bf452246240598b4a3970a284828f>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Entity

<a id="legal-entity"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/LegalEntity` |
| **SubClass Of** | `isa2core:LegalEntity`, `ncbv:Agent` |
| **Equivalent To** | `<N382768fcd1244427ac44d6b5edc9a017>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Resource

<a id="legal-resource"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/LegalResource` |
| **SubClass Of** | `ncbv:Source` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Status

<a id="legal-status"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/LegalStatus` |
| **Description** | An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity. |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<Nd3fc9823dff8475493303b913a84ab61>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Location

<a id="location"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Location` |
| **SubClass Of** | `isa2core:Location` |
| **Equivalent To** | `<N06795e8b191445a9beee2cc26fc2b3c8>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Mandate

<a id="mandate"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Mandate` |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N62d574268ee4487c828bd7258d815af4>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Mandate Transfer

<a id="mandate-transfer"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/MandateTransfer` |
| **Description** | A class for documenting the possible transfer (or delegation) of a Mandate from a previous Mandatee to another; example: Mandate is granted by CEO of Company, is delegable, the first Mandatee delegated the Mandate to another Agent who becomes the new Mandatee; the transfer of the Mandate is logged in this class. |
| **SubClass Of** | `ncbv:Source` |
| **Equivalent To** | `<N74077e46f4974648812399ca148fa246>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Membership

<a id="membership"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Membership` |
| **Description** | The Membership class describes certain types of relationships between agents (persons and legal entities). 

A person can be a member of an association, employed by a company, be a board member in or the CEO of a limited company.

The official definition of Membership can be found here: 
https://www.w3.org/TR/vocab-org/#org:Membership

This technical note does not change the content of the official definition of the Membership class.

Upper class: 
https://www.w3.org/ns/org#Membership |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N352f8ea25a24486c9dd2e88eae363cde>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Membership Based Representation Rule

<a id="membership-based-representation-rule"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/MembershipBasedRepresentationRule` |
| **Description** | A class that replaces the previous "Simple Representation Rule" class (partially); example: a mandate granted to "a man on the street", pointing at a certain person as a  Member of the Mandator (Membership in this case could be "mandatee" or similar). |
| **SubClass Of** | `ncbv:RepresentationRule` |
| **Equivalent To** | `<N6b9b8a2f7e16488ab78fe3ff5f087cc7>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Object

<a id="object"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Object` |
| **Description** | Example: can be a specific house, car; has an Identifier (car registration number) |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N360d867e6e4f487ea4cc7d9510896b6e>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Period of Time

<a id="period-of-time"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/PeriodOfTime` |
| **SubClass Of** | `dct:PeriodOfTime` |
| **Equivalent To** | `<N1901231132bc4815a084e9774a76bc6c>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Person

<a id="person"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Person` |
| **Description** | A individual human being who may be dead or alive, but not imaginary. |
| **SubClass Of** | `ncbv:Agent`, `isa2core:Person`, `foaf:Person` |
| **Equivalent To** | `<N567d59137e7e4fd282514d08ebe88391>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Representation Rule (Signatory Rule)

<a id="representation-rule-signatory-rule"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/RepresentationRule` |
| **Description** | A rule that describes who or which agents a mandate is granted to. 

The rule can be used both in the case of legal representation, when a CEO or a board member signs for the agent (company) based on their official role in the company, as well as when a mandate is given to a specific person ("a man on the street") who has no previous affiliation to the mandating agent. |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<Nef3e7ede9f894312a352a368b8cff889>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Restriction

<a id="restriction"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Restriction` |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N71e335a2031b49ec8d9b0b162bab5ed3>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Restriction Type

<a id="restriction-type"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/RestrictionType` |
| **Description** | A class for describing what the value in the Restriction class means; example: Restriction.value: 10000; RestrictionType: Datatype: Decimal or Integer; Unit: SEK, NOK, EUR... Name: Monetary Amount restriction; Description: "The maximum monetary amount to be used with the Mandate (like: "purchasing a car")   |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<Nc7bbed84028a45e9a530d29ed866cd97>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Role

<a id="role"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Role` |
| **Description** | In the context of Mandates, the Role class 
indicates the Role that the Agent plays in a Membership relationship with a legal entity. 

Upper class: https://www.w3.org/TR/vocab-org/#class-role

Suggested code list for Nordic use cases: http://uri.suomi.fi/codelist/verotus/membershiproletypes |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N125e32f5d40c4e55aa06b336e765f60e>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Role Based Representation Rule

<a id="role-based-representation-rule"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/RoleBasedRepresentationRule` |
| **Description** | A class that replaces (partially) the Simple Representation Rule in previous versions; example: signatory rights rule "CEO alone" |
| **SubClass Of** | `ncbv:RepresentationRule` |
| **Equivalent To** | `<Nd7d2d04ef3794dd28b3dc25fe05fbc90>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Rule

<a id="rule"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Rule` |
| **Description** | eli:Rule |
| **SubClass Of** | `ncbv:Source` |
| **Equivalent To** | `<Nab7853b07df844bf880ad147cb479f1d>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Scope

<a id="scope"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Scope` |
| **Description** | A class to define what powers the Mandator grants to the Mandatee through the Mandate.

Example: A gives signatory power to B. A grants B the power to buy a car for the company.  |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N58655f9441fd443e8a9fe5172668db4b>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Share Capital

<a id="share-capital"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/ShareCapital` |
| **Description** | Share capital refers to the total amount of capital raised by a legal entity through the issuance of shares to shareholders. |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<N36bc20bb4a754934b50bea92ec9160ae>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Source

<a id="source"></a>

| Field | Value |
|---|---|
| **Type** | Class |
| **IRI** | `https://iri.suomi.fi/model/ncbv/Source` |
| **Description** | A class to describe what the powers that are delegated by the Mandator are originally based on;  example: "law", "statutes of company"; "another mandate" etc. |
| **SubClass Of** | `owl:Thing` |
| **Equivalent To** | `<Nb61adab0d69a4cda92002c0a9ca89b2d>` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |
## Object Properties

**Alphabetical index**: [(Has) Geographical Scope/ Has Location / (Has) Geographical Coverage](#has-geographical-scope-has-location--has-geographical-coverage) · [(Has) Mandator](#has-mandator) · [Activity](#activity) · [All of](#all-of) · [Alone](#alone) · [And](#and) · [Applies to Object](#applies-to-object) · [Beneficial Owners](#beneficial-owners) · [Consists of Representation Rule](#consists-of-representation-rule) · [Contact Point](#contact-point) · [Defines Valid Membership](#defines-valid-membership) · [Defines Valid Role ](#defines-valid-role) · [Five of](#five-of) · [Four of](#four-of) · [Grants Mandate](#grants-mandate) · [Grants Representation Right](#grants-representation-right) · [Has Code](#has-code) · [Has Duration](#has-duration) · [Has Member](#has-member) · [Has Representation Rule](#has-representation-rule) · [Has Restriction](#has-restriction) · [Has Scope](#has-scope) · [Has Source](#has-source) · [Held by Legal Entity](#held-by-legal-entity) · [Held by Person](#held-by-person) · [Identifier](#identifier) · [Implements](#implements) · [Is a Person](#is-a-person) · [Jointly](#jointly) · [Legal Form](#legal-form) · [Legal Identifier](#legal-identifier) · [Legal Status](#legal-status) · [Majority of](#majority-of) · [Mandatee](#mandatee) · [Member](#member) · [Member Quantifier](#member-quantifier) · [One of](#one-of) · [Or](#or) · [Original Mandate](#original-mandate) · [Postal Address](#postal-address) · [Power](#power) · [Registered Address](#registered-address) · [Role](#role) · [Role Holder Quantifier](#role-holder-quantifier) · [Share Capital](#share-capital) · [Subject](#subject) · [Three of](#three-of) · [Total Capital Amount](#total-capital-amount) · [Transfer of Mandate](#transfer-of-mandate) · [Two of](#two-of) · [Type](#type)

### (Has) Geographical Scope/ Has Location / (Has) Geographical Coverage

<a id="has-geographical-scope-has-location--has-geographical-coverage"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasGeographicalScope` |
| **Description** | The association geographical scope points at a location; this describes the geographic region the mandate is valid.   |
| **SubProperty Of** | `dct:spatial` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### (Has) Mandator

<a id="has-mandator"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasMandator` |
| **Description** | The Mandator association points always to the "primary mandator", who is the original source of the delegated power. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Activity

<a id="activity"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasActivity` |
| **Description** | An active deed or action carried out by a legal entity |
| **SubProperty Of** | `isa2core:companyActivity` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### All of

<a id="all-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/allOf` |
| **Description** | Constraint property that requires all of the agents holding a post to sign. |
| **SubProperty Of** | `ncbv:jointly` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Alone

<a id="alone"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/alone` |
| **Description** | Requires holder of the post to sign alone. |
| **Range** | `ncbv:Membership` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### And

<a id="and"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/and` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Applies to Object

<a id="applies-to-object"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/appliesToObject` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Beneficial Owners

<a id="beneficial-owners"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/beneficialOwners` |
| **Description** | A natural person(s) who ultimately owns or controls the agent. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Consists of Representation Rule

<a id="consists-of-representation-rule"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/consistsOfRepresentationRule` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Contact Point

<a id="contact-point"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasContactPoint` |
| **Description** | The main contact information of the resource. |
| **SubProperty Of** | `isa2core:contactPoint_`, `m8g:contactPoint` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Defines Valid Membership

<a id="defines-valid-membership"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/definesValidMembership` |
| **Description** | The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Defines Valid Role 

<a id="defines-valid-role"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/definesValidRole` |
| **Description** | The Simple Representation Rule class cannot at the same time be defined by a Valid Membership and Valid Role, it's either or. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Five of

<a id="five-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/fiveOf` |
| **Description** | Requires five of the defined agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Four of

<a id="four-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/fourOf` |
| **Description** | Requires four of the defined agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Grants Mandate

<a id="grants-mandate"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/grantsMandate` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Grants Representation Right

<a id="grants-representation-right"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/grantsRepresentationRight` |
| **Description** | The signatory rights that is registered for the legal entity. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Code

<a id="has-code"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasCode` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Duration

<a id="has-duration"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasDuration` |
| **Description** | The association "has duration" points to "Period of Time"and indicates the validity period of the mandate; like "1.1.2025-31.12.2025" |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Member

<a id="has-member"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasMember` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Representation Rule

<a id="has-representation-rule"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasRepresentationRule` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Restriction

<a id="has-restriction"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasRestriction` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Scope

<a id="has-scope"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasScope` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Source

<a id="has-source"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasSource` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Held by Legal Entity

<a id="held-by-legal-entity"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/heldByLegalEntity` |
| **Description** | Indicates the legal entity that is holding the post. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Held by Person

<a id="held-by-person"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/heldByPerson` |
| **Description** | Indicates the person that holds the post.
 |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Identifier

<a id="identifier"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasIdentifier` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Implements

<a id="implements"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/implements` |
| **SubProperty Of** | `isa2core:implements` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Is a Person

<a id="is-a-person"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/isPerson` |
| **Range** | `ncbv:Person` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Jointly

<a id="jointly"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/jointly` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Form

<a id="legal-form"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasLegalForm` |
| **Description** | The legal form of a legal entity. |
| **Range** | `ncbv:Code` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Identifier

<a id="legal-identifier"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/legalIdentifier` |
| **Description** | An identifier that is given to a legal entity at registration. |
| **SubProperty Of** | `isa2core:legalidentifier` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Status

<a id="legal-status"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasLegalStatus` |
| **Description** | An indication of whether a registration authority has registered some extraordinary proceedings for the legal entity. |
| **SubProperty Of** | `isa2core:companyStatus` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Majority of

<a id="majority-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/majorityOf` |
| **Description** | Constraint property that requires majority of agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Mandatee

<a id="mandatee"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/mandatee` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Member

<a id="member"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/member` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Member Quantifier

<a id="member-quantifier"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/memberQuantifier` |
| **Description** | Specifies a qualitative quantity or proportion of members required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”). |
| **Range** | `skos:Concept` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### One of

<a id="one-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/oneOf` |
| **Description** | Requires one of the defined agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Or

<a id="or"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/or` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Original Mandate

<a id="original-mandate"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/originalMandate` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Postal Address

<a id="postal-address"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/postalAddress` |
| **Description** | The address to which mail can be sent to the legal entity. |
| **SubProperty Of** | `isa2core:address_` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Power

<a id="power"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/power` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Registered Address

<a id="registered-address"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/registeredAddress` |
| **Description** | The address to which formal communications can be sent to the legal entity. |
| **SubProperty Of** | `isa2core:registeredAddress` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Role

<a id="role"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasRole` |
| **Description** | Indicates the Role that the Agent plays in a Membership relationship with a legal entity. |
| **SubProperty Of** | `m8g:role` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Role Holder Quantifier

<a id="role-holder-quantifier"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/roleHolderQuantifier` |
| **Description** | Specifies a qualitative quantity or proportion of role holders required for the rule, used when the number cannot be expressed as a specific numeric value (e.g., “all”, “half”, “majority”). |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Share Capital

<a id="share-capital"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasShareCapital` |
| **Description** | The total registered share capital for the legal entity. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Subject

<a id="subject"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/subject` |
| **SubProperty Of** | `sh:subject` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Three of

<a id="three-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/threeOf` |
| **Description** | Requires two of the defined agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Total Capital Amount

<a id="total-capital-amount"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/totalCapitalAmount` |
| **Description** | The total capital amount of the Legal Entity's (company's) share capital, expressed in monetary values. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Transfer of Mandate

<a id="transfer-of-mandate"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/transferOfMandate` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Two of

<a id="two-of"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/twoOf` |
| **Description** | Requires two of the defined agents holding a post to sign. |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Type

<a id="type"></a>

| Field | Value |
|---|---|
| **Type** | Object Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/type` |
| **SubProperty Of** | `owl:topObjectProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

## Datatype Properties

**Alphabetical index**: [Admin Unit Level 1](#admin-unit-level-1) · [Admin Unit Level 2](#admin-unit-level-2) · [Alternative Name](#alternative-name) · [Amount](#amount) · [Capital Type](#capital-type) · [Care of](#care-of) · [Code](#code) · [Code Identifier](#code-identifier) · [Code name](#code-name) · [Contact Page](#contact-page) · [Currency](#currency) · [Datatype](#datatype) · [Date](#date) · [Date Of Birth](#date-of-birth) · [Date of Issue](#date-of-issue) · [Delegable](#delegable) · [Description](#description) · [End Date](#end-date) · [Full Address](#full-address) · [Full Name](#full-name) · [Geographic Identifier](#geographic-identifier) · [Geographic Name](#geographic-name) · [Has Email](#has-email) · [Has Telephone](#has-telephone) · [Identifier](#identifier) · [In Classification](#in-classification) · [Interest Control](#interest-control) · [Interest Direct Or Indirect](#interest-direct-or-indirect) · [Interest Type](#interest-type) · [Legal Name](#legal-name) · [Locator Designator](#locator-designator) · [Locator Name](#locator-name) · [Minimum Number of Members](#minimum-number-of-members) · [Minimum Number of Role Holders](#minimum-number-of-role-holders) · [Modified](#modified) · [Name](#name) · [Notation](#notation) · [Number of Shares](#number-of-shares) · [Object Type](#object-type) · [Post Code](#post-code) · [Post Name](#post-name) · [Post Office Box](#post-office-box) · [Preferred Label](#preferred-label) · [Reference](#reference) · [Registration Date](#registration-date) · [Schema Agency](#schema-agency) · [Scheme Name](#scheme-name) · [Scheme URI](#scheme-uri) · [Sequence](#sequence) · [Start Date](#start-date) · [Status](#status) · [Thoroughfare](#thoroughfare) · [Title](#title) · [Unit](#unit) · [Value](#value)

### Admin Unit Level 1

<a id="admin-unit-level-1"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/adminUnitLevel1` |
| **Description** | The uppermost administrative unit for the address, almost always a country. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:adminUnitLevel1` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Admin Unit Level 2

<a id="admin-unit-level-2"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/adminUnitLevel2` |
| **Description** | The name of a secondary level/region of the address, usually a county, state or other such area that typically encompasses several localities. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:adminUnitLevel2` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Alternative Name

<a id="alternative-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/alternativeName` |
| **Description** | Any other registered name by which a legal entity is known. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Amount

<a id="amount"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/amount` |
| **Description** | The amount of money. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Capital Type

<a id="capital-type"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/capitalType` |
| **Description** | Values expressed in a separate code list, could contain the following: 

Capital Type	Description
Authorized Share Capital	Maximum capital a company is legally allowed to issue, as stated in its statutes

Issued Share Capital	Capital corresponding to the total number of shares that have actually been issued

Subscribed Share Capital	Part of issued capital that investors have agreed to purchase

Paid-up Share Capital	Subscribed capital for which the company has received payment

Called-up Share Capital	Subscribed capital where payment has been requested (called), but not necessarily received

Unpaid Capital	Portion of called-up capital still owed by shareholders

Nominal / Par Value	The base value assigned to each share; may also be relevant at share type level

Equity vs Debt hybrid	Some instruments may qualify as equity under certain laws but be treated as debt elsewhere |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Care of

<a id="care-of"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/careOf` |
| **Description** | Used when an address is at the address of another person or legal entity.
 |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Code

<a id="code"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/codeValue` |
| **Description** | The actual code value from a selected code list. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `skos:notation` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Code Identifier

<a id="code-identifier"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/codeIdentifier` |
| **Description** | An identifier for the code, can be of any format like an URI or just alphanumeric. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `dct:identifier` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Code name

<a id="code-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/codeName` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `skos:prefLabel` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Contact Page

<a id="contact-page"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/contactPage` |
| **Description** | A web page that could be used to reach out the Contact Point. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Currency

<a id="currency"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/currency` |
| **Description** | The currency in which the monetary amount is expressed. ISO 4217 currency format, e.g. "EUR". |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Datatype

<a id="datatype"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/datatype` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Date

<a id="date"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/date` |
| **Description** | The date when the legal status was registered. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Date Of Birth

<a id="date-of-birth"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/dateOfBirth` |
| **Description** | The point in time on which the Person was born. Persons can be registered with a membership in a legal entity whithout a identifier being a national registration number. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `m8g:birthDate` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Date of Issue

<a id="date-of-issue"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/dateOfIssue` |
| **Description** | The date on which the something was issued; in this context for instance a Mandate or an Identifier. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:dateOfIssue` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Delegable

<a id="delegable"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/delegable` |
| **Description** | An indicator of whether the Mandate can be delegated or not. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Description

<a id="description"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/description` |
| **Description** | An attribute used to describe a Class.

Examples:
Class: Representation Rule; description: "CEO can sign alone" or "two board members can sign jointly"; 

Class: Mandate Type; description: "a person is entitled to file a tax declaration on behalf of the company (Mandator)" 

http://purl.org/dc/terms/description
 |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:description` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### End Date

<a id="end-date"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/endDate` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Full Address

<a id="full-address"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/fullAddress` |
| **Description** | The complete address written as a string. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:fullAddress` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Full Name

<a id="full-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/fullName` |
| **Description** | The complete name of the Person as one string. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `foaf:name` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Geographic Identifier

<a id="geographic-identifier"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/geographicIdentifier` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:geographicIdentifier` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Geographic Name

<a id="geographic-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/geographicName` |
| **Description** | A recognizable name for a place, like "Eiffel Tower" or "Madrid".  |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:geographicName` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Email

<a id="has-email"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/email` |
| **Description** | An electronic address through which the Contact Point can be contacted.

Equivalent with schema:email |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `m8g:email` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Has Telephone

<a id="has-telephone"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/hasTelephone` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `m8g:telephone` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Identifier

<a id="identifier"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/identifierValue` |
| **Description** | The identifier of a mandate is used to separate different mandates from each other, making it unique. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `dct:identifier` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### In Classification

<a id="in-classification"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/inClassification` |
| **Description** | NACE codes are published in scheme http://publications.europa.eu/resource/authority/ux2/nace2/nace2. Description in text for all NACE codes in all EU languages can be found there. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Interest Control

<a id="interest-control"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/interestControl` |
| **Description** | Extent of the control. 25%, 25-50%, 50%, 50-75%, 75%, 100% |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Interest Direct Or Indirect

<a id="interest-direct-or-indirect"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/interestDirectOrIndirect` |
| **Description** | How directly the interest is exercised by the interested party. The value MUST be 'indirect' if intermediate entities or agents are known to exist, and MUST be 'direct' if such intermediaries are known not to exist. Otherwise the value MUST be 'unknown'. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Interest Type

<a id="interest-type"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/interestType` |
| **Description** | The type of interest held by a Natural person in an agent. In Sweden this is free text but can have enum like: shareholding, votingRights, appointmentOfBoard, otherInfluenceOrControl, ,seniorManagingOfficial, settlor, trustee, protector, beneficiaryOfLegalArrangement, rightsToSurplusAssetsOnDissolution, rightsToProfitOrIncome, rightsGrantedByContract, conditionalRightsGrantedByContract, controlViaCompanyRulesOrArticles, controlByLegalFramework, boardMember, boardChair, unknownInterest, unpublishedInterest, enjoymentAndUseOfAssets, rightToProfitOrIncomeFromAssets |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Legal Name

<a id="legal-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/legalName` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:legalName` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Locator Designator

<a id="locator-designator"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/locatorDesignator` |
| **Description** | A number or a sequence of characters that uniquely identifies the locator within the relevant scope. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:locatorDesignator` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Locator Name

<a id="locator-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/locatorName` |
| **Description** | Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:locatorName` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Minimum Number of Members

<a id="minimum-number-of-members"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/minimumNumberOfMembers` |
| **Description** | The number of members required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5... |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Minimum Number of Role Holders

<a id="minimum-number-of-role-holders"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/minimumNumberOfRoleHolders` |
| **Description** | The number of role holders required for the Representation Rule to be valid; examples are 1, 2, 3, 4, 5... |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Modified

<a id="modified"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/modified` |
| **Description** | The date of the last update of something like a Mandate.

upper attribute
http://purl.org/dc/terms/modified


dcterms:modified |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Name

<a id="name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/name` |
| **Description** | A word or a combination of characters by which an entity/agent/thing is designated, called, or known. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `foaf:name`, `skos:prefLabel` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Notation

<a id="notation"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/notation` |
| **Description** | A string of characters to uniquely identify a concept. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `skos:notation` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Number of Shares

<a id="number-of-shares"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/numberOfShares` |
| **Description** | The total number of individual shares associated with the specified share capital value.

This count represents the share units issued, authorized, subscribed, or paid-up, depending on the type of capital being described (capitalType). |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Object Type

<a id="object-type"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/objectType` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Post Code

<a id="post-code"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/postCode` |
| **Description** | The code created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Post Name

<a id="post-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/postName` |
| **Description** | A name created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Post Office Box

<a id="post-office-box"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/postOfficeBox` |
| **Description** | A location designator for a postal delivery point at a post office, usually a number. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:poBox` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Preferred Label

<a id="preferred-label"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/prefLabel` |
| **Description** | The preferred label attribute is used to name the actual scope of the Mandate; example: "Car Purchase"; "Filing a Declaration (of some type)"; or using a specific national eService (mandates given in the Swedish Mina Ombud or the Finnish Suomi.fi eAuthorizations).   |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `skos:prefLabel` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Reference

<a id="reference"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/reference` |
| **Description** | Reference to the description of the NACE code. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Registration Date

<a id="registration-date"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/registrationDate` |
| **Description** | The date when a public authority has registered the legal entity. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `m8g:registrationDate` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Schema Agency

<a id="schema-agency"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/schemaAgency` |
| **Description** | The name of the agency that issued the identifier. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:issuingAuthorityName` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Scheme Name

<a id="scheme-name"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/schemeName` |
| **Description** | Name of the scheme used to construct the identifier. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:schemeName` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Scheme URI

<a id="scheme-uri"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/schemeURI` |
| **Description** | URI of the scheme used to construct the identifier. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Sequence

<a id="sequence"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/sequence` |
| **Description** | An indicator for the order of a series of values; "1, 2, 3..." |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Start Date

<a id="start-date"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/startDate` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Status

<a id="status"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/status` |
| **Description** | A mandate's status can be for instance: active, withdrawn/inactive > Tore checks values 

Upper attribute: adms:status |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Thoroughfare

<a id="thoroughfare"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/thoroughfare` |
| **Description** | The name of a passage or way through from one location to another. |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:thoroughfare` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Title

<a id="title"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/title` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `foaf:title` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Unit

<a id="unit"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/unit` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `owl:topDataProperty` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |

### Value

<a id="value"></a>

| Field | Value |
|---|---|
| **Type** | Datatype Property |
| **IRI** | `https://iri.suomi.fi/model/ncbv/value` |
| **Range** | `rdfs:Literal` |
| **SubProperty Of** | `isa2core:value` |
| **isDefinedBy** | `<https://iri.suomi.fi/model/ncbv/>` |
