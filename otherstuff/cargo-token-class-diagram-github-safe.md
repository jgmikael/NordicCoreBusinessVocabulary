# Cargo Token – Class Diagram (GitHub-safe Mermaid)

This document contains a **GitHub-renderable Mermaid class diagram** for the Cargo Token concept,
modelled strictly using **NCBV** and **KTDDE** classes and properties.

⚠️ Note: Relationship labels have been made Mermaid-safe (no namespace colons, no cardinalities)
to avoid GitHub parsing errors. The original ontology IRIs are preserved in class titles.

---

```mermaid
classDiagram
direction LR

class ncbv_Document["ncbv:Document (CargoToken)"] {
  + hasIdentifier -> ncbv_Identifier
  + status
}

class ncbv_Identifier["ncbv:Identifier"] {
  + identifierValue
}

class ktddecv_Consignment["ktddecv:Consignment"] {
  + consignmentIdentifier
  + consignorParty -> ktddecv_Party
  + consigneeParty -> ktddecv_Party
}

class ktddecv_Shipment["ktddecv:Shipment"] {
  + shipmentIdentifier
  + carrierParty -> ktddecv_Party
  + hasConsignment -> ktddecv_Consignment
  + hasTransportEquipment -> ktddecv_TransportEquipment
  + placeOfLoading -> ktddecv_Location
  + placeOfDelivery -> ktddecv_Location
  + placeOfReceiptUNLocode
  + placeOfDeliveryUNLocode
}

class ktddecv_TransportEquipment["ktddecv:TransportEquipment"] {
  + equipmentIdentifier
  + sealIdentifier
  + vehicleRegistrationIdentifier
  + railWagonIdentifier
}

class ktddecv_Party["ktddecv:Party"] {
  + partyIdentifier
}

class ktddecv_Location["ktddecv:Location"] {
  + locationID
  + locationName
  + locationCountry
}

class ktddecv_TransportDocument["ktddecv:TransportDocument"] {
  + documentIdentifier
}

ncbv_Document --> ktddecv_Consignment : relatesToConsignment
ncbv_Document --> ktddecv_Shipment : hasShipment
ncbv_Document --> ktddecv_TransportDocument : relatesToTransportDocument

ncbv_Document --> ncbv_Identifier : hasIdentifier
ktddecv_Shipment --> ktddecv_Consignment : hasConsignment
ktddecv_Shipment --> ktddecv_TransportEquipment : hasTransportEquipment
```

---

## Implementation note

This diagram is intended for **conceptual documentation** in GitHub.
Cardinalities, datatypes, and full IRIs should be expressed in:
- OWL (ontology files)
- SHACL shapes
- JSON-LD contexts

not inside Mermaid diagrams.
