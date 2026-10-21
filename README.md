# Repolex Knowledge Graph of jupyterhub/jupyterhub-sphinx-theme

RDF knowledge graph data for [jupyterhub/jupyterhub-sphinx-theme](https://github.com/jupyterhub/jupyterhub-sphinx-theme), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/jupyterhub-sphinx-theme
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 33139829eb7840b41cfcdcbff603701e7e468391
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 33139829eb7840b41cfcdcbff603701e7e468391
│           └── chunk-001.nq.gz
├── blob
│   ├── 097bb8acace979a8e96bb74371f6528f7a28b085.nq.gz
│   ├── 0ba463971975bee3a8ffd002f1c729089de0fd1d.nq.gz
│   ├── 3521bdf2881385e76452d8a0f7d0feaff6e38671.nq.gz
│   ├── 3ba2403f336dbe1725ecbfd202121e1b2e79dd9a.nq.gz
│   ├── 3d9a3e78694477f43329bbfb71a43a303ec7b5e6.nq.gz
│   ├── 462817b594e00311002805290c7baf78ba894a70.nq.gz
│   ├── 5ae425e94e44b7012f7ee994c1f991985720579f.nq.gz
│   ├── 66d02a3c3f9b1b59b1b359d7ff8d847cf85f779e.nq.gz
│   ├── 6a944f765860506269017f99a5936b6bf729f4ba.nq.gz
│   ├── 7019936761eb592591c0e65829370a41ce07475f.nq.gz
│   ├── 7124d7e0079ad123acfd3726828a4a6939280073.nq.gz
│   ├── 83126a03db8ae79ce5ce77fb9f00ded12c630823.nq.gz
│   ├── 9254df9928593bf4c82cae1445bdf24f967331cc.nq.gz
│   ├── 94f950227beeb81c039eeac45185a693a98ca056.nq.gz
│   ├── 989941b4665a807909d27849edc491c82e70a054.nq.gz
│   ├── 9e8ae9593de21b292044691dd5946e05a08e0544.nq.gz
│   ├── a2bd794c96d87f97ffafa2bdb87bf1e24fe1cda4.nq.gz
│   ├── a3a28fd46f6881a79fc5f972d676c26f49f47a99.nq.gz
│   ├── a3a7848d811abfae3af5ab3672866ec87f37b93c.nq.gz
│   ├── a3fda6e5bc17701d2d6b4d15d433a05d3391f9ad.nq.gz
│   ├── a970704d290ecbfa99ddb725799e90a12f57ea06.nq.gz
│   ├── ba71ef597144142c67acfa030f11fb9dd01d27d0.nq.gz
│   ├── cec0dad52e754b4b24fd9f5e412aae7e3e26a230.nq.gz
│   ├── d34dc1e2e24d3a4984714fe9b5cb9377d043e000.nq.gz
│   ├── d92d8d465aec14aa788352c8d908d80a5b25544d.nq.gz
│   ├── e13f0d49fd5c75546976f4a23bb24b7b85cdba08.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ffdf84e2314ca24a8b508642368dbba3bc61c7cc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 33139829eb7840b41cfcdcbff603701e7e468391.nq.gz
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

[jupyterhub/jupyterhub-sphinx-theme](https://github.com/jupyterhub/jupyterhub-sphinx-theme)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
