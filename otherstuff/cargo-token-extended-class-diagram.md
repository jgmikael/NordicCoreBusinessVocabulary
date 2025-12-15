# Cargo Token – Extended Conceptual Model (eFTI / EUDI Wallet)

This document presents an **extended Mermaid class diagram** for the proposed **Cargo Token**
concept, based on a close reading of the draft email discussion.

The diagram:
- Reuses **existing concepts from NCBV and KTDDE** where possible
- **Explicitly introduces NEW concepts** that are **not present** in NCBV or KTDDE but are
  required to satisfy the functional, technical, and governance requirements described
  in the email (eFTI, EUDI Wallets, offline verification).

NEW concepts are clearly marked with `<<NEW>>`.

---

```mermaid
classDiagram
direction LR

%% =========================
%% EXISTING (NCBV / KTDDE)
%% =========================

class ncbv_Document["ncbv:Document"] {
  status
}

class ncbv_Identifier["ncbv:Identifier"] {
  identifierValue
}

class ktddecv_Consignment["ktddecv:Consignment"] {
  consignmentIdentifier
}

class ktddecv_Shipment["ktddecv:Shipment"] {
  shipmentIdentifier
}

class ktddecv_TransportEquipment["ktddecv:TransportEquipment"] {
  equipmentIdentifier
  sealIdentifier
  vehicleRegistrationIdentifier
}

class ktddecv_Party["ktddecv:Party"] {
  partyIdentifier
}

%% =========================
%% NEW CONCEPTS (NOT IN NCBV / KTDDE)
%% =========================

class CargoToken["CargoToken <<NEW>>"] {
  tokenId
  validFrom
  validUntil
}

class UIL["eFTI Unique Identifier Link <<NEW>>"] {
  uilValue
}

class EftiPlatform["eFTI Platform <<NEW>>"] {
  platformId
}

class EftiGate["eFTI Gate <<NEW>>"] {
  gateId
}

class WalletHolder["Authenticated Holder / Wallet <<NEW>>"] {
  holderId
}

class VerifiableProof["Cryptographic Proof <<NEW>>"] {
  proofType
  signature
}

%% =========================
%% RELATIONSHIPS
%% =========================

CargoToken --> ncbv_Document : specializes
CargoToken --> ncbv_Identifier : hasTokenIdentifier
CargoToken --> UIL : encapsulatesUIL
CargoToken --> VerifiableProof : hasProof

CargoToken --> ktddecv_Consignment : bindsConsignment
CargoToken --> ktddecv_Shipment : bindsShipment
CargoToken --> ktddecv_TransportEquipment : bindsEquipment

CargoToken --> WalletHolder : boundToHolder

EftiPlatform --> CargoToken : issues
EftiPlatform --> VerifiableProof : signsWithSeal

EftiGate --> CargoToken : validates
EftiGate --> UIL : resolvesUIL
```

---

## Interpretation notes

- **CargoToken** is a verifiable control artifact that binds a physical consignment
  to its authoritative eFTI dataset via the **UIL**.
- The **eFTI Platform** is responsible for issuing and sealing the token.
- The **eFTI Gate** validates the token and resolves the UIL when online access is possible.
- Offline verification is enabled through the **cryptographic proof** embedded in the token.
- The underlying eFTI dataset and KTDDE documents remain the authoritative sources of data.

This file is intended for publication directly in GitHub; the Mermaid diagram is
GitHub-renderer safe.
