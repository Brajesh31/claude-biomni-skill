# Claude Biomni Skill

A Claude skill for using Biomni, an autonomous biomedical AI agent framework, to support multi-step research tasks across genomics, molecular biology, drug discovery, and clinical analysis.

## What It Covers

- **Biomedical reasoning:** Break down complex research questions into multi-step workflows.
- **CRISPR screening:** Support screen design, gene prioritization, and interpretation.
- **Single-cell RNA sequencing:** Guide quality control, cell clustering, annotation, and differential expression analysis.
- **Drug discovery:** Work with ADMET prediction, target identification, and compound optimization.
- **GWAS interpretation:** Connect variants to genes, pathways, and potential functional consequences.
- **Clinical genomics:** Support rare-disease and variant interpretation workflows.
- **Laboratory protocols:** Assist with protocol analysis and optimization.
- **Data integration:** Work with biomedical databases, literature, pathways, and related resources.

## Installation

Clone this repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-biomni-skill.git ~/.claude/skills/biomni
```

Install Biomni in the Python environment used for execution:

```bash
uv pip install biomni --upgrade
```

Configure the required LLM provider credentials through environment variables or a secure `.env` file. Do not commit credentials.

## Using the Skill

Example request:

```text
Use the biomni skill to plan a single-cell RNA-seq analysis, including
quality control, clustering, cell-type annotation, and differential
expression.
```

Other workflows can include CRISPR screen planning, ADMET prediction, GWAS interpretation, and protocol optimization. Supply the organism, biological context, input data paths, constraints, and desired output format.

## Safety and Execution

Biomni may execute generated code with broad system privileges. Use an isolated environment, review generated code before running it on sensitive systems, and avoid exposing credentials or confidential data. Biomedical and clinical outputs require domain-appropriate validation and must not be treated as a substitute for expert review.

## Repository Resources

- [SKILL.md](SKILL.md) contains the main instructions and workflows.
- `references/api_reference.md` documents the API and configuration.
- `references/llm_providers.md` describes LLM provider setup.
- `references/use_cases.md` provides examples across biomedical domains.
- `scripts/` contains environment setup and report-generation helpers.
