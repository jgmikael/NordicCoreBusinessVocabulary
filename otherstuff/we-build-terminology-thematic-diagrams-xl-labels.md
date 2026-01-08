# WE BUILD Terminology (SKOS) — Thematic Concept Diagrams

Source: `WE BUILD Terminology.ttl`

Node labels are taken from the Turtle file via **`skos:prefLabel` pointing to a SKOS-XL label resource**, using **`skos-xl:literalForm` (English where available)**.

## Thematic split (heuristic)
The diagrams are grouped into the following themes (keyword-based, for navigation).

## Contents
- [Governance](#governance)
- [Data spaces](#data-spaces)
- [Trust and assurance](#trust-and-assurance)
- [Wallets and digital identity](#wallets-and-digital-identity)
- [Interoperability and architecture](#interoperability-and-architecture)
- [Other / cross-cutting](#other-cross-cutting)
- [Cross-cutting links](#cross-cutting-links)

## Governance

- Concepts included: **29**

```mermaid
flowchart LR
  N001["activity"]
  N002["address"]
  N003["agent"]
  N004["auditor"]
  N005["board member"]
  N006["chairman of the board"]
  N007["company"]
  N008["company status"]
  N009["composite representation rule"]
  N010["deputy board member"]
  N011["deputy managing director"]
  N012["formal organisation"]
  N013["identifier"]
  N014["legal entity"]
  N015["legal resource"]
  N016["legal status"]
  N017["mandate"]
  N018["membership"]
  N019["membership based representation rule"]
  N020["postal address"]
  N021["registered address"]
  N022["registered organisation"]
  N023["registration"]
  N024["registration date"]
  N025["representation right"]
  N026["representation rule"]
  N027["role"]
  N028["role based representation rule"]
  N029["source"]
  N001 --> N023
  N002 --> N020
  N002 --> N021
  N005 --> N006
  N012 --> N014
  N012 --> N022
  N026 --> N009
  N026 --> N019
  N026 --> N028
  N027 --> N004
  N027 --> N005
  N001 -.-> N014
  N014 -.-> N001
  N003 -.-> N018
  N018 -.-> N003
  N003 -.-> N027
  N027 -.-> N003
  N004 -.-> N014
  N014 -.-> N004
  N004 -.-> N015
  N015 -.-> N004
  N005 -.-> N010
  N010 -.-> N005
  N005 -.-> N014
  N014 -.-> N005
  N005 -.-> N018
  N018 -.-> N005
  N005 -.-> N025
  N025 -.-> N005
  N006 -.-> N014
  N014 -.-> N006
  N006 -.-> N017
  N017 -.-> N006
  N006 -.-> N025
  N025 -.-> N006
  N007 -.-> N005
  N005 -.-> N007
  N007 -.-> N014
  N014 -.-> N007
  N007 -.-> N024
  N024 -.-> N007
  N009 -.-> N019
  N019 -.-> N009
  N009 -.-> N028
  N028 -.-> N009
  N016 -.-> N003
  N003 -.-> N016
  N016 -.-> N008
  N008 -.-> N016
  N018 -.-> N019
  N019 -.-> N018
  N021 -.-> N020
  N020 -.-> N021
  N022 -.-> N014
  N014 -.-> N022
  N023 -.-> N013
  N013 -.-> N023
  N023 -.-> N014
  N014 -.-> N023
  N023 -.-> N015
  N015 -.-> N023
  N023 -.-> N029
  N029 -.-> N023
  N024 -.-> N003
  N003 -.-> N024
  N027 -.-> N018
  N018 -.-> N027
  N027 -.-> N028
  N028 -.-> N027
  N028 -.-> N019
  N019 -.-> N028
```

## Data spaces

- Concepts included: **11**

```mermaid
flowchart LR
  N001["document"]
  N002["electronic attestation of attributes"]
  N003["European Business Wallet"]
  N004["European Business Wallet owner"]
  N005["European Business Wallet owner identification data"]
  N006["identifier"]
  N007["legal identifier"]
  N008["qualified attestation of attributes"]
  N009["registration"]
  N010["schema agency"]
  N011["wallet unit attestation"]
  N001 --> N002
  N001 --> N005
  N001 --> N011
  N002 --> N008
  N006 --> N007
  N003 -.-> N001
  N001 -.-> N003
  N003 -.-> N004
  N004 -.-> N003
  N005 -.-> N002
  N002 -.-> N005
  N005 -.-> N004
  N004 -.-> N005
  N005 -.-> N006
  N006 -.-> N005
  N005 -.-> N007
  N007 -.-> N005
  N005 -.-> N008
  N008 -.-> N005
  N009 -.-> N006
  N006 -.-> N009
```

## Trust and assurance

- Concepts included: **13**

```mermaid
flowchart LR
  N001["auditor"]
  N002["document"]
  N003["electronic attestation of attributes"]
  N004["European Business Wallet owner identification data"]
  N005["European Business Wallet solution"]
  N006["European Business Wallet unit"]
  N007["legal entity"]
  N008["legal resource"]
  N009["mandate"]
  N010["qualified attestation of attributes"]
  N011["representation rule"]
  N012["role"]
  N013["wallet unit attestation"]
  N002 --> N003
  N002 --> N004
  N002 --> N013
  N003 --> N010
  N005 --> N006
  N012 --> N001
  N001 -.-> N007
  N007 -.-> N001
  N001 -.-> N008
  N008 -.-> N001
  N003 -.-> N009
  N009 -.-> N003
  N003 -.-> N011
  N011 -.-> N003
  N004 -.-> N003
  N003 -.-> N004
  N004 -.-> N010
  N010 -.-> N004
  N013 -.-> N005
  N005 -.-> N013
  N013 -.-> N006
  N006 -.-> N013
```

## Wallets and digital identity

- Concepts included: **49**

```mermaid
flowchart LR
  N001["activity"]
  N002["agent"]
  N003["alternative name"]
  N004["auditor"]
  N005["beneficial owner"]
  N006["board member"]
  N007["chairman of the board"]
  N008["company"]
  N009["contact point"]
  N010["date of birth"]
  N011["document"]
  N012["duration of the legal entity"]
  N013["economic operator"]
  N014["electronic attestation of attributes"]
  N015["entity"]
  N016["European Business Wallet"]
  N017["European Business Wallet owner"]
  N018["European Business Wallet owner identification data"]
  N019["European Business Wallet relying party"]
  N020["European Business Wallet solution"]
  N021["European Business Wallet unit"]
  N022["formal organisation"]
  N023["identifier"]
  N024["legal entity"]
  N025["legal form"]
  N026["legal identifier"]
  N027["legal name"]
  N028["legal person"]
  N029["legal status"]
  N030["mandate"]
  N031["mandatee"]
  N032["mandator"]
  N033["membership"]
  N034["natural person"]
  N035["organisation"]
  N036["post"]
  N037["public sector body"]
  N038["qualified attestation of attributes"]
  N039["registered organisation"]
  N040["registration"]
  N041["registration date"]
  N042["representation right"]
  N043["representation rule"]
  N044["role"]
  N045["share"]
  N046["share capital"]
  N047["shareholder"]
  N048["signatory"]
  N049["wallet unit attestation"]
  N001 --> N040
  N002 --> N017
  N002 --> N019
  N002 --> N031
  N002 --> N032
  N002 --> N034
  N002 --> N035
  N006 --> N007
  N011 --> N014
  N011 --> N018
  N011 --> N049
  N014 --> N038
  N015 --> N002
  N016 --> N020
  N020 --> N021
  N022 --> N024
  N022 --> N039
  N023 --> N026
  N024 --> N013
  N024 --> N037
  N034 --> N005
  N035 --> N022
  N044 --> N004
  N044 --> N006
  N001 -.-> N024
  N024 -.-> N001
  N002 -.-> N033
  N033 -.-> N002
  N002 -.-> N044
  N044 -.-> N002
  N003 -.-> N024
  N024 -.-> N003
  N004 -.-> N024
  N024 -.-> N004
  N005 -.-> N002
  N002 -.-> N005
  N006 -.-> N024
  N024 -.-> N006
  N006 -.-> N033
  N033 -.-> N006
  N006 -.-> N042
  N042 -.-> N006
  N007 -.-> N024
  N024 -.-> N007
  N007 -.-> N030
  N030 -.-> N007
  N007 -.-> N042
  N042 -.-> N007
  N008 -.-> N006
  N006 -.-> N008
  N008 -.-> N013
  N013 -.-> N008
  N008 -.-> N024
  N024 -.-> N008
  N008 -.-> N041
  N041 -.-> N008
  N013 -.-> N017
  N017 -.-> N013
  N014 -.-> N030
  N030 -.-> N014
  N014 -.-> N043
  N043 -.-> N014
  N016 -.-> N011
  N011 -.-> N016
  N016 -.-> N017
  N017 -.-> N016
  N016 -.-> N019
  N019 -.-> N016
  N016 -.-> N021
  N021 -.-> N016
  N016 -.-> N030
  N030 -.-> N016
  N016 -.-> N043
  N043 -.-> N016
  N017 -.-> N019
  N019 -.-> N017
  N018 -.-> N014
  N014 -.-> N018
  N018 -.-> N017
  N017 -.-> N018
  N018 -.-> N023
  N023 -.-> N018
  N018 -.-> N026
  N026 -.-> N018
  N018 -.-> N038
  N038 -.-> N018
  N024 -.-> N009
  N009 -.-> N024
  N024 -.-> N036
  N036 -.-> N024
  N024 -.-> N046
  N046 -.-> N024
  N025 -.-> N002
  N002 -.-> N025
  N027 -.-> N024
  N024 -.-> N027
  N029 -.-> N002
  N002 -.-> N029
  N030 -.-> N017
  N017 -.-> N030
  N030 -.-> N019
  N019 -.-> N030
  N030 -.-> N031
  N031 -.-> N030
  N030 -.-> N032
  N032 -.-> N030
  N032 -.-> N031
  N031 -.-> N032
  N034 -.-> N009
  N009 -.-> N034
  N034 -.-> N010
  N010 -.-> N034
  N037 -.-> N017
  N017 -.-> N037
  N039 -.-> N024
  N024 -.-> N039
  N040 -.-> N023
  N023 -.-> N040
  N040 -.-> N024
  N024 -.-> N040
  N041 -.-> N002
  N002 -.-> N041
  N042 -.-> N017
  N017 -.-> N042
  N043 -.-> N019
  N019 -.-> N043
  N044 -.-> N033
  N033 -.-> N044
  N045 -.-> N024
  N024 -.-> N045
  N045 -.-> N046
  N046 -.-> N045
  N047 -.-> N002
  N002 -.-> N047
  N047 -.-> N045
  N045 -.-> N047
  N047 -.-> N046
  N046 -.-> N047
  N048 -.-> N002
  N002 -.-> N048
  N049 -.-> N020
  N020 -.-> N049
  N049 -.-> N021
  N021 -.-> N049
```

## Interoperability and architecture

- Concepts included: **4**

```mermaid
flowchart LR
  N001["legal entity"]
  N002["share"]
  N003["share capital"]
  N004["shareholder"]
  N001 -.-> N003
  N003 -.-> N001
  N002 -.-> N001
  N001 -.-> N002
  N002 -.-> N003
  N003 -.-> N002
  N004 -.-> N002
  N002 -.-> N004
  N004 -.-> N003
  N003 -.-> N004
```

## Other / cross-cutting

- Concepts included: **21**

```mermaid
flowchart LR
  N001["business name"]
  N002["care of"]
  N003["company name"]
  N004["company type"]
  N005["complex representation rule"]
  N006["delegable"]
  N007["economic activity"]
  N008["full name"]
  N009["jurisdiction"]
  N010["location"]
  N011["mandate transfer"]
  N012["monetary amount"]
  N013["name"]
  N014["notation"]
  N015["object"]
  N016["power"]
  N017["restriction"]
  N018["scope"]
  N019["simple representation rule"]
  N020["site"]
  N021["Union entity"]
  N013 --> N001
  N013 --> N008
```

## Cross-cutting links

Relationships where the two concepts fall under different *primary* themes.

| Theme A | Theme B | Concept A | Relationship | Concept B |
|---|---|---|---|---|
| Data spaces | Governance | electronic attestation of attributes | related | mandate |
| Data spaces | Governance | electronic attestation of attributes | related | representation rule |
| Data spaces | Governance | European Business Wallet | related | mandate |
| Data spaces | Governance | European Business Wallet | related | representation rule |
| Data spaces | Governance | European Business Wallet owner identification data | related | identifier |
| Data spaces | Trust and assurance | European Business Wallet | broader/narrower | European Business Wallet solution |
| Data spaces | Trust and assurance | European Business Wallet | related | European Business Wallet unit |
| Data spaces | Trust and assurance | wallet unit attestation | related | European Business Wallet solution |
| Data spaces | Trust and assurance | wallet unit attestation | related | European Business Wallet unit |
| Data spaces | Wallets and digital identity | European Business Wallet | related | European Business Wallet relying party |
| Data spaces | Wallets and digital identity | European Business Wallet owner | related | European Business Wallet relying party |
| Governance | Data spaces | agent | broader/narrower | European Business Wallet owner |
| Governance | Data spaces | identifier | broader/narrower | legal identifier |
| Governance | Data spaces | mandate | related | European Business Wallet owner |
| Governance | Data spaces | representation right | related | European Business Wallet owner |
| Governance | Other / cross-cutting | activity | broader/narrower | economic activity |
| Governance | Other / cross-cutting | mandate | related | mandate transfer |
| Governance | Other / cross-cutting | representation rule | broader/narrower | complex representation rule |
| Governance | Other / cross-cutting | representation rule | broader/narrower | simple representation rule |
| Governance | Wallets and digital identity | agent | broader/narrower | European Business Wallet relying party |
| Governance | Wallets and digital identity | agent | broader/narrower | mandatee |
| Governance | Wallets and digital identity | agent | broader/narrower | mandator |
| Governance | Wallets and digital identity | agent | broader/narrower | natural person |
| Governance | Wallets and digital identity | agent | broader/narrower | organisation |
| Governance | Wallets and digital identity | company | related | economic operator |
| Governance | Wallets and digital identity | legal entity | related | contact point |
| Governance | Wallets and digital identity | legal entity | broader/narrower | economic operator |
| Governance | Wallets and digital identity | legal entity | related | post |
| Governance | Wallets and digital identity | legal entity | broader/narrower | public sector body |
| Governance | Wallets and digital identity | legal entity | related | share capital |
| Governance | Wallets and digital identity | mandate | related | European Business Wallet relying party |
| Governance | Wallets and digital identity | mandate | related | mandatee |
| Governance | Wallets and digital identity | mandate | related | mandator |
| Governance | Wallets and digital identity | representation rule | related | European Business Wallet relying party |
| Other / cross-cutting | Wallets and digital identity | economic activity | related | economic operator |
| Other / cross-cutting | Wallets and digital identity | name | broader/narrower | alternative name |
| Other / cross-cutting | Wallets and digital identity | name | broader/narrower | legal name |
| Wallets and digital identity | Data spaces | economic operator | related | European Business Wallet owner |
| Wallets and digital identity | Data spaces | public sector body | related | European Business Wallet owner |
| Wallets and digital identity | Governance | alternative name | related | legal entity |
| Wallets and digital identity | Governance | beneficial owner | related | agent |
| Wallets and digital identity | Governance | entity | broader/narrower | agent |
| Wallets and digital identity | Governance | legal form | related | agent |
| Wallets and digital identity | Governance | legal name | related | legal entity |
| Wallets and digital identity | Governance | organisation | broader/narrower | formal organisation |
| Wallets and digital identity | Governance | share | related | legal entity |
| Wallets and digital identity | Governance | shareholder | related | agent |
| Wallets and digital identity | Governance | signatory | related | agent |
| Wallets and digital identity | Other / cross-cutting | legal form | related | company type |
| Wallets and digital identity | Other / cross-cutting | legal name | related | company name |
| Wallets and digital identity | Other / cross-cutting | public sector body | broader/narrower | Union entity |

> Note: If you want a stricter thematic split, the most robust method is to anchor themes on specific top concepts and take their narrower closure (once the hierarchy is final).