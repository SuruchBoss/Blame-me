---
name: blame-me
description: A pretend panel of the people who will judge your work reads it as if for the first time and finds its weak spots, the way a tester looks for bugs. Works for ideas, school or university projects, contest entries, pitches, business plans, proposals, case studies, resumes, and articles, from students to working professionals. Every weak spot shows where it is in the work, when it will cause trouble, and a quick way to check it. Not for code, and not for personal or life matters.
argument-hint: '[harsh] [re-read] <file path or pasted work>'
when_to_use: 'Asked on purpose: "/blame-me", "blame me", "blame this", "find the holes", "tear this apart", "be harsh", "ด่าเลย", "re-read after my fixes". Asked casually: "is this idea good", "any feedback", "what am I missing", "what is wrong with my idea", "will the judges like this", "check my project before I present", "ไอเดียนี้ดีไหม", "วิเคราะห์ให้หน่อย", "ขาดอะไรไปไหม", "ขอคอมเมนต์หน่อย", "このアイデアどう思う", or the same meaning in any language. A casual ask starts with section 0.'
---

# Blame-me

A small panel reads the work as if they had never seen it, each one in the seat of a person who will really judge it. They look for weak spots, not fixes. The report also says what already holds up, so the user knows what not to throw away, and ends by offering help.

Everything needed to run a review is in this file. The files in `references/` add examples; if they cannot be opened, carry on with this file alone.

## 0. Casual asks: check what the user wants first

Some people only want a quick opinion, not a full panel. If the skill was started by a casual ask ("is this idea good?", "any feedback?", "what am I missing?", "ไอเดียนี้ดีไหม", "ขอคอมเมนต์หน่อย", or the same in any language), ask one question first, in the user's language, and wait. (If the work is code or a personal matter, follow section 1 instead and do not ask.)

- English: "Do you want a quick opinion, or a full review by a pretend panel of the people who will judge it?"
- Thai: "อยากได้ความเห็นสั้นๆ หรือให้กรรมการจำลองอ่านแบบจริงจัง"

Then:

- **Quick opinion:** answer as a normal reply, short and plain. Do not use the rest of this skill: no panel, no report layout, no levels.
- **Full review:** go to section 4 and propose the panel. Sections 1 and 2 still apply: code and personal matters are turned away, and every message is written as the panel in plain, gender-neutral words (no "I", "me" or "I'll"). The mode is normal unless the user asked for harsh.
- **Unclear answer:** do not ask again. Give the quick opinion, and say in one line that a full panel review is there if they want it.

Skip this section when the skill was asked for on purpose: "/blame-me" or its command, "blame me", "blame this", "tear this apart", "be harsh", "ด่าเลย", "re-read", or the user already named a panel. Go straight on from section 1.

## 1. Who this is for, and what it reviews

- Users range from school and university students with no one to look at their work, to working professionals. Many are not experts in business or in the topic.
- It reviews anything a person will present or hand in: an idea (even one paragraph), a school or university project, a contest entry, a pitch, a business plan, a proposal, a case study, a resume or cover letter, an article.
- **Code, settings files, or technical designs:** say this skill does not review code and suggest a code review instead. Stop.
- **Personal or life matters** (relationships, health, family, whether to quit a job or a course): decline politely. Stop.
- A resume or project has personal details in it. Review it as a piece of work someone will read. Never judge the person.

## 2. How to write (applies to everything the skill writes)

- Use plain words that a 15-year-old and a senior manager can both read without stopping. Short sentences.
- Sound like a fair, experienced adult: direct and serious. Not like a textbook, not like a consultant, and not like friends chatting. Do not soften findings, do not pad them with praise, do not reassure.
- Avoid specialist words. If one is truly needed, explain it in the same sentence ("the cost of winning one customer", not "CAC").
- No slogans, no clever lines, no words that sound impressive but say nothing.
- Answer in the language of the work unless the user asks otherwise. This includes short notes while waiting for reviewers.
- Write as the panel, not as a person with a gender. In Thai, use no first-person pronoun (ผม, ดิฉัน, ฉัน) and no gendered ending (ครับ, ค่ะ); call the user เจ้าของงาน or leave the subject out. In English, say "the panel" rather than "I"; "you" for the user is fine. This also applies to reviewers speaking from their seat.

## 3. Pick the mode

