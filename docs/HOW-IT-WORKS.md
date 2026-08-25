# How Requesting Code Review Works

The visuals on this page are static SVGs, so they render directly on GitHub on phones and desktop browsers. Each one is generated from a model specific to this skill.

## System architecture

![Detailed system map for Requesting Code Review](../assets/system-map.svg)

### Components

- **1. Local changes:** participates in inspect the exact change set.
- **2. Security scan:** participates in run secrets and dependency checks.
- **3. Quality checks:** participates in run tests lint and formatting.
- **4. Review brief:** participates in fix safe mechanical issues.
- **5. Reviewer handoff:** participates in summarize behavior risk and evidence.

## Actor and data sequence

![Actor and data sequence for Requesting Code Review](../assets/operation-sequence.svg)

### 1. Inspect the exact change set

**Primary surface:** `Local changes`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 2. Run secrets and dependency checks

**Primary surface:** `Security scan`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 3. Run tests lint and formatting

**Primary surface:** `Quality checks`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 4. Fix safe mechanical issues

**Primary surface:** `Review brief`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 5. Summarize behavior risk and evidence

**Primary surface:** `Reviewer handoff`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 6. Request review with a focused brief

**Primary surface:** `Local changes`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.

## Example output shape

![Illustrative output for Requesting Code Review](../assets/example-output.svg)

The example is a visual contract: a real run may look different, but it should expose comparable state, provenance, and verification information. It is not presented as evidence of a live external action.

## Decision and stop conditions

![Decision guide for Requesting Code Review](../assets/decision-guide.svg)

The workflow stops when the target is ambiguous, the relevant surface is unavailable or unauthorized, or the final artifact cannot be checked. A logged-in session or successful tool call is not by itself proof that the requested outcome is complete.

## Verification checklist

- Confirm every component shown in the system map exists in the target environment.
- Trace the actor sequence using actual tool output or artifact state.
- Compare the result with the example-output information contract.
- Re-read or reopen the final artifact instead of trusting an attempt message.
- Report omitted stages, unsupported capabilities, and remaining human decisions.
