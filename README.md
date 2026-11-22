# Repolex Knowledge Graph of rust-pretty-assertions/rust-pretty-assertions

RDF knowledge graph data for [rust-pretty-assertions/rust-pretty-assertions](https://github.com/rust-pretty-assertions/rust-pretty-assertions), parsed by [repolex](https://repolex.ai).

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
rlex download rust-pretty-assertions/rust-pretty-assertions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f5c5b24258739cf3918d4165a17b43c1cddadfc2
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f5c5b24258739cf3918d4165a17b43c1cddadfc2.nq.gz
│   └── repolex
│       └── f5c5b24258739cf3918d4165a17b43c1cddadfc2
│           └── chunk-001.nq.gz
├── blob
│   ├── 029e7350cdcd5bed0b7e3f4e9eeb9e980e058ee5.nq.gz
│   ├── 03ea059b73d272aa8ec804935fc556e3626e19a1.nq.gz
│   ├── 07b171490676edfb3382bde45c250c618c88ddfc.nq.gz
│   ├── 0a612c82e32098402f62d809b80c63b7cfcdbed8.nq.gz
│   ├── 0ef251f14d27763cc10f9a9897c3e4b2a88148cf.nq.gz
│   ├── 1deb632a9ad158467515c2ada5a9cd153e948581.nq.gz
│   ├── 1e5b645f0c8bb884101cefdee5497a6c7e6fc034.nq.gz
│   ├── 1e62372cb13087f1935b068ebbeb5d291c2d3173.nq.gz
│   ├── 20afa273afd2e77fb54fc540274f4ea7d987a5e0.nq.gz
│   ├── 21af80d2cb7fb2d1444ce401d50ec037aef43c5e.nq.gz
│   ├── 32d46ee883b58d6a383eed06eb98f33aa6530ded.nq.gz
│   ├── 35e74d4ac9fb1eea25387ab1b8db47dc818060e5.nq.gz
│   ├── 39db5cbd92f5e815427a95f0cebfda9aea3fcd8a.nq.gz
│   ├── 3dc90a8782642a6d9fd0ca95aef4abb1fd251abf.nq.gz
│   ├── 40b4f0fa85b33b713030aae1b0f66490b7527138.nq.gz
│   ├── 48b7653f40ed716119cb7f81280fa563a0b673d1.nq.gz
│   ├── 4ca115d5a792a59f7fe49ea51fd927271c4fc45e.nq.gz
│   ├── 63246c6d71a33eacb404e4b84242b91e90069757.nq.gz
│   ├── 712d55c82c51e2b8efc55175d14266d3c7eac0c7.nq.gz
│   ├── 719423337d09140bf952cd0d99599cdbc689d0f0.nq.gz
│   ├── 76219eb72e8524f15c21ec93b9b2592da49b5460.nq.gz
│   ├── 7bbb4cc3b0f6ce6b2bcc54ff89dab492e1b4cf4e.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 8f71f43fee3f78649d238238cbde51e6d7055c82.nq.gz
│   ├── 965b606f331b51d566b46025f9ff311a7aad0c12.nq.gz
│   ├── 9d68a9c5c793b33d50c18d59f6bb545c171448dc.nq.gz
│   ├── 9f430333c20c15af63cdeb62d2e99f48a0fbf66d.nq.gz
│   ├── aa5f3697cb690d6d745daa993dd4972c0f3ff19a.nq.gz
│   ├── b92af08e498b710dd5308eafdb745fe5914c511c.nq.gz
│   ├── c4423da9b8f90388d6d895725dfc021df782d883.nq.gz
│   ├── d5dea5964b9006a43f774d3e5d2d1cada0069cab.nq.gz
│   ├── dc192d08181e3499d86803639eef1dd2f12f7d10.nq.gz
│   ├── f04b67b413eeb7ce6c7197916f735113435d7eaa.nq.gz
│   └── fe932c8fac5e652ee321329e34d57637d71c4530.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f5c5b24258739cf3918d4165a17b43c1cddadfc2.nq.gz
├── filetree
│   └── f5c5b24258739cf3918d4165a17b43c1cddadfc2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 44 files
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

[rust-pretty-assertions/rust-pretty-assertions](https://github.com/rust-pretty-assertions/rust-pretty-assertions)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
