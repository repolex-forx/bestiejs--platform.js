# Repolex Knowledge Graph of bestiejs/platform.js

RDF knowledge graph data for [bestiejs/platform.js](https://github.com/bestiejs/platform.js), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download bestiejs/platform.js
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dbddee14240800718d03b1a905e0538cf0ac4c45
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── dbddee14240800718d03b1a905e0538cf0ac4c45.nq.gz
│   └── repolex
│       └── dbddee14240800718d03b1a905e0538cf0ac4c45
│           └── chunk-001.nq.gz
├── blob
│   ├── 176a458f94e0ea5272ce67c36bf30b6be9caf623.nq.gz
│   ├── 2dfda64b337525f84eff5b955d31a075cdc5fec0.nq.gz
│   ├── 43979e42d67d570ffaf6d13e7b4c8e8a2c3d1e7f.nq.gz
│   ├── 74b101811dca53aa4a051583fa8e218537efbc29.nq.gz
│   ├── 7556b47244f7b4e4aabb5dff9360b9a87c3eab32.nq.gz
│   ├── 76645acb1b719a1a0acca29991d726700a6f5903.nq.gz
│   ├── 77f935b974eb0302e5afc7da577650b64192707c.nq.gz
│   ├── 97ff3f8edeb9d9519e418a2eeb3a4b3939edf795.nq.gz
│   ├── b64e10ae509fb71333fc00a7c778e5ff1722f8a0.nq.gz
│   ├── c00456bb6e424a57c26ffb86ad9e0853fcfcf313.nq.gz
│   ├── d2b761de0f376c86e006076743ec3e0924811dc0.nq.gz
│   ├── d7e3a4e8e327902b0cdcfeae6e00745ee48f38d2.nq.gz
│   ├── dbfb940e3824ca2e14eb188030ccfc9aad7f877f.nq.gz
│   └── f202f446b8ee4009314da567c2b23705ab8f07f3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── dbddee14240800718d03b1a905e0538cf0ac4c45.nq.gz
├── filetree
│   └── dbddee14240800718d03b1a905e0538cf0ac4c45.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 24 files
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

## Source repository

[bestiejs/platform.js](https://github.com/bestiejs/platform.js)

---
*Parsed on 2026-09-15 by [repolex](https://repolex.ai)*