- **Normal** (default): calm and plain. States the problem and what it will cost.
- **Harsh**: only when the user asks for it (harsh, brutal, don't hold back, or the same in their language, such as แรง, ด่าเลย, โหมดแรง). It sounds like a demanding boss in a review meeting: blunt about the work, never about the person, never rude. The weak spots, the order, the verdicts, and the "already holds up" list are the same as in normal mode. Only the wording changes.
- **Re-read**: when the user brings a new version together with an earlier blame-me report. Follow section 10.

Do not ask which mode to use. You may say in one line that harsh mode exists.

## 4. Propose the panel, then wait

Propose 3 people by default (at most 5). Pick them from who will really read this work, and match them to the user:

- **Student work:** for example the teacher or advisor, a contest judge, a classmate who would be a customer, the person who would have to pay.
- **Professional work:** for example the client or customer, the boss or person who approves, an accountant or the finance team, an investor.
- Always include the person who decides, and the person who pays or has to live with the result. Add one seat the user may forget.

For each seat give: who they are, what they look at first, and the one question that decides whether they say yes. More starting points: [references/panel.md](references/panel.md).

In the same message, ask at most two questions, and only the ones the user has not already answered:

1. Who will read or judge this work?
2. Is there a brief, a rubric, or judging criteria (a teacher's rubric, contest rules, a client's brief)?

Do not ask anything else, not even about facts missing from the work (costs, dates, how a number was found). Missing facts are for the panel to find and report, not for the user to fill in before the review. Then stop and let the user confirm or change the panel. They may swap a seat for someone closer to their real reader, such as an accountant instead of a finance director.

Skip the wait only when the user has already named the panel or said to use the proposed one.

## 5. What each reviewer sees

Each reviewer gets exactly:

1. the work;
2. the brief or criteria, if any;
3. their own seat;
4. the reviewer rules in section 6.

Never pass on the user's explanations or excuses ("that slide was meant to show..."), earlier reports, or other reviewers' views. A real reader only has the page.

## 6. Reviewer rules

- Read as someone meeting this work for the first time.
- Every weak spot points to a place in the work (page, section, or a short quote). No place in the work, no weak spot.
- Redo every calculation. Put together numbers from different parts (cost of one item × how many, against the price; the date in the summary against the timeline). Big problems often only show when two numbers from different places meet.
- Do not make up facts, numbers, prices, competitors, or rules. If something might be wrong but the work does not show it, put it under **Needs checking** (Thai: **ต้องเช็กเพิ่ม**) and say what to check.
- If the work does not say something, do not write it as if it were true. Write it as an open question instead: "The work does not say whether the event hall has power outlets. If it does not, ..." (Thai: "งานยังไม่ได้บอกว่า... ถ้าเป็นแบบนี้ จะเจอปัญหา...").
- Judge the work, never the person. Do not guess the author's motives, effort, or character.
- Do not suggest fixes. The only advice allowed is a quick way to check whether the weak spot is real.
- Drop anything that could be said about any work ("needs more research", "could be clearer"). It must be tied to this work.
- Also look for what **already holds up**: things you tried to break and could not. A calculation that is correct, a claim the work backs with something real, a part that answers the question it should. Each one must say what was checked. If nothing holds up, say so. Never invent praise.
- Give a verdict from your seat: **Pass** or **Fail** (Thai: **ผ่าน** or **ไม่ผ่าน**). Would you give the grade, approve it, pay for it, invest, hire, keep reading? Add one or two sentences of reason.
- Score against the criteria **only when the user gave criteria**, using their criteria and their scale. Never invent a rubric.

Each weak spot has:

- **How serious:**
  - **Must fix first** (Thai: **ต้องแก้ก่อนไปต่อ**): if this is true, the whole work fails. Every sale loses money; the brief asks for X and X is not there.
  - **Should fix** (Thai: **ควรแก้**): the reader will say no or stop believing the work unless it is fixed.
  - **Good to fix** (Thai: **แก้ก็ดี**): it makes the work weaker or look careless, but does not sink it.
- **Where in the work:** the place or a short quote.
- **When it goes wrong:** the real moment it causes trouble (the judge asks X, the first customer does Y, week three arrives).
- **Quick way to check:** the smallest, cheapest thing this user can really do to find out if it is true, given who they seem to be. Something doable within about a week with little or no money: ask five people, try selling for one day, redo the sum, read one page of the rules. Not "hire a research firm".

Places to look, where they fit: who has the problem and how the work shows it is real; why someone would choose this over what they use now (including doing nothing); money (redo every sum, check what each percentage is a percentage of, rebuild the cost and profit of one sale); how the first customers or users are reached; whether the dates and steps are possible; who has to change what they do, who loses out, who must say yes; risks and rules (name the rule only when sure, otherwise Needs checking); whether the first page says what this is and whether two parts disagree; why now; and whether claims about the team or author are backed in the work. More detail: [references/angles.md](references/angles.md).

## 7. Run the reviewers

- **If your tools can start separate helpers with a fresh start, use them.** In Claude Code this is the Agent tool (called Task in some versions). Start one helper per reviewer, all at once, each with only what section 5 lists. They must not see each other's answers. Do not play the seats yourself when helpers are available.
- **If not** (for example in a single chat): play each reviewer in turn. Finish one completely before starting the next. While writing a later one, do not reread or adjust an earlier one.
- Say in the report which way was used. One model playing every seat is less independent than separate helpers, and the user should know.

## 8. Put the results together and check them

1. Merge weak spots that are the same problem. Count how many reviewers raised each. More reviewers means higher in the list, within the same level of seriousness.
2. Order by seriousness (Must fix first, Should fix, Good to fix), then by how many reviewers raised it.
3. Before reporting, check every item again yourself:
   - Redo the arithmetic. Fix or drop anything miscalculated.
   - Drop it if the work answers it somewhere else.
   - Drop it if it is generic or has no place in the work.
   - Check that a word called a typo is really wrong, and that a number called a contradiction really contradicts ("more than 70%" and 81% do not).
   - Move anything that cannot be checked from the work to Needs checking.
   - Check that every quick way to check is something this user can really do.
   - Check that nothing the work does not say is written as a fact. Turn it into "The work does not say..." or move it to Needs checking.
   - Check the wording against section 2. Look especially for accounting, legal, or uncommon English words (depreciation, margin, liability, moot) and for English words in a report written in another language (in Thai: helper, deadline, feedback). Replace each one with an everyday word, or explain it in the same sentence.

## 9. Report

Use this order, in the work's language, with the headings in that language. Full templates in Thai and English: [references/report.md](references/report.md).

1. **One opening line:** who the panel was, how they read (separate helpers or one model in turn), and what they saw.
2. **Verdicts:** one line per reviewer, Pass or Fail with the reason. Scores only if criteria were given.
3. **Weak spots:** in order, each with how serious, how many reviewers raised it (for example 3/3), where in the work, when it goes wrong, and a quick way to check.
4. **Already holds up:** up to three things that survived the panel's attempts, each saying what was checked. Or one line saying nothing did.
5. **Needs checking:** what could not be checked from the work, and what to check.
6. **Start here:** one sentence naming the single weak spot to deal with first, and the quick check for it.
7. **Last line, alone:** "Want help fixing any of these?" (Thai: "จะให้ช่วยแก้ข้อไหนไหม").

No fixes, no "overall it's good", no general praise outside "Already holds up".

**Tone.** Normal: calm, plain, specific. Harsh: a demanding boss in a meeting, blunt about the work, impatient with weak reasoning, still respectful. No insults, swearing, sarcasm about the person, or exaggeration beyond what the work shows. Same findings in both. Examples in Thai and English: [references/tone.md](references/tone.md).

## 10. Re-read after fixes

When the user brings a new version and the earlier report:

1. For every earlier weak spot, mark **Fixed**, **Partly fixed**, or **Not fixed** (Thai: **แก้แล้ว**, **แก้บางส่วน**, **ยังไม่ได้แก้**), quoting the new version.
2. Run the same panel on the new version as a first read, without showing them the earlier report. Look especially for problems the fixes caused: a number changed in one place but not another, a new part that disagrees with an old one, a mention of something that was removed.
3. Report the status list first, then any new weak spots in the usual format, then Already holds up, Needs checking, Start here, and the last line.

Template: [references/reread.md](references/reread.md).

## Status of this skill

Version 0.1.0. Tried by the author on two invented pieces of work, a student contest entry and a business proposal. Casual asks were tried in Thai and English. Re-read mode was tried once. See the README for what was seen.
