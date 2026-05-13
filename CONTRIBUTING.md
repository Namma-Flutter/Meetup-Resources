# Contributing to Namma Flutter Event Resources

Thank you for being part of the Namma Flutter community! This guide explains how speakers and community members can add event resources to this repository.

---

## Who Can Contribute

- **Speakers** — add your slides, code samples, or resource links from your sessions
- **Event organizers** — add event summaries or missing session resources
- **Community members** — help improve existing resource entries (fix links, add descriptions, correct typos)

---

## Repository Structure

```
event_resources/
└── {year}/
    └── {month}/
        └── {event-slug}/
            ├── README.md
            └── {session-title_speaker-name}/
                └── (slides, code, links, or a README.md with external links)
```

**Example:**

```
event_resources/
└── 2026/
    └── march/
        └── fossxnf-cbe/
            ├── README.md
            └── improving-app-performance_nareshkumar-k/
                └── slides.pdf
```

---

## Naming Conventions

### Event folder (`{event-slug}`)

Use a short, lowercase, hyphen-separated identifier for the event.

| Event                               | Slug                |
| ----------------------------------- | ------------------- |
| FOSS x Namma Flutter, Coimbatore    | `fossxnf-cbe`       |
| Namma Flutter Meetup #5, Chennai    | `nf-meetup-5-che`   |
| Namma Flutter Jan Meetup, Bangalore | `nf-jan-meetup-blr` |

### Session folder (`{session-title_speaker-name}`)

- Use lowercase and hyphens only
- Separate the session title and speaker name with an underscore `_`
- Keep it concise

| Session                        | Speaker            | Folder name                                |
| ------------------------------ | ------------------ | ------------------------------------------ |
| Improving App Performance      | Nareshkumar K      | `improving-app-performance_nareshkumar-k`  |
| Beyond Chatbots: Generative UI | Balaji Venkatraman | `beyond-chatbots-genui_balaji-venkatraman` |

### Resource files

Name files descriptively. Accepted formats:

| Type       | Examples                                                                     |
| ---------- | ---------------------------------------------------------------------------- |
| Slides     | `slides.pdf`, `slides.pptx`                                                  |
| Code       | Any source file or a link in `README.md`                                     |
| Notes      | `notes.md`                                                                   |
| Links only | `README.md` with links to external resources (Google Drive, GitHub, YouTube) |

---

## Step-by-Step Guide

### 1. Fork and clone the repository

```bash
git clone https://github.com/Namma-Flutter/event_resources.git
cd event_resources
```

### 2. Create a branch

Use one of these branch naming formats depending on what you're doing:

| Purpose                    | Format                                      | Example                                               |
| -------------------------- | ------------------------------------------- | ----------------------------------------------------- |
| Add session resources      | `{event-slug}/{session-title_speaker-name}` | `fossxnf-cbe/improving-app-performance_nareshkumar-k` |
| Create a new event folder  | `create/{event-slug}`                       | `create/fossxnf-cbe`                                  |
| Documentation              | `docs/{short-description}`                  | `docs/update-installation-guide`                      |
| Fix a broken link or typo  | `fix/{short-description}`                   | `fix/broken-link-fossxnf-cbe`                         |
| Maintenance / housekeeping | `chore/{short-description}`                 | `chore/update-contributing-guide`                     |

Rules: **lowercase**, **hyphens** between words, **no spaces or uppercase**.

```bash
git checkout -b fossxnf-cbe/improving-app-performance_nareshkumar-k
```

### 3. Navigate to the correct event folder

```bash
cd 2026/march/fossxnf-cbe
```

If the event folder does not exist yet, create it along with a `README.md` following the [event README template](#event-readme-template) below.

### 4. Add your resources

Create a session folder and add your files:

```bash
mkdir improving-app-performance_nareshkumar-k
cd improving-app-performance_nareshkumar-k
# Add your slides, code, or a README.md with links
```

If your resources are hosted externally (Google Slides, GitHub repo, YouTube), create a `README.md` inside the session folder with the links instead of uploading large files.

### 5. Update the event README

Make sure the event's `README.md` lists your session. See the [Event README Template](#event-readme-template).

### 6. Commit and push

Commit messages follow the format: **`<type>: <short description>`**

| Type    | When to use                            | Example                                                  |
| ------- | -------------------------------------- | -------------------------------------------------------- |
| `add`   | Adding new session resources           | `add: improving app performance slides by nareshkumar-k` |
| `feat`  | Creating a new event folder            | `feat: create fossxnf-cbe event`                         |
| `fix`   | Fixing a broken link or typo           | `fix: correct speaker name in fossxnf-cbe README`        |
| `chore` | Maintenance, formatting, minor updates | `chore: update session resources formatting`             |
| `docs`  | Documentation-only changes             | `docs: add event README for fossxnf-cbe`                 |

```bash
git add .
git commit -m "add: improving app performance slides by nareshkumar-k"
git push origin fossxnf-cbe/improving-app-performance_nareshkumar-k
```

### 7. Open a pull request

Open a pull request against the `main` branch. Use a clear title and briefly describe what you've added.

> **Note:** The `main` branch is protected. All contributions go through a pull request reviewed by the maintainers.

---

## Event README Template

When creating a new event folder, add a `README.md` using this template:

```markdown
# {Event Name}

**Date:** {ddd Month, YYYY}

**Location:** {City / Venue}

**Type:** {Meetup | Workshop | Hackathon | Collaborative Event}

{One or two lines describing the event and any co-organizers.}

---

## Sessions

| Session           | Speaker                                | Resources                                                              |
| ----------------- | -------------------------------------- | ---------------------------------------------------------------------- |
| Session Title One | [Speaker Name](linkedin-or-github-url) | [Slides](./session-folder/slides.pdf)                                  |
| Session Title Two | [Speaker Name](linkedin-or-github-url) | [Code](https://github.com/...) · [Slides](./session-folder/slides.pdf) |

---

## Event Links

- Recording: {YouTube link or N/A}
- Photos: {link or N/A}
- Event page: {Meetup / lu.ma / LinkedIn event link}
```

---

## Pull Request Guidelines

- One PR per event or session — keep PRs focused
- PR title format: `type: <short description>` (same types as commit messages)
- Do not commit large binary files (> 15 MB) — link to external hosting instead
- Make sure all links are working before submitting

### Automated checks

Every PR to `main` is automatically validated by GitHub Actions:

| Check           | What it validates                                |
| --------------- | ------------------------------------------------ |
| Branch name     | Must match a valid pattern (see step 2 above)    |
| PR title        | Must follow `<type>: <description>`              |
| Commit messages | Every commit must follow `<type>: <description>` |
| File sizes      | No file may exceed 15 MB                          |

All checks must pass before a PR can be merged.

---

## Questions?

Open an issue in this repository or reach out to the community on [Telegram](https://t.me/nammaflutter).
