# Standards and Governance Crosswalk

**Document type:** Standards crosswalk  
**Last reviewed:** 2026-08-12  
**Important:** Conceptual alignment does not establish certification, legal compliance, security authorization, or ethical success.

## Purpose

This crosswalk connects the repository's personal ethical framework and AI Guardian design concepts with established public guidance. The relationship is directional: standards help translate values into governance outcomes, while the personal framework adds commitments such as Unified Love, bounded moral learning, anti-concentration of power, accessibility, non-retaliation, and redress.

## Reference Set

- [NIST AI Risk Management Framework (AI RMF 1.0)](https://doi.org/10.6028/NIST.AI.100-1)
- [NIST AI RMF Playbook](https://airc.nist.gov/airmf-resources/playbook/)
- [NIST AI 600-1, Generative AI Profile](https://doi.org/10.6028/NIST.AI.600-1)
- [NIST SP 800-207, Zero Trust Architecture](https://doi.org/10.6028/NIST.SP.800-207)
- [CISA Zero Trust Maturity Model, Version 2.0](https://www.cisa.gov/resources-tools/resources/zero-trust-maturity-model)
- [NIST Cybersecurity Framework (CSF) 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [NIST Privacy Framework](https://www.nist.gov/privacy-framework)
- [CISA Secure by Design](https://www.cisa.gov/securebydesign)
- [Regulation (EU) 2024/1689, Artificial Intelligence Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)

Frameworks and laws evolve. A production project should record the exact version, access date, jurisdiction, organizational role, and controls actually assessed.

## NIST AI RMF Core

The AI RMF organizes risk management through `GOVERN`, `MAP`, `MEASURE`, and `MANAGE`.

| AI RMF function | Connection to this repository | Example evidence |
|---|---|---|
| `GOVERN` | Protected ethical core; named responsibility; shared governance; prohibited uses; change control; appeal and redress | Governance charter, role matrix, policy versions, stakeholder records, dissent log, stop authority |
| `MAP` | Intended-use definition; affected-party analysis; cultural context; power imbalance; civil-liberties and accessibility impact | Context map, data-flow map, impact assessment, misuse cases, affected-community analysis |
| `MEASURE` | Reliability, harmful bias, privacy, accessibility, security, functional-empathy, and adversarial evaluations | Test plans, subgroup results, red-team findings, accessibility testing, explanation studies, uncertainty calibration |
| `MANAGE` | `ALLOW`, `ASK`, `CONSTRAIN`, and `BLOCK`; risk prioritization; incident response; safe shutdown; retirement and repair | Decision rules, risk register, mitigation owners, incident exercises, rollback evidence, remedy records |

The protected core should be treated as part of governance, not as a model prompt that can be bypassed silently.

## NIST AI Trustworthiness Characteristics

| NIST characteristic | Related project commitment |
|---|---|
| Valid and reliable | Test in the real use context; state uncertainty and known limits |
| Safe | Prevent serious foreseeable harm; define stop conditions and human fallback |
| Secure and resilient | Zero trust, least privilege, separated trust domains, tamper evidence, tested recovery |
| Accountable and transparent | Named human owners, decision logs, policy history, notice, appeal, and repair |
| Explainable and interpretable | Reasons understandable to affected people, not only developers |
| Privacy-enhanced | Data minimization, local encryption where feasible, blind storage, retention limits, honest plaintext boundaries |
| Fair with harmful bias managed | Structural and subgroup analysis, affected-community participation, and ongoing outcome monitoring |

Unified Love and accessibility add a behavioral requirement: trustworthiness must also be visible in how a system treats people during uncertainty, distress, disagreement, and refusal.

## NIST SP 800-207 Zero Trust Architecture

NIST zero trust removes implicit trust based only on network location or asset ownership and focuses protection on resources.

| Zero-trust concept | AI Guardian application | Ethical limitation |
|---|---|---|
| No implicit trust | Evaluate identity, device, role, MFA, anomaly, and resource sensitivity | Signals must not become unlimited behavioral surveillance |
| Explicit authentication and authorization | Verify subject and device before protected-resource access | Collect only signals necessary for the decision |
| Least privilege | Grant the minimum resource and action scope | Do not infer that a verified identity deserves broad access |
| Resource-centered protection | Seal privacy vaults independently of network zone | Human dignity is not a trust score; only access is evaluated |
| Continuous evaluation | Reassess material context changes | Inform users where continuous monitoring is present and apply retention limits |
| Policy decision and enforcement | Separate policy logic from enforcement points | Preserve explainability, audit, and safe human intervention |

The Guardian Labyrinth extends denial with an optional isolated deception route. That extension is not automatically endorsed by SP 800-207 and requires its own legal, safety, and civil-liberties analysis.

## CISA Zero Trust Maturity Model 2.0

CISA describes five pillars and three cross-cutting capabilities.

| CISA area | AI Guardian example |
|---|---|
| Identity | MFA, roles, identity assurance, and rapid revocation |
| Devices | Device trust and integrity without permanent blanket trust |
| Networks | Segmentation, isolated deception environments, and protected traffic paths |
| Applications and workloads | Service identity, workload authorization, dependency control, and secure updates |
| Data | Owner-only vault rules, encryption, classification, minimization, and retention |
| Visibility and analytics | Explainable access decisions, anomaly evidence, and privacy-limited telemetry |
| Automation and orchestration | Reversible policy enforcement, safe routing, alerting, and tested human escalation |
| Governance | Ethical core, responsibility matrix, audit, change control, civil-liberties review, and remedies |

Maturity should not be measured only by how much monitoring or automation exists. It should also measure restraint, false-positive handling, accessibility, data reduction, and the ability to correct harm.

## NIST CSF 2.0

| CSF function | Related repository practice |
|---|---|
| `GOVERN` | Mission, stakeholder expectations, risk tolerance, roles, policy, supply-chain and AI governance |
| `IDENTIFY` | Asset, data, dependency, threat, privacy, and affected-party inventories |
| `PROTECT` | Least privilege, encryption, secure design, training, and protected vaults |
| `DETECT` | Contextual anomalies, honeytoken activation, integrity failure, and documented confidence |
| `RESPOND` | Containment without retaliation, evidence preservation, communication, and legal review |
| `RECOVER` | Safe restoration, key and policy recovery, correction of records, lessons learned, and repair |

AI risk should be integrated with cybersecurity and enterprise governance rather than isolated in a separate ethics document.

## NIST Privacy Framework

The privacy crosswalk should focus on risks to individuals, not only risks that data loss creates for the organization.

Related commitments include:

- identifying processing purpose and affected people;
- mapping data, metadata, inferences, recipients, and retention;
- governing privacy roles and risk decisions;
- minimizing and protecting data throughout its lifecycle;
- communicating understandable practices and choices;
- enabling access, correction, deletion, and complaint processes;
- assessing whether the design causes loss of autonomy, exclusion, stigma, or surveillance chilling effects.

## CISA Secure by Design

The AI Guardian approach aligns conceptually with CISA's emphasis on treating customer security as a core business requirement and taking ownership of customer security outcomes.

Applied expectations include:

- safe defaults rather than requiring expert users to secure the product;
- transparent disclosure of incidents and material limitations;
- reduction of entire vulnerability classes;
- secure development and dependency practices;
- responsibility at executive and product levels;
- no transfer of preventable security burden to the person least able to manage it.

This repository extends that idea to **ethical by design**: dignity, consent, accessibility, appeal, and non-retaliation should also be architectural requirements.

## EU Artificial Intelligence Act Context

The EU AI Act uses a risk-based legal structure and establishes obligations that vary by system category, use case, provider/deployer role, and other facts. Potentially relevant themes include:

- prohibited AI practices;
- classification and obligations for high-risk AI systems;
- risk management and data governance;
- technical documentation and recordkeeping;
- transparency and information for deployers or affected people;
- human oversight;
- accuracy, robustness, and cybersecurity;
- post-market monitoring and incident reporting;
- requirements involving general-purpose AI models;
- fundamental-rights protections.

The personal framework's dignity, non-manipulation, human control, accessibility, transparency, and redress commitments can support legal analysis, but they do not determine whether the Act applies or whether its requirements are satisfied. That determination requires current legal review.

## Gaps Standards Do Not Resolve Automatically

Standards can organize governance, but they do not settle:

- whose moral values belong in a protected core;
- whether an AI could ever deserve moral status;
- when compassion becomes emotional manipulation;
- which tradeoffs among rights are justified;
- whether a specific deception deployment is legally or ethically proportionate;
- how much power corporations or governments should hold;
- what repair is owed after algorithmic harm;
- whether affected communities possess meaningful decision authority.

These remain philosophical, democratic, empirical, and legal questions.

## Minimum Assurance Package

A project claiming alignment should publish or retain an appropriate assurance package containing:

1. system purpose, scope, prohibited uses, and responsible owners;
2. architecture, data flows, model and supplier inventory;
3. affected-party, accessibility, privacy, security, and civil-liberties impact assessments;
4. evaluation methods, representative results, and known limitations;
5. policies for human review, override, appeal, correction, and remedy;
6. incident, disclosure, retention, shutdown, recovery, and retirement procedures;
7. policy and model change history;
8. unresolved risks, dissent, and accepted residual risk;
9. independent review appropriate to impact;
10. evidence that safeguards operate in practice.

Alignment is a claim to be demonstrated, not a badge produced by a table.
