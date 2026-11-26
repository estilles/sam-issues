# SAM — Stremio Addon Manager

[SAM] is a web app that enhances your [Stremio] experience, It allows you to manage your Stremio Addons, with features not currently available in Stremio clients. See everything you have installed in one place, reorder it, check for updates and refresh without deleting and reinstalling, remove what you don't need, and install new addons from addon catalogs, all in one simple interface.

> **SAM is currently in beta.** Things may break or change. Your feedback is what will shape it. See [Reporting issues](#reporting-issues).

---

<img width="1125" height="766" alt="image" src="https://github.com/user-attachments/assets/4d412d0c-39ce-4abe-a6e8-5de45fbcd86a" />


---

## Features

### Sign in with your Stremio account
- Log in with your [Stremio] email and password.
- SAM does not store personal data. Your Stremio auth key lives only in a `Secure`, `HttpOnly` session cookie, which is cleared when the browser session ends.

### My Addons
- **Drag-and-drop reordering** with drag handles. Changes are saved automatically (debounced). Protected addons can't be moved, removed or refreshed.
- **Installed / Official / Community tabs**, each with a count.
- **Filter by type** (movies, series, etc.) with the Types dropdown.
- **Search** addon titles and descriptions.
- **Quick actions** on each non-protected addon: copy the manifest URL, refresh, and uninstall.
- **Refresh** allows you to update an already installed addon in-place, without having to remove it and re-install it.
- **Offline badge** shown when an addon is unreachable.
- **Add Addon** by manifest URL. Add a new or replace an existing addon when you already have the addon/manifest URL. Useful for installing addons that do not appear in any of the installed addon catalogs.

### Install from Catalog
- Browse addons published in the addon catalogs of the addons you already have installed.
- Pick a catalog from a dropdown, then install or uninstall addons with one click.

### Polish
- Light and dark theme with a single toggle (your choice is remembered).
- Skeleton loaders while data loads.
- Built with accessibility in mind.

---

## Tech stack

SAM was build using:

- [TypeScript](https://www.typescriptlang.org/)
- [Effect](https://effect.website/) v4
- [Foldkit](https://foldkit.dev/) (soon to be Effect UI)
- [Tailwind CSS](https://tailwindcss.com/) with shadcn-style components
- [Vite](https://vite.dev/) and [Vitest](https://vitest.dev/)
- [Bun](https://bun.sh/) for scripts and package management
- [oxlint](https://oxc.rs/) / oxfmt for linting and formatting
- Runs on Cloudflare Workers

---

## Reporting issues

Thanks for testing SAM! Please open an issue on the repository [issue tracker][issues] and include:

- What you did and what you expected to happen
- What actually happened (screenshots help a lot)
- Your browser and operating system
- For addon problems: the addon's name and manifest URL (**never** share your Stremio password or auth key)

Feature ideas and UX feedback are welcome too.

---

## Privacy

- SAM never stores your credentials or personal data.
- Your session lives only in a session cookie and ends when you log out or close the browser.
- Addon manifests are fetched server-side so SAM can show status and metadata.

---

## Disclaimer

SAM is an unofficial community project. It is not affiliated with or endorsed by Stremio.

[SAM]: https://sam.estilles.workers.com/
[Stremio]: https://www.stremio.com/
[Issues]: https://github.com/estilles/sam-issues/issues
