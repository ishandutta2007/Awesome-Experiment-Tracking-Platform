# Awesome-Experiment-Tracking-Platform

# Top Experiment Tracking Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on ML Experiment Logging, Run Comparison, Artifact Versioning & Model Lineage*  
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Experiment Tracking**. These tools help ML engineers and data scientists log metrics, hyperparameters, and artifacts across training runs, compare experiment results, and maintain reproducibility across the model development lifecycle.

**Examples** include Weights & Biases, MLflow, Neptune.ai, Comet ML, ClearML, Aim, Guild AI, Sacred, DagsHub, DVC Studio, AimStack, and Polyaxon (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom tracking backends, and transparent experiment data — ideal for ML teams that need full control over training metadata without per-seat SaaS fees or vendor lock-in.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Weights & Biases](https://wandb.ai/)**
  AI developer platform for experiment tracking, model management, and hyperparameter tuning. Log metrics and artifacts with a few lines of code, review results in interactive dashboards, and export data via Public API. Integrated with Keras, PyTorch, HuggingFace, XGBoost, and more . W&B Sweeps provides hyperparameter optimization. Free tier available.

- **[Neptune.ai](https://neptune.ai/)**
  Scalable experiment tracker for teams training foundation models. Neptune Scale (v3) is built on a new architecture focused on responsiveness and accuracy at scale, with experiment forking, charts, and multi-project reports . Custom views, dashboards, and reports for analyzing runs across projects .

- **[Comet ML](https://www.comet.com/)**
  Experiment management platform with automatic logging, dataset versioning, and model registry. Add two lines of code to track experiments with any framework (Keras, PyTorch, etc.). VPC and on-premises deployments treated as first-class citizens . Free tier available with no credit card .

- **[ClearML](https://clear.ml/)**
  Open-core MLOps platform with experiment tracking as a core module. Tracks code, configurations, results, and datasets; compares runs; reproduces experiments; manages artifacts . Used by WSC Sports for scaling ML with Kubernetes and ArgoCD . The open-source core is free; enterprise features are commercial.

- **[DagsHub](https://dagshub.com/)**
  Collaborative platform for AI teams built on MLflow. Send experiments to a collaborative, reproducible experiment manager with custom charts and artifact comparisons. Integrates DVC for data versioning and lineage . Free tier includes unlimited public repos and up to 100 tracked experiments in private repos; Team at $99/user/month .

- **[DVC Studio](https://studio.iterative.ai/)**
  Central hub for teams to manage projects, experiments, and models. Built on DVC (Data Version Control) with Git-based experiment tracking. Run experiments in the cloud and compare results in terminal, VS Code extension, or DVC Studio .

- **[Polyaxon](https://polyaxon.com/)**
  AI engineering control plane for training, agents, evaluation, observability, and infrastructure. Experiment and run tracking with parameters, metrics, logs, code versions, artifacts, visualizations, lineage, and runtime state. Runs on your own Kubernetes infrastructure .

- **[Guild AI](https://guild.ai/)**
  Experiment tracking and Bayesian optimization platform. Automatically records model runs, hyperparameters, and outputs without manual logging. Supports hyperparameter tuning with Bayesian optimization . Python-based with `pip install guildai` and `guild run your_script.py` .

- **[Sacred](https://github.com/IDSIA/sacred)**
  Open-source experiment tracking tool (see Open-Source section below).

## Open-Source GitHub Projects

- **[MLflow](https://github.com/mlflow/mlflow)**
  The most widely adopted open-source ML lifecycle platform. Experiment tracking via `mlflow.log_param()`, `mlflow.log_metric()`, and `mlflow.log_artifact()`. Runs are organized into experiments; models are collections of artifacts . Tracking API communicates with an MLflow tracking server (Python, Java, R APIs) . Databricks provides a hosted tracking server with no setup required . Also includes Model Registry and Projects. **Apache-2.0**.

- **[Aim](https://github.com/aimhubio/aim)**
  Easy-to-use and supercharged open-source experiment tracker. Built to handle thousands of training runs with fast UI comparison . Tracked params are first-class citizens — search, group, aggregate via params across metrics, images, and distributions . Aim QL query language for advanced filtering (`metric.name == 'loss'`). Remote tracking server for multi-host environments; Docker image and Kubernetes deployment guide available . Python SDK for programmatic access (`Repo.query_metrics()`, `Repo.query_runs()`) . **Apache-2.0**.

- **[ClearML](https://github.com/allegroai/clearml)** (Open-Source Core)
  The open-source core of ClearML's MLOps platform. Experiment tracking, data management, and orchestration. WSC Sports uses ClearML as the central hub for managing ML experiments, tracking code/configurations/results, comparing runs, and reproducing experiments . Ultraleap uses ClearML for managing model lineage across 90+ hand tracking model variations . **Apache-2.0** (core).

- **[Guild AI](https://github.com/guildai/guildai)** (Open-Source Core)
  Open-source experiment tracking and hyperparameter optimization. Automatically records model runs, hyperparameters, outputs, and system metrics without code changes. Bayesian optimization for hyperparameter tuning . R interface available via `guildai` package . **Apache-2.0**.

- **[Sacred](https://github.com/IDSIA/sacred)**
  Open-source experiment tracking and configuration management tool. Helps configure, organize, log, and reproduce experiments. MongoDB backend for storing experiment data. **MIT**.

- **[DVC (Data Version Control)](https://github.com/iterative/dvc)**
  Git-based experiment tracking and data versioning. Captures changesets (input data, source code, hyperparameters, artifacts) automatically. DVC Experiments organized along Git commits, branches, and tags . Language-agnostic — works with Jupyter notebooks, CSV data frames, HDFS, or Scala . **Apache-2.0**.

### Additional Strong Open-Source Options

- **Lightweight Trackers**: **Aim** (fast UI, param-first comparison), **Sacred** (MongoDB-backed, research-focused).
- **Full MLOps Platforms**: **MLflow** (most adopted, model registry), **ClearML** (orchestration + tracking), **Polyaxon** (Kubernetes-native control plane).
- **Git-Native Tracking**: **DVC** (Git-based experiment tracking), **DagsHub** (MLflow + DVC collaboration layer).
- **Hyperparameter Optimization**: **Guild AI** (Bayesian optimization built-in), **Optuna** (integration with MLflow and others).

**Frameworks for building custom systems**: Combine **MLflow** for the tracking server and model registry, **Aim** for fast run comparison UI, **DVC** for Git-based data and experiment versioning, and **PostgreSQL** for backend persistence. Add **Guild AI** for Bayesian hyperparameter optimization and **Docker** for deployment.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Experiment tracking platforms store sensitive model metadata; ensure proper access controls and data retention policies.
- Self-hosted open-source solutions require infrastructure for the tracking server, database, and artifact storage (S3, GCS, or local filesystem).

---

**Made for ML engineers, data scientists, MLOps practitioners, and research teams.**  
Let's make experiment tracking more open, reproducible, and scalable.
