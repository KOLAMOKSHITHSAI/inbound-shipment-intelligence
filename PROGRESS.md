# Progress Log

## Checkpoint 1 (2026-10-04)

**Current phase:** Phase 0 (Setup), nearly complete. Next is Phase 2 (Dataset design).

### What I built
- Project folder `inbound-shipment-intelligence` with a Python 3.12.4 virtual environment in `.venv`
- VS Code set up to activate `.venv` automatically. Anaconda's Python 3.14.6 was shadowing it before.
- Git repository with `.gitignore` covering `.venv/`, `__pycache__/`, `.DS_Store`, and `.env`
- `README.md` with a one-sentence project description
- Pushed to GitHub: https://github.com/KOLAMOKSHITHSAI/inbound-shipment-intelligence

### Concepts I understand
- The business problem: predict whether an inbound shipment will be late, and by how many hours, so the receiving team can reallocate docks and staff
- Classification predicts a category (Delayed or On-time). Regression predicts a number (hours late).
- A model only sees information available before the outcome. It never sees the real delay.
- Many zero-delay shipments pull regression predictions toward zero.
- Why `.venv` stays out of Git: commit `requirements.txt`, the recipe, and not the environment itself
- Git routine: `add`, then `commit` (local), then `push` (remote)

### Concepts I struggled with
- At first, I thought the model would know a shipment was 10 hours late. It can't, because that's the answer it is predicting.
- Virtual environment activation: why `python --version` showed the wrong version

### Open questions
- Use the existing synthetic CSV, or write my own data generator?
- Regression design: train on all shipments, or only on delayed ones? To be tested in Phase 9.

### Exact next step
Phase 2: Dataset design. Learn row, column, feature, target, and identifier, then go through which fields are unavailable at prediction time.
