# Contributing to Traffic Masters Squad

> Guide for contributing to the Traffic Masters Squad repository — adding content, improving documentation, and maintaining quality.

---

## Contribution Types

| Type | Description | Examples |
|------|-------------|---------|
| **Content Addition** | New files, phrases, frameworks, or templates | New phrase library, new checklist, new script |
| **Content Update** | Improving existing content with better data or examples | Updated benchmarks, new case studies, additional phrases |
| **Bug Fix** | Correcting errors in documentation, templates, or data | Typo fixes, incorrect formulas, broken references |
| **Structure Change** | Reorganizing files, directories, or naming | File renaming, directory restructuring |
| **Process Improvement** | Improving workflows, checklists, or quality gates | New quality gate, streamlined workflow step |

---

## Before You Contribute

### Understand the System
1. Read `docs/getting-started.md` for system overview
2. Review `docs/naming-conventions.md` for naming standards
3. Understand the directory structure and file organization
4. Review the `docs/glossary.md` for standard terminology

### Check Existing Content
Before creating something new:
1. Search existing files to avoid duplication
2. Check if the content fits better as an update to an existing file
3. Review the relevant catalog (agent, framework, checklist, template, task, workflow) to see what already exists

---

## Contribution Standards

### File Naming
- All documentation files: `kebab-case.md`
- All data files: `kebab-case.yaml`
- No spaces, no special characters
- Descriptive names that indicate content

### Document Structure
Every new document should include:

```markdown
# Title

> One-line description of the file's purpose and contents.

---

## Section 1
[Content]

## Section 2
[Content]

---

## Usage Guidelines
[How to use this content effectively]
```

### Writing Style
- **Clear and direct** — Write for practitioners, not academics
- **Specific over vague** — Use concrete numbers, examples, and references
- **Actionable** — Every piece of content should be usable, not just informational
- **Consistent terminology** — Use terms as defined in the glossary
- **No jargon without definition** — If you use a technical term, ensure it's in the glossary
- **No emojis** — Maintain professional formatting throughout

### Content Quality Standards
- **Accuracy** — All data, benchmarks, and claims must be verifiable
- **Completeness** — Every section should be fully populated; no placeholder content
- **Currency** — Content should reflect current platform capabilities and industry standards
- **Relevance** — Content must serve a clear purpose within the squad system

---

## How to Contribute

### Step 1: Plan Your Contribution
- Identify the type of contribution
- Determine which directory and files are affected
- Review naming conventions and standards

### Step 2: Create or Modify Content
- Follow the document structure templates
- Use consistent formatting (headings, tables, lists)
- Include usage guidelines where applicable
- Cross-reference related files

### Step 3: Validate Your Contribution
- **Accuracy check** — Are all facts, numbers, and references correct?
- **Completeness check** — Are all sections filled in?
- **Convention check** — Does the file name and internal structure follow standards?
- **Cross-reference check** — Do all references to other files resolve correctly?
- **Glossary check** — Are any new terms added to the glossary?

### Step 4: Update Supporting Files
- **Changelog** — Add an entry to `docs/changelog.md`
- **Catalogs** — Update the relevant catalog (agent, framework, checklist, template, task, workflow)
- **Getting Started** — If the contribution adds a significant capability, reference it
- **Registry** — If the contribution adds a new entity type, update `docs/data-model.md`

### Step 5: Submit Your Contribution
- Ensure all files are saved and properly formatted
- Verify no existing files were accidentally modified
- Confirm the changelog is updated

---

## Directory Guidelines

### Where to Add New Files

| Content Type | Directory |
|-------------|-----------|
| Ad copy phrases, hooks, templates | `phrases/` |
| How-to guides, references, catalogs | `docs/` |
| Automation routines, workflows | `scripts/` |
| Reusable strategy components | `lib/components/` |
| Campaign patterns | `lib/patterns/` |
| Decision-making tools | `lib/utilities/` |
| Category definitions | `lib/taxonomies/` |
| Creative examples | `swipe/` |
| Tone and voice guidance | `voice/` |
| Data schemas and records | `data/registries/` |
| Performance snapshots | `data/metrics/` |

### Adding a New Agent
1. Create the agent definition file in `agents/`
2. Add the agent to `docs/agent-catalog.md`
3. Define the agent's tasks in `docs/task-catalog.md`
4. Add the agent to relevant workflows in `docs/workflow-catalog.md`
5. Update `docs/changelog.md`

### Adding a New Framework
1. Create the framework file in the appropriate `lib/` subdirectory
2. Add the framework to `docs/framework-catalog.md`
3. Cross-reference with related agents and other frameworks
4. Update `docs/changelog.md`

### Adding a New Checklist
1. Create the checklist file in `checklists/` (or add to an existing collection)
2. Add the checklist to `docs/checklist-catalog.md`
3. Define the trigger conditions
4. Update `docs/changelog.md`

---

## Review Process

### Self-Review Checklist
Before submitting, verify:

- [ ] File name follows `kebab-case.md` convention
- [ ] Document has a title (H1), description block, and usage guidelines
- [ ] Content is accurate, complete, and actionable
- [ ] No placeholder text (e.g., "[TBD]", "TODO", "insert here")
- [ ] All cross-references to other files are correct
- [ ] No duplicate content — checked existing files
- [ ] Terminology is consistent with the glossary
- [ ] Changelog has been updated
- [ ] Relevant catalog has been updated

### Peer Review
For significant contributions (new frameworks, agent modifications, workflow changes), request a review from the squad owner or a senior contributor.

---

## Common Mistakes to Avoid

1. **Creating a file that duplicates existing content** — Always search first
2. **Using inconsistent terminology** — Refer to the glossary
3. **Leaving sections incomplete** — Every section should have real content
4. **Not updating the changelog** — Every change should be logged
5. **Not updating catalogs** — New items must appear in the relevant catalog
6. **Breaking cross-references** — If you rename a file, update all references to it
7. **Using relative file paths** — Use paths relative to the squad root for consistency
8. **Adding content without usage context** — Every file should explain when and how to use it
