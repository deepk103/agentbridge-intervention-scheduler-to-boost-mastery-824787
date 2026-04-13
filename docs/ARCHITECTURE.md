# Architecture Documentation

## Overview
This Reflection implements Intervention Scheduler to boost mastery for Education use cases.

## Components
1. **Module Intake**: Collect, validate and normalize attendance from Identity/SSO; attach a runId and timestamp for traceability.
2. **Draft**: Execute draft phase for the Reflection pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Self-Critique**: Execute self-critique phase for the Reflection pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Intervention**: Intervention across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Personalized Plan**: Personalized Plan across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **Progress Review**: Progress Review across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Readiness Check**: Readiness Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
8. **Practice Recommendation**: Practice Recommendation across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
9. **Transcript Update**: Assemble final payload with status, artifacts, KPIs and audit trail; store to Identity/SSO; return response JSON for the client.

## Data Flow
- Input: Module Intake
- Processing: 9 sequential steps
- Output: Transcript Update
