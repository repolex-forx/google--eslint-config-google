# Repolex Knowledge Graph of google/eslint-config-google

RDF knowledge graph data for [google/eslint-config-google](https://github.com/google/eslint-config-google), parsed by [repolex](https://repolex.ai).

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
rlex download google/eslint-config-google
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0273839fbd6f934258886ca8f875ea4b101a51a6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0273839fbd6f934258886ca8f875ea4b101a51a6
│           └── chunk-001.nq.gz
├── blob
│   ├── 11038e4b6c4c208fc2697ea43055b79d4072f4a1.nq.gz
│   ├── 176a458f94e0ea5272ce67c36bf30b6be9caf623.nq.gz
│   ├── 3c3629e647f5ddf82548912e337bea9826b434af.nq.gz
│   ├── 57a79ff25bae4258629c13b4e56138dd687331f2.nq.gz
│   ├── 99989d76c9dc23b367aab5f0a9ea9a00b516947f.nq.gz
│   ├── c6c8b3621938a4691225a870a59bf382af1883dd.nq.gz
│   ├── e891ca4ec9a46c21990fb358619cf592b9b439e1.nq.gz
│   └── f38fc6e24b4cf34b0b19a0dd2ee41f019f7d57dc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0273839fbd6f934258886ca8f875ea4b101a51a6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 16 files
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

[google/eslint-config-google](https://github.com/google/eslint-config-google)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
