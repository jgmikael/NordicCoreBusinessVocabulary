# SEPA Request-to-Pay — Verifiable Credential Example  
*(based on KTDDE and NCBV vocabularies)*

---

> **Purpose of this document**  
> This example illustrates, in both narrative and structured form, how a  
> **SEPA Request-to-Pay (SRTP)** can be expressed as a **W3C Verifiable Credential (VC)**.  
> It shows how the creditor’s request for payment — a standard ISO 20022 dataset —  
> can be represented semantically using the **KTDDE (Key Trade Documents & Data Elements)**  
> and **NCBV (Nordic Core Business Vocabulary)** ontologies.  
>
> For non-experts:  
> - *KTDDE* describes business documents and their data fields (e.g., “amount,” “expiry date”).  
> - *NCBV* describes business entities and identifiers (e.g., “legal entity,” “IBAN,” “LEI”).  
> - The **Verifiable Credential** format allows this information to be cryptographically signed  
>   and shared across systems or wallets with full traceability.

---

## 🧩 Example: Verifiable Credential (JSON-LD)

```json
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    {
      "xsd": "http://www.w3.org/2001/XMLSchema#",
      "ktddecv": "https://iri.suomi.fi/model/ktddecv/0.0.4/",
      "ncbv": "https://iri.suomi.fi/model/ncbv/0.0.5/"
    }
  ],
  "id": "urn:uuid:5c87e2d5-9e88-49ef-9a8d-bf9a7f7d3e61",
  "type": ["VerifiableCredential", "RequestToPayCredential"],
  "issuer": "did:lei:5493001KJTIIGC8Y1R12",
  "issuanceDate": "2025-10-16T10:00:00Z",
  "credentialSubject": {
    "@type": "ktddecv:RequestToPayDocument",
    "id": "urn:uuid:0fcd6112-9645-4403-9f72-bd1c3fd90b8e",
    "documentDate": "2025-10-16",
    "requestedExecutionDate": "2025-10-20",
    "expiryDate": "2025-10-30",
    "documentStatusCode": {
      "@type": "ncbv:Code",
      "codeName": "Pending",
      "schemeName": "SRTPDocumentStatusCode"
    },
    "creditor": {
      "@type": "ncbv:LegalEntity",
      "legalName": "Nordic Timber Export Ltd",
      "hasIdentifier": [
        { "@type": "ncbv:Identifier", "identifierValue": "FI1234567-8", "schemeName": "Finnish Business ID" },
        { "@type": "ncbv:Identifier", "identifierValue": "549300ABCDTIMERX1234", "schemeName": "LEI" }
      ],
      "postalAddress": {
        "@type": "ncbv:Address",
        "fullAddress": "Sahatien 10, FI-80100 Joensuu, Finland"
      }
    },
    "debtor": {
      "@type": "ncbv:LegalEntity",
      "legalName": "Tokyo Building Materials Co. Ltd",
      "hasIdentifier": {
        "@type": "ncbv:Identifier",
        "identifierValue": "JP987654321",
        "schemeName": "Japanese Corporate ID"
      },
      "postalAddress": {
        "@type": "ncbv:Address",
        "fullAddress": "2-3-12 Chuo, Tokyo 104-0031, Japan"
      }
    },
    "hasCreditorAccount": {
      "@type": "ktddecv:BankAccount",
      "bankAccountIdentifier": {
        "@type": "ncbv:Identifier",
        "identifierValue": "FI2112345600000785",
        "schemeName": "IBAN"
      }
    },
    "hasDebtorAccount": {
      "@type": "ktddecv:BankAccount",
      "bankAccountIdentifier": {
        "@type": "ncbv:Identifier",
        "identifierValue": "JP11TOKY00000123456",
        "schemeName": "IBAN"
      }
    },
    "creditorAgent": {
      "@type": "ktddecv:Bank",
      "hasIdentifier": {
        "@type": "ncbv:Identifier",
        "identifierValue": "NDEAFIHHXXX",
        "schemeName": "BIC"
      }
    },
    "debtorAgent": {
      "@type": "ktddecv:Bank",
      "hasIdentifier": {
        "@type": "ncbv:Identifier",
        "identifierValue": "SMBCJPJTXXX",
        "schemeName": "BIC"
      }
    },
    "ultimateCreditor": { "@type": "ncbv:LegalEntity", "legalName": "FinnForest Group Oy" },
    "ultimateDebtor": { "@type": "ncbv:LegalEntity", "legalName": "Tokyo Building Holdings K.K." },
    "hasAmount": {
      "@type": "ktddecv:Amount",
      "amountValue": "23800.00",
      "currencyCode": "EUR"
    },
    "paymentMethodCode": { "@type": "ncbv:Code", "codeName": "TRF", "schemeName": "ISO20022PaymentMethod" },
    "serviceLevelCode": { "@type": "ncbv:Code", "codeName": "SEPA", "schemeName": "ExternalServiceLevel1Code" },
    "localInstrumentCode": { "@type": "ncbv:Code", "codeName": "SRTP", "schemeName": "ExternalLocalInstrument1Code" },
    "paymentPurposeCode": { "@type": "ncbv:Code", "codeName": "GDDS", "schemeName": "ExternalPurpose1Code" },
    "paymentChargeBearerCode": { "@type": "ncbv:Code", "codeName": "SLEV", "schemeName": "ChargeBearerCode" },
    "remittanceText": "Invoice 2025/045 - Gluelam timber batch #JP-55",
    "hasRemittanceLocation": {
      "@type": "ncbv:ContactPoint",
      "contactPage": "https://nordictimber.fi/remittance/2025-045"
    }
  },
  "proof": {
    "type": "Ed25519Signature2020",
    "created": "2025-10-16T10:05:00Z",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "did:lei:5493001KJTIIGC8Y1R12#key-1",
    "jws": "eyJhbGciOiJFZERTQSJ9..."
  }
}
```

