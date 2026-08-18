# Labrador Help Center: project instructions

This repo is the published Help Center at
[docs.testwithlabrador.com](https://docs.testwithlabrador.com).
It is built on [Mintlify](https://mintlify.com): pages are MDX with YAML
frontmatter, and the sidebar is defined in `docs.json`. Pushing to `main`
publishes, so every change arrives through a pull request.

Labrador is a WCAG accessibility auditing tool. These pages document how to use
the product, for the people who use it. They do not document how it is built,
and they are not a changelog. Everything here should earn its place by helping
someone do something.

Use British spelling, matching the pages already here: behaviour, colour,
organisation.

## How work arrives here

There is a pipeline behind most issues in this repo, and it exists to answer one
question: **did a change to the product just make the user documentation wrong?**

Every time a change merges in the Labrador app repo, a workflow there reads it
and decides whether a reader of these pages would notice. A new or removed
capability, a changed rule or limit, a renamed control, a different flow: those
are worth documenting. Refactors, performance work, styling, internal renames,
and bug fixes that restore what the docs already describe are not. Only the
first kind reaches this repo, as an issue naming the pages it probably affects.

That issue describes the change in product terms. It has not read the pages it
names.

Treat it as a lead, not a specification:

- Open the pages it names and read them as they stand.
- Make the smallest edit that makes them true again.
- Where the brief and the existing docs disagree about how the product behaves,
  say so in the pull request instead of picking one and writing it up.
- If nothing needs to change, say why and close the issue. A closed issue is a
  correct outcome, not a failure.

## Show your work in the pull request

Open the pull request as a **draft**. It is a proposal, not a finished change,
and the person merging it is the one who decides whether it is true.

The description is the part they read first, so write it for someone who has not
seen the diff and does not know what changed in the product. Use this shape:

```markdown
## What changed in the product
One or two sentences, from the brief. Link the originating issue.

## What I changed here
Page by page. For anything a reader would notice, show the wording:
- `projects/user-journeys.mdx`: "Steps are added from the Add menu"
  becomes "Steps are renamed from the journey's Edit button"

## What I left alone
Pages the brief named that turned out to be fine, and why. This is not
padding: it is how the reviewer knows the page was read, not skipped.

## What I could not verify
Anything asserted on the brief alone, with no confirmation from the docs
as they stand. If this section is empty, say so explicitly.
```

Never describe an edit you did not make, and never leave a change out of the
list because it seemed minor. A reviewer who finds one undocumented change in
the diff has to re-read all of them.

## Do not publish what you cannot verify

The brief describes a code change. It is not evidence of what the interface
says. Never invent a button label, a menu path, a plan limit, a keyboard
shortcut, or a security property. Where you cannot confirm the wording from the
brief or from what is already documented, name the gap in the pull request
description and leave the sentence unwritten.

This matters most for security and compliance claims. Phrases like "end to end
encrypted" and "SOC 2 compliant" are terms of art with specific meanings, and
using one loosely has already cost a correction in production. If a claim would
be embarrassing to retract, verify it before writing it.

## Style

- No em dashes anywhere in published copy. This is a house rule across all of
  Labrador. Restructure with a comma, a colon, or a second sentence instead.
- Second person and active voice. "You add a page", not "a page can be added".
- One idea per sentence.
- Sentence case for headings.
- Bold for anything the reader clicks or reads on screen: click **Add**.
- Backticks for file names, paths, commands, and values the reader types.
- Describe what the reader does and what they see, not what the system does
  internally.

## Terminology

Use the label the product shows. Where the stored value and the label differ,
the label is what belongs in the docs.

| In the product | What it is |
| --- | --- |
| **Project** | One audit. Holds tracked items, journeys, and issues. |
| **Page** | A tracked item that has its own URL. |
| **Component** | A reusable piece of interface, tracked and audited once. |
| **Flow state** | A tracked item that exists only as a step in a user journey. Not directly creatable. |
| **Pages & Components** | The grid of tracked items on a project. |
| **User journeys** | The shelf of journey cards above that grid. |
| **User journey steps** | The section listing the flow states backing journey steps. Collapsed by default. |
| **Criterion test** | One WCAG criterion tested against one tracked item. |
| **Issue** | One discrete failure found inside a criterion test. |
| **Audit version** | A snapshot of a project, used for retesting. |

Severity is stored as `advisory`, `low`, `medium`, `high`, and `critical`, but a
reader sees **Advisory**, **Minor**, **Moderate**, **Serious**, and
**Critical**. A brief quoting `high` is quoting the database, not the interface.
Write the label.

A project runs one of two methodologies, and each has its own vocabulary:

- **WCAG**: a criterion is Pass, Fail, Not applicable, or Not tested.
- **VPAT**: a criterion is Supports, Partially supports, Does not support,
  Not applicable, or Not evaluated.

Never mix the two sets in one sentence.

## Adding a page

Add a page only when an existing one genuinely cannot carry the change. A new
page needs both of:

- Frontmatter with `title`, `sidebarTitle`, and `description`. Open a
  neighbouring page in the same folder and match its shape.
- An entry in `docs.json`, under the right group in `navigation.tabs`. A page
  missing from `docs.json` does not appear in the sidebar at all.

## Content boundaries

- Document what a customer can do. Leave out admin and staff only features,
  internal tooling, and anything behind a flag that is not live.
- `sources/` is scraped marketing copy kept for reference, and `.mintignore`
  excludes it from the build. Never edit it, and never cite it as evidence of
  current behaviour.
- Do not restate pricing or plan limits from memory. Link to the pricing page
  instead, so the numbers have one home.

## Checking your work

When working locally, preview before opening a pull request:

```bash
npm i -g mint
```

```bash
mint dev
```

Confirm the page renders, the sidebar entry lands where you expect, and every
component you used is closed. Broken MDX fails the Mintlify build.

## Mintlify reference

For component syntax, configuration, and Mintlify's own writing standards,
install the Mintlify skill:

```bash
npx skills add https://mintlify.com/docs
```

Mintlify also exposes MCP servers: `https://mcp.mintlify.com` to edit content
and settings, and `https://www.mintlify.com/docs/mcp` to query how Mintlify
works.
