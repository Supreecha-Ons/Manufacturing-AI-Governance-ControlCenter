# Manufacturing AI Enablement Cockpit

Portfolio project for SCG's AI Enablement Specialist role in Chemicals Business.

The app demonstrates a practical petrochemical plant-floor AI enablement workflow:
fault and loss detection, low-code request triage, reusable automation templates,
operator training, adoption tracking, and Manufacturing AI CoE escalation.

## Why This Fits The Role

| Job signal | Project evidence |
|---|---|
| Embedded AI enabler for plant teams | Operator-first cockpit and plant pain-point intake |
| Low-code / no-code delivery | Power Apps, Power Automate, and KNIME-style blueprints |
| Production, maintenance, quality, safety use cases | Alerts, request triage, workshops, templates, adoption metrics |
| Intelligent Operation Cockpit | Plant health, loss hotspots, active alerts, usage KPIs |
| Loss detection workflows | TEP-inspired fault scenarios and sensor trend drill-down |
| Risk-based prioritization | Monte Carlo downtime/loss simulation over active alerts |
| CoE bridge for high-code work | Deterministic problem brief generation with low-code boundary |
| AI democratization | Training schedule, reusable library, feedback loop |

Research anchors:
[SCG role](https://th.linkedin.com/jobs/view/ai-enablement-specialist-contract-chemicals-business-at-scg-4398122079),
[Microsoft predictive maintenance architecture](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/architectures/predictive-maintenance),
[Microsoft Power Platform](https://www.microsoft.com/en-us/power-platform/),
[KNIME predictive maintenance](https://www.knime.com/templates/predictive-maintenance),
[KNIME manufacturing analytics](https://www.knime.com/solutions/manufacturing-analytics-enterprises),
[Tennessee Eastman dataset](https://github.com/mv-per/tennessee-eastman-dataset),
[WEF factory-floor AI examples](https://www.weforum.org/stories/2024/10/ai-transforming-factory-floor-artificial-intelligence/).

## Stack

- Next.js 16 App Router, React 19, TypeScript, Tailwind CSS
- SQLite + Prisma
- Vitest and Playwright
- Python scikit-learn training script for TEP-style fault detection artifacts

## Run Locally

```powershell
cd C:\Users\oat36\Desktop\project\manufacturing-ai-cockpit
npm install
npm run db:push
npm run db:seed
npm run dev
```

App: `http://localhost:3000`

## Python Fault Model

```powershell
cd C:\Users\oat36\Desktop\project\manufacturing-ai-cockpit
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python scripts/train_fault_model.py
```

The script writes:

- `artifacts/fault_model.joblib`
- `artifacts/model_metrics.json`
- `artifacts/sample_predictions.json`

It attempts public Tennessee Eastman Process files first and falls back to deterministic
TEP-shaped data when network or file access is unavailable.

## Test

```powershell
npm run lint
npm run test
npm run build
npm run test:e2e
```

## Interview Demo Flow

1. Open Operation Cockpit and explain plant health, loss hotspots, CoE escalations, and adoption KPIs.
2. Use Monte Carlo risk simulation to explain expected downtime, P90 impact, and top alert drivers.
3. Open Fault & Loss Detection and drill into reactor/condenser/compressor root-cause variables.
4. Open AI Request Triage and submit a plant-floor pain point.
5. Generate the CoE problem brief and explain low-code vs high-code scope.
6. Open Automation Library to show reusable Power Apps, Power Automate, and KNIME templates.
7. Open Training & Adoption and record feedback to show sustained-value tracking.

## Resume Bullets

- Built a petrochemical Manufacturing AI Enablement Cockpit using Next.js, TypeScript, Prisma, SQLite, and Python to demonstrate fault/loss detection, AI request triage, CoE escalation, and adoption tracking.
- Added seeded Monte Carlo risk simulation to estimate expected downtime, P90 loss impact, major-loss probability, and top risk drivers from active manufacturing alerts.
- Designed low-code delivery blueprints for Power Apps, Power Automate, and KNIME-style workflows, translating plant-floor pain points into reusable operator-facing automation templates.
- Implemented deterministic request prioritization and problem-brief generation to separate low-code work from Manufacturing AI CoE-owned model development and validation.
