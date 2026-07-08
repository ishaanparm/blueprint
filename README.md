# BlueprintNYC

**Find help in NYC.** A simple, friendly router that takes New Yorkers straight to the city service they need — the number to call, the official link, and exactly what to say when someone picks up.

🔗 **Live site:** [blueprint-nyc.org](https://blueprint-nyc.org)

---

## The problem

NYC already has real resources — ACCESS NYC, 311, HRA, and dozens of programs for food, housing, jobs, benefits, and legal help. The help exists. What's hard is knowing *where to click, what you qualify for, and what to say when you call.* People bounce off twenty confusing government pages before they ever reach help.

Blueprint is a thin, plain-language layer on top of those official services. It doesn't replace them — it points people at them, fast.

## What it does

Answer two questions — *What do you need help with?* and *Which borough?* — and Blueprint shows you clean cards for that need, each with:

- **What it helps with**, in plain language
- **A phone number** you can tap to call
- **The official NYC link**
- **What to say when you call** — a ready-made script
- **What documents they may ask for**
- **A "last verified" date**, so nothing looks more current than it is

There's also an always-visible **"Help right now?"** button for emergencies (911 / 311 / 988 / Homebase / the DV hotline), and a separate visitor guide for tourists that's kept clearly apart from the help services.

## Categories

Food · Housing / Rent · Mental Health · Immigrant Family Help · Jobs & Young Adults · Money & Benefits · (plus a separate Visiting NYC guide)

## Languages

The footer guidance is available in NYC's official language-access set (the ten Local Law 30 languages, which are the city's most commonly spoken) plus English: Spanish, Chinese, Russian, Bengali, Haitian Creole, Korean, Arabic, Urdu, French, and Polish. Arabic and Urdu render right-to-left.

> ⚠️ The non-English translations are a first pass and should be reviewed by a native speaker before being treated as authoritative.

## Tech

- A single self-contained `index.html` — HTML, CSS, and vanilla JavaScript, **no frameworks or build step.**
- All resource data lives in a `RESOURCES` array at the top of the script, with fields (`category`, `boroughs`, `name`, `phone`, `link`, `script`, `documents`, `verified`) that map cleanly to a JSON file or SQLite table later.
- Accessible: keyboard focus states, reduced-motion support, tap-to-call links, high-contrast text.
- Hosted free on GitHub Pages with a custom domain.

## Running it

It's one file. Open `index.html` in any browser — that's the whole thing. No install, no dependencies.

To deploy your own copy: put `index.html` in a public GitHub repo, enable **Settings → Pages → Deploy from a branch → main → /(root)**, and (optionally) point a custom domain at it.

## Data & accuracy

All resources were verified against official NYC sources in **July 2026**. Phone numbers, hours, and eligibility rules change, so every card links back to the official page as the source of truth and reminds people to confirm details by calling 311.

**This is not an official City of New York website.** It's an independent project that links to city services; it does not collect anyone's information or determine what they qualify for.

## Roadmap

- [ ] Borough-specific office addresses (currently the borough step mostly reframes citywide resources rather than filtering to a local office)
- [ ] Translate the full entry flow — hero question and category tiles — not just the footer
- [ ] Native-speaker review pass on all translations
- [ ] Move resource data out of the HTML into a separate `resources.json`
- [ ] A lightweight way to flag out-of-date info

## Contributing

Spotted a wrong number, a dead link, or a resource that should be added? Open an issue — accuracy is the whole point of this project, so corrections are the most valuable contribution.

## Credits

Built by Ishaan Parmar ([@ishaanparm](https://github.com/ishaanparm). Resource data from official NYC / 311 sources.

## License

Released under the [MIT License](LICENSE) — free to use, adapt, and build on.
