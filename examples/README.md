# Examples

Two invented pieces of work, written to test the skill, and the reports the skill produced from them. Neither is real. No number in them comes from real data. Both were written with some weak spots on purpose; some of them only show when numbers from different sections are put together. Both also have parts that are fine, to see whether the skill notices.

| Work | Who it is from |
|---|---|
| `student-idea.th.md` and `student-criteria.th.md` | A business idea contest entry by two second-year university students, with the contest's scoring rules |
| `brewbox-proposal.th.md` | A small company asking an investor for money |
| `student-idea-v2.th.md` | The same contest entry, revised after the first report. Some weak spots are fixed, some partly, some not, and one fix causes a new mistake on purpose: fuel is added to the costs, but the profit per box is not changed |

How the reports were made: Claude Code 2.1.316, headless (`claude -p`) on Linux, 2026-11-01, plugin loaded from a local folder (`--plugin-dir`), default model, in a clean home folder so that no personal instruction or memory files were loaded. One run each. In the runs the files were named `idea.th.md`, `criteria.th.md`, and `proposal.th.md`, so the reports use those names.

| Report | What was asked | How the panel read |
|---|---|---|
| `student-panel.th.md` | `/blame-me:blame-me idea.th.md`, nothing else | The skill proposed three seats (a contest judge, a classmate who would buy, someone who already sells lunch boxes), asked for the scoring rules, and waited |
| `student-report-normal.th.md` | the same, with that panel and the scoring rules | Three separate helpers |
| `student-report-harsh.th.md` | the same, in harsh mode (`โหมดแรง`) | Three separate helpers |
| `brewbox-report-normal.th.md` | panel given: an early-stage investor, the HR manager of a 30-person office (who decides to pay), an accountant; no brief | Three separate helpers |
| `brewbox-report-in-turn.en.md` | the same panel, report in English, helper tool switched off | One model playing each seat in turn |
| `student-reread.th.md` | `/blame-me:blame-me re-read idea-v2.th.md`, with the earlier normal report as `report.th.md`, the scoring rules, and the same panel | Three separate helpers. Made with the current rules (after the two-question limit was added) |

The only edit: in the three helper runs, the first lines were progress notes written while waiting for the helpers ("the panel is reading", "one reviewer is back") and were removed. Nothing else was changed, including the problems below.

Which rules each report was made with: after the first round of runs, two rules were added to the skill (look for hard words before reporting; do not state as fact what the work does not say). The two student reports and the English report were run again with those rules and replaced. `student-panel.th.md` and `brewbox-report-normal.th.md` come from the round before.

Problems in these reports, left in on purpose:

- The idea says "เตาแก๊ส" (a gas stove) without saying how many. The harsh student report, item 5, handles this the way the new rule asks ("งานยังไม่ได้บอกว่ามีกี่เตา", the work does not say how many stoves). The normal student report, item 6, still says "เตาลูกเดียว", which can be read as assuming there is only one.
- `brewbox-report-in-turn.en.md`, item 2, still says flatly that the company pays nothing for coffee today, even with the new rule. The proposal says staff buy coffee but not who would pay. `brewbox-report-normal.th.md` (made before the new rule) puts the same question under "Needs checking", which is the better handling.
- In the first round, a few words were less plain than the skill asks for ("helper" in a Thai report, "ค่าเสื่อม" for depreciation, "moot"). None of these appear in the three reports run again with the new rule. ("ค่าเสื่อม" in the English report is a quote from the proposal itself.)
- Some of the removed progress notes in the Thai student runs were in English. A rule asking for those notes in the work's language was added afterwards and has not been tried.
- Normal and harsh mode are meant to find the same weak spots. In the two student runs most weak spots match, but a few are ranked differently (starting to cook before knowing how many orders came in is "Must fix first" in harsh mode and "Should fix" in normal mode). Each mode was a separate run, so some difference between runs is expected.
- `student-reread.th.md`: all three reviewers gave exactly the same scores in every part (22 / 17 / 14). The report points this out itself. The reviewers ran as separate helpers, so this is not expected, and it was seen in one run only.

The short conversations quoted in the main README (a casual ask, a quick opinion, a panel proposal, code turned away) come from the same kind of runs and are quoted there in full or shortened with "…".
