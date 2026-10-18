# How to update the site

Everything in this `_templates` folder is ignored by the website build. These are copy-and-fill templates.

## Post a journal update (most common)

1. Copy `journal-update.md` into `docs/_posts/`.
2. Rename it `YYYY-MM-DD-short-title.md`, for example `2026-10-25-first-test-users-created.md`.
3. Fill in the front matter between the `---` lines and write the update in Markdown.
4. Commit and push. GitHub builds the page within a minute or two. It appears on the homepage and in the Journal automatically.

## Update a project chapter

Each project’s chapters live in their own folder: `docs/_iam/` for Identity Before Detection, `docs/_domain_email/` for Domain and Business Email. Open the chapter, rewrite its content, and update these front-matter fields:

- `status`: use exactly one of `Documented`, `In progress`, `Needs validation`, `Planned`
- `status_note`: one sentence on where it stands
- `updated`: today’s date, `YYYY-MM-DD`
- `headline`: the big magazine-style headline, in quotes, e.g. `"The mailbox works. DKIM doesn’t, yet."` (falls back to `title`)

The site turns `status` into plain words automatically: `Documented` shows as “Written 18 Oct 2026”, `In progress` as “Under way”, `Needs validation` as “Written …, under review”, and `Planned` as “Not started” (or “Up next” for the chapter marked `current: true`).

The route strip on the front page, the chapter list and the screenshot counts all update automatically. Move the `current: true` line to the next stage when one is finished, and it becomes the red “Up next” stage on the route.

## Add a new chapter

Copy `chapter.md` into the project’s folder. Number the filename and `order:` to slot it in, then fill it in. Previous and next links are worked out automatically.

## Add a screenshot

1. Redact it first: tenant and subscription IDs, names, emails, billing, phone numbers, addresses, personal inbox details.
2. Save it in `docs/assets/evidence/` with a clear name, for example `vw-intune-001-device-overview.png`.
3. In the chapter, replace the placeholder’s `source=...` with `image=` and `alt=`:

```
{% raw %}{% include evidence.html title="Device overview showing zero devices" where="Microsoft Intune admin centre · Devices" image="/assets/evidence/vw-intune-001-device-overview.png" alt="Intune device overview with 0 devices on every platform" shows="Windows, Apple mobile, macOS, Android and Linux, each with 0 devices." proves="The starting point: nothing was enrolled at the time of capture." %}{% endraw %}
```

The `alt` text is read aloud by screen readers. Describe what the image shows, not just its title.

Figures are numbered automatically (Fig. 1, Fig. 2 …) and the chapter header shows an estimated read time. `where` is the portal name shown on the placeholder until the image is added.

## Add a pull quote

Pull a strong sentence out of the chapter to break up long text:

```
{% raw %}{% include quote.html text="Mail can still land in the inbox on SPF alone, which is why the tests passed." %}{% endraw %}
```

## Add a new project

1. In `_config.yml`, add the project under `collections:` and add a `defaults` block for it (copy the `domain_email` one and change the names).
2. Create a folder `docs/_<collection>/` for its chapters.
3. Create a landing page `docs/<project-slug>/index.html` with `layout: project`, `collection: <collection>`, `slug`, `title`, `topic`, `summary` and `order`.

The project then appears on the front page and the Projects page automatically.

## Writing rules

- Never describe planned work as done. A licence or a menu option isn’t a working control.
- Use only genuine, redacted screenshots.
- Department names are fixed: Management, Finance, HR, Operations, Delivery Team, IT.
