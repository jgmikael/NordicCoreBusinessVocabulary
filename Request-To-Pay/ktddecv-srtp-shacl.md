
> **What is this file?**  
> This document is designed for non-experts. It shows how a *SEPA Request‑to‑Pay* can be modelled using the **KTDDE (trade & payment documents)** and **NCBV (identities & codes)** vocabularies.  
> - **OWL** defines the *types* and *properties* that exist.  
> - **SHACL** sets *validation rules* (what is required/optional).  
> - **JSON‑LD @context** makes the data easy to use in *Verifiable Credentials*.


# KTDDE × SRTP — SHACL Shape for `ktddecv:RequestToPayDocument`

This SHACL shape constrains the **credential subject** for an SRTP Request-to-Pay when expressed with KTDDE/NCBV terms.  
Fields marked **PROPOSAL** correspond to properties/classes not present in your current vocabularies and should be added (or renamed) before strict validation is applied.

> Prefixes (adjust if needed): `ktddecv: https://iri.suomi.fi/model/ktddecv/0.0.4/`, `ncbv: https://iri.suomi.fi/model/ncbv/0.0.5/`

```turtle
@prefix sh:      <http://www.w3.org/ns/shacl#> .
@prefix xsd:     <http://www.w3.org/2001/XMLSchema#> .
@prefix ktddecv: <https://iri.suomi.fi/model/ktddecv/0.0.4/> .
@prefix ncbv:    <https://iri.suomi.fi/model/ncbv/0.0.5/> .

ktddecv:RequestToPayDocumentShape
    a sh:NodeShape ;
    sh:targetClass ktddecv:RequestToPayDocument ;

    # Parties
    sh:property [
        sh:path ktddecv:creditor ;
        sh:class ncbv:LegalEntity ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:debtor ;
        sh:class ncbv:LegalEntity ;
        sh:minCount 1 ;
    ] ;

    # Accounts (PROPOSAL properties)
    sh:property [
        sh:path ktddecv:hasCreditorAccount ;           # PROPOSAL
        sh:class ktddecv:BankAccount ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:hasDebtorAccount ;             # PROPOSAL
        sh:class ktddecv:BankAccount ;
        sh:minCount 0 ;
    ] ;

    # Agents
    sh:property [
        sh:path ktddecv:creditorAgent ;
        sh:class ktddecv:Bank ;
        sh:minCount 0 ;
    ] ;
    sh:property [
        sh:path ktddecv:debtorAgent ;
        sh:class ktddecv:Bank ;
        sh:minCount 0 ;
    ] ;

    # Optional look-through parties (PROPOSAL properties)
    sh:property [
        sh:path ktddecv:ultimateCreditor ;             # PROPOSAL
        sh:class ncbv:LegalEntity ;
        sh:maxCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:ultimateDebtor ;               # PROPOSAL
        sh:class ncbv:LegalEntity ;
        sh:maxCount 1 ;
    ] ;

    # Amount (as value object)
    sh:property [
        sh:path ktddecv:hasAmount ;
        sh:class ktddecv:Amount ;
        sh:minCount 1 ;
    ] ;

    # Codes (service level, local instrument, purpose, charge bearer)
    sh:property [
        sh:path ktddecv:paymentMethodCode ;            # PROPOSAL
        sh:class ncbv:Code ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:serviceLevelCode ;             # PROPOSAL (if not already present)
        sh:class ncbv:Code ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:localInstrumentCode ;          # PROPOSAL
        sh:class ncbv:Code ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:paymentPurposeCode ;           # PROPOSAL (if absent)
        sh:class ncbv:Code ;
        sh:minCount 0 ;
    ] ;
    sh:property [
        sh:path ktddecv:paymentChargeBearerCode ;      # PROPOSAL
        sh:class ncbv:Code ;
        sh:minCount 0 ;
    ] ;

    # Dates
    sh:property [
        sh:path ktddecv:documentDate ;
        sh:datatype xsd:date ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:requestedExecutionDate ;       # PROPOSAL
        sh:datatype xsd:date ;
        sh:minCount 1 ;
    ] ;
    sh:property [
        sh:path ktddecv:expiryDate ;
        sh:datatype xsd:date ;
        sh:minCount 0 ;
    ] ;

    # Remittance
    sh:property [
        sh:path ktddecv:remittanceText ;               # PROPOSAL
        sh:datatype xsd:string ;
        sh:minCount 0 ;
        sh:maxLength 140 ;
    ] ;
    sh:property [
        sh:path ktddecv:hasRemittanceLocation ;        # PROPOSAL
        sh:class ncbv:ContactPoint ;
        sh:minCount 0 ;
    ] ;

    # Lifecycle status (code)
    sh:property [
        sh:path ktddecv:documentStatusCode ;           # PROPOSAL
        sh:class ncbv:Code ;
        sh:minCount 0 ;
    ] .
```
