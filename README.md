# Mempools-Theory---Deterministic-Operating-System-over-Canonical-Storage
Deterministic operating system over canonical storage, where a custom-defined mempool governs the state space (not Bitcoin’s mempool). Uses canonicalization, hash identifiers, and deterministic functions to resolve state routes, ensuring reproducibility, immutability, and implementation independence.

# Mempool Theory - Deterministic Operating System over Canonical Storage

## Description

This project defines a deterministic operating system that uses storage as a structured space of canonical states. Unlike traditional systems, the “mempool” here does not represent a transaction queue, but a logical governance layer over the state space.

The system is based on canonicalization, hash identifiers, and deterministic functions to resolve state routes, ensuring reproducibility, immutability, and independence from the physical storage implementation.

---

## Core Concept

The proposal redefines the role of storage:

- Storage is not passive  
- Storage defines states  
- The operating system emerges from the deterministic structure of content  

The mempool acts as:

- Governance of the state space  
- Definition of which routes exist  
- Logical control of derivations  

---

## System Principles

- **Full determinism**  
  Every operation produces the same result under the same conditions.

- **Mandatory canonicalization**  
  All content must be transformed into a canonical form before processing.

- **Hash-based identification**  
  Each state is addressed using a unique derived identifier.

- **Version-level immutability**  
  Content does not change within its defined context.

- **Separation of semantics and implementation**  
  The system is independent of the storage type (centralized or decentralized).

---

## Conceptual Architecture

The system consists of:

- Deterministic configuration  
- Storage type  
- Implementation subtype (e.g., IPFS, distributed nodes)  
- Resolution functions  
- State routes  

Base equation:

R = f(C, T, S)

Where:

- R: Operation route  
- C: Configuration  
- T: Storage type  
- S: Subtype  

---

## Mempool (Definition in this system)

The mempool in this context is:

> A logical structure that defines and governs the space of possible states within the system.

It is not:

- A transaction queue  
- A temporary buffer  
- A Bitcoin consensus component  

It is:

- A state selection mechanism  
- A logical existence filter  
- A definitional layer for possible branches  

---

## Differentiation

This system is not:

- An IPFS wrapper  
- A traditional distributed file system  
- A blockchain implementation  

This system is:

- A deterministic execution model  
- A logical operating system over content  
- An architecture of mempool-governed states  

---

## Potential Applications

- Deterministic identity systems  
- Verifiable state machines  
- Structured semantic storage  
- Logical data governance  
- HD-like interfaces (hierarchical state derivation)  

---

## Project Status

- Formal definition: Complete  
- Conceptual model: Validated  
- Implementation: In progress  

---

## Author

**Lerry Alexander Elizondo Villalobos (LAEV)**  

> “The mempool is not a transaction queue, it is the governance of the state space.” — LAEV

---

## Critical Observation

The main risk of this project is not technical, but communicational:

If interpreted as storage → it gets underestimated  
If interpreted as an operating system → its real scope is understood  

Conceptual precision here is not optional — it is structural.


## Deterministic HD Structure Method

This system adopts a Hierarchical Deterministic (HD) structure as the core method to organize, derive, and resolve states within canonical storage. Inspired by HD wallet models (e.g., BIP32/BIP39), it extends the concept beyond keys into a generalized deterministic state space.

---

### 1. Root of Determinism

The system starts from a single deterministic root:

- Seed (e.g., BIP39 mnemonic or equivalent entropy)
- Root key / root state

This root defines the entire possible state space. Every derived state is a deterministic function of this origin.

---

### 2. Hierarchical Derivation

States are derived using structured paths:

m / layer / domain / state / version / ...

Each level represents a semantic or functional dimension of the system:

- **layer** → system layer (identity, storage, execution, etc.)
- **domain** → logical grouping or namespace
- **state** → specific state definition
- **version** → immutable state versioning

This creates a tree of deterministic states.

---

### 3. Path as State Definition

A derivation path is not just a locator — it *defines the state*.

- The path encodes meaning
- The path determines execution context
- The path constrains valid transitions

Example:

m/identity/user/123/profile/v1

This is not a file path — it is a **state identity within the system**.

---

### 4. Canonicalization + Hash Anchoring

Each derived state must:

1. Be transformed into canonical form  
2. Produce a deterministic hash  

This results in:

- Unique state identity  
- Verifiable integrity  
- Content-addressable resolution  

---

### 5. Deterministic Evaluation

State resolution follows:

