# 📈 CS336 Assignment 3 — Scaling: Fitting a Scaling Law

You're in charge of ClosedAI's next model, with a fixed compute budget and an Antarctic ice shelf on the
line. 🧊 The job: spend a **12 B200-hour** experiment budget on a training API, fit a scaling law relating
loss to model size and compute, and use it to predict the compute-optimal configuration (and final loss) for
the big **48 B200-hour** run. Handout: [`cs336_assignment3_scaling.pdf`](./cs336_assignment3_scaling.pdf).

**Progress** — ⬜⬜ **0 / 2 pieces** written (55 pts). Scaffolding only. ☕

## 📋 Build plan

- [ ] **IsoFLOPs scaling laws** · 5 pts — reproduce the IsoFLOPs analysis and derive the loss-optimal model
  size for a compute budget 📐
- [ ] **Scaling-law leaderboard** · 50 pts — design the ≤12 B200-hr query schedule, fit the law, then submit
  the predicted optimal hyperparameters + final validation loss 🔮
  
<!-- ## 📊 Completed results -->

## 🏃 Getting it running

1. `uv sync` — deps are managed with [`uv`](https://docs.astral.sh/uv/).
2. `export A3_API_KEY=<your 8-digit student ID>` 🔑
3. Hit the hosted API at `http://hyperturing.stanford.edu:8000` — see the
   [docs](http://hyperturing.stanford.edu:8000/docs) and
   [dashboard](http://hyperturing.stanford.edu:8000/dashboard).
4. Start from [`examples/client_example.ipynb`](./examples/client_example.ipynb) to submit and inspect runs 🔁

> 💡 Offline / non-student? `uv sync --extra server`, pull tokenized data with
> `uv run modal run scripts/1_download_tokenized_data.py`, then `uv run cs336_scaling/training/run.py`.

## 🧭 Repo layout

- `cs336_scaling/client.py` — the API client (`get_budget`, `submit_experiment`, `list_experiments`, …)
- `cs336_scaling/schemas/` · `training/` · `scheduler/` · `api/` — request/response types and the training side
- `examples/client_example.ipynb` — minimal submit-and-inspect example
- `scripts/` · `tests/` — utilities and the scheduler/API tests
- `pyproject.toml` · `cs336_assignment3_scaling.pdf`

---

Extrapolate responsibly. 🔮
