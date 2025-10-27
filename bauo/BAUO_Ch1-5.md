# 🏛 Business Activity Upper Ontology (BAUO)
**Version:** 0.0.1 (Draft)  
**Purpose:** To provide a simple, high-level semantic structure for describing what happens in *doing business* — who acts, what they do, what they use or produce, and in what context.

---

## 1. What is the BAUO?

The **Business Activity Upper Ontology (BAUO)** defines a small set of universal concepts that describe how organisations and people (called *agents*) carry out activities — such as exporting goods, issuing invoices, or submitting reports — within a business or regulatory environment.

It sits **above** the two main vocabularies:
- **NCBV** (Nordic Core Business Vocabulary) – covers legal entities, persons, roles, identifiers, locations, and documents.  
- **KTDDE** (Key Trade Documents and Data Elements) – covers international trade processes, goods, transport, and trade documents.

BAUO ties them together by introducing the central idea of a **business activity**.

---

## 2. Key Concepts (Classes)

### **bauo:Activity**
Something that happens and involves one or more agents using or producing resources.  
Every real-world business action — for example “Issue a Commercial Invoice” or “Load goods onto vessel” — is an *Activity*.

- **Properties:**  
  - **bauo:hasAgent** → the person or organisation involved.  
  - **bauo:usesResource** → what is used (like a Purchase Order, Goods, or Data).  
  - **bauo:producesResource** → what is produced (like an Invoice or Shipping Document).  
  - **bauo:hasOutcome** → the resulting event or effect.  
  - **bauo:hasLocation** → where it happens.  
  - **bauo:hasContext** → under what contract, mandate, or regulation.  
  - **bauo:activityName**, **bauo:activityDescription**, **bauo:activityStatus** → human-readable details.  
  - **ncbv:startDate**, **ncbv:endDate** → time period.

---

### **bauo:BusinessActivity**
A special type of Activity that occurs in a commercial, regulatory, or service environment.  
Examples include “Submit VAT Declaration,” “Export Goods,” or “Pay Invoice.”

It inherits all properties from **bauo:Activity**.

---

### **bauo:Agent**
An actor that can perform activities or hold responsibilities.  
It can be either a **Person** or a **Legal Entity (Organisation)**.

- **Subclasses:**  
  - **ncbv:Person** – an individual.  
  - **ncbv:LegalEntity** – a registered company or organisation.  
- **Properties:**  
  - **ncbv:hasRole** → defines what role they play (e.g., exporter, importer).  
  - **ncbv:hasIdentifier** → connects to identifiers like Business ID, EORI, or LEI.  
  - **bauo:hasCapability** (proposed) → optional description of the authorisation or competence to act.

---

### **bauo:Role**
A function or capacity that an agent plays in a given activity.  
Examples: *Exporter*, *Importer*, *Carrier*, *Issuing Bank*.

---

### **bauo:Resource**
Anything that is used, transformed, or produced in an activity.  
Resources can be physical goods, services, documents, or data.

- **Subclasses and examples:**  
  - **ncbv:Document** – e.g., Invoice, Contract, Permit.  
  - **ktddecv:TradeProduct / TradeItem** – physical goods.  
- **Properties:**  
  - **ncbv:hasIdentifier** → serial number, UN/LOCODE, GTIN, etc.  
  - **bauo:isProducedBy / bauo:isUsedIn** (inverse of above) – links to the activities that use or produce it.

---

### **bauo:Event**
Something that occurs at a point in time — often as a result of an activity.  
For example, “Goods Loaded on Vessel” or “Payment Confirmed.”

- **Properties:**  
  - **ktddecv:eventDateTime** → timestamp.  
  - **bauo:hasLocation** → where the event took place.

---

### **bauo:Process**
A collection or sequence of activities aimed at a common goal.  
Examples: *Export Process*, *Tax Reporting Process*.

- **Properties:**  
  - **bauo:includesActivity** → which activities form part of it.  
  - **bauo:hasOutcome** → final result (e.g., delivery completed).

---

### **bauo:BusinessContext**
The environment in which an activity occurs — such as a contract, regulation, or business agreement.  
In legal terms, this can be represented using **ncbv:Mandate** or **ncbv:LegalResource**.

---

### **bauo:Plan**
A specification or design of an intended activity.  
For example, a “Delivery Plan” or “Shipment Schedule.”

---

### **bauo:Location**
A place where an activity or event occurs.  
Reuses **ncbv:Location**, which can hold an address or coordinates.

