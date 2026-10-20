# How to update the site

Everything in this `_templates` folder is ignored by the website build. These are copy-and-fill templates.

## How a project is organised

A project is a set of **topics**, and each topic has **steps** underneath it.

- A **topic** page (`kind: topic`) is the overview: why the topic matters and what it covers. The list of its steps appears automatically under "Explore this topic".
- A **step** page (`kind: page`) is one piece of work: what it is, why it matters, what was done, how it was checked, and the screenshots.

Files are numbered so they sort in reading order. Topic 5 is `050-...`, and its steps are `051-...`, `052-...` and so on. The `order` field uses the same number.

Identity Before Detection lives in `docs/_iam/`. Domain and Business Email lives in `docs/_domain_email/`.

## Post a journal update (most common)

1. Copy `journal-update.md` into `docs/_posts/`.
2. Rename it `YYYY-MM-DD-short-title.md`, for example `2026-10-25-first-test-users-created.md`.
3. Fill in the front matter between the `---` lines and write the update in Markdown.
4. Commit and push. GitHub builds the page within a minute or two, and it appears on the front page and in the Journal automatically.

## Write up a step you have done

Open the step’s file and replace the "Not started yet" note and placeholder sections with what actually happened. Then update the front matter:

- `status`: one of `Documented`, `In progress`, `Needs validation`, `Planned`
- `updated`: today’s date, `YYYY-MM-DD`
- `headline` (optional): a magazine-style headline, in quotes

The site shows these as plain words: `Documented` is “Written 20 Oct 2026”, `In progress` is “Under way”, `Needs validation` is “Written …, under review”, and `Planned` is “Not started”. The topic marked `current: true` shows as “Up next” on the route; move that line when a stage is finished.

## Add a new step

Copy `chapter.md` into the project’s folder, give it the next number in its topic (e.g. `057-...` and `order: 57`), set `topic` to the topic’s slug, and fill it in. Previous and next links, the topic’s step list and the contents page all update automatically.

## Add a screenshot

1. Redact it first: tenant and subscription IDs, names, emails, billing, phone numbers, addresses, personal inbox details.
2. Save it in `docs/assets/evidence/` with a clear name, for example `vw-intune-001-device-overview.png`.
3. In the step, replace the placeholder’s `source=...` with `image=` and `alt=`:

```
{% raw %}{% include evidence.html title="Device overview showing zero devices" where="Microsoft Intune admin centre · Devices" image="/assets/evidence/vw-intune-001-device-overview.png" alt="Intune device overview with 0 devices on every platform" shows="Windows, Apple mobile, macOS, Android and Linux, each with 0 devices." proves="The starting point: nothing was enrolled at the time of capture." %}{% endraw %}
```

The `alt` text is read aloud by screen readers. Describe what the image shows. Figures are numbered automatically.

## Add a pull quote

```
{% raw %}{% include quote.html text="A strong sentence from the page." %}{% endraw %}
```

## Add a new project

1. In `_config.yml`, add the project under `collections:` and add a `defaults` block for it (copy the `domain_email` one and change the names).
2. Create a folder `docs/_<collection>/` with at least one topic (`kind: topic`) and its steps.
3. Create a landing page `docs/<project-slug>/index.html` with `layout: project`, `collection`, `slug`, `title`, `topic`, `summary` and `order`.

The project then appears on the front page and the Projects page automatically.

## Writing rules

- Never describe planned work as done. A licence or a menu option isn’t a working control.
- Use only genuine, redacted screenshots.
- Department names are fixed: Management, Finance, HR, Operations, Delivery Team, IT.
