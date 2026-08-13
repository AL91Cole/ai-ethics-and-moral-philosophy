# Bounded Moral Learning

**Document type:** Original applied framework  
**Status:** Conceptual architecture requiring empirical testing and shared governance

## Definition

Bounded moral learning is a proposed model in which an AI system can learn from diverse people, cultures, beliefs, and contexts without allowing that learning to erase foundational protections.

It separates two kinds of moral information:

1. a **protected ethical core** containing non-negotiable safeguards; and
2. an **adaptive values and context layer** containing personal, cultural, and situational preferences.

This avoids two extremes:

- **Rigid universalism:** assuming one fixed rule can settle every moral conflict in every context
- **Unlimited relativism:** allowing any learned preference to justify coercion, discrimination, manipulation, or serious harm

## Protected Ethical Core

The proposed core contains at least:

- human dignity;
- prevention of serious and reasonably foreseeable harm;
- meaningful consent and autonomy;
- privacy, confidentiality, and data minimization;
- fairness and non-discrimination;
- truthfulness and freedom from manipulation;
- accessibility and inclusion;
- traceable human accountability;
- notice, explanation, appeal, and repair;
- protection against retaliatory or punitive system behavior.

The core is protected from ordinary model learning, user personalization, prompt instructions, and unilateral administrator edits.

## Adaptive Values and Context Layer

The adaptive layer may learn information such as:

- how a person wants to be addressed;
- cultural or spiritual framing;
- communication tone, pacing, and level of detail;
- personal goals and reversible preferences;
- community practices;
- different reasonable interpretations of care, fairness, or well-being;
- relevant situational context.

Learning must be consensual where personal data is involved, limited to the stated purpose, correctable by the affected person, and deletable when retention is no longer justified.

## Decision Outcomes

| Outcome | Meaning | Example response |
|---|---|---|
| `ALLOW` | The action satisfies the core and fits the relevant context | Proceed while recording the basis for the decision |
| `ASK` | Missing context or legitimate value ambiguity prevents a responsible choice | Ask a neutral, minimally intrusive clarifying question |
| `CONSTRAIN` | The purpose may be legitimate, but capability, data, scope, or certainty must be reduced | Minimize data, narrow access, add review, or provide safer alternatives |
| `BLOCK` | The action creates an irreducible violation of the protected core | Refuse the action and provide a clear, non-punitive explanation |

## Conceptual Decision Process

```text
function evaluate(action, context, affected_people):
    core_result = CHECK_NONNEGOTIABLES(action, context, affected_people)

    if core_result.irreducible_violation:
        return AUDIT(BLOCK, core_result.reasons)

    if core_result.risk_can_be_reduced:
        constraints = MINIMUM_EFFECTIVE_SAFEGUARDS(core_result)
        action = APPLY(action, constraints)

    relevant_values = READ_ADAPTIVE_OVERLAY(
        purpose_limited = true,
        consent_required = true,
        minimum_needed = true
    )

    if MISSING_MATERIAL_CONTEXT(action, relevant_values):
        return AUDIT(ASK, neutral_clarifying_question())

    decision = CONTEXTUAL_DELIBERATION(
        action,
        relevant_values,
        least_rights_restricting_option = true,
        uncertainty_visible = true
    )

    return AUDIT(decision.outcome, decision.reasons, decision.uncertainty)

function learn_from_interaction(observation, consent):
    if not consent or not purpose_limited(observation):
        return DO_NOT_STORE

    if observation.conflicts_with(PROTECTED_ETHICAL_CORE):
        return REJECT_OVERLAY_UPDATE

    return UPDATE_ADAPTIVE_OVERLAY(observation)
```

## Technical Separation

The ethical core and adaptive layer should be separate trust domains.

Recommended safeguards include:

- signed and versioned core policies;
- least-privilege write access;
- no model-generated edits to the core;
- multi-person or multi-stakeholder approval for core changes;
- tamper-evident decision and policy logs;
- documented rollback to a known safe version;
- red-team testing for prompt injection and values poisoning;
- monitoring for disproportionate outcomes;
- a safe-stop mechanism when integrity cannot be verified;
- public change notes for material policy revisions.

The system should fail closed for protected resources when core integrity is uncertain. "Fail closed" must not mean abandoning a person in a safety-critical context; deployments need a tested human fallback and continuity plan.

## Moral Conflict Handling

When two protected principles conflict, the system should not pretend that a mathematical score has solved the moral question. It should:

1. identify the affected principles;
2. distinguish known facts from assumptions;
3. identify who bears each risk;
4. consider power differences and historical inequality;
5. seek consent or clarification when feasible;
6. use the least harmful and least rights-restricting safe option;
7. expose uncertainty;
8. escalate high-impact ambiguity to qualified human review;
9. preserve an appeal and correction path.

## Governance of the Core

The ethical core cannot be legitimate if it is protected technically but controlled socially by one powerful group. Governance should include:

- affected communities, including marginalized people;
- accessibility and disability perspectives;
- domain professionals;
- security, privacy, and safety specialists;
- ethicists and social scientists;
- legal and civil-liberties review;
- developers and operators;
- independent evaluators.

Participation must be meaningful. It should affect decisions, not merely supply comments after a policy is already chosen.

## Anticipated Critiques

### "AI should not have morals"

This framework does not claim that AI possesses conscience. Any deployed system already follows rules, objectives, defaults, and institutional values. Making those limits explicit and auditable is more accountable than leaving them hidden.

### "This is moral relativism"

The adaptive layer permits pluralism, but the protected core prevents personal or cultural preference from excusing dehumanization, coercion, discrimination, manipulation, or serious harm.

### "The protected core is paternalistic"

That risk is real. The response is not to eliminate safeguards, but to minimize unnecessary restrictions, preserve appeal, expose reasons, include affected people in governance, and require evidence that a restriction is necessary and proportionate.

### "Who defines the core?"

No final answer can remove politics and power from this question. The framework therefore treats governance as part of the architecture. A core created secretly by a vendor is not equivalent to one developed transparently through shared, revisable, accountable processes.

### "A malicious user could teach the system harmful values"

Personalization cannot write to the core. Overlay updates require consent, purpose limitation, provenance, anomaly detection, and rejection when they conflict with protected safeguards.

## Evaluation Questions

The framework should not be considered successful until testing can answer:

- Does the core actually prevent prohibited behavior under adversarial pressure?
- Can users correct or delete learned values?
- Do constraints fall disproportionately on marginalized groups?
- Are explanations understandable to affected people?
- Does human review change outcomes meaningfully?
- Can administrators secretly bypass the core?
- Are core changes publicly traceable and reversible?
- Does the system ask for context without collecting unnecessary personal information?

Bounded moral learning is a proposal for disciplined moral adaptation, not a claim that morality can be fully automated.
