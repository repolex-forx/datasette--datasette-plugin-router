# Repolex Knowledge Graph of datasette/datasette-plugin-router

RDF knowledge graph data for [datasette/datasette-plugin-router](https://github.com/datasette/datasette-plugin-router), parsed by [repolex](https://repolex.ai).

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
rlex download datasette/datasette-plugin-router
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 63e93bafcc54ab7b1ddf599a83c8624a208d63b6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 63e93bafcc54ab7b1ddf599a83c8624a208d63b6
│           └── chunk-001.nq.gz
├── blob
│   ├── 10e2a5456523c97c9eca92f7e3882954386119e2.nq.gz
│   ├── 1f7590aabdbcd5a5a173ced0ea5fc2c35f7ec498.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 3eb871944ba060e652582342cecb018b41f78bda.nq.gz
│   ├── 5390e9d171a99a9d1fdb0632d3fd2d629065a6fd.nq.gz
│   ├── 84a1dd596f804b804f182285d07595410f4091ed.nq.gz
│   ├── b2cbc024a52fc6ec58220395194bb47c76849846.nq.gz
│   ├── c498fb0c70eb054e6b879ed0c10fe56844ee2d70.nq.gz
│   ├── ca46042bf542b3ac1dde52807643367770e8da64.nq.gz
│   ├── caf73c3e1377850c5228b944f5d82a84f9aa666e.nq.gz
│   ├── d49d309499efb2c0c1d38efdd53056249a7d74d8.nq.gz
│   ├── e678a9a2ecc2918ade2fe745d4c70d5535bc218c.nq.gz
│   ├── eb22e74eaaaf0edc4aa2c0f8900a55750d1660f9.nq.gz
│   ├── fc079a8389b519ade7d4c459d2ad1891e9fccd87.nq.gz
│   └── ffb34f27b07633fd71bbb034f131dad8ab1c702a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 63e93bafcc54ab7b1ddf599a83c8624a208d63b6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[datasette/datasette-plugin-router](https://github.com/datasette/datasette-plugin-router)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
