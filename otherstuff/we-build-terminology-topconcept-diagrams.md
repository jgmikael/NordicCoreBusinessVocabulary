# WE BUILD Terminology (SKOS) — Diagrams by Top Concept

Source: `WE BUILD Terminology.ttl`

Node labels come from **SKOS-XL** (`skos:prefLabel` → label resource → `skos-xl:literalForm`, English where available).

Conventions in diagrams:
- **Hierarchy:** solid arrows labeled **narrower** (top → down) and **broader** (child → up).
- **Related:** dotted arrows (less prominent).

## Index
- [activity](#activity)
- [address](#address)
- [care of](#care-of)
- [company](#company)
- [company name](#company-name)
- [company status](#company-status)
- [company type](#company-type)
- [contact point](#contact-point)
- [date of birth](#date-of-birth)
- [delegable](#delegable)
- [deputy board member](#deputy-board-member)
- [deputy managing director](#deputy-managing-director)
- [document](#document)
- [duration of the legal entity](#duration-of-the-legal-entity)
- [entity](#entity)
- [European Business Wallet](#european-business-wallet)
- [identifier](#identifier)
- [jurisdiction](#jurisdiction)
- [legal form](#legal-form)
- [legal person](#legal-person)
- [legal resource](#legal-resource)
- [legal status](#legal-status)
- [location](#location)
- [mandate](#mandate)
- [mandate transfer](#mandate-transfer)
- [membership](#membership)
- [monetary amount](#monetary-amount)
- [name](#name)
- [notation](#notation)
- [object](#object)
- [post](#post)
- [power](#power)
- [registration date](#registration-date)
- [representation right](#representation-right)
- [representation rule](#representation-rule)
- [restriction](#restriction)
- [role](#role)
- [schema agency](#schema-agency)
- [scope](#scope)
- [share](#share)
- [share capital](#share-capital)
- [shareholder](#shareholder)
- [signatory](#signatory)
- [site](#site)
- [source](#source)

## activity

- Concepts in subtree (narrower closure): **3**
- Hierarchy links in subtree: **2**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["activity"]
  N002["economic activity"]
  N003["registration"]
  N001 -->|narrower| N002
  N002 -->|broader| N001
  N001 -->|narrower| N003
  N003 -->|broader| N001
```

## address

- Concepts in subtree (narrower closure): **3**
- Hierarchy links in subtree: **2**
- Related links in subtree: **1**

```mermaid
flowchart LR
  N001["address"]
  N002["postal address"]
  N003["registered address"]
  N001 -->|narrower| N002
  N002 -->|broader| N001
  N001 -->|narrower| N003
  N003 -->|broader| N001
  N003 -.-> N002
  N002 -.-> N003
```

## care of

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["care of"]
```

## company

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["company"]
```

## company name

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["company name"]
```

## company status

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["company status"]
```

## company type

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["company type"]
```

## contact point

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["contact point"]
```

## date of birth

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["date of birth"]
```

## delegable

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["delegable"]
```

## deputy board member

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["deputy board member"]
```

## deputy managing director

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["deputy managing director"]
```

## document

- Concepts in subtree (narrower closure): **5**
- Hierarchy links in subtree: **4**
- Related links in subtree: **2**

```mermaid
flowchart LR
  N001["document"]
  N002["electronic attestation of attributes"]
  N003["European Business Wallet owner identification data"]
  N004["qualified attestation of attributes"]
  N005["wallet unit attestation"]
  N001 -->|narrower| N002
  N002 -->|broader| N001
  N001 -->|narrower| N003
  N003 -->|broader| N001
  N001 -->|narrower| N005
  N005 -->|broader| N001
  N002 -->|narrower| N004
  N004 -->|broader| N002
  N003 -.-> N002
  N002 -.-> N003
  N003 -.-> N004
  N004 -.-> N003
```

## duration of the legal entity

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["duration of the legal entity"]
```

## entity

- Concepts in subtree (narrower closure): **15**
- Hierarchy links in subtree: **14**
- Related links in subtree: **6**

```mermaid
flowchart LR
  N001["agent"]
  N002["beneficial owner"]
  N003["economic operator"]
  N004["entity"]
  N005["European Business Wallet owner"]
  N006["European Business Wallet relying party"]
  N007["formal organisation"]
  N008["legal entity"]
  N009["mandatee"]
  N010["mandator"]
  N011["natural person"]
  N012["organisation"]
  N013["public sector body"]
  N014["registered organisation"]
  N015["Union entity"]
  N001 -->|narrower| N005
  N005 -->|broader| N001
  N001 -->|narrower| N006
  N006 -->|broader| N001
  N001 -->|narrower| N009
  N009 -->|broader| N001
  N001 -->|narrower| N010
  N010 -->|broader| N001
  N001 -->|narrower| N011
  N011 -->|broader| N001
  N001 -->|narrower| N012
  N012 -->|broader| N001
  N004 -->|narrower| N001
  N001 -->|broader| N004
  N007 -->|narrower| N008
  N008 -->|broader| N007
  N007 -->|narrower| N014
  N014 -->|broader| N007
  N008 -->|narrower| N003
  N003 -->|broader| N008
  N008 -->|narrower| N013
  N013 -->|broader| N008
  N011 -->|narrower| N002
  N002 -->|broader| N011
  N012 -->|narrower| N007
  N007 -->|broader| N012
  N013 -->|narrower| N015
  N015 -->|broader| N013
  N002 -.-> N001
  N001 -.-> N002
  N003 -.-> N005
  N005 -.-> N003
  N005 -.-> N006
  N006 -.-> N005
  N010 -.-> N009
  N009 -.-> N010
  N013 -.-> N005
  N005 -.-> N013
  N014 -.-> N008
  N008 -.-> N014
```

## European Business Wallet

- Concepts in subtree (narrower closure): **3**
- Hierarchy links in subtree: **2**
- Related links in subtree: **1**

```mermaid
flowchart LR
  N001["European Business Wallet"]
  N002["European Business Wallet solution"]
  N003["European Business Wallet unit"]
  N001 -->|narrower| N002
  N002 -->|broader| N001
  N002 -->|narrower| N003
  N003 -->|broader| N002
  N001 -.-> N003
  N003 -.-> N001
```

## identifier

- Concepts in subtree (narrower closure): **2**
- Hierarchy links in subtree: **1**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["identifier"]
  N002["legal identifier"]
  N001 -->|narrower| N002
  N002 -->|broader| N001
```

## jurisdiction

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["jurisdiction"]
```

## legal form

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["legal form"]
```

## legal person

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["legal person"]
```

## legal resource

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["legal resource"]
```

## legal status

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["legal status"]
```

## location

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["location"]
```

## mandate

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["mandate"]
```

## mandate transfer

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["mandate transfer"]
```

## membership

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["membership"]
```

## monetary amount

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["monetary amount"]
```

## name

- Concepts in subtree (narrower closure): **5**
- Hierarchy links in subtree: **4**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["alternative name"]
  N002["business name"]
  N003["full name"]
  N004["legal name"]
  N005["name"]
  N005 -->|narrower| N001
  N001 -->|broader| N005
  N005 -->|narrower| N002
  N002 -->|broader| N005
  N005 -->|narrower| N003
  N003 -->|broader| N005
  N005 -->|narrower| N004
  N004 -->|broader| N005
```

## notation

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["notation"]
```

## object

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["object"]
```

## post

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["post"]
```

## power

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["power"]
```

## registration date

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["registration date"]
```

## representation right

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["representation right"]
```

## representation rule

- Concepts in subtree (narrower closure): **6**
- Hierarchy links in subtree: **5**
- Related links in subtree: **3**

```mermaid
flowchart LR
  N001["complex representation rule"]
  N002["composite representation rule"]
  N003["membership based representation rule"]
  N004["representation rule"]
  N005["role based representation rule"]
  N006["simple representation rule"]
  N004 -->|narrower| N001
  N001 -->|broader| N004
  N004 -->|narrower| N002
  N002 -->|broader| N004
  N004 -->|narrower| N003
  N003 -->|broader| N004
  N004 -->|narrower| N005
  N005 -->|broader| N004
  N004 -->|narrower| N006
  N006 -->|broader| N004
  N002 -.-> N003
  N003 -.-> N002
  N002 -.-> N005
  N005 -.-> N002
  N005 -.-> N003
  N003 -.-> N005
```

## restriction

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["restriction"]
```

## role

- Concepts in subtree (narrower closure): **4**
- Hierarchy links in subtree: **3**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["auditor"]
  N002["board member"]
  N003["chairman of the board"]
  N004["role"]
  N002 -->|narrower| N003
  N003 -->|broader| N002
  N004 -->|narrower| N001
  N001 -->|broader| N004
  N004 -->|narrower| N002
  N002 -->|broader| N004
```

## schema agency

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["schema agency"]
```

## scope

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["scope"]
```

## share

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["share"]
```

## share capital

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["share capital"]
```

## shareholder

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["shareholder"]
```

## signatory

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["signatory"]
```

## site

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["site"]
```

## source

- Concepts in subtree (narrower closure): **1**
- Hierarchy links in subtree: **0**
- Related links in subtree: **0**

```mermaid
flowchart LR
  N001["source"]
```
