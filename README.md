# ALLENNLP

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-academia_rd-lightgrey)

> Anticloud-hardened packaging of the upstream project `ALLENNLP` in category **ACADEMIA RD**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** ACADEMIA RD · **Upstream:** https://github.com/allenai/allennlp · **Upstream pin:** `80fb6061e568cb9d6ab5d45b661e86eb61b92c82` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<div align="center">
    <br>
    <img src="https://raw.githubusercontent.com/allenai/allennlp/main/docs/img/allennlp-logo-dark.png" width="400"/>
    <p>
    An Apache 2.0 NLP research library, built on PyTorch, for developing state-of-the-art deep learning models on a wide variety of linguistic tasks.
    </p>
    <hr/>
</div>
<p align="center">
    <a href="https://github.com/allenai/allennlp/actions">
        <img alt="CI" src="https://github.com/allenai/allennlp/workflows/CI/badge.svg?event=push&branch=main">
    </a>
    <a href="https://pypi.org/project/allennlp/">
        <img alt="PyPI" src="https://img.shields.io/pypi/v/allennlp">
    </a>
    <a href="https://github.com/allenai/allennlp/blob/main/LICENSE">
        <img alt="License" src="https://img.shields.io/github/license/allenai/allennlp.svg?color=blue&cachedrop">
    </a>
    <a href="https://codecov.io/gh/allenai/allennlp">
        <img alt="Codecov" src="https://codecov.io/gh/allenai/allennlp/branch/main/graph/badge.svg">
    </a>
    <a href="https://optuna.org">
        <img alt="Optuna" src="https://img.shields.io/badge/Optuna-integrated-blue">
    </a>
    <br/>
</p>

⚠️ **NOTICE:** The AllenNLP library is now in maintenance mode. That means we are no longer adding new features or upgrading dependencies. We will still respond to questions and address bugs as they arise up until December 16th, 2022. If you have any concerns or are interested in maintaining AllenNLP going forward, please open an issue on this project.

