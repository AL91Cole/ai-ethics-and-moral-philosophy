# Governance, Accountability, and Redress

**Document type:** Applied governance proposal

## Purpose

Ethical principles matter only when they change who has authority, what evidence must be produced, how affected people can challenge a decision, and what happens after harm. This document turns the repository's philosophical commitments into governance expectations.

## Accountability Follows Control

Responsibility should be allocated according to the choices each actor can make.

| Actor | Primary responsibilities |
|---|---|
| Governing body or executive leadership | Approve purpose, prohibited uses, risk tolerance, resources, independent oversight, and deployment decisions |
| Product owner | Maintain the use-case definition, affected-party analysis, documentation, and stop criteria |
| Developers and data teams | Document design assumptions, data provenance, limitations, tests, security controls, and foreseeable misuse |
| Deploying institution | Confirm that the system is appropriate for its real context; train operators; provide notice, appeal, and human alternatives |
| Operators | Use the system only within authorization; recognize uncertainty; document interventions; report failures |
| Privacy, security, legal, ethics, and accessibility reviewers | Conduct independent domain review and document disagreements rather than serving as symbolic approval |
| Auditors and evaluators | Test claims against evidence, including disparate impact and adversarial behavior |
| Vendors and suppliers | Disclose material limitations, dependencies, incidents, model changes, and data practices |

Shared responsibility must not become diluted responsibility. Every material decision should still have an accountable owner.

## Shared Governance

AI governance should not be controlled solely by the organization that profits from deployment or by the government body that seeks new power. Depending on the use case, governance should include:

- people directly affected by the system;
- marginalized communities likely to bear disproportionate risk;
- disability and accessibility representatives;
- domain professionals and frontline workers;
- privacy, security, safety, civil-liberties, and legal expertise;
- independent researchers or auditors;
- developers, operators, and organizational leadership.

Participation should begin before the intended use is fixed. Stakeholders need enough information, time, and authority to influence the outcome. Consultation after deployment is not shared governance.

## Lifecycle Decision Gates

### 1. Purpose and legitimacy

- What problem is being addressed?
- Is AI necessary, or would a simpler and less invasive process work?
- Who benefits, and who carries the risk?
- Which uses are prohibited from the beginning?

### 2. Context and impact mapping

- Which individuals and communities are affected directly or indirectly?
- What power differences already exist?
- What rights, accessibility needs, and civil liberties are implicated?
- What happens when the system is wrong?

### 3. Evidence before deployment

- Has the system been tested in conditions representative of the intended use?
- Are harmful bias, security, privacy, reliability, and accessibility evaluated?
- Are limitations understandable to operators and affected people?
- Is a non-AI or human fallback available?

### 4. Controlled deployment

- Is authority least-privileged and purpose-limited?
- Are notices, consent processes, explanations, and appeal channels active?
- Are logs tamper-evident and privacy-preserving?
- Are stop conditions and incident procedures rehearsed?

### 5. Continuous monitoring

- Are actual outcomes compared with the claims used to approve deployment?
- Are complaints and overrides analyzed as safety evidence rather than dismissed as user error?
- Are model, data, policy, or vendor changes reassessed?
- Are emerging harms reported to the governing body and affected people?

### 6. Retirement and repair

- Can the system and its integrations be disabled safely?
- Is unjustified retained data deleted?
- Are affected records corrected?
- Are people informed of material harm and available remedies?
- Are lessons incorporated into future governance?

## Meaningful Human Control

Human oversight is not meaningful when a person is expected to approve hundreds of outputs automatically, lacks authority to disagree, or cannot understand the system's limitations.

Meaningful control requires:

- sufficient time and information;
- relevant training and domain competence;
- authority to pause, reject, or change the outcome;
- protection from retaliation for raising safety or ethics concerns;
- a documented reason for high-impact interventions;
- review of automation bias and excessive override patterns;
- a safe alternative when the system is unavailable or stopped.

## Operational Override and Core Revision

An authorized human must be able to stop a system or override a case-level decision. This intervention should be logged, reviewable, and appealable.

No single person should be able to remove the protected ethical core secretly. Material core changes require:

1. a documented proposal and justification;
2. affected-party and rights analysis;
3. multi-stakeholder approval;
4. testing and independent review;
5. signed versioning and rollback capability;
6. public change notes appropriate to the system's risk;
7. renewed deployment authorization.

## Rights of Affected People

Where an AI system materially affects a person, the governance design should provide as many of the following as the context supports:

- notice that AI is being used;
- an understandable statement of purpose;
- access to relevant information about the decision;
- correction of inaccurate personal data;
- an explanation appropriate to the decision and audience;
- an opportunity to provide missing context;
- review by a qualified and empowered human;
- an accessible appeal process;
- protection from retaliation for appealing;
- timely correction and remedy;
- a non-AI alternative for high-stakes services when feasible.

An explanation is not meaningful if it is technically accurate but inaccessible, generic, or unrelated to the actual reason for the outcome.

## Remedy and Repair

Accountability does not end when an organization identifies who made a mistake. Repair may require:

- stopping or limiting the harmful use;
- correcting records and downstream systems;
- notifying affected people clearly;
- restoring access, opportunity, or benefits;
- financial or other appropriate compensation;
- changing policies, models, data, or staffing;
- publishing incident findings without exposing victims;
- monitoring whether the remedy actually worked.

Forgiveness and accountability can coexist. A person responsible for harm retains human dignity, while the institution still owes truth, consequences, and repair to those affected.

## Evidence Against Ethics-Washing

An organization should not call a system ethical based only on principles or a committee. Evidence should include:

- named accountable owners;
- documented prohibited uses and stop criteria;
- impact and risk assessments;
- representative test results and known limitations;
- accessibility evaluation with disabled participants;
- disparate-impact monitoring;
- override, appeal, complaint, and remedy statistics;
- policy and model change history;
- independent findings and unresolved dissent;
- examples of a deployment delayed, constrained, or stopped for ethical reasons.

Ethics becomes governance when it can change a decision made by power.
