# Story Generator

A staged, hands-on **conversion course** that turns a working FastAPI Q&A app into a children's bedtime-story generator that calls Google's Gemini API and deploys to Vercel + Render — *one fundamental at a time, across eight modules.*

> **License:** [PolyForm Noncommercial 1.0.0](LICENSE). You may use this code freely for personal learning and non-commercial educational use (and you can publish your forked deploy as a portfolio piece per `docs/publish_your_work.md`). You may not use it as the curriculum for a fee-charging course. See [NOTICE.md](NOTICE.md) for plain-English allowed/not-allowed lists.

This repo is your starting point. You'll work through it module-by-module during the live session and on your own afterwards. By the end, you'll have an app on the internet — Vercel-hosted frontend, Render-hosted backend, managed Postgres — that a parent on a different network can use to generate a bedtime story for their child. You'll publish the result to your own GitHub as a portfolio piece.

## Welcome

This repo is part of the SCTP **DSAI** course. It applies knowledge from class to create an AI application (children's bedtime stories) using Gemini API, structured form and public deply.


(macOS / Linux / WSL2 Ubuntu — same commands.)

> **Windows learners:** do this *inside an Ubuntu terminal* (your WSL2 environment from the FastAPI course), NOT native PowerShell. Clone into `~/code/` (Ubuntu's native filesystem) — not `/mnt/c/...`. The cross-filesystem bridge is 10–50× slower for `pip install` and `psycopg[binary]`. If you accidentally clone into `/mnt/c/`, just re-clone into `~/code/`.

### Set up the shared venv (once per machine)

The shared `venv/` lives at the cohort repo root. Every dist folder activates it via `../../venv/bin/activate`.

```bash
python3 -m venv venv
source venv/bin/activate
```
(macOS / Linux / WSL2 Ubuntu — same commands. The `(venv)` prefix in your prompt is the visual confirmation.)

Then install **all** dependencies in one shot. The root `requirements.txt` is the union of every module's deps:

```bash
pip install -r requirements.txt
```

That's it for Python packages — you won't `pip install` again for the rest of the course.

### Prove your services are running (the "am I ready?" check)

Binary on PATH ≠ service running. From the repo root with the venv active:

```bash
./scripts/verify_setup.sh
```
(macOS / Linux / WSL2 Ubuntu — same command. Run from inside your Ubuntu terminal for WSL2.)

