# How Requesting Code Review Works

Run a pre-commit quality and security pass and prepare a focused review request.

![Detailed systems blueprint for Requesting Code Review](../assets/system-blueprint.png)

## Stages

### 1. Inspect the exact change set

**Primary surface:** `Local changes`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 2. Run secrets and dependency checks

**Primary surface:** `Security scan`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 3. Run tests lint and formatting

**Primary surface:** `Quality checks`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 4. Fix safe mechanical issues

**Primary surface:** `Review brief`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 5. Summarize behavior risk and evidence

**Primary surface:** `Reviewer handoff`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 6. Request review with a focused brief

**Primary surface:** `Reviewer handoff`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.

## Failure handling

- **Authorization failure:** do not probe credentials or broaden access; report the missing authority.
- **Target ambiguity:** stop before mutation and request the minimum identifying information.
- **Tool or service failure:** retain error evidence, retry only safe transient failures, and cap retries.
- **Verification failure:** classify the run as incomplete even when the preceding operation returned success.

## Completion evidence

The handoff should contain the original request, inspection state, preview or plan, exact execution result, direct verification, and a final receipt naming limitations and withheld actions.
