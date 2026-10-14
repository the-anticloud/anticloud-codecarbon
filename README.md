# CODECARBON

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-carbon_capture-lightgrey)

> Anticloud-hardened packaging of the upstream project `CODECARBON` in category **CARBON CAPTURE**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** CARBON CAPTURE · **Upstream:** https://github.com/the-anticloud/anticloud-codecarbon.git · **Upstream pin:** `7929a4fced51669db1ed9eda21cfd342f76d8abf` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

![banner](docs/images/banner.png)

# Track & reduce CO₂ emissions from your local computing

Estimate and track carbon emissions from your computer, quantify and analyze their impact.

[![](https://img.shields.io/pypi/v/codecarbon?color=024758)](https://pypi.org/project/codecarbon/) [![DOI](https://zenodo.org/badge/263364731.svg)](https://zenodo.org/badge/latestdoi/263364731) [![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/mlco2/codecarbon/badge)](https://scorecard.dev/viewer/?uri=github.com/mlco2/codecarbon) [![codecov](https://codecov.io/gh/mlco2/codecarbon/graph/badge.svg)](https://codecov.io/gh/mlco2/codecarbon) [![Discord](https://img.shields.io/badge/Discord-Join%20Community-7289da?logo=discord&logoColor=white)](https://discord.gg/GS9js2XkJR)

- **A lightweight, easy to use Python library** – Simple API to track emissions
- **Open source, free & community driven** – Built by and for the community
- **Effective visual outputs** – Put emissions in context with real-world equivalents

> **Tracking GenAI API calls?** CodeCarbon measures emissions from **local computing** (your hardware). To track emissions from remote GenAI API calls (OpenAI, Anthropic, Mistral, etc.), use [**EcoLogits**](https://ecologits.ai/). Both tools are complementary.

> **Join the community!** Have questions, want to share your work, or contribute? Join us on [**Discord**](https://discord.gg/GS9js2XkJR) – we're here to help and excited to hear from you!

## Installation

```bash
pip install codecarbon
```

If you use Conda:

```bash
conda activate your_env
pip install codecarbon
```

More installation options: [installation docs](https://docs.codecarbon.io/latest/how-to/installation/).

## Quickstart (Python)

```python
from codecarbon import EmissionsTracker

tracker = EmissionsTracker()
tracker.start()

# Your code here

emissions = tracker.stop()
print(f"Emissions: {emissions} kg CO₂")
```

[**Learn more** →](https://docs.codecarbon.io/latest/tutorials/first-tracking/)

## Quickstart (CLI)

Track a command without changing your code:

```bash
codecarbon monitor --no-api -- python train.py
```

Detect your hardware:

```bash
codecarbon detect
```

Full CLI guide: [CLI tutorial](https://docs.codecarbon.io/latest/tutorials/cli/).

## Configuration

You can configure CodeCarbon using:

- `~/.codecarbon.config` (global)
- `./.codecarbon.config` (project-local)
- `CODECARBON_*` environment variables
- Python arguments (`EmissionsTracker(...)`)

Configuration precedence and examples: [configuration guide](https://docs.codecarbon.io/latest/how-to/configuration/).

## How it works

We created a Python package that estimates your hardware electricity power consumption (GPU + CPU + RAM) and we apply to it the carbon intensity of the region where the computing is done.

CodeCarbon focuses on the main compute components it can measure or estimate directly: CPU, GPU, and RAM. It does not separately model disk I/O, network transfers, displays, cooling, or other peripherals because those sources are usually much smaller for local code-level experiments and are not exposed through the same low-overhead measurement interfaces.

![calculation Summary](docs/images/calculation.png)

We explain more about this calculation in the [**Methodology**](https://docs.codecarbon.io/latest/explanation/methodology/) section of the documentation.

## Visualize

You can visualize your experiment emissions on the [dashboard](https://dashboard.codecarbon.io/) or locally with [carbonboard](https://docs.codecarbon.io/latest/how-to/visualize/).

![dashboard](docs/images/dashboard.png)

## Quick links

| Section                                                                                               | Description                                |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| [Quickstart](https://docs.codecarbon.io/latest/tutorials/first-tracking/)                             | Get started in 5 minutes                   |
| [Installation](https://docs.codecarbon.io/latest/how-to/installation/)                                | Install CodeCarbon                         |
| [CLI Tutorial](https://docs.codecarbon.io/latest/tutorials/cli/)                                      | Track emissions from the command line      |
| [Python API Tutorial](https://docs.codecarbon.io/latest/tutorials/python-api/)                        | Track emissions in Python code             |
| [Comparing Model Efficiency](https://docs.codecarbon.io/latest/tutorials/comparing-model-efficiency/) | Measure carbon efficiency across ML models |
| [API Reference](https://docs.codecarbon.io/latest/reference/api/)                                     | Full parameter documentation               |
| [Framework examples (scikit-learn)](https://docs.codecarbon.io/latest/how-to/scikit-learn/)           | Task-oriented ML framework examples        |
| [Methodology](https://docs.codecarbon.io/latest/explanation/methodology/)                             | How emissions are calculated               |
| [When to use CodeCarbon vs EcoLogits](https://docs.codecarbon.io/latest/explanation/when-to-use/)     | Choose the right tool                      |
| [EcoLogits](https://ecologits.ai/)                                                                    | Track emissions from GenAI API calls       |
| [Discord Community](https://discord.gg/GS9js2XkJR)                                                    | Chat with us and the community             |

## Links

- [Main website](https://codecarbon.io) to learn why we do this.
- [Dashboard](https://dashboard.codecarbon.io/) to see your emissions.
- [Documentation](https://docs.codecarbon.io/) to learn how to use the package and our methodology.
- [EcoLogits](https://ecologits.ai/) to track emissions from GenAI API calls (OpenAI, Anthropic, etc.).
- [mlco2 on GitHub](https://github.com/mlco2) for our othe

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml; scanned in UPSTREAM_CLONE)
- Top-level source layout: `act/`, `benchmarks/`, `carbonserver/`, `codecarbon/`, `deploy/`, `docker/`, `examples/`, `requirements/`, `scripts/`, `tests/`, `webapp/`
- Snapshot size: **622 files**, **53579 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (278), `.tsx` (85), `.md` (51), `.ts` (35), `.csv` (29), `.png` (23)
- Upstream commit pinned for this packaging: `7929a4fced51669db1ed9eda21cfd342f76d8abf`

---

## Installation

```bash
pip install codecarbon
```

If you use Conda:

```bash
conda activate your_env
pip install codecarbon
```

More installation options: [installation docs](https://docs.codecarbon.io/latest/how-to/installation/).

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- **Open source, free & community driven** – Built by and for the community
- **Effective visual outputs** – Put emissions in context with real-world equivalents

> **Tracking GenAI API calls?** CodeCarbon measures emissions from **local computing** (your hardware). To track emissions from remote GenAI API calls (OpenAI, Anthropic, Mistral, etc.), use [**EcoLogits**](https://ecologits.ai/). Both tools are complementary.

> **Join the community!** Have questions, want to share your work, or contribute? Join us on [**Discord**](https://discord.gg/GS9js2XkJR) – we're here to help and excited to hear from you!

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

- **A lightweight, easy to use Python library** – Simple API to track emissions
- **Open source, free & community driven** – Built by and for the community
- **Effective visual outputs** – Put emissions in context with real-world equivalents

> **Tracking GenAI API calls?** CodeCarbon measures emissions from **local computing** (your hardware). To track emissions from remote GenAI API calls (OpenAI, Anthropic, Mistral, etc.), use [**EcoLogits**](https://ecologits.ai/). Both tools are complementary.

> **Join the community!** Have questions, want to share your work, or contribute? Join us on [**Discord**](https://discord.gg/GS9js2XkJR) – we're here to help and excited to hear from you!

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml |
| Files in snapshot | 622 |
| Lines of code | 53579 |
| Dependency references | 58 |
| Dependencies by ecosystem | npm: 45, pypi: 13 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| pypi | arrow | - | pyproject.toml |
| pypi | authlib | >=1.2.1 | pyproject.toml |
| pypi | joserfc | >=1.0.0 | pyproject.toml |
| pypi | click | - | pyproject.toml |
| pypi | pandas | >=2.3.3 | pyproject.toml |
| pypi | 3.14 | - | pyproject.toml |
| npm | @radix-ui/react-dialog | ^1.1.15 | webapp/package.json |
| npm | @radix-ui/react-dropdown-menu | ^2.1.16 | webapp/package.json |
| npm | @radix-ui/react-label | ^2.1.8 | webapp/package.json |
| npm | @radix-ui/react-popover | ^1.1.15 | webapp/package.json |
| npm | @radix-ui/react-select | ^2.2.6 | webapp/package.json |
| npm | @radix-ui/react-separator | ^1.1.8 | webapp/package.json |
| npm | @radix-ui/react-slot | ^1.2.4 | webapp/package.json |
| npm | @radix-ui/react-switch | ^1.2.6 | webapp/package.json |
| npm | @radix-ui/react-tabs | ^1.1.13 | webapp/package.json |
| ... | (43 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- `.env.example`
- `.isort.cfg`
- `docker-compose.yml`
- `pyproject.toml`
- `pytest.ini`

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `CODECARBON` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2019 Mila, BCG Gamma, CometML, Haverford College
Copyright (c) 2023 Code Carbon NGO

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `CODECARBON` (category: CARBON CAPTURE)
- **Upstream URL:** https://github.com/the-anticloud/anticloud-codecarbon.git
- **Pinned commit (SHA):** `7929a4fced51669db1ed9eda21cfd342f76d8abf`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`abc83f2b4774dd5dc83bc38b2363b7f90b14739da11a38c661bc322bdb36399d`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

