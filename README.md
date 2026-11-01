# Blame-me

**Let a pretend panel find what is wrong with your work, before the real one does.**

[ภาษาไทย](README.th.md)

Tomorrow you present. Maybe it is a class project, an idea for a contest, or a proposal for your boss. You have read it three times and it looks fine, because you know what every part means. The people judging it tomorrow do not. They will read it for the first time, and one of them may put two of your numbers side by side and see that the plan cannot work.

Blame-me is for the night before. Give it your work, and the rules or the brief if there are any. It suggests a small panel of the people who will really judge it: a teacher, a contest judge, a customer, an accountant. You can change who sits on it. Then each of them reads your work as if for the first time, without your explanations, and looks for weak spots the way a tester looks for bugs.

You get back a list of weak spots, most serious first. Each one shows where it is in your work, when it will cause trouble, and a quick way to check it that you can do this week. You also get a short list of what already holds up, so you know what not to throw away, and the one thing to start with. It does not rewrite your work for you. At the end it asks which weak spots you want help with.

It is for anyone who has to present work: a student with no one to look at their project, or a professional getting ready for a client. The wording is plain on purpose.

There are two modes. **Normal** is calm and plain. **Harsh** sounds like a demanding boss in a meeting: blunt about the work, never about you, never rude. Both are meant to find the same weak spots; only the wording changes.

If grill-me is the friend who keeps asking "why?" until your plan is clear, blame-me is the reviewer who points at the page and says "this is where it falls over".

