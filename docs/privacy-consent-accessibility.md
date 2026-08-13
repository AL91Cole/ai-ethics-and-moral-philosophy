# Privacy, Consent, and Accessibility

**Document type:** Applied ethical and design requirements

## Central Position

Privacy, consent, and accessibility are not secondary product features. Together they determine whether a person has meaningful control.

- Privacy protects a person's ability to control intimate information.
- Consent protects a person's ability to choose knowingly and freely.
- Accessibility makes that knowledge and choice practically possible.

A consent screen cannot make an invasive practice ethical when refusal is impossible, consequences are hidden, or the interface cannot be understood by the people affected.

## Privacy Principles

### Data minimization

Collect the minimum information needed for a defined purpose. Do not collect broad identity, location, emotional, medical, or behavioral data because it might become useful later.

### Purpose limitation

Information given for support, safety, authentication, or accessibility should not quietly become material for advertising, employment scoring, policing, insurance, or unrelated model training.

### Local protection and blind storage

For highly sensitive information, designs should consider:

- encrypting on the client before storage or transmission;
- AES-256-GCM or another appropriately reviewed authenticated-encryption method;
- keys derived or held locally when the threat model supports it;
- ciphertext-only backend storage;
- separation of identity data from sensitive content;
- secure deletion and crypto-shredding of keys;
- tamper-evident integrity records;
- short and explicit retention periods.

These controls require professional implementation and testing. Naming an algorithm is not proof that the full system is secure.

### Honest encryption claims

A service should not claim that "only the user can read the conversation" if plaintext is sent to a server or model provider for generation. Documentation must state:

- where plaintext exists;
- which process can access it;
- how long it remains available;
- what metadata is retained;
- which third parties receive it;
- what happens during logging, backup, moderation, and incident response.

Transparency about an architectural limitation is more ethical than using stronger privacy language than the design supports.

## Meaningful Consent

Consent should be:

- **informed:** the person understands the purpose, data, risks, and alternatives;
- **specific:** one choice does not authorize unrelated uses;
- **freely given:** refusal does not carry an unfair or hidden penalty;
- **affirmative:** silence and preselected boxes are not treated as agreement;
- **revocable:** future processing can be stopped where possible;
- **accessible:** information and controls can be understood and operated;
- **renewed:** material changes require a new decision, not quiet policy drift.

Consent is not the only ethical or legal basis for processing. In high-power settings such as employment, education, public benefits, or law enforcement, a person may lack a genuine ability to refuse. The organization must not use a consent form to disguise coercion.

## User Data Rights

People should be able to:

- see what personal information and learned preferences are retained;
- correct inaccurate information;
- delete information that no longer has a justified retention requirement;
- export information in an understandable form where appropriate;
- disable personalization without losing unrelated core functionality;
- learn which parties received their data;
- challenge an inference rather than only the raw data behind it;
- receive notice of a material breach or harmful use.

Deleting a visible conversation while retaining embeddings, profiles, backups, or derived scores is not complete deletion unless those exceptions are disclosed and justified.

## Distress and Emergency Disclosure

Support systems should distinguish emotional venting from credible, immediate physical danger. Broad surveillance of historical conversations is not justified merely because safety is important.

A proportionate process should:

1. use calm, minimal questions to determine immediacy;
2. rely on current context rather than opening unrelated sealed history;
3. provide voluntary support and local resources when danger is not immediate;
4. disclose only the minimum necessary information when an emergency threshold is met;
5. document the threshold, decision, recipient, and information disclosed;
6. permit later review and correction;
7. avoid presenting an AI risk score as certainty.

Exact duties vary by jurisdiction and service type. They require legal and professional review before deployment.

## Accessibility as Justice

An ethical AI system should account for visual, auditory, motor, cognitive, learning, language, and sensory differences from the beginning.

Design expectations include:

- plain-language summaries before detailed explanations;
- clear headings and manageable steps;
- readable typography, spacing, and contrast;
- keyboard and assistive-technology compatibility;
- captions, transcripts, and non-audio alternatives;
- alternatives to color-only meaning;
- the ability to slow, repeat, simplify, or enlarge information;
- confirmation before destructive or high-impact actions;
- forgiving input for spelling, handwriting, or communication differences;
- no unnecessary time limits;
- accessible appeal and support channels;
- testing with disabled people rather than automated checks alone.

Accessibility preferences may be stored only with consent and should not be repurposed to infer medical status, employability, risk, or value.

## Zero-Trust Privacy Model

Zero trust should apply to data and services, not to a person's human worth. Architecturally, it means no identity, device, service, network location, or administrator receives implicit access.

Controls should include:

- explicit authentication and authorization;
- least privilege;
- continuous and context-aware evaluation;
- separation of duties;
- protected resources rather than trusted network zones;
- auditable access decisions;
- rapid revocation;
- resilience when a component is compromised.

Behavioral or location signals should not become invisible mass surveillance. Risk signals must be necessary, proportionate, secured, and subject to retention limits.

## Review Questions

- Could the same purpose be achieved with less personal information?
- Can a person refuse without losing an essential service unfairly?
- Does the system explain every place where plaintext exists?
- Are derived profiles and inferences visible and correctable?
- Can a disabled person exercise the same privacy and appeal rights?
- Are emergency disclosures narrow, reviewable, and based on current evidence?
- Do administrators have more access than their role requires?
- Is deletion real across primary data, derived data, and backup policy?

Privacy is not an obstacle to care. It is one of the ways care becomes trustworthy.