AllenNLP has been a big success, but as the field is advancing quickly it's time to focus on new initiatives. We're working hard to make [AI2 Tango](https://github.com/allenai/tango) the best way to organize research codebases. If you are an active user of AllenNLP, here are some suggested alternatives:
* If you like the trainer, the configuration language, or are simply looking for a better way to manage your experiments, check out [AI2 Tango](https://github.com/allenai/tango).
* If you like AllenNLP's `modules` and `nn` packages, check out [delmaksym/allennlp-light](https://github.com/delmaksym/allennlp-light). It's even compatible with [AI2 Tango](https://github.com/allenai/tango)!
* If you like the framework aspect of AllenNLP, check out [flair](https://github.com/flairNLP/flair). It has multiple state-of-art NLP models and allows you to easily use pretrained embeddings such as those from transformers.
* If you like the AllenNLP metrics package, check out [torchmetrics](https://torchmetrics.readthedocs.io/en/stable/). It has the same API as AllenNLP, so it should be a quick learning curve to make the switch.
* If you want to vectorize text, try [the transformers library](https://github.com/huggingface/transformers).
* If you want to maintain the AllenNLP Fairness or Interpret components, please get in touch. There is no alternative to it, so we are looking for a dedicated maintainer.
* If you are concerned about other AllenNLP functionality, please create an issue. Maybe we can find another way to continue supporting your use case.

## Quick Links

- ↗️ [Website](https://allennlp.org/)
- 🔦 [Guide](https://guide.allennlp.org/)
- 🖼 [Gallery](https://gallery.allennlp.org)
- 💻 [Demo](https://demo.allennlp.org)
- 📓 [Documentation](https://docs.allennlp.org/) ( [latest](https://docs.allennlp.org/latest/) | [stable](https://docs.allennlp.org/stable/) | [commit](https://docs.allennlp.org/main/) )
- ⬆️ [Upgrade Guide from 1.x to 2.0](https://github.com/allenai/allennlp/discussions/4933)
- ❓ [Stack Overflow](https://stackoverflow.com/questions/tagged/allennlp)
- ✋ [Contributing Guidelines](CONTRIBUTING.md)
- 🤖 [Officially Supported Models](https://github.com/allenai/allennlp-models)
    - [Pretrained Models](https://github.com/allenai/allennlp-models/blob/main/allennlp_models/pretrained.py)
    - [Documentation](https://docs.allennlp.org/models/) ( [latest](https://docs.allennlp.org/models/latest/) | [stable](https://docs.allennlp.org/models/stable/) | [commit](https://docs.allennlp.org/models/main/) )
- ⚙️ [Continuous Build](https://github.com/allenai/allennlp/actions)
- 🌙 [Nightly Releases](https://pypi.org/project/allennlp/#history)

## In this README

- [Getting Started Using the Library](#getting-started-using-the-library)
- [Plugins](#plugins)
- [Package Overview](#package-overview)
- [Installation](#installation)
    - [Installing via pip](#installing-via-pip)
    - [Installing using Docker](#installing-using-docker)
    - [Installing from source](#installing-from-source)
- [Running AllenNLP](#running-allennlp)
- [Issues](#issues)
- [Contributions](#contributions)
- [Citing](#citing)
- [Team](#team)

## Getting Started Using the Library

If you're interested in using AllenNLP for model development, we recommend you check out the
[AllenNLP Guide](https://guide.allennlp.org) for a thorough introduction to the library, followed by our more advanced guides
on [GitHub Discussions](https://github.com/allenai/allennlp/discussions/categories/guides).

When you're ready to start your project, we've created a couple of template projects that you can use as a starting place:

* If you want to use `allennlp train` and config files to specify experiments, use [this
  template](https://github.com/allenai/allennlp-template-config-files). We recommend this approach.
* If you'd prefer to use python code to configure your experiments and run your training loop, use
  [this template](https://github.com/allenai/allennlp-template-python-script). There are a few
  things that are currently a little harder in this setup (loading a saved model, and using
  distributed training), but otherwise it's functionality equivalent to the config files
  setup.

In addition, there are external tutorials:

* [Hyperparameter optimization for AllenNLP using Optuna](https://medium.com/optuna/hyperparameter-optimization-for-allennlp-using-optuna-54b4bfecd78b)
* [Training with multiple GPUs in AllenNLP](https://medium.com/ai2-blog/tuto

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml, requirements.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `allennlp/`, `benchmarks/`, `scripts/`, `test_fixtures/`, `tests/`
- Upstream commit pinned for this packaging: `80fb6061e568cb9d6ab5d45b661e86eb61b92c82`

---

## Installation

- 🌙 [Nightly Releases](https://pypi.org/project/allennlp/#history)

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

* If you like the AllenNLP metrics package, check out [torchmetrics](https://torchmetrics.readthedocs.io/en/stable/). It has the same API as AllenNLP, so it should be a quick learning curve to make the switch.
* If you want to vectorize text, try [the transformers library](https://github.com/huggingface/transformers).
* If you want to maintain the AllenNLP Fairness or Interpret components, please get in touch. There is no alternative to it, so we are looking for a dedicated maintainer.
* If you are concerned about other AllenNLP functionality, please create an issue. Maybe we can find another way to continue supporting your use case.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

* If you like the framework aspect of AllenNLP, check out [flair](https://github.com/flairNLP/flair). It has multiple state-of-art NLP models and allows you to easily use pretrained embeddings such as those from transformers.
* If you like the AllenNLP metrics package, check out [torchmetrics](https://torchmetrics.readthedocs.io/en/stable/). It has the same API as AllenNLP, so it should be a quick learning curve to make the switch.
* If you want to vectorize text, try [the transformers library](https://github.com/huggingface/transformers).
* If you want to maintain the AllenNLP Fairness or Interpret components, please get in touch. There is no alternative to it, so we are looking for a dedicated maintainer.
* If you are concerned about other AllenNLP functionality, please create an issue. Maybe we can find another way to continue supporting your use case.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml, requirements.txt |
| Files in snapshot | not captured in this benchmark snapshot |
| Lines of code | not captured in this benchmark snapshot |
| Dependency references | not captured in this benchmark snapshot |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

* If you like AllenNLP's `modules` and `nn` packages, check out [delmaksym/allennlp-light](https://github.com/delmaksym/allennlp-light). It's even compatible with [AI2 Tango](https://github.com/allenai/tango)!
* If you like the framework aspect of AllenNLP, check out [flair](https://github.com/flairNLP/flair). It has multiple state-of-art NLP models and allows you to easily use pretrained embeddings such as those from transformers.
* If you like the AllenNLP metrics package, check out [torchmetrics](https://torchmetrics.readthedocs.io/en/stable/). It has the same API as AllenNLP, so it should be a quick learning curve to make the switch.
* If you want to vectorize text, try [the transformers library](https://github.com/huggingface/transformers).
* If you want to maintain the AllenNLP Fairness or Interpret components, please get in touch. There is no alternative to it, so we are looking for a dedicated maintainer.
* If you are concerned about other AllenNLP functionality, please create an issue. Maybe we can find another way to continue supporting your use case.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing

Thanks for considering contributing!  We want AllenNLP to be *the way* to do cutting-edge NLP research, but we cannot
get there without community support.

## How Can I Contribute?

### Bug fixes and new features

**Did you find a bug?**

First, do [a quick search](https://github.com/allenai/allennlp/issues) to see whether your issue has already been reported.
If your issue has already been reported, please comment on the existing issue.

Otherwise, open [a new GitHub issue](https://github.com/allenai/allennlp/issues).  Be sure to include a clear title
and description.  The description should include as much relevant information as possible.  The description should
explain how to reproduce the erroneous behavior as well as the behavior you expect to see.  Ideally you would include a
code sample or an executable test case demonstrating the expected behavior.

**Do you have a suggestion for an enhancement?**

We use GitHub issues to track enhancement requests.  Before you create an enhancement request:

* Make sure you have a clear idea of the enhancement you would like.  If you have a vague idea, consider discussing
it first on a GitHub issue.

* Check the documentation to make sure your feature does not already exist.

* Do [a quick search](https://github.com/allenai/allennlp/issues) to see whether your enhancement has already been suggested.

When creating your enhancement request, please:

* Provide a clear title and description.

* Explain why the enhancement would be useful.  It may be helpful to highlight the feature in other libraries.

* Include code examples to demonstrate how the enhancement would be used.

### Making a pull request

When you're ready to contribute code to address an open issue, please follow these guidelines to help us be able to review your pull request (PR) quickly.

1. **Initial setup** (only do this once)

    <details><summary>Expand details 👇</summary><br/>

    If you haven't already done so, please [fork](https://help.github.com/en/enterprise/2.13/user/articles/fork-a-project) this project on GitHub.
    
    Then source your fork locally with
    
        git source https://github.com/USERNAME/allennlp.git
    
    or 
    
        git source git@github.com:USERNAME/allennlp.git
    
    At this point the local source of your fork only knows that it came from *your* project, github.com/USERNAME/allennlp.git, but doesn't know anything the *main* project, [https://github.com/allenai/allennlp.git](https://github.com/a

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                                 Apache License
                           Version 2.0, January 2004
                        https://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `ALLENNLP` (category: ACADEMIA RD)
- **Upstream URL:** https://github.com/allenai/allennlp
- **Pinned commit (SHA):** `80fb6061e568cb9d6ab5d45b661e86eb61b92c82`
- **Branch:** main
- **Pin provenance:** GitHub API commits/<branch> (response quoted in report). The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`f62bf093e1f03d08ab20f297e46f9053edce5e5632aff98b131b977f6712f0bb`.

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
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