---

### **bauo:Capability**
The ability or authorisation to perform a certain activity.  
For example, a customs broker’s licence or a bank’s authorisation to issue letters of credit.

---

## 3. How the Classes Relate

A **BusinessActivity** connects:
- **Agents** (who act)  
- **Roles** (what capacity they act in)  
- **Resources** (what is used and produced)  
- **Events** (what happens as a result)  
- **Context** (why and under what rules it happens)  
- **Location** and **Time** (where and when it happens)

These links make business actions machine-understandable, traceable, and interoperable across systems and countries.

---

## 4. Example in Practice  
Below is a JSON-LD example of an international trade activity:  
**“Exporting timber beams from Finland to Japan.”**

```json
{
  "@context": {
    "bauo": "https://example.org/bauo#",
    "ncbv": "https://iri.suomi.fi/model/ncbv/",
    "ktddecv": "https://iri.suomi.fi/model/ktddecv/"
  },
  "@type": "bauo:BusinessActivity",
  "bauo:activityName": "Export of Glulam Beams to Japan",
  "bauo:activityDescription": "Finnlamelli Oy issues a commercial invoice and transport document for timber beams exported from HaminaKotka port to Yokohama.",
  "bauo:activityStatus": "Completed",
  "ncbv:startDate": "2025-10-18",
  "ncbv:endDate": "2025-10-26",

  "bauo:hasAgent": {
    "@id": "urn:org:finnlamelli",
    "@type": "ncbv:LegalEntity",
    "ncbv:legalName": "Finnlamelli Oy",
    "ncbv:hasIdentifier": {
      "@type": "ncbv:Identifier",
      "ncbv:notation": "FI1234567-8",
      "ncbv:schemeName": "Business ID"
    },
    "ncbv:hasRole": {
      "@type": "ncbv:Role",
      "rdfs:label": "Exporter"
    }
  },

  "bauo:usesResource": [
    {
      "@id": "urn:item:glulam-beams",
      "@type": "ktddecv:TradeProduct",
      "ktddecv:productDescription": "Glued laminated timber beams, spruce",
      "ktddecv:quantity": "25.0",
      "ktddecv:unitCode": "m3"
    },
    {
      "@id": "urn:doc:purchaseorder-789",
      "@type": "ncbv:Document",
      "ncbv:documentType": "Purchase Order",
      "ncbv:documentIdentifier": "PO-789-JP"
    }
  ],

  "bauo:producesResource": [
    {
      "@id": "urn:doc:invoice-2025-001",
      "@type": "ktddecv:CommercialInvoice",
      "ktddecv:invoiceNumber": "INV-2025-001",
      "ktddecv:currencyCode": "EUR",
      "ktddecv:totalAmount": "75000.00"
    },
    {
      "@id": "urn:doc:fbl-2025-002",
      "@type": "ktddecv:TransportDocument",
      "ktddecv:documentNumber": "FBL-2025-002",
      "ktddecv:placeOfIssue": "HaminaKotka",
      "ktddecv:placeOfLoading": "FIHAM",
      "ktddecv:placeOfDelivery": "JPYOK"
    }
  ],

  "bauo:hasOutcome": {
    "@id": "urn:event:shipment-001",
    "@type": "ktddecv:TransportEvent",
    "ktddecv:eventDescription": "Shipment departed from HaminaKotka port",
    "ktddecv:eventDateTime": "2025-10-26T09:30:00Z"
  },

  "bauo:hasContext": {
    "@id": "urn:contract:lc-jp-2025-01",
    "@type": "ncbv:Mandate",
    "ncbv:legalResourceType": "Letter of Credit",
    "ncbv:contractIdentifier": "LC-JP-2025-01",
    "ncbv:startDate": "2025-09-01",
    "ncbv:endDate": "2026-03-01"
  },

  "bauo:hasLocation": {
    "@type": "ncbv:Location",
    "rdfs:label": "HaminaKotka Port, Finland",
    "ncbv:geographicIdentifier": "FIHAM"
  }
}
```

---

## 5. Why This Matters

Using this structure, business activities become interoperable digital records that can be:
- Verified (for example, through verifiable credentials in an EU Business Wallet).  
- Shared across systems (B2B, B2G, supply chains).  
- Linked to documents, events, and roles in a consistent way.  
- Mapped to global standards like UN/CEFACT, UBL, or ISO 20022.
