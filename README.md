# Repolex Knowledge Graph of agronholm/docker-vernemq

RDF knowledge graph data for [agronholm/docker-vernemq](https://github.com/agronholm/docker-vernemq), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/docker-vernemq
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dca9e7ba5ac75fe107946e3b186472bc15ffcdc2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dca9e7ba5ac75fe107946e3b186472bc15ffcdc2
│           └── chunk-001.nq.gz
├── blob
│   ├── 00f11bcb63e48677b4f497f9e33e9f081302f475.nq.gz
│   ├── 13e39b4753a4024198297f87d5b052c7f4331897.nq.gz
│   ├── 1796b9afd2befda485de68a8adf1729108e92f70.nq.gz
│   ├── 1b64e950e8aa2a72ddc255ec51a3633c458ce76e.nq.gz
│   ├── 2b22bb90335471030c05d5fb748c946be97fca36.nq.gz
│   ├── 2caccea84f5b6b38483273c77e202555b7006e00.nq.gz
│   ├── 2ce47dd086f6b0b3c1f82f0a82332f2110093dc7.nq.gz
│   ├── 2e54dd30c81a24eb6d679e4d859e3fdf1cb6134c.nq.gz
│   ├── 3a38348ebfca434ab67604294bc9ca672df46222.nq.gz
│   ├── 3b4120025c1e0bc944471844d0a6a37a49033327.nq.gz
│   ├── 4375c9869cf0bd4b5c17ada1485c355bc7b6affb.nq.gz
│   ├── 43c34f5cf6b7514d83c0831583e207d1cfa2baf0.nq.gz
│   ├── 45ce732a6a1d51260c652bbdf34ae2ae128381d0.nq.gz
│   ├── 653a8f5bd512f7273096e05444bb5b699d33f65e.nq.gz
│   ├── 8dada3edaf50dbc082c9a125058f25def75e625a.nq.gz
│   ├── 90d82444ec79ea1a1f3a040dd71f3430cf025f81.nq.gz
│   ├── 91063de832e138a31711767e0e5d6b2d4ca2ff03.nq.gz
│   ├── a7db4074f0464b985ac679d1c24addcb735e1209.nq.gz
│   ├── a995edb6ded66b7abd1026afa1e70560b11777cc.nq.gz
│   ├── b8abec91d6e1c9bbceb73b9a7f84a257161fc53c.nq.gz
│   ├── c0a4d32c93e19b0dfe5cd1acbc9ca681c25ddded.nq.gz
│   ├── df8eac5b9723b694f1bd9f7b4120a14d3533ec57.nq.gz
│   ├── eb21d13641203db098ca61fcd84b74a333705e2d.nq.gz
│   ├── f0c13194444163d1cba5c67d9e79231a62bc8f44.nq.gz
│   ├── f3675f46cb1bdbe3a2dd12aa5eac4c19a40d85ff.nq.gz
│   ├── f77df69f016b2e637f3248844e99ade1f0378237.nq.gz
│   └── f8ab3716af84536cab305fce2ba42d9bb751da7f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dca9e7ba5ac75fe107946e3b186472bc15ffcdc2.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 33 files
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

[agronholm/docker-vernemq](https://github.com/agronholm/docker-vernemq)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
