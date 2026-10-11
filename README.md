# Repolex Knowledge Graph of pytest-dev/pytest-stress

RDF knowledge graph data for [pytest-dev/pytest-stress](https://github.com/pytest-dev/pytest-stress), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-stress
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2f4a6fb8a3be26963854a3ed7f341668b3cdeefa
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2f4a6fb8a3be26963854a3ed7f341668b3cdeefa
│           └── chunk-001.nq.gz
├── blob
│   ├── 00c33a352c1389369605b96a5c9a2f8f49716b78.nq.gz
│   ├── 1ade348bb74d5b25edb2813cc00395dfc3e6c53f.nq.gz
│   ├── 26c47cc7599864181c6cdccd55e9e4b54feeb823.nq.gz
│   ├── 2baacb64c4fc4651dd41d422e4ffc6ca8331208a.nq.gz
│   ├── 2c4861a11f9a0d61812b85ca4bf7667618ddce14.nq.gz
│   ├── 2d3788f5249bc7a8e078c0f53242a3807fcad173.nq.gz
│   ├── 4079a340cbab888bcb2ff0dad7a8d83b51b2e30b.nq.gz
│   ├── 491a3d33f8c2459e06e9a37b7aaf96daa9daddab.nq.gz
│   ├── 4b7fe0f73b0a52ea934bce0e9d6c9e4598f6507b.nq.gz
│   ├── 65b1c126f0b9c6a1cd7371fa82dc3f3a44d9a0ff.nq.gz
│   ├── a2d7a05aa9b2bb6caab2fb43067da2a85608d927.nq.gz
│   ├── a3a7289ff2632e4d0ff5ab9bed982d1e8738ecfc.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f88aab601c1db23497a99c79a3958a812a47aaf6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2f4a6fb8a3be26963854a3ed7f341668b3cdeefa.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[pytest-dev/pytest-stress](https://github.com/pytest-dev/pytest-stress)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
