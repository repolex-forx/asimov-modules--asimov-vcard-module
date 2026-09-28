# Repolex Knowledge Graph of asimov-modules/asimov-vcard-module

RDF knowledge graph data for [asimov-modules/asimov-vcard-module](https://github.com/asimov-modules/asimov-vcard-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-vcard-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f0ff028289c5113a5b2adbe6249bb2b9426a20f5
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f0ff028289c5113a5b2adbe6249bb2b9426a20f5.nq.gz
│   └── repolex
│       └── f0ff028289c5113a5b2adbe6249bb2b9426a20f5
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 5862fe1217f0d5413c5cbaecf62ec433a5502efe.nq.gz
│   ├── 69d9dce66fba559ae35b7f5556371a9b7c06bbfe.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 77d6f4ca23711533e724789a0a0045eab28c5ea6.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── abc1216388beaaf18b36a352ac4f8b6543190c9f.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d7aa181d68ad7f8ab916b68af836bdec9d81bd7a.nq.gz
│   ├── e30daf184594c29cce8dafc9a6a3b78047cc83d2.nq.gz
│   ├── e38c74a6f05d86eaa2377554b416da74c6fa6fc8.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f0ff028289c5113a5b2adbe6249bb2b9426a20f5.nq.gz
├── filetree
│   └── f0ff028289c5113a5b2adbe6249bb2b9426a20f5.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[asimov-modules/asimov-vcard-module](https://github.com/asimov-modules/asimov-vcard-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
