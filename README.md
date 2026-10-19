# Repolex Knowledge Graph of amitt001/delegator.py

RDF knowledge graph data for [amitt001/delegator.py](https://github.com/amitt001/delegator.py), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download amitt001/delegator.py
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 194aa92543fbdbfbae0bcc24ca217819a7805da2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 194aa92543fbdbfbae0bcc24ca217819a7805da2
│           └── chunk-001.nq.gz
├── blob
│   ├── 00bf847d1b55d4e63b5a3f73df3188ca9f8dad21.nq.gz
│   ├── 10434987ae13f9aed4735f6206fd4f1496c92afb.nq.gz
│   ├── 108e6788db144c1afb2b4c4a33833c802676ed16.nq.gz
│   ├── 2c562e0353a5b11a152473ac8e8074450537b064.nq.gz
│   ├── 47800a2da56b348d289ebe4203bb7a3e5f3b44e8.nq.gz
│   ├── 645eb1360872f250e067d5fefa8b1efe2ba02565.nq.gz
│   ├── 9ac7613cb0ac75941535e4a99cc117cccf789755.nq.gz
│   ├── aae603d25a26f645e43c03d476c51ed1cc9afced.nq.gz
│   ├── aea5d1a5d68ca034199b928198227a29f1957393.nq.gz
│   └── e19a6e4f600d786a48fc2ec45727a448cb7a54ed.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 194aa92543fbdbfbae0bcc24ca217819a7805da2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 18 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[amitt001/delegator.py](https://github.com/amitt001/delegator.py)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
