# Repolex Knowledge Graph of pallets-eco/wtforms-django

RDF knowledge graph data for [pallets-eco/wtforms-django](https://github.com/pallets-eco/wtforms-django), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/wtforms-django
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d35ac883d0060cc3257fc74a3a8bc5363f86de0b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d35ac883d0060cc3257fc74a3a8bc5363f86de0b
│           └── chunk-001.nq.gz
├── blob
│   ├── 032d2d28320beb7800da3e6012fc4f43dfbfcf6d.nq.gz
│   ├── 0857d55b90caff6f4b0e6b8e36058466d994f3bc.nq.gz
│   ├── 1636492568ccdd1bf7e4639278387a27de0ab455.nq.gz
│   ├── 170a53f6e9ffe9f3df3fe98bf32d64fb2d6549da.nq.gz
│   ├── 1acc5bbd9e4ce92b8539d36c76d6792509dad04d.nq.gz
│   ├── 2138f5728452867a184d45512e98c967fc80d1c6.nq.gz
│   ├── 278c02bd6802f1d4b5fef97c39a398e1bb92b272.nq.gz
│   ├── 314e815cfa3318be0701b7d3ea36e539cfc2fdd7.nq.gz
│   ├── 45068eb288a11517b0692bd5cb5c2a8b8f8f51ad.nq.gz
│   ├── 47b59b7e16c6a765b31b78c8b8bb59961b970089.nq.gz
│   ├── 551a68d478f68f1b003d956bce18e38782c5527c.nq.gz
│   ├── 5569bf58b6d3db259da832c3a0e4bb0898efdafb.nq.gz
│   ├── 5a9a6e9f0d735e226db68d5152de6fbe2242ccfb.nq.gz
│   ├── 6369a78d185290fafa712170fb6ce5e6caeb678f.nq.gz
│   ├── 6bb1491e8ba9f2a9f26a21d31cfee5df05e418ae.nq.gz
│   ├── 746ab80121a4509a6adcc0bd2f23f10feb435871.nq.gz
│   ├── 8397fc99511cbc412aa75cd6e4761b04ca1700ae.nq.gz
│   ├── 92a16da895139f0a91c91654bf0d34680670eab9.nq.gz
│   ├── 92eea3ee9bf6eb7316751935ff91a6aff03dee13.nq.gz
│   ├── ad85083a4af5610c3f2dc923b9159e9cb97e1677.nq.gz
│   ├── b394a91d5f03c60050944696595580e9143aa1ff.nq.gz
│   ├── b8796f676ed7db8f68a88ee6e3128871b39203b9.nq.gz
│   ├── bd8e4f549018135e2f3c6ce456428899843aed3a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f095203ec2a178e201fdca0d6bc9b8d41744f8af.nq.gz
│   ├── f2a89b68b44420afb807ed47c33e7e9409aa4044.nq.gz
│   ├── f849f125dbc31fbbccf109129f64e93f4e84019f.nq.gz
│   └── fd129343aef54431db3e33794d71d1cbb7863971.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d35ac883d0060cc3257fc74a3a8bc5363f86de0b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[pallets-eco/wtforms-django](https://github.com/pallets-eco/wtforms-django)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
