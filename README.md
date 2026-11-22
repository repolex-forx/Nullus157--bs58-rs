# Repolex Knowledge Graph of Nullus157/bs58-rs

RDF knowledge graph data for [Nullus157/bs58-rs](https://github.com/Nullus157/bs58-rs), parsed by [repolex](https://repolex.ai).

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
rlex download Nullus157/bs58-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2b0d73b9955f6a745f9b6fbb387bba2b96ea89fd
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 2b0d73b9955f6a745f9b6fbb387bba2b96ea89fd.nq.gz
│   └── repolex
│       └── 2b0d73b9955f6a745f9b6fbb387bba2b96ea89fd
│           └── chunk-001.nq.gz
├── blob
│   ├── 05ef147d534b045e33c4c76af79e4fb64734f3a2.nq.gz
│   ├── 11027ea544642ad88f8212137fb8e36568e027ed.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 3f028b136fbdc5b8ac6cc79391a9ccc903b76ed2.nq.gz
│   ├── 3fabf456695a6b84cb2f3d13607521ac8700bc25.nq.gz
│   ├── 463c5ae6704212dbb59843ca56e5e9ebe6055b9b.nq.gz
│   ├── 48c77aa4fe84088b7e696bf4f9604b2de77b9502.nq.gz
│   ├── 4a253fd0e7781bdcda99e51c66d043c3d00988f7.nq.gz
│   ├── 4bc8ed4b4fc2a71702d5b1c3cb3a19b0a87270c6.nq.gz
│   ├── 6d5b3bbdb1954db74b687cfe3b3b4dc0b8b50aa7.nq.gz
│   ├── 74b7327f4ade6b79463ec511848b83b6d865c475.nq.gz
│   ├── 75a61395888ddcba726277424bfafe23517a5da3.nq.gz
│   ├── 76219eb72e8524f15c21ec93b9b2592da49b5460.nq.gz
│   ├── 88ede6bc9ec0004576a3eabf17d1b2dd440297f3.nq.gz
│   ├── 8b455247caa16a229ce18b31945ca006cea20893.nq.gz
│   ├── 8c545b9917b60aa863f5db1e914683d1c083535e.nq.gz
│   ├── 94fca93643691b7759ac8ea28311618d3a61222e.nq.gz
│   ├── 965b606f331b51d566b46025f9ff311a7aad0c12.nq.gz
│   ├── 9d715c6cdca2b1012b46ea7a4aa8240915087678.nq.gz
│   ├── a8ed27024a383513f1f7e3823530c07d7550142b.nq.gz
│   ├── aa15c57ff3097371df1618a47fe43cc868e69dd8.nq.gz
│   ├── ab43a2760be47f6eef645d86d6079657ae544c7e.nq.gz
│   ├── b58b99ae3cc59b82d014909e5e61c1d4f7410961.nq.gz
│   ├── d7d42e697016a47d69edc5beea89ee2971ceba86.nq.gz
│   ├── e60058490df8913c9b689820502f1f7d9d8dc50b.nq.gz
│   ├── eb5a316cbd195d26e3f768c7dd8e1b47299e17f8.nq.gz
│   ├── f521b49c09b1809b308f301e4b5c85ef8299e43a.nq.gz
│   └── fe498128d3b8f14e51c84a78fc1cd54a62bafb45.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 2b0d73b9955f6a745f9b6fbb387bba2b96ea89fd.nq.gz
├── filetree
│   └── 2b0d73b9955f6a745f9b6fbb387bba2b96ea89fd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 38 files
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

[Nullus157/bs58-rs](https://github.com/Nullus157/bs58-rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
