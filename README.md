# Repolex Knowledge Graph of marshmallow-code/marshmallow-validators

RDF knowledge graph data for [marshmallow-code/marshmallow-validators](https://github.com/marshmallow-code/marshmallow-validators), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/marshmallow-validators
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2985068c86f961b5150a6c3ea3169d398ab4bc48
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2985068c86f961b5150a6c3ea3169d398ab4bc48
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d08bd22fa352eb82e1866418bf31fe7f34e8056.nq.gz
│   ├── 1005e265973ba976766d336b6c043d066e663d6e.nq.gz
│   ├── 19326447a9cfb982465dd1b043fdb1e8dff3dbae.nq.gz
│   ├── 2b4476477fe314cdf9e221f94cecc0727f32d8c9.nq.gz
│   ├── 3c345456c7b4b5f064632fea5cf11228fdcb0eef.nq.gz
│   ├── 41ff9990a971d7e4e0256806713d363578c4254a.nq.gz
│   ├── 47be343918509d1ec143363b59c74eeae9f88611.nq.gz
│   ├── 64da955e8c86fd507f4ee2ee7c50d90693b49465.nq.gz
│   ├── 68d9d27f1a0c904f71270a0cee466f11d1af69dc.nq.gz
│   ├── 709fdc7f8cf36462bc6d1c4f3f442e8d1fa7f43f.nq.gz
│   ├── 7e7d024a1fa63204e9e60457f645a72b31ba08ea.nq.gz
│   ├── 8924dcf86cfeb4d43e20e0d5306245199b4a2b63.nq.gz
│   ├── c8b23b8805ae381a12c7be4dfe037f3649de8c5c.nq.gz
│   ├── cf353a65e1a8a1cfb00d8e7fe30f29280cc43389.nq.gz
│   ├── d293c5fd81c89c35b1029f25dccb9f77401aaca0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e86cfd4eb10b95f56b6aea720b5ead398cf9a481.nq.gz
│   ├── e984708b5a06c71f41ab82bb8e808d1cb88853a4.nq.gz
│   ├── eb48b27c68fc200c9ef53dbc6e49b0d3ef08afb3.nq.gz
│   ├── ee27d586aaa2af945468dadfaf570c2fec52bcf7.nq.gz
│   ├── fa07e9e9a0a642238290e1e531c015e7134401fa.nq.gz
│   ├── fab9557a83a4877551be22672e2cb06c7cdf26c5.nq.gz
│   └── fc293e15d9dbfb78005a713d28ffab09639b9503.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2985068c86f961b5150a6c3ea3169d398ab4bc48.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[marshmallow-code/marshmallow-validators](https://github.com/marshmallow-code/marshmallow-validators)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