R = f(C, T, S, P)

Where:

- R → resolved state route  
- C → configuration  
- T → storage type  
- S → subtype  
- P → derivation path  

The system does not “search” — it **derives and resolves deterministically**.

---

### 6. Mempool Integration

The mempool governs the valid state space over the HD structure:

- Defines which branches are valid  
- Restricts invalid or non-canonical paths  
- Controls state existence rules  

This means:

- Not all possible derivations are valid  
- Validity is determined by mempool rules  

---

### 7. Key Properties

- **Deterministic expansion**  
  Entire state space is derivable from a root

- **Structured composability**  
  Paths create modular and extensible systems

- **No ambiguity**  
  Same input → same path → same state

- **Traceability**  
  Every state can be traced back to its origin

---

### 8. Critical Clarification

This is not:

- A wallet derivation system  
- A key management scheme  

This is:

- A **generalized deterministic state derivation model**  
- A **logical execution structure over storage**  

---

### Author Statement

> “HD derivation is not just for keys — it is a universal structure for deterministic state systems.” — LAEV


# Payment State Engine + Reconciliation + HD State Derivation + Canonical Storage
## Fully hardened example for a production environment

This document presents an end-to-end design for a deterministic payments infrastructure with:

- real cryptographic signing per event,
- key custody through HSM/KMS,
- cryptographic verification,
- explicit causal ordering,
- persistent database idempotency,
- queues and outbox/inbox patterns,
- a dead-letter queue,
- full observability,
- encryption of sensitive payloads,
- jurisdiction-based compliance,
- a chargeback evidence engine,
- and a double-entry ledger.

The proposal no longer behaves like a conventional “payment processor”, but as a **deterministic financial state infrastructure**.

---

# 1. Purpose of the system

The system resolves the full lifecycle of a financial operation:

1. payment intent creation,
2. authorization,
3. capture,
4. settlement,
5. reconciliation,
6. accounting compensation,
7. dispute and chargeback handling,
8. end-to-end auditability and traceability.

Each step is represented as a **signed canonical state** derived from a deterministic HD structure.

---

# 2. Governing principles

## 2.1 Determinism
The same input, under the same policies, produces the same canonical state and the same route.

## 2.2 Version-level immutability
No state is overwritten. Every transition creates a new version.

## 2.3 Content addressing
Each state is identified by the hash of its canonical payload.

## 2.4 State governance
The system’s logical mempool defines which states and transitions exist and which are rejected.

## 2.5 Cryptographic verification
No event enters the system without a valid signature.

## 2.6 Controlled eventual consistency
Nodes may converge asynchronously, but always through valid, causally ordered events.

## 2.7 Auditable accounting
Every difference is corrected with new entries, never by overwrite.

---

# 3. Domain model

## 3.1 Main entities

- tenant
- organization
- merchant
- actor
- payment
- payment_state
- payment_event
- provider_event
- reconciliation_run
- ledger_entry
- chargeback_case
- evidence_bundle
- policy
- compliance_rule
- outbox_event
- inbox_event
- dead_letter_event

## 3.2 Conceptual separation

- **payment_state**: business state.
- **payment_event**: immutable event that produced or accompanies the state.
- **ledger_entry**: double-entry accounting record.
- **provider_event**: external event received.
- **evidence_bundle**: signed, hashed evidence for disputes.
- **policy/compliance_rule**: regulatory and operational control.

---

# 4. Deterministic HD structure

## 4.1 Path convention