---

## 🗂️ How to read this example

| Section | Explanation |
|----------|--------------|
| **issuer** | The legal entity or wallet that issues the Request-to-Pay — identified by its LEI (Legal Entity Identifier). |
| **credentialSubject** | The actual Request-to-Pay information: amount, parties, payment codes, and references. |
| **hasAmount** | Combines value and currency in a single semantic object. |
| **requestedExecutionDate** | The date when payment execution is requested — this was a newly proposed KTDDE property. |
| **hasCreditorAccount / hasDebtorAccount** | Newly proposed object properties linking each party to their IBAN account. |
| **creditorAgent / debtorAgent** | Banks, identified through BIC (as `ncbv:Identifier` instances). |
| **ultimateCreditor / ultimateDebtor** | Optional “look-through” roles, common in ISO 20022 messages. |
| **remittanceText** | Free-form text visible to payer and payee, matching the “Ustrd” field in ISO 20022. |
| **hasRemittanceLocation** | Electronic address (URL) for structured remittance details. |
| **documentStatusCode** | Indicates lifecycle state — here, “Pending.” |

---

## 💡 Why this is important

This example demonstrates that **a Request-to-Pay message can be issued as a self-contained, verifiable digital document**:
- It can be **signed and validated** without relying on proprietary APIs.
- It can be **shared across wallets, banks, and public authorities** using the same semantic vocabulary.
- It ensures **interoperability** between business, banking, and regulatory ecosystems.

For non-experts, this means:
- **Less manual work** — payment requests can be automatically processed.  
- **Better transparency** — each data point (amount, payer, reference) is defined by shared EU/Nordic standards.  
- **Trustable automation** — AI agents or accounting systems can verify authenticity via the credential’s digital signature.

---

> 📎 *Next step:*  
> The same example can be presented as a **visual PDF certificate** for human users  
> (see the `RequestToPayCredential_HumanReadable.pdf` file).
