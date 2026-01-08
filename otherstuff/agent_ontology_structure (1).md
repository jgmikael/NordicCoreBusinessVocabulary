# Agent Ontology Structure (with registration-based legal/organisational form)

## Core structure (key additions)

- **Thing**
  - **Entity**
    - **Agent** (Actor): an Entity capable of acting.

### Kind-of-agent axis (kept separate)
- **NaturalPerson** ⊑ Agent  
- **Organisation** ⊑ Agent  
- `NaturalPerson` **disjointWith** `Organisation`

### Organisation refinement
- **FormalOrganisation** ⊑ Organisation  
- **RegisteredOrganisation** ⊑ FormalOrganisation  

### Registration and form classification (new feature)
Registration (especially for organisations) typically includes a **classification of the agent into a legal/organisational form** (e.g., “limited liability company”, “public limited company”, “association”). Comparable forms may also exist for natural persons (e.g., “sole trader / proprietor”).

To represent this cleanly:
- **Registration** is a record/event associated with an Agent (typically a RegisteredOrganisation, but not limited to it).
- **AgentForm** is a classification concept used to type the legal/organisational form of an Agent.
  - **OrganisationalForm** ⊑ AgentForm (forms primarily used for organisations)
  - **NaturalPersonForm** ⊑ AgentForm (forms applicable to natural persons)
    - **SoleTraderForm** ⊑ NaturalPersonForm (example)

Key properties:
- `hasRegistration` : Agent → Registration
- `registeredForm` : Registration → AgentForm  
  (the form as recorded in the registration event/record)
- `hasLegalOrOrganisationalForm` : Agent → AgentForm  
  (a convenience projection; can be inferred from `hasRegistration/registeredForm`)

### Legalistic and economic operator dimensions (kept orthogonal)
- **Role**
  - **LegalEntityStatus** ⊑ Role
  - **EconomicOperatorRole** ⊑ Role
- **LegalEntity** ≡ Agent AND (hasRole SOME LegalEntityStatus)
- **EconomicOperator** ≡ Agent AND (hasRole SOME EconomicOperatorRole)

## Mermaid diagram

```mermaid
classDiagram
direction TB

class Thing
class Entity
class Agent

Thing <|-- Entity
Entity <|-- Agent

%% Kind-of-agent axis
class NaturalPerson
class Organisation
Agent <|-- NaturalPerson
Agent <|-- Organisation
NaturalPerson <|.. Organisation : disjoint

%% Organisation refinement
class FormalOrganisation
class RegisteredOrganisation
Organisation <|-- FormalOrganisation
FormalOrganisation <|-- RegisteredOrganisation

%% Registration + form classification (NEW)
class Registration
class AgentForm
class OrganisationalForm
class NaturalPersonForm
class SoleTraderForm

Agent --> Registration : hasRegistration
Registration --> AgentForm : registeredForm
Agent --> AgentForm : hasLegalOrOrganisationalForm

AgentForm <|-- OrganisationalForm
AgentForm <|-- NaturalPersonForm
NaturalPersonForm <|-- SoleTraderForm

%% Legal person
class LegalPerson
RegisteredOrganisation <|-- LegalPerson

%% Role/status pattern
class Role
class LegalEntityStatus
class EconomicOperatorRole
Role <|-- LegalEntityStatus
Role <|-- EconomicOperatorRole

%% Defined classifications
class LegalEntity
class EconomicOperator

Agent --> Role : hasRole

LegalEntity ..> Agent : equivalentTo
LegalEntity ..> LegalEntityStatus : hasRole some

EconomicOperator ..> Agent : equivalentTo
EconomicOperator ..> EconomicOperatorRole : hasRole some
```
