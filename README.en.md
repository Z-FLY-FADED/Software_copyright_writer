# Software Copyright Writer

[简体中文](README.md) · **English**

`Software_copyright_writer` is a Codex skill for preparing Chinese software copyright registration materials. It uses source code, project documentation, reference applications, and Word templates to draft software design specifications, software user guides, and operation manuals. It can also prepare architecture diagrams, flowcharts, and tables covering modules, runtime requirements, and test cases.

## When to use it

- Draft a software copyright document from a source tree.
- Adapt the structure and writing style of a reference document to a different codebase.
- Lay out a `.docx` using a supplied Word template.
- Document system architecture, modules, interfaces, runtime requirements, data flows, verification, and maintenance.
- Prepare a user manual or operating guide from the implementation.
- Expand, edit, restructure, or review an existing draft against the supplied requirements.

## Repository layout

| Path | Purpose |
| --- | --- |
| [`SKILL.md`](SKILL.md) | Codex skill instructions |
| [`README.md`](README.md) | Chinese overview and maintenance notes |
| [`使用手册.md`](使用手册.md) | Detailed guide in Chinese |

As the repository grows, `assets/` can hold Word templates and cover art, `references/` can hold reference materials and specifications, and `scripts/` can hold reusable analysis, conversion, and rendering tools.

## What to provide

| Input | Details |
| --- | --- |
| Source tree | Code, configuration, dependency manifests, scripts, database schema, and frontend and backend files |
| Reference documents | Existing specifications or user guides to reference for structure and style |
| Word template | A `.docx` with the required cover, headers, footers, fonts, headings, and page numbering |
| Software details | Name, version, implementation language, runtime, audience, and deployment method |
| Output requirements | Document type, target length, PDF export, figures and tables, and destination path |

## Example prompt

```text
Use the Software_copyright_writer skill to prepare a Chinese software design specification.
Source tree: [path to source]
Reference materials: [path to sample documents]
Word template: [path to template.docx]
Output directory: [path to output]

1. Prepare at least 20 pages of body text for this example.
2. Describe the actual structure and features shown in the source.
3. Follow the reference document’s organization and write original text for this software.
4. Include system architecture, functional structure, main workflow, and data flow diagrams.
5. Include tables for runtime requirements, modules, source files, core functions, and test cases.
6. Produce a Word document and export a PDF if the available tooling supports it.
```

## Example output structure

```text
output/
├─ final/
│  ├─ software-design-specification.docx
│  └─ software-design-specification.pdf
├─ diagrams/
│  ├─ 01-system-architecture.png
│  ├─ 02-functional-structure.png
│  └─ 03-main-workflow.png
├─ tables/
│  └─ tables.xlsx
└─ intermediate/
   ├─ code_analysis.md
   ├─ document_outline.md
   └─ mermaid_diagrams.md
```

## Maintenance

- Keep `SKILL.md` focused on invocation, the core workflow, and essential constraints.
- Put detailed examples, prompts, and manual steps in `使用手册.md`.
- Use reference material for structure and style. Write fresh prose that reflects the target software.
- Put templates and cover assets in `assets/` and reusable analysis and conversion tools in `scripts/` when adding them.
