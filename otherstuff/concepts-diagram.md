# Legal and Business Concept Model (EU Context)

This diagram illustrates a conceptual hierarchy around persons, legal persons, legal entities, organisations, and economic operators in an EU / Member State context.  
It is expressed using a Mermaid graph so GitHub can render it directly.

```mermaid
graph TD

  %% Core nodes
  Entity["Entity"]
  Agent["Agent"]
  LegalSubject["Legal Subject"]
  Person["Person"]
  Organisation["Organisation"]
  Group["Group"]
  NaturalPerson["Natural Person"]
  LegalPerson["Legal Person"]
  LegalEntity["Legal Entity (organisational)"]
  FormalOrg["Formal Organisation"]
  InformalOrg["Informal Organisation"]
  RegOrg["Registered Organisation"]
  PublicOrg["Public Organisation"]
  PrivateOrg["Private Organisation"]
  Alliance["Alliance"]
  SoleTrader["Sole Trader"]
  SelfEmployed["Self-employed Person"]
  EconOp["Economic Operator"]
  Undertaking["Undertaking"]
  PubAuth["Public Authority"]

  %% Top relations
  Entity --> Agent
  Entity --> LegalSubject

  %% Agent branch
  Agent --> Person
  Agent --> Organisation
  Agent --> Group
  Agent --> EconOp

  %% Legal subject branch
  LegalSubject --> NaturalPerson
  LegalSubject --> LegalPerson

  %% Person / Natural Person specialisations
  Person --> NaturalPerson
  NaturalPerson --> SoleTrader
  NaturalPerson --> SelfEmployed

  %% Legal person / legal entity
  LegalPerson --> LegalEntity
  LegalPerson --> PubAuth

  %% Organisation structure
  Organisation --> FormalOrg
  Organisation --> InformalOrg

  FormalOrg --> RegOrg
  FormalOrg --> PublicOrg
  FormalOrg --> PrivateOrg

  InformalOrg --> Alliance

  %% Legal Entity as organisation with legal personality
  Organisation --> LegalEntity
  LegalEntity --> RegOrg
  LegalEntity --> PublicOrg
  LegalEntity --> PrivateOrg

  %% Economic Operator / Undertaking
  EconOp --> SoleTrader
  EconOp --> SelfEmployed
  EconOp --> RegOrg
  EconOp --> PrivateOrg
  EconOp --> PublicOrg

  EconOp --> Undertaking

  %% Public Authority
  PublicOrg --> PubAuth
