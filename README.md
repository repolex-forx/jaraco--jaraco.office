# Repolex Knowledge Graph of jaraco/jaraco.office

RDF knowledge graph data for [jaraco/jaraco.office](https://github.com/jaraco/jaraco.office), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.office
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cfce41767ac8e91fe02e17ddf4cf551a6a0e565e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cfce41767ac8e91fe02e17ddf4cf551a6a0e565e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a693b0530f8dbb1d122a263dc39368435475a20.nq.gz
│   ├── 0c45117262f7978fbaf878e79998bf224ba128f2.nq.gz
│   ├── 0d1f7edf5dc6343538563a8caa7de6829752c4f9.nq.gz
│   ├── 0de6ab9dd7d7fd5fb43a1f2814cc98094f7de0d6.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 287f07d68fd7bd0da6b28c0e49626ad58e56d89e.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 2feefcc32d5ad7aeb0736f4204745ec4d14715f8.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 379253094796e81bf041d60251b3e73b2855fa78.nq.gz
│   ├── 48a7b5b128d0922edc40fd8df245747c2bf561f9.nq.gz
│   ├── 4e3cdfa0ce6f33743914da45b09c5d45bb078b65.nq.gz
│   ├── 51f34aeca9d8e87f0a34b3e1474d2195a893fce6.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 84528af98ad8a61b1f828668e058ce0ebba23e3f.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── d32850a107750d686abd8d415157c3d9630d24a9.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7b93230e58828c49843778d241360e6a1f8607d.nq.gz
│   ├── e8162753cfb2c67c23ff528f879d3b914935a8b7.nq.gz
│   ├── ea06dc745300fd2f627d64c8c27013b4ad46a42b.nq.gz
│   └── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cfce41767ac8e91fe02e17ddf4cf551a6a0e565e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 37 files
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

[jaraco/jaraco.office](https://github.com/jaraco/jaraco.office)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
