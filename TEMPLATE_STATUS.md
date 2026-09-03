# Template Status & Verification

**Classification:** Configurable n8n template asset — not a verified production deployment.

The workflow export and documentation are inspectable template evidence. They are not proof of a configured production lead-scoring system, conversion improvement, SLA, ROI, or client outcome.

## Verification gate
1. Parse/import into a clean current n8n instance.
2. Inspect all connections, score calculations, model prompts, thresholds, branches, and Code nodes.
3. Replace placeholder credentials, model IDs, CRM/data destinations, URLs, webhooks, and resource IDs.
4. Run representative HOT/WARM/COLD inputs plus malformed-model-output and provider-failure cases.
5. Verify deterministic thresholds remain separate from AI interpretation and that alerts/CRM writes match the final score.
6. Record configured test date/result.

## Security
Never commit API keys, CRM credentials, private webhooks, lead PII, or production data. Use synthetic leads and fresh test credentials.

## Change record
- **2026-09-03:** Added repository verification/security/status control. No workflow-logic change or runtime pass is implied.
