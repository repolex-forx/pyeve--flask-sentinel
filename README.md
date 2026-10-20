# Repolex Knowledge Graph of pyeve/flask-sentinel

RDF knowledge graph data for [pyeve/flask-sentinel](https://github.com/pyeve/flask-sentinel), parsed by [repolex](https://repolex.ai).

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
rlex download pyeve/flask-sentinel
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 05ddb184ac203e9c80c5f25d82122e58c5d8005f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 05ddb184ac203e9c80c5f25d82122e58c5d8005f
│           └── chunk-001.nq.gz
├── blob
│   ├── 09a9f9bb9eee27ac99967a5d43175235650ed7ef.nq.gz
│   ├── 19bb19530bfd44255a14fbf86ade3a6cd12e0df5.nq.gz
│   ├── 23b686a3bb90e7429a77177cfe243bf13fb5c32c.nq.gz
│   ├── 2964c064c4659f056381321f6cebe82dde7075a7.nq.gz
│   ├── 2bce0963759282ef2ce1186d1ee06f400beb20b8.nq.gz
│   ├── 3c26c8be0d77735830e26d16486afbab39208336.nq.gz
│   ├── 429e56936479e6229b47faa54269db4e6c60e8cf.nq.gz
│   ├── 49377e93f6a21583b7d1147e2a65681116bbbc16.nq.gz
│   ├── 54bc84552a3703b0db79e9bf5ad2bcb133574383.nq.gz
│   ├── 63b9499f6aaae63d759c1c1ef38e9582e1652f3e.nq.gz
│   ├── 6df99b94746d21232a81ba469618ff0ef7b64d9f.nq.gz
│   ├── 8731ab872954858a3d03fa85b7292af4db6ba01f.nq.gz
│   ├── 93e4d55f8a8ed4cee22518bee61f47b7d08e0492.nq.gz
│   ├── 988b30a5f9a5aea3cffeeeee0e8f47036a980f1f.nq.gz
│   ├── 99d5176e5c916bbac5a616136fe80dad389650f0.nq.gz
│   ├── b52044829e0f44e69882ae2a69bdc58d354cb717.nq.gz
│   ├── b69bce5a099e791b06ac655e5f48e360dec71873.nq.gz
│   ├── c7e1a55419f49829e78c0310586cd4ab8e7992ce.nq.gz
│   ├── cf4846cd34bbef98635142dfeab7ba4bd699ff59.nq.gz
│   ├── e12db7d5cb7eeb0b46185dec6aa8e750f14c111b.nq.gz
│   ├── e324f6876d999b0b8c7dba0ff7ae8045ac6ad13e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f53c454ee652e13db209db06b4f56ff2bb655872.nq.gz
│   └── fbed8e33af697ea2291ac3d107a841a8c169ceea.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 05ddb184ac203e9c80c5f25d82122e58c5d8005f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[pyeve/flask-sentinel](https://github.com/pyeve/flask-sentinel)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