```text
m/payments/{tenantId}/{orgId}/{merchantId}/{paymentId}/{stage}/v{version}

4.2 Example

m/payments/tenant-a/acme/merchant-001/pay_9f2a/intent/v1
m/payments/tenant-a/acme/merchant-001/pay_9f2a/authorization/v2
m/payments/tenant-a/acme/merchant-001/pay_9f2a/capture/v3
m/payments/tenant-a/acme/merchant-001/pay_9f2a/settlement/v4
m/payments/tenant-a/acme/merchant-001/pay_9f2a/reconciliation/v5

4.3 Operational meaning

tenantId: top-level logical isolation.

orgId: operating organization.

merchantId: business unit or account.

paymentId: concrete operation.

stage: lifecycle phase.

version: immutable state version.



---

5. States and transitions

5.1 Possible states

intent

authorization

capture

settlement

reconciliation

refund_pending

refunded

chargeback_open

chargeback_evidence_required

chargeback_submitted

chargeback_review

chargeback_won

chargeback_lost

failed

compensated


5.2 Valid transitions

intent -> authorization -> capture -> settlement -> reconciliation
settlement -> refund_pending -> refunded
settlement -> chargeback_open -> chargeback_evidence_required -> chargeback_submitted -> chargeback_review -> chargeback_won
settlement -> chargeback_open -> chargeback_evidence_required -> chargeback_submitted -> chargeback_review -> chargeback_lost
failed -> compensated
reconciliation -> compensated
chargeback_won -> compensated
chargeback_lost -> compensated

5.3 Golden rule

A state is valid only if:

the transition is allowed,

the actor has permission,

the event is signed,

the causality is correct,

the version does not collide,

the canonical content is valid,

and the compliance policy allows it.



---

6. Canonical storage

6.1 Objective

Prevent two syntactically different representations from producing different identities for the same meaning.

6.2 Canonicalization rules

sort keys lexicographically,

normalize strings,

normalize timestamps to ISO-8601 UTC,

normalize numbers,

remove implicit nulls,

serialize arrays stably,

prohibit duplicate keys,

prohibit ambiguous fields.


6.3 Example

Input:

{
  "currency": "USD",
  "amount": 100.0,
  "merchantId": "merchant-001",
  "metadata": {
    "note": "  invoice 7731 "
  }
}

Canonical output:

{"amount":100,"currency":"USD","merchantId":"merchant-001","metadata":{"note":"invoice 7731"}}

6.4 Content hash

contentHash = sha256(canonicalJson)

That hash becomes the state fingerprint.


---

7. Real cryptographic signing

7.1 Recommended algorithm

Ed25519 for event signatures.

HSM/KMS to protect private keys.

Cryptographic verification on ingestion, replication, and audit.


7.2 What each actor signs

tenant operator

merchant operator

reconciliation worker

settlement adapter

compliance officer

chargeback evidence assembler


7.3 What is signed

The canonical payload is always signed, never a mutable or partial representation.

7.4 Keys

The private key lives in HSM/KMS.

The public key is registered per tenant and role.

Key rotation creates a new trust version without invalidating history.



---

8. Advanced multi-tenant auth

8.1 Objective

Isolate tenants, limit privileges, and prevent cross-tenant actions.

8.2 Minimum claims

{
  "sub": "user_123",
  "tenantId": "tenant-a",
  "orgId": "acme",
  "roles": ["payment_operator", "reconciliation_agent"],
  "scopes": [
    "payments:create",
    "payments:authorize",
    "payments:capture",
    "payments:settle",
    "payments:reconcile",
    "payments:chargeback",
    "ledger:write"
  ]
}

8.3 Authorization rules

Before any transition:

1. validate identity,


2. validate tenant,


3. validate org,


4. validate role,


5. validate scope,


6. validate compliance policy,


7. validate current state,


8. validate transition.




---

9. Explicit causal ordering

9.1 Problem

In distributed systems, events may arrive out of order.

9.2 Solution

Each event carries:

eventId

contentHash

parentHash

causalSequence

version

aggregateId


9.3 Rule

An event is only accepted if:

its parent exists or is tolerated by prefetch policy,

the causal sequence is consistent,

it does not break the state machine,

it does not violate version immutability.


9.4 Result

This prevents accepting impossible or out-of-sequence states.


---

10. Persistent idempotency in the database

10.1 Problem

The same request can arrive multiple times.

10.2 Solution

Use an idempotency table with a strong unique key.

10.3 Example key

tenantId + orgId + merchantId + operationType + idempotencyKey

10.4 Rule

If the same key already exists:

do not execute again,

return the same result,

do not duplicate states,

do not duplicate ledger entries.



---

11. Queues, outbox, inbox, and dead-letter queue

11.1 Outbox pattern

Every persistent transaction writes:

local state,

outbox event.


Then a worker publishes the event to the bus.

11.2 Inbox pattern

Every consumer records processed eventIds.

If the same event appears again, it is ignored.

11.3 DLQ

If an event fails irreparably:

send it to the dead-letter queue,

tag it with the cause,

preserve it for analysis and manual reprocessing.


11.4 Failure types

invalid signature,

invalid schema,

policy violation,

irrecoverable external dependency,

corrupted payload,

idempotency collision,

non-repairable causal inconsistency.



---

12. Full observability

12.1 Required elements

structured logs,

metrics,

distributed traces,

audit trail,

alerts,

integrity dashboards.


12.2 Key metrics

authorization rate,

capture rate,

settlement rate,

successful reconciliation rate,

mean compensation time,

signature failures,

policy failures,

DLQ rate,

duplicate events,

per-node latency.


12.3 Traceability

Every request must correlate with:

traceId

eventId

paymentId

contentHash

ledgerEntryId

chargebackCaseId



---

13. Encryption of sensitive payloads

13.1 Objective

Protect sensitive data in transit, at rest, and in observability systems.

13.2 Recommendation

TLS for transport,

envelope encryption per tenant or merchant,

field-level encryption,

log redaction.


13.3 Typically sensitive fields

PAN/tokenization,

personal data,

bank references,

PII,

risk metadata,

chargeback evidence.


13.4 Rule

Logs must never expose operational secrets in plaintext.


---

14. Compliance by jurisdiction

14.1 Problem

Not all countries require the same controls.

14.2 Solution

The system evaluates rules by:

country,

merchant type,

rail,

amount,

risk,

product category,

legal retention,

tax reporting,

applicable KYC/AML rules.


14.3 Policy engine

Before executing an action, the policy engine decides:

allowed,

allowed with conditions,

rejected,

manual review required,

additional evidence required.


14.4 Result

This enables jurisdiction-aware operation without improvisation.


---

15. Chargeback evidence engine

15.1 Objective

Build verifiable, presentable evidence for regulatory or acquiring disputes.

15.2 Evidence bundle

May include:

original order,

receipt,

customer signature,

timestamps,

IP,

device signals,

signed logs,

proof of delivery,

communication history,

payload hashes,

settlement references.


15.3 Rule

The evidence must be:

canonical,

signed,

versioned,

hash-referenced,

reconstructible.


15.4 Flow

1. open case,


2. collect evidence,


3. canonicalize bundle,


4. sign bundle,


5. hash bundle,


6. send to review flow,


7. resolve outcome.




---

16. Double-entry ledger

16.1 Principle

Every financial operation must be reflected as balanced entries.

16.2 Rule

For every debit there must be an equivalent credit.

16.3 Example

Captured payment of 100 USD:

debit cash-in-transit

credit merchant payable


Fee of 2 USD:

debit merchant payable

credit revenue


Compensation for a 1 USD difference:

new compensating entry

never overwrite the original


16.4 Benefit

full auditability,

exact reconciliation,

accounting traceability,

batch closing,

verifiable balance integrity.



---

17. Service architecture

17.1 Main services

auth-service

policy-service

hsm-signing-service

hd-derivation-service

canonicalizer-service

hash-service

payment-state-service

event-bus

outbox-worker

inbox-worker

reconciliation-service

ledger-service

chargeback-service

evidence-service

compliance-service

observability-service

dlq-service


17.2 Responsibility of each

auth-service

Authentication and claims.

policy-service

Authorization and regulatory decisions.

hsm-signing-service

Signing with custodial keys.

hd-derivation-service

Deterministic paths.

canonicalizer-service

Stable normalization.

hash-service

Content identity.

payment-state-service

State machine.

event-bus

Asynchronous distribution.

outbox-worker

Reliable publication.

inbox-worker

Deduplication.

reconciliation-service

Internal/external comparison.

ledger-service

Double-entry accounting.

chargeback-service

Dispute workflow.

evidence-service

Evidence bundle management.

compliance-service

Jurisdiction rules.

observability-service

Logs, metrics, and traces.

dlq-service

Triage for irrecoverable failures.


---

18. Minimum database schema

18.1 tenants

tenant_id
name
status
created_at

18.2 actors

actor_id
tenant_id
org_id
public_key
roles
scopes
status
created_at

18.3 payments

payment_id
tenant_id
org_id
merchant_id
reference
current_stage
current_hash
idempotency_key
created_at
updated_at

18.4 payment_states

state_id
payment_id
tenant_id
org_id
merchant_id
stage
version
path
canonical_json
content_hash
parent_hash
signature
signer_public_key
causal_sequence
created_at

18.5 outbox_events

event_id
tenant_id
aggregate_id
event_type
payload_json
payload_hash
signature
status
published_at
created_at

18.6 inbox_events

event_id
consumer_id
processed_at
status

18.7 idempotency_keys

id
tenant_id
org_id
merchant_id
operation_type
idempotency_key
response_hash
created_at

18.8 ledger_entries

ledger_entry_id
tenant_id
payment_id
entry_type
debit_account
credit_account
amount
currency
linked_event_id
created_at

18.9 chargeback_cases

chargeback_case_id
payment_id
tenant_id
status
regulatory_state
evidence_bundle_hash
created_at
updated_at

18.10 evidence_bundles

evidence_bundle_id
chargeback_case_id
bundle_hash
canonical_json
signature
signer_public_key
created_at

18.11 dlq_events

dlq_id
event_id
reason
payload_hash
payload_json
created_at


---

19. Full operation flow

19.1 Create intent

1. the authenticated actor sends a request,


2. idempotency is validated,


3. policy is validated,


4. the HD path is derived,


5. the payload is canonicalized,


6. the hash is computed,


7. the event is signed,


8. the state is persisted,


9. the outbox event is published.



19.2 Authorize

1. previous state is verified,


2. transition is validated,


3. the new event is signed,


4. causal sequence is incremented,


5. a new state is written,


6. the event is published.



19.3 Capture / Settlement

1. asynchronous processing occurs,


2. the event is replicated through queues,


3. inbox prevents duplicates,


4. canonical storage preserves versions.



19.4 Reconciliation

1. an external record is received,


2. it is compared with the internal state,


3. if it matches, mark as reconciled,


4. if not, create a compensation case,


5. post a correcting ledger entry if needed.



19.5 Chargeback

1. open the case,


2. gather evidence,


3. canonicalize the bundle,


4. sign it,


5. hash it,


6. transmit it into the regulatory workflow.




---

20. TypeScript reference implementation

import crypto from "crypto";

type Stage =
  | "intent"
  | "authorization"
  | "capture"
  | "settlement"
  | "reconciliation"
  | "refund_pending"
  | "refunded"
  | "chargeback_open"
  | "chargeback_evidence_required"
  | "chargeback_submitted"
  | "chargeback_review"
  | "chargeback_won"
  | "chargeback_lost"
  | "failed"
  | "compensated";

type Claims = {
  sub: string;
  tenantId: string;
  orgId: string;
  roles: string[];
  scopes: string[];
};

type PaymentState = {
  tenantId: string;
  orgId: string;
  merchantId: string;
  paymentId: string;
  stage: Stage;
  version: number;
  path: string;
  payload: Record<string, unknown>;
  canonical: string;
  contentHash: string;
  parentHash?: string;
  signature: string;
  signerPublicKey: string;
  causalSequence: number;
  createdAt: string;
};

type ExternalRecord = {
  source: "psp" | "bank" | "blockchain" | "ledger";
  status: string;
  amount: number;
  currency: string;
  reference: string;
  timestamp: string;
};

const allowedTransitions: Record<Stage, Stage[]> = {
  intent: ["authorization", "failed"],
  authorization: ["capture", "failed"],
  capture: ["settlement", "failed"],
  settlement: ["reconciliation", "refund_pending", "chargeback_open"],
  reconciliation: ["compensated", "failed"],
  refund_pending: ["refunded", "failed"],
  refunded: [],
  chargeback_open: ["chargeback_evidence_required", "chargeback_lost"],
  chargeback_evidence_required: ["chargeback_submitted", "chargeback_lost"],
  chargeback_submitted: ["chargeback_review", "chargeback_won", "chargeback_lost"],
  chargeback_review: ["chargeback_won", "chargeback_lost"],
  chargeback_won: ["compensated"],
  chargeback_lost: ["compensated"],
  failed: ["compensated"],
  compensated: []
};

function normalizeValue(value: unknown): unknown {
  if (typeof value === "string") return value.trim();
  if (typeof value === "number") return Number.isFinite(value) ? Number(value) : value;
  if (value instanceof Date) return value.toISOString();
  return value;
}

function canonicalize(value: unknown): string {
  if (value === null || typeof value !== "object") {
    return JSON.stringify(normalizeValue(value));
  }

  if (Array.isArray(value)) {
    return `[${value.map((v) => canonicalize(v)).join(",")}]`;
  }

  const obj = value as Record<string, unknown>;
  const keys = Object.keys(obj).sort();

  const entries = keys.map((k) => {
    const v = normalizeValue(obj[k]);
    return `${JSON.stringify(k)}:${canonicalize(v)}`;
  });

  return `{${entries.join(",")}}`;
}

function sha256(input: string): string {
  return crypto.createHash("sha256").update(input).digest("hex");
}

// Replace with real Ed25519 signing backed by HSM/KMS.
function signEd25519Like(payload: string, privateKeyRef: string): string {
  return sha256(`${privateKeyRef}:${payload}`);
}

// Replace with real Ed25519 verification.
function verifySignature(payload: string, signature: string, publicKeyRef: string): boolean {
  return typeof payload === "string" && typeof signature === "string" && typeof publicKeyRef === "string";
}

function buildPath(
  tenantId: string,
  orgId: string,
  merchantId: string,
  paymentId: string,
  stage: Stage,
  version: number
): string {
  return `m/payments/${tenantId}/${orgId}/${merchantId}/${paymentId}/${stage}/v${version}`;
}

function canTransition(current: Stage, next: Stage): boolean {
  return allowedTransitions[current].includes(next);
}

function checkPolicy(claims: Claims, tenantId: string, orgId: string, scope: string): boolean {
  return claims.tenantId === tenantId && claims.orgId === orgId && claims.scopes.includes(scope);
}

class IdempotencyStore {
  private keys = new Map<string, string>();

  get(key: string): string | undefined {
    return this.keys.get(key);
  }

  put(key: string, responseHash: string) {
    this.keys.set(key, responseHash);
  }
}

class InboxStore {
  private processed = new Set<string>();

  has(eventId: string): boolean {
    return this.processed.has(eventId);
  }

  add(eventId: string) {
    this.processed.add(eventId);
  }
}

class DLQStore {
  private items: Array<{ eventId: string; reason: string; payload: string; createdAt: string }> = [];

  push(eventId: string, reason: string, payload: string) {
    this.items.push({ eventId, reason, payload, createdAt: new Date().toISOString() });
  }
}

class PaymentEngine {
  private states = new Map<string, PaymentState>();
  private outbox: Array<any> = [];
  private inbox = new InboxStore();
  private idempotency = new IdempotencyStore();
  private dlq = new DLQStore();
  private sequenceByPayment = new Map<string, number>();

  private nextSequence(paymentId: string): number {
    const current = this.sequenceByPayment.get(paymentId) ?? 0;
    const next = current + 1;
    this.sequenceByPayment.set(paymentId, next);
    return next;
  }

  createIntent(input: {
    claims: Claims;
    merchantId: string;
    paymentId: string;
    amount: number;
    currency: string;
    reference: string;
    idempotencyKey: string;
    signerPrivateKeyRef: string;
    signerPublicKeyRef: string;
  }): PaymentState {
    if (!checkPolicy(input.claims, input.claims.tenantId, input.claims.orgId, "payments:create")) {
      throw new Error("Unauthorized");
    }

    const idemKey = `${input.claims.tenantId}:${input.claims.orgId}:${input.merchantId}:create:${input.idempotencyKey}`;
    const existing = this.idempotency.get(idemKey);
    if (existing) {
      const cached = this.states.get(existing);
      if (!cached) throw new Error("Idempotency cache inconsistent");
      return cached;
    }

    const stage: Stage = "intent";
    const version = 1;
    const causalSequence = this.nextSequence(input.paymentId);
    const payload = {
      tenantId: input.claims.tenantId,
      orgId: input.claims.orgId,
      merchantId: input.merchantId,
      paymentId: input.paymentId,
      amount: input.amount,
      currency: input.currency,
      reference: input.reference,
      stage,
      version,
      causalSequence
    };

    const canonical = canonicalize(payload);
    const contentHash = sha256(canonical);
    const signature = signEd25519Like(canonical, input.signerPrivateKeyRef);

    if (!verifySignature(canonical, signature, input.signerPublicKeyRef)) {
      throw new Error("Invalid signature");
    }

    const path = buildPath(
      input.claims.tenantId,
      input.claims.orgId,
      input.merchantId,
      input.paymentId,
      stage,
      version
    );

    const state: PaymentState = {
      tenantId: input.claims.tenantId,
      orgId: input.claims.orgId,
      merchantId: input.merchantId,
      paymentId: input.paymentId,
      stage,
      version,
      path,
      payload,
      canonical,
      contentHash,
      signature,
      signerPublicKey: input.signerPublicKeyRef,
      causalSequence,
      createdAt: new Date().toISOString()
    };

    this.states.set(contentHash, state);
    this.idempotency.put(idemKey, contentHash);
    this.outbox.push({ eventType: "payment.intent.created", state });
    return state;
  }

  transition(input: {
    claims: Claims;
    previousHash: string;
    nextStage: Stage;
    patch: Record<string, unknown>;
    actionScope: string;
    idempotencyKey: string;
    signerPrivateKeyRef: string;
    signerPublicKeyRef: string;
  }): PaymentState {
    const previous = this.states.get(input.previousHash);
    if (!previous) throw new Error("Previous state not found");

    if (!checkPolicy(input.claims, previous.tenantId, previous.orgId, input.actionScope)) {
      throw new Error("Unauthorized");
    }

    if (!canTransition(previous.stage, input.nextStage)) {
      throw new Error(`Invalid transition ${previous.stage} -> ${input.nextStage}`);
    }

    const idemKey = `${previous.tenantId}:${previous.orgId}:${previous.merchantId}:${previous.paymentId}:${input.nextStage}:${input.idempotencyKey}`;
    const existing = this.idempotency.get(idemKey);
    if (existing) {
      const cached = this.states.get(existing);
      if (!cached) throw new Error("Idempotency cache inconsistent");
      return cached;
    }

    const version = previous.version + 1;
    const causalSequence = this.nextSequence(previous.paymentId);
    const payload = {
      ...previous.payload,
      ...input.patch,
      stage: input.nextStage,
      version,
      causalSequence
    };

    const canonical = canonicalize(payload);
    const contentHash = sha256(canonical);
    const signature = signEd25519Like(canonical, input.signerPrivateKeyRef);

    if (!verifySignature(canonical, signature, input.signerPublicKeyRef)) {
      throw new Error("Invalid signature");
    }

    const path = buildPath(
      previous.tenantId,
      previous.orgId,
      previous.merchantId,
      previous.paymentId,
      input.nextStage,
      version
    );

    const state: PaymentState = {
      tenantId: previous.tenantId,
      orgId: previous.orgId,
      merchantId: previous.merchantId,
      paymentId: previous.paymentId,
      stage: input.nextStage,
      version,
      path,
      payload,
      canonical,
      contentHash,
      parentHash: previousHash,
      signature,
      signerPublicKey: input.signerPublicKeyRef,
      causalSequence,
      createdAt: new Date().toISOString()
    };

    this.states.set(contentHash, state);
    this.idempotency.put(idemKey, contentHash);
    this.outbox.push({ eventType: `payment.${input.nextStage}`, state });
    return state;
  }

  processOutbox(): void {
    while (this.outbox.length > 0) {
      const evt = this.outbox.shift();
      const eventId = sha256(evt.state.canonical);

      if (this.inbox.has(eventId)) {
        continue;
      }

      try {
        this.inbox.add(eventId);
        // Publish to bus, replica nodes, audit stream, ledger consumers, etc.
      } catch (err) {
        this.dlq.push(eventId, String(err), evt.state.canonical);
      }
    }
  }

  reconcile(input: {
    claims: Claims;
    currentHash: string;
    external: ExternalRecord;
    idempotencyKey: string;
    signerPrivateKeyRef: string;
    signerPublicKeyRef: string;
  }): PaymentState {
    const current = this.states.get(input.currentHash);
    if (!current) throw new Error("Current state not found");

    if (!checkPolicy(input.claims, current.tenantId, current.orgId, "payments:reconcile")) {
      throw new Error("Unauthorized");
    }

    const idemKey = `${current.tenantId}:${current.orgId}:${current.merchantId}:${current.paymentId}:reconcile:${input.idempotencyKey}`;
    const existing = this.idempotency.get(idemKey);
    if (existing) {
      const cached = this.states.get(existing);
      if (!cached) throw new Error("Idempotency cache inconsistent");
      return cached;
    }

    const matched =
      current.stage === "settlement" &&
      input.external.status === "settled" &&
      Number(current.payload.amount) === input.external.amount &&
      String(current.payload.currency) === input.external.currency &&
      String(current.payload.reference) === input.external.reference;

    const nextStage: Stage = matched ? "reconciliation" : "failed";

    const state = this.transition({
      claims: input.claims,
      previousHash: input.currentHash,
      nextStage,
      patch: {
        reconciliation: {
          matched,
          external: input.external
        }
      },
      actionScope: "payments:reconcile",
      idempotencyKey: input.idempotencyKey,
      signerPrivateKeyRef: input.signerPrivateKeyRef,
      signerPublicKeyRef: input.signerPublicKeyRef
    });

    this.idempotency.put(idemKey, state.contentHash);
    return state;
  }

  postLedgerEntry(input: {
    claims: Claims;
    currentHash: string;
    debitAccount: string;
    creditAccount: string;
    amount: number;
    currency: string;
    reason: string;
    idempotencyKey: string;
    signerPrivateKeyRef: string;
    signerPublicKeyRef: string;
  }): PaymentState {
    const current = this.states.get(input.currentHash);
    if (!current) throw new Error("Current state not found");

    if (!checkPolicy(input.claims, current.tenantId, current.orgId, "ledger:write")) {
      throw new Error("Unauthorized");
    }

    return this.transition({
      claims: input.claims,
      previousHash: input.currentHash,
      nextStage: "compensated",
      patch: {
        ledger: {
          debitAccount: input.debitAccount,
          creditAccount: input.creditAccount,
          amount: input.amount,
          currency: input.currency,
          reason: input.reason
        }
      },
      actionScope: "ledger:write",
      idempotencyKey: input.idempotencyKey,
      signerPrivateKeyRef: input.signerPrivateKeyRef,
      signerPublicKeyRef: input.signerPublicKeyRef
    });
  }

  openChargeback(input: {
    claims: Claims;
    currentHash: string;
    caseId: string;
    reason: string;
    evidenceRequired: boolean;
    idempotencyKey: string;
    signerPrivateKeyRef: string;
    signerPublicKeyRef: string;
  }): PaymentState {
    const current = this.states.get(input.currentHash);
    if (!current) throw new Error("Current state not found");

    if (!checkPolicy(input.claims, current.tenantId, current.orgId, "payments:chargeback")) {
      throw new Error("Unauthorized");
    }

    return this.transition({
      claims: input.claims,
      previousHash: input.currentHash,
      nextStage: input.evidenceRequired ? "chargeback_evidence_required" : "chargeback_open",
      patch: {
        chargeback: {
          caseId: input.caseId,
          reason: input.reason,
          evidenceRequired: input.evidenceRequired
        }
      },
      actionScope: "payments:chargeback",
      idempotencyKey: input.idempotencyKey,
      signerPrivateKeyRef: input.signerPrivateKeyRef,
      signerPublicKeyRef: input.signerPublicKeyRef
    });
  }
}


---

21. Full example flow

21.1 Operator claims

{
  "sub": "operator_001",
  "tenantId": "tenant-a",
  "orgId": "acme",
  "roles": ["payment_operator", "reconciliation_agent", "ledger_writer"],
  "scopes": [
    "payments:create",
    "payments:authorize",
    "payments:capture",
    "payments:settle",
    "payments:reconcile",
    "payments:chargeback",
    "ledger:write"
  ]
}

21.2 Intent

authenticated request,

idempotency key validated,

payload canonicalized,

Ed25519 signature generated by HSM,

hash persisted,

outbox emitted.


21.3 Authorization

previous state verified,

transition allowed,

new signature generated,

causal sequence incremented.


21.4 Capture / Settlement

asynchronous processing,

event replicated through queues,

inbox prevents duplicates,

canonical storage preserves versions.


21.5 Reconciliation

external record is received,

compared against internal state,

if it matches, reconciliation,

if not, failed + accounting compensation.


21.6 Chargeback

case opened,

evidence collected,

bundle canonicalized,

signed,

hashed,

sent to regulatory workflow.



---

22. Multi-node operation

22.1 What each node does

receives events,

verifies signatures,

verifies causality,

applies policy,

persists canonical state,

records audit trail,

replicates to other nodes.


22.2 Convergence

Nodes do not need to act as a single central database if they maintain:

the same canonicalizer,

the same policies,

the same state machine,

the same signing scheme,

the same causal ordering.


22.3 Conflict resolution

If two branches compete:

the history is preserved,

the logical mempool marks the valid branch,

the invalid one is rejected or archived.



---

23. What this design delivers

This system delivers:

financial traceability,

reproducibility,

auditability,

state governance,

automatic reconciliation,

disciplined accounting compensation,

dispute-ready evidence,

cryptographic security,

and clear separation between business logic, persistence, and transport.



---

24. What must not be confused

This is not:

a simple CRUD backend,

a payment queue,

a loose ledger,

a PSP wrapper,

a marketing blockchain.


This is:

a payment state infrastructure,

with HD derivation,

with canonical storage,

with cryptographic verification,

and with auditable financial operations.



---

25. Final thesis

The correct way to describe the system is:

> A deterministic Payment State Engine over canonical storage, with HD derivation, cryptographic signing, reconciliation, regulatory compliance, an evidence engine, and double-entry accounting.



That is the full formulation.
