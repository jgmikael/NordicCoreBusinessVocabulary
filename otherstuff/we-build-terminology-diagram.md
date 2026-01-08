# WE BUILD Terminology (SKOS) — Concept Relationship Diagram

This file was generated from the Turtle source: `WE BUILD Terminology.ttl`.

## Overview

- Concepts found: **82**
- Hierarchical links (skos:broader / skos:narrower): **37**
- Associative links (skos:related, unique undirected pairs): **75**

## Complete Mermaid diagram

```mermaid
flowchart LR
  C001["concept-0"]
  C002["concept-1"]
  C003["concept-100"]
  C004["concept-1000"]
  C005["concept-101"]
  C006["concept-102"]
  C007["concept-103"]
  C008["concept-104"]
  C009["concept-105"]
  C010["concept-106"]
  C011["concept-107"]
  C012["concept-109"]
  C013["concept-14"]
  C014["concept-15"]
  C015["concept-16"]
  C016["concept-18"]
  C017["concept-2000"]
  C018["concept-2001"]
  C019["concept-22"]
  C020["concept-23"]
  C021["concept-24"]
  C022["concept-26"]
  C023["concept-27"]
  C024["concept-28"]
  C025["concept-30"]
  C026["concept-3000"]
  C027["concept-3002"]
  C028["concept-3003"]
  C029["concept-3006"]
  C030["concept-3007"]
  C031["concept-3008"]
  C032["concept-3009"]
  C033["concept-3010"]
  C034["concept-3012"]
  C035["concept-3021"]
  C036["concept-33"]
  C037["concept-4"]
  C038["concept-41"]
  C039["concept-42"]
  C040["concept-43"]
  C041["concept-48"]
  C042["concept-5001"]
  C043["concept-51"]
  C044["concept-6003"]
  C045["concept-6004"]
  C046["concept-6005"]
  C047["concept-6006"]
  C048["concept-6011"]
  C049["concept-6012"]
  C050["concept-6013"]
  C051["concept-6040"]
  C052["concept-6042"]
  C053["concept-6043"]
  C054["concept-6044"]
  C055["concept-6045"]
  C056["concept-7"]
  C057["concept-74"]
  C058["concept-75"]
  C059["concept-76"]
  C060["concept-77"]
  C061["concept-78"]
  C062["concept-79"]
  C063["concept-80"]
  C064["concept-81"]
  C065["concept-82"]
  C066["concept-83"]
  C067["concept-84"]
  C068["concept-85"]
  C069["concept-86"]
  C070["concept-87"]
  C071["concept-88"]
  C072["concept-89"]
  C073["concept-90"]
  C074["concept-91"]
  C075["concept-92"]
  C076["concept-93"]
  C077["concept-94"]
  C078["concept-95"]
  C079["concept-96"]
  C080["concept-97"]
  C081["concept-98"]
  C082["concept-99"]
  C002 --> C041
  C005 --> C006
  C008 --> C010
  C010 --> C011
  C016 --> C009
  C016 --> C021
  C016 --> C043
  C016 --> C049
  C018 --> C017
  C018 --> C025
  C028 --> C031
  C037 --> C039
  C037 --> C040
  C038 --> C002
  C038 --> C046
  C038 --> C059
  C038 --> C060
  C038 --> C081
  C038 --> C082
  C041 --> C023
  C041 --> C047
  C045 --> C028
  C045 --> C033
  C046 --> C027
  C047 --> C077
  C047 --> C079
  C048 --> C063
  C048 --> C064
  C048 --> C065
  C048 --> C066
  C048 --> C067
  C056 --> C013
  C076 --> C003
  C076 --> C005
  C076 --> C007
  C078 --> C038
  C079 --> C080
  C001 -.-> C019
  C019 -.-> C001
  C001 -.-> C028
  C028 -.-> C001
  C001 -.-> C047
  C047 -.-> C001
  C001 -.-> C077
  C077 -.-> C001
  C003 -.-> C005
  C005 -.-> C003
  C003 -.-> C006
  C006 -.-> C003
  C003 -.-> C013
  C013 -.-> C003
  C003 -.-> C056
  C056 -.-> C003
  C003 -.-> C081
  C081 -.-> C003
  C005 -.-> C048
  C048 -.-> C005
  C005 -.-> C058
  C058 -.-> C005
  C007 -.-> C010
  C010 -.-> C007
  C007 -.-> C011
  C011 -.-> C007
  C008 -.-> C011
  C011 -.-> C008
  C008 -.-> C048
  C048 -.-> C008
  C008 -.-> C058
  C058 -.-> C008
  C008 -.-> C076
  C076 -.-> C008
  C008 -.-> C081
  C081 -.-> C008
  C008 -.-> C082
  C082 -.-> C008
  C009 -.-> C022
  C022 -.-> C009
  C009 -.-> C047
  C047 -.-> C009
  C015 -.-> C024
  C024 -.-> C015
  C015 -.-> C038
  C038 -.-> C015
  C017 -.-> C077
  C077 -.-> C017
  C018 -.-> C047
  C047 -.-> C018
  C019 -.-> C038
  C038 -.-> C019
  C020 -.-> C036
  C036 -.-> C020
  C020 -.-> C038
  C038 -.-> C020
  C023 -.-> C047
  C047 -.-> C023
  C025 -.-> C047
  C047 -.-> C025
  C025 -.-> C056
  C056 -.-> C025
  C025 -.-> C073
  C073 -.-> C025
  C025 -.-> C074
  C074 -.-> C025
  C026 -.-> C035
  C035 -.-> C026
  C026 -.-> C038
  C038 -.-> C026
  C026 -.-> C051
  C051 -.-> C026
  C027 -.-> C038
  C038 -.-> C027
  C028 -.-> C030
  C030 -.-> C028
  C028 -.-> C044
  C044 -.-> C028
  C028 -.-> C047
  C047 -.-> C028
  C028 -.-> C061
  C061 -.-> C028
  C031 -.-> C044
  C044 -.-> C031
  C031 -.-> C047
  C047 -.-> C031
  C031 -.-> C058
  C058 -.-> C031
  C032 -.-> C038
  C038 -.-> C032
  C033 -.-> C047
  C047 -.-> C033
  C033 -.-> C073
  C073 -.-> C033
  C035 -.-> C047
  C047 -.-> C035
  C035 -.-> C051
  C051 -.-> C035
  C038 -.-> C045
  C045 -.-> C038
  C038 -.-> C061
  C061 -.-> C038
  C039 -.-> C040
  C040 -.-> C039
  C043 -.-> C047
  C047 -.-> C043
  C044 -.-> C081
  C081 -.-> C044
  C045 -.-> C061
  C061 -.-> C045
  C045 -.-> C066
  C066 -.-> C045
  C046 -.-> C050
  C050 -.-> C046
  C046 -.-> C054
  C054 -.-> C046
  C047 -.-> C051
  C051 -.-> C047
  C047 -.-> C054
  C054 -.-> C047
  C047 -.-> C055
  C055 -.-> C047
  C048 -.-> C082
  C082 -.-> C048
  C058 -.-> C059
  C059 -.-> C058
  C058 -.-> C060
  C060 -.-> C058
  C058 -.-> C072
  C072 -.-> C058
  C058 -.-> C081
  C081 -.-> C058
  C058 -.-> C082
  C082 -.-> C058
  C059 -.-> C060
  C060 -.-> C059
  C061 -.-> C067
  C067 -.-> C061
  C065 -.-> C066
  C066 -.-> C065
  C065 -.-> C067
  C067 -.-> C065
  C066 -.-> C067
  C067 -.-> C066
  C077 -.-> C081
  C081 -.-> C077
  C079 -.-> C081
  C081 -.-> C079
  C081 -.-> C082
  C082 -.-> C081
```
