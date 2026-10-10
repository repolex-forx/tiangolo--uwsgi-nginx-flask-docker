# Repolex Knowledge Graph of tiangolo/uwsgi-nginx-flask-docker

RDF knowledge graph data for [tiangolo/uwsgi-nginx-flask-docker](https://github.com/tiangolo/uwsgi-nginx-flask-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/uwsgi-nginx-flask-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0547cf8ecbbf76d582e4173dbe7850f28f725455
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0547cf8ecbbf76d582e4173dbe7850f28f725455
│           └── chunk-001.nq.gz
├── blob
│   ├── 08cf630419248e25fc181744dddc9a3c537f039d.nq.gz
│   ├── 1f9a122b1dd9d29b994569dad9c3a7a4d2c4dd42.nq.gz
│   ├── 2811ded3331f0482bdee78628f167c7668741729.nq.gz
│   ├── 2e0c3ad6139016a4542a9164306fc597e9a2b8e9.nq.gz
│   ├── 327bbb237ddec8e0b246b3672fb74dab7e9a1449.nq.gz
│   ├── 3981ea8992d130f07731f6384bc6838fa13c168e.nq.gz
│   ├── 3c16631faef9c227ce8ae2ce412aa530b81a62f1.nq.gz
│   ├── 3d0372b5afe5727a7550ac57b918f6faf7717740.nq.gz
│   ├── 3d9d5d9104604921177a198d453e3a5b7db720a4.nq.gz
│   ├── 46c8988f1d0e2be0b9dc1031690527b03658aaad.nq.gz
│   ├── 472d2e447835d491a2ecaae7bc78e5d6b3ff6441.nq.gz
│   ├── 4ba40eaca218d2c111ad0e31c1020efa4b33f07d.nq.gz
│   ├── 4d025ed155eb8dad06a2977a24f64c8d1be4f0b7.nq.gz
│   ├── 55eec6eb458d17b0a36c90625488d8fafbda90d5.nq.gz
│   ├── 5fc5f542be61a8ec27f104a4685be273a6350ebd.nq.gz
│   ├── 72d7a762c502b410a9956dc0f3704e22248fd107.nq.gz
│   ├── 7bc3ad2f07be284b5ddab47fbbe6bc241388b709.nq.gz
│   ├── 7d04c80755e75b279bce14d247c8b16e381e3ca1.nq.gz
│   ├── 7f8744773568099727a2d746d2e6858d1fcc7be8.nq.gz
│   ├── 895bb4cc0862ee8415e083f1240143e9ddb532f0.nq.gz
│   ├── 931e56fc11800a8313f4332af32321cfb8f9d3c0.nq.gz
│   ├── 94143827ed065ca0d7d5be1b765d255c5c32cd9a.nq.gz
│   ├── 99bcb1d2d6c6c0901539295c17a5e2757c9f2b46.nq.gz
│   ├── 9d011a7120cca207f9acca44578c8a6d7184b630.nq.gz
│   ├── a3c07031ac4cd9776abe329bd4f98d421292c424.nq.gz
│   ├── ab19af4a32da512387236e8165e76eb9758efe30.nq.gz
│   ├── bb48ddc91df9c2b3560b8c21a9cdbebf4ec27816.nq.gz
│   ├── be56c5b1dd9ffaf17496daafc1926abc77598958.nq.gz
│   ├── c94d562277a586c63f96f5e08e85cef15d9b1a4f.nq.gz
│   ├── ce9df978e06820ea457270fd9adad0bca8141a37.nq.gz
│   ├── da03cc3311e52886fb13f77b2c47df9add315168.nq.gz
│   ├── e6365da06a26a01d40f1af8d71f9d84977a6deb4.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0547cf8ecbbf76d582e4173dbe7850f28f725455.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[tiangolo/uwsgi-nginx-flask-docker](https://github.com/tiangolo/uwsgi-nginx-flask-docker)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
