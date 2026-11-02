# Repolex Knowledge Graph of sean2077/jsonpath-python

RDF knowledge graph data for [sean2077/jsonpath-python](https://github.com/sean2077/jsonpath-python), parsed by [repolex](https://repolex.ai).

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
rlex download sean2077/jsonpath-python
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 03c547cccb3b0b44c3fccdcc25a193fca8550816
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 03c547cccb3b0b44c3fccdcc25a193fca8550816
│           └── chunk-001.nq.gz
├── blob
│   ├── 052eb1ead3dd4edcd4fb44ea71504d7577a95764.nq.gz
│   ├── 09cf6a2701838b043e252f25f30f85b449152223.nq.gz
│   ├── 18233fc63cf77efec6014d50de52dc2102d900e4.nq.gz
│   ├── 1c080e726839233a5c51e68d323f576526508562.nq.gz
│   ├── 1c6f5e319431264d43801aa95cc18c360de62aac.nq.gz
│   ├── 3bd80a3d6371f8ad42e8b0294b06159c28788c13.nq.gz
│   ├── 44e6c77b25862d1905c7f4f3f53440ff16dab2b2.nq.gz
│   ├── 5c2d91b9a6d47b27ea06b9c9cbdd99c3bd1061b2.nq.gz
│   ├── 61b867d5a9b46c084a23bb63c20f799c9088f221.nq.gz
│   ├── 6b5b356089032d5b4dbe3f16bb7bea43409f00b9.nq.gz
│   ├── 795a5bbdc2de01007eca0ba6b60994a2d8626404.nq.gz
│   ├── 84b503d1a2bea8e4aa18e5bb96c9f1dc5de299e3.nq.gz
│   ├── 84e2a9d6585dedcc4349d4b9cb63662aaf138bb3.nq.gz
│   ├── 935f90be7322c55dac784a847142432a0494fc82.nq.gz
│   ├── a0fe54ceb2fe71203e153791894ef0f23e0d4a42.nq.gz
│   ├── b64669235147ac2d22c3ae71f003da10e8cd1dae.nq.gz
│   ├── c276ea983b25d784dbaaa88c662a627ffb6b277a.nq.gz
│   ├── e0ecee3178ee10ab19b2b3b282f6a80aa257ce83.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7287a3bddc5a3b59095c32035e8f28b953734e4.nq.gz
│   ├── ebf8639b4bd99dd5c17cb151ed059521e64c009c.nq.gz
│   ├── edd944c14745e29eac7deda3f179ba977d0fd469.nq.gz
│   ├── f7f5082344f6d3a285d2aa7673fca71a13df63f9.nq.gz
│   └── fb9e5cac8c61aea8d26ec26c0ca52e9e01374fc8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 03c547cccb3b0b44c3fccdcc25a193fca8550816.nq.gz
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

[sean2077/jsonpath-python](https://github.com/sean2077/jsonpath-python)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
