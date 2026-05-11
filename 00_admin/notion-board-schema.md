---
title: "Notion Board Schema"
doc_type: "playbook"
status: "draft"
owner: "Producer / PM"
reviewers: []
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-04-30"
language: "es"
audience: ["internal", "ops", "creative", "production"]
tags: ["notion", "board", "schema"]
ai_use_cases: ["notion-setup", "task-management"]
source_of_truth: "local-project"
confidence: "medium"
assumptions: []
related_docs:
  - "open-questions.md"
---

# Notion Board Schema

Tablero creado en la página Notion T1mundial:

- Página: `https://www.notion.so/T1mundial-3437f7e6f1a2803c923ae48e2f67b5c8`
- Database: `T1 Mundial - Production Board`
- Data source: `collection://ab0fe4be-5bae-48d9-8835-0a8fb06594cc`

## Database: T1 Mundial - Production Board

Propiedades:

| Propiedad | Tipo | Opciones / formato |
|---|---|---|
| Task | Title | Nombre claro de tarea o asset. |
| Area | Select | Admin, Strategy, References, Creative, AI Generation, Edit, Audio, Post, Legal, Delivery, Metrics. |
| Status | Status | Backlog, Ready, In Progress, Review, Blocked, Approved, Done, Dropped. |
| Priority | Select | P0, P1, P2, P3. |
| Sprint | Select | Sprint 0, Sprint 1, Sprint 2, Sprint 3, Sprint 4. |
| Owner | Person | Responsable directo. |
| Approver | Person | Quien aprueba. |
| Due date | Date | Fecha límite. |
| Shot ID | Text | Ej: 01, 02, 11. |
| Asset link | URL | Drive, Frame.io, Figma, Adobe, etc. |
| Legal risk | Select | Low, Medium, High, Critical. |
| Creative QA | Checkbox | Aprobación creativa. |
| Legal QA | Checkbox | Aprobación legal. |
| Notes | Text | Contexto breve. |

## Vistas recomendadas

- Board by Status.
- Calendar by Due date.
- Table by Sprint.
- Legal Review.
- Shot Tracker.
- Blocked / Hands-up.
- Delivery Checklist.

## Vistas creadas

- Board by status.
- Sprint plan.
- Legal review.
- Calendar.
