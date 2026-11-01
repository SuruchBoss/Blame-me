# Changelog

## 0.1.0 (unreleased)

First version.

- A pretend panel that reads a piece of work as if for the first time and finds its weak spots. For ideas, school and university projects, contest entries, pitches, business plans, proposals, case studies, resumes, applications, and articles. Code and personal matters are turned away.
- Written for a wide range of users, from students with no one to look at their work to working professionals. Plain words everywhere, in the skill's own files and in the reports it writes.
- The skill suggests 3 seats (at most 5) that fit the work and the user, asks who the work is for and whether there are scoring rules, and waits for the user to confirm or change the panel.
- Reviewers see only the work, the rules, and their own seat. They run as separate helpers where the tool allows, or one model plays each seat in turn; the report says which.
- Each weak spot has a level (Must fix first, Should fix, Good to fix), how many reviewers raised it, where it is in the work, when it goes wrong, and a quick way to check it that the user can really do. Sums are redone; anything that cannot be checked from the work goes under "Needs checking".
- Every report also lists what already holds up (things the panel tried to break and could not), names one place to start, and ends by offering help.
- Scores only when the user gives scoring rules, using those rules.
- Before reporting, the skill looks for hard words (accounting, legal, uncommon English, English words in a Thai report) and replaces or explains them.
- What the work does not say is written as an open question ("The work does not say..."), not as a fact. In the trial runs this worked in one report out of three.
- Notes while waiting for reviewers use the work's language (added after the trial runs; untested).
- A casual ask ("is this idea good?", "any feedback?", "ไอเดียนี้ดีไหม", or the same in any language) first gets one question: a quick opinion, or a full panel review. A quick opinion is a normal reply without the panel. Asking on purpose ("/blame-me", "blame this", "ด่าเลย") skips the question.
- Two modes: normal and harsh. Harsh changes the wording, not the findings.
- Re-read mode marks earlier weak spots as fixed, partly fixed, or not fixed, then reads the new version fresh.
- Report layouts in English and Thai.