**What has actually been tried** (by the author, once each, on two invented pieces of work, 2026-11-01; details in [Limits and untested parts](#limits-and-untested-parts)):

- A student contest entry (lunch boxes delivered to classroom buildings) and a business proposal (coffee for offices), both invented, each with weak spots planted in it. In every run the panel found the main planted ones. For the students: 100 boxes at 2 minutes each cannot be delivered in a one-hour lunch break; only 20 friends back the target of 100 a day; the monthly target counts 30 days although they only sell on weekdays. For the proposal: every office loses money at the stated price, which only shows when numbers from three sections are multiplied together. The author redid every sum in the reports; they were right.
- "Already holds up" picked out the parts that were fine on purpose: the students' own count of the lunchtime queue, and the sums that were correct.
- Given no panel, it suggested seats that fit students (a contest judge, a classmate who would buy, someone who already sells lunch boxes) and asked for the scoring rules.
- With the contest's scoring rules, each reviewer scored against those rules, and the scores added up.
- The quick checks were things a student can really do: deliver 20 boxes and time it, take paid pre-orders for three days, count the queue on four more days.
- Harsh mode was blunter about the work and said nothing about the students themselves.
- It still made mistakes, kept in the examples. A rule against stating what the work does not say worked in one report and not in two others: one still reads as if the students have only one stove, and one states as a fact who pays for the office coffee, which the proposal does not say. See [examples/README.md](examples/README.md).

The two pieces of work and the five reports are in [examples/](examples/).

**Not tried yet:** re-read after fixes, Claude.ai or other chat apps, installing from GitHub, and real work by anyone other than the author.

## What it is for

- Ideas, even a single paragraph
- School and university projects, reports, and presentations
- Contest entries and pitches
- Business plans and proposals to a client or a boss
- Case studies and take-home tasks for a job
- Resumes, cover letters, and scholarship or university applications
- Articles and posts

It is **not** for code or technical designs (use a code review), and it does not touch personal or life matters. A resume is read as a piece of work someone will judge, never as a judgement of you.

## Quick start

You need Claude Code.

```bash
claude plugin marketplace add SuruchBoss/Blame-me
claude plugin install blame-me@blame-me
```

Then open a new session (a skill installed during a session is not available in that same session) and type:

```
/blame-me:blame-me path/to/your-work.md
```

or just say it: "blame this proposal", "find the holes in my project". If you ask more casually, such as "is this idea good?" or "any feedback?", it first asks one question: do you want a quick opinion, or a full review by the panel? A quick opinion is a normal short reply without the panel. For harsh mode, add `harsh`, or say "be harsh":

```
/blame-me:blame-me harsh path/to/your-work.md
```

Without the marketplace, copy the folder `plugins/blame-me/skills/blame-me/` into `~/.claude/skills/` or into your project's `.claude/skills/`.

## How a review goes

1. **It checks what you gave it.** Code and personal matters are turned away.
2. **It suggests a panel.** Three people by default, at most five, each with who they are, what they look at first, and the one question that decides whether they say yes. You keep them or change them. It also asks who the work is for and whether there are rules or a scoring sheet.
3. **Each person reads on their own.** They see only your work, the rules, and their own role. Not your explanations, and not each other's views. In Claude Code they run as separate helpers. Where that is not possible, one model plays each role in turn, and the report says so.
4. **The results are put together and checked.** The same weak spot raised by several people moves up the list. Every sum is redone. Anything without a place in your work, anything that could be said about any work, and anything your work already answers is dropped. Things that cannot be checked from your work go under "Needs checking" instead of being stated as facts.
5. **You get the report.** A pass or fail from each person with a reason (scores only if you gave scoring rules), the weak spots, what already holds up, what needs checking, where to start, and one last line: "Want help fixing any of these?"
6. **Re-read.** After you change your work, give it the new version and the old report. It marks each old weak spot as fixed, partly fixed, or not fixed, then reads the new version fresh to catch anything the changes broke.

Weak spots have three levels: **Must fix first** (if true, the whole work fails), **Should fix** (the reader will say no unless it is fixed), and **Good to fix** (it makes the work weaker but does not sink it).

Each weak spot looks like this (item 1 of [examples/brewbox-report-in-turn.en.md](examples/brewbox-report-in-turn.en.md), shortened; the Thai quotes are translated):

```
1. Each office costs more than it pays (Must fix first, raised by 3/3)
   Where: "Cost per office per month" table, and "gross profit about 60%".
   When it goes wrong: 20 people × 2 cups × 15 g × 22 days = 13.2 kg of beans, 7,920 baht.
     With shipping and equipment wear, 8,390 baht. The price is 4,900 baht,
     so every office loses about 3,490 baht a month.
   Quick way to check: Redo the bean sum in a spreadsheet using only numbers
     from the proposal. It takes ten minutes.
```

## Normal and harsh, side by side

The same weak spot in an invented school idea, a tutoring app where students pay 20 baht a session and the only support is "my friends said it's a good idea":

> **Normal:** The whole income section depends on 1,200 students using it every week. The only support is that friends liked the idea. Liking an idea is not the same as paying 20 baht for it every week.

> **Harsh:** Every number in the income section stands on "my friends said it's a good idea". That will not survive the first question from a judge. Friends being nice does not mean people will buy.

More examples in both languages: [references/tone.md](plugins/blame-me/skills/blame-me/references/tone.md).

## What is in the package

```
plugins/blame-me/skills/blame-me/
  SKILL.md              everything needed to run a review
  references/
    panel.md            who to put on the panel, for student and professional work
    angles.md           places to look, and what does not count as a weak spot
    report.md           report layout, English and Thai, and plain-word swaps
    tone.md             normal and harsh, with examples
    reread.md           re-read after fixes
examples/               two invented pieces of work and the reports made from them
```

`SKILL.md` holds every rule on its own, so a review still works if the tool cannot open the other files.

## Limits and untested parts

All runs below: Claude Code 2.1.316, headless (`claude -p`), Linux, 2026-11-01, plugin loaded with `--plugin-dir`, default model, one run each. Costs are what the CLI reported for that run.

| Part | Status |
|---|---|
| Suggesting a panel and waiting | Tried once with this version (student idea): seats fitted a student, it asked for the scoring rules and waited (about $0.08). An earlier draft did the same with the business proposal. |
| Reviewers as separate helpers | Tried in five runs: three helpers started together each time (about $0.5 to $0.8 a run). |
| One model playing each seat in turn | Tried once with the helper tool switched off, report in English. The report said which way was used (about $0.1). |
| Scoring against rules | Tried twice with a contest's scoring rules: scores used the rules' parts and added up. |
| Normal and harsh finding the same things | Mostly. In the two student runs the main weak spots matched; a few were ranked differently. |
| Plain words | In the first round, a few harder words got through ("helper", "ค่าเสื่อม" for depreciation, "moot"). After a rule to look for them was added, the three reports run again had none. |
| Gender-neutral wording in Thai | Before the rule was added, one early run wrote "ผม" (a male "I"). After it, no report did. |
| Notes while waiting, in the work's language | Some notes in Thai runs were in English. A rule was added afterwards; untested. |
| Accuracy | Every sum the author checked was right. Some findings still go further than the work says, even after a rule against it was added (see [examples/README.md](examples/README.md)). Read the findings before acting on them. |
| Re-read after fixes | Untested |
| Casual asks ("is this idea good?") | Tried with one Thai and one English idea, in Claude Code 2.1.316. A casual ask loaded the skill on its own each time, and it asked the one question in the user's language and waited (6 runs). Answering "short" gave a plain reply with no panel (Thai, 1 run). Answering "full review" went to the panel (Thai 1, English 2). The first English run wrote "tell me" and "I'll run it"; after a rule was added, the re-run did not. The Thai full-review run asked six questions instead of the two the skill allows. Asking on purpose (`/blame-me:blame-me`, with and without "ด่าเลย") skipped the question (2 runs). About $0.06 to $0.15 a turn. Other languages untested. |
| Turning away code and personal matters | Untested |
| Resumes, applications, articles | Untested |
| Claude.ai or other chat apps | Untested |
| Installing from GitHub | Untested; only `--plugin-dir` was used |
| Your own instruction files | If a CLAUDE.md or similar sets a voice or pronouns, the report may follow it. Seen once during development; the example runs used a clean home folder. |
| Real work by other people | Untested |

A pretend panel is not a real one. It does not know your market, your teacher, or the person who will read your resume. It can only read what is on the page, carefully and without taking your side. Treat "Needs checking" as homework, not as findings.

## License

Apache License 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

This project is not affiliated with or endorsed by Anthropic.
