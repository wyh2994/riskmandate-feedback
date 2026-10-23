# Power-user test: context and report format

**Site:** PHP October 2026 · https://php.oct.2026.newsroom.sgit.ai/
**Tester:** Vicky (project manager on the team, testing here as a power user)
**Purpose:** use the site as a power user would, on a real device, and give Dinis feedback he can turn into work on the board.
**Reference example:** the join-link test Claude ran as "Sam" on 23 Oct 2026 (site v0.8.1). This test follows the same format, and does not repeat its findings.
**Where this fits:** steps 3 to 5 of [How to help](https://newsroom.sgit.ai/articles/how-to-help.html): try the product as a user, publish the work on GitHub Pages, report back with the link.

---

## 1. Who I am in this test

- A real person, not a simulated reader. I can press buttons that need a human (for example "Make my key and join").
- Non-technical newcomer: I know what a website, an app and an AI assistant are; I do not know what a vault, a signing key, OpenRouter or `window.__tools` are.
- Reader I pick on Start here: **Project or programme manager** (closest to my real job). Its question: *what unplanned work does this create, who do I chase, and what do I tell stakeholders?*
- Devices: phone first (the site says "Now" is best on a phone), then laptop.

## 2. What to test

1. **Ask 001** on `/collaborators/`: follow its five steps and answer its four questions:
   1. Which reader did you pick, and did the site answer that reader's question?
   2. What did you expect to find and could not?
   3. What would make you come back on Monday?
   4. One thing to remove, and one to add.
2. **The join flow, end to end** (the part the reference test could not do):
   - Before pressing anything, note the role my invitation shows (`editor`, `team` or `power-user`).
   - Press "Make my key and join". Record what happens and what the page says afterwards.
   - Send one signed piece of feedback with the Feedback button. Record whether the page confirms it.
3. **Now, the phone app** on a real phone.
4. **The fact-check desk:** find one claim I care about. Do I trust its grade, and do I understand A0 to A6?
5. **The team page:** does it explain how the site is made, to someone like me?

## 3. Rules while testing

- **Record the site version** (badge at the top, e.g. v0.8.1) and the date at the start. The site changes several times a day.
- **Quote the page's own words** in "What I see". Paraphrase only in "What I think".
- **Do not repeat the reference test's findings.** If I hit the same issue, write one line: "Also seen in the reference test: X." Spend the space on new findings.
- **Contradictions are the most useful finding.** When one page says something another page denies, note both pages and both texts.
- **Say what works, too.** Anything that should be kept.
- **Note what I could not do, and why.**
- **This report goes on GitHub, so it is public.** Before adding a screenshot, check it shows no key, token, vault ID, invitation link, email address or phone number. Crop or blur if needed. Never paste the invitation link itself (it is a credential).

## 4. Report format

Folder: this task's folder in the [feedback collection](../). The report replaces this folder's `README.md`; this brief stays as `context.md`; screenshots go in `screenshots/`, named `01-join-first-view.png`, `02-…` in the order taken. When the report is done, add a row to the collection's `README.md` and a card to its `index.html`.

```markdown
# Power-user test: PHP October 2026, <what was tested>

Tester: Vicky, as a power user (reader: Project or programme manager)
Date: <date> · <device and browser> · site <version>
Tested: <pages and flows, in order>
Persona: non-technical newcomer; knows AI assistants, not keys or vaults; <how much time I had>.

## The short version
3 to 5 sentences: the most important findings, the one thing that worked best,
and anything I could not finish.

## Step by step

### 1. <Page or screen name>
![<caption>](screenshots/01-....png)

**What I see:** the page's own words, quoted.
**What I think:** my honest reaction. Mark confusion as **WTF:** <question>.
**Fix:** one concrete change (optional).

### 2. ...

## Ask 001: my answers
1. Which reader, and was the question answered:
2. What I expected and could not find:
3. What would bring me back on Monday:
4. One thing to remove, one to add:

## Contradictions between pages
| Page A says | Page B says | Why it matters |
|-------------|-------------|----------------|

## What worked (keep this)
- ...

## What I could not do
- <step>: <why>.

## Top changes, in order
1. <one line each, most important first>
```

## 5. Already known before this test (do not re-report as new)

From the reference test (23 Oct, v0.8.1):

- The join link enrols as `editor`, not `power-user`.
- A group invitation runs out after three devices.
- The join page explains crypto before saying what the site is about; the one-line pitch is only in the footer.
- Feedback before joining loops back to "ask Dinis for an invitation".
- The side panel asks for an OpenRouter key, vault key and vault token without saying they are optional.
- Unexplained header items: £5.00 pill (drops to £4.99 on scroll), Newsprint, "342 new", Your desk, fade/hide/show.
- "Newsprint" and "Tell us who you are" appeared to do nothing.
- Source chips cut off (e.g. "Matthew Prince, Cloudflare CEO on…").

From my own first look at `/collaborators/` and `/team/` (23 Oct, v0.8.1), to confirm during the test:

- Ask 001's title says "four new features"; the page lists five.
- `/collaborators/` says the site has fifteen readers; `/team/` lists 16 audiences and the form offers 16.
- The feedback form can say "sent" but never "arrived", and does not say who reads feedback or how fast.
