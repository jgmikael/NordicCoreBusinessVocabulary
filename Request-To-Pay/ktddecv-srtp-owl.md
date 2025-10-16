
> **What is this file?**  
> This document is designed for non-experts. It shows how a *SEPA Request‑to‑Pay* can be modelled using the **KTDDE (trade & payment documents)** and **NCBV (identities & codes)** vocabularies.  
> - **OWL** defines the *types* and *properties* that exist.  
> - **SHACL** sets *validation rules* (what is required/optional).  
> - **JSON‑LD @context** makes the data easy to use in *Verifiable Credentials*.


# KTDDE × SRTP — OWL snippet (with explicit **PROPOSAL** markers)

This snippet introduces **`ktddecv:RequestToPayDocument`** as a subclass of `ktddecv:FinancialDocument` and reuses existing terms from **KTDDE** and **NCBV** wherever possible.  
Any **new** terms that are **not** present in your current KTDDE/NCBV are marked with **`# PROPOSAL`** comments next to their declarations and uses.

> Prefixes used (adjust if your canonical URIs differ):
> - `@prefix ktddecv: <https://iri.suomi.fi/model/ktddecv/0.0.4/> .`
> - `@prefix ncbv:   <https://iri.suomi.fi/model/ncbv/0.0.5/> .`
> - `@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .`
> - `@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .`
> - `@prefix owl:    <http://www.w3.org/2002/07/owl#> .`

```turtle
@prefix ktddecv: <https://iri.suomi.fi/model/ktddecv/0.0.4/> .
@prefix ncbv:   <https://iri.suomi.fi/model/ncbv/0.0.5/> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix owl:    <http://www.w3.org/2002/07/owl#> .

#################################################################
# Classes
#################################################################

# Existing (assumed in KTDDE Core Vocabulary)
ktddecv:FinancialDocument a owl:Class .

# New document class for SEPA Request-to-Pay
ktddecv:RequestToPayDocument a owl:Class ;
  rdfs:subClassOf ktddecv:FinancialDocument ;
  rdfs:label "Request to Pay Document"@en ;
  rdfs:comment "A business document by which a creditor requests a debtor to execute a SEPA payment in response to an underlying commercial transaction."@en .

#################################################################
# Object properties (reuse where available; mark new)
#################################################################

# Link to the creditor and debtor (reuse existing party-role relations if already present)
ktddecv:creditor a owl:ObjectProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:LegalEntity ;
  rdfs:label "creditor"@en .

ktddecv:debtor a owl:ObjectProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:LegalEntity ;
  rdfs:label "debtor"@en .

# PROPOSAL: explicit links from the RTP doc to the *accounts* used by each party
ktddecv:hasCreditorAccount a owl:ObjectProperty ;                  # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ktddecv:BankAccount ;
  rdfs:label "has creditor account"@en ;
  rdfs:comment "Links the RequestToPayDocument to the creditor’s receiving account (e.g., IBAN)."@en .

ktddecv:hasDebtorAccount a owl:ObjectProperty ;                    # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ktddecv:BankAccount ;
  rdfs:label "has debtor account"@en ;
  rdfs:comment "Links the RequestToPayDocument to the debtor’s paying account (e.g., IBAN or proxy account)."@en .

# Financial institutions (agents); identified via ncbv:Identifier (schemeName "BIC", "LEI" ...)
ktddecv:creditorAgent a owl:ObjectProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ktddecv:Bank ;
  rdfs:label "creditor agent"@en .

ktddecv:debtorAgent a owl:ObjectProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ktddecv:Bank ;
  rdfs:label "debtor agent"@en .

# Optional "look-through" parties (ISO 20022 UltmtCdtr / UltmtDbtr)
ktddecv:ultimateCreditor a owl:ObjectProperty ;                    # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:LegalEntity ;
  rdfs:label "ultimate creditor"@en .

ktddecv:ultimateDebtor a owl:ObjectProperty ;                      # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:LegalEntity ;
  rdfs:label "ultimate debtor"@en .

# Remittance location (URL/email) as a contact point
ktddecv:hasRemittanceLocation a owl:ObjectProperty ;               # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:ContactPoint ;
  rdfs:label "has remittance location"@en ;
  rdfs:comment "Electronic address (e.g., URL or email) where additional remittance details are available."@en .

#################################################################
# Datatype properties (reuse where available; mark new)
#################################################################

# Amount as a value object (KTDDE)
ktddecv:hasAmount a owl:ObjectProperty ;                           
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ktddecv:Amount ;
  rdfs:label "has amount"@en .

# Payment method and type (codes)
ktddecv:paymentMethodCode a owl:ObjectProperty ;                   # PROPOSAL (range a code concept)
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "payment method code"@en .

ktddecv:serviceLevelCode a owl:ObjectProperty ;                    # PROPOSAL (or reuse existing if present)
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "service level code"@en .

ktddecv:localInstrumentCode a owl:ObjectProperty ;                 # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "local instrument code"@en .

ktddecv:paymentPurposeCode a owl:ObjectProperty ;                  # if not present, treat as PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "payment purpose code"@en .

ktddecv:paymentChargeBearerCode a owl:ObjectProperty ;             # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "payment charge bearer code"@en .

# Dates
ktddecv:documentDate a owl:DatatypeProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  xsd:date ;
  rdfs:label "document date"@en .

ktddecv:requestedExecutionDate a owl:DatatypeProperty ;            # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  xsd:date ;
  rdfs:label "requested execution date"@en .

ktddecv:expiryDate a owl:DatatypeProperty ;
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  xsd:date ;
  rdfs:label "expiry date"@en .

# Free-text remittance line (ISO 20022 <Ustrd>)
ktddecv:remittanceText a owl:DatatypeProperty ;                    # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  xsd:string ;
  rdfs:label "remittance text"@en .

# Document lifecycle (Accepted/Rejected/Pending... as code)
ktddecv:documentStatusCode a owl:ObjectProperty ;                  # PROPOSAL
  rdfs:domain ktddecv:RequestToPayDocument ;
  rdfs:range  ncbv:Code ;
  rdfs:label "document status code"@en .
```
