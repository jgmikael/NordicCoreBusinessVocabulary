# Cargo Token – Class Diagram (NCBV + KTDDE)

This document contains the Mermaid class diagram for the **Cargo Token** concept,
modelled strictly using classes and properties from the **Nordic Core Business Vocabulary (NCBV)**
and the **Key Trade Documents and Data Elements (KTDDE) Core Vocabulary**.

---

```mermaid
classDiagram
direction LR

class ncbv_Document["ncbv:Document (CargoToken)"] {
  + ncbv:hasIdentifier -> ncbv:Identifier (token-id) [1..*]
  + ncbv:status -> xsd:string [0..1]
}

class ncbv_Identifier["ncbv:Identifier"] {
  + ncbv:identifierValue -> xsd:string [0..1]
}

class ktddecv_Consignment["ktddecv:Consignment"] {
  + ktddecv:consignmentIdentifier -> xsd:string [0..1]
  + ktddecv:consignorParty -> ktddecv:Party [0..1]
  + ktddecv:consigneeParty -> ktddecv:Party [0..1]
}

class ktddecv_Shipment["ktddecv:Shipment"] {
  + ktddecv:shipmentIdentifier -> xsd:string [0..1]
  + ktddecv:carrierParty -> ktddecv:Party [0..1]
  + ktddecv:hasConsignment -> ktddecv:Consignment [0..*]
  + ktddecv:hasTransportEquipment -> ktddecv:TransportEquipment [0..*]
  + ktddecv:placeOfLoading -> ktddecv:Location [0..1]
  + ktddecv:placeOfDelivery -> ktddecv:Location [0..1]
  + ktddecv:placeOfReceiptUNLocode -> xsd:string [0..1]
  + ktddecv:placeOfDeliveryUNLocode -> xsd:string [0..1]
}

class ktddecv_TransportEquipment["ktddecv:TransportEquipment"] {
  + ktddecv:equipmentIdentifier -> xsd:string [0..1]
  + ktddecv:sealIdentifier -> xsd:string [0..1]
  + ktddecv:vehicleRegistrationIdentifier -> xsd:string [0..1]
  + ktddecv:railWagonIdentifier -> xsd:string [0..1]
}

class ktddecv_Party["ktddecv:Party"] {
  + ktddecv:partyIdentifier -> xsd:string [0..1]
}

class ktddecv_Location["ktddecv:Location"] {
  + ktddecv:locationID -> xsd:string [0..1]
  + ktddecv:locationName -> xsd:string [0..1]
  + ktddecv:locationCountry -> xsd:string [0..1]
}

class ktddecv_TransportDocument["ktddecv:TransportDocument"] {
  + ktddecv:documentIdentifier -> xsd:string [0..1]
}

ncbv_Document --> ktddecv_Consignment : ktddecv:relatesToConsignment [0..1]
ncbv_Document --> ktddecv_Shipment : ktddecv:hasShipment [0..1]
ncbv_Document --> ktddecv_TransportDocument : ktddecv:relatesToTransportDocument [0..*]

ncbv_Document --> ncbv_Identifier : ncbv:hasIdentifier [1..*]
ktddecv_Shipment --> ktddecv_Consignment : ktddecv:hasConsignment [0..*]
ktddecv_Shipment --> ktddecv_TransportEquipment : ktddecv:hasTransportEquipment [0..*]
```

---

## Usage notes

- Save this file in a GitHub repository with a `.md` extension.
- GitHub will automatically render the Mermaid diagram.
- The diagram intentionally avoids introducing any classes or properties
  that are not present in the uploaded NCBV and KTDDE ontologies.
