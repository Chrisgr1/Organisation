Here’s how to use the SmartPersonalAssistant_Template.xlsx effectively—step by step, with rigor and long-term maintainability in mind.


---

1. Start with the Goals tab

Think long-term. You’re defining your strategic compass here.

Fields to fill:

Tips:

Keep goals fewer than 10. Clarity beats breadth.

Update LastReviewDate after every review.



---

2. Add Projects

Every project helps you reach a goal.

Fill in:


---

3. Add Actions

This is your daily driver. Concrete, small, focused.

Fill in:

Only one NextAction = TRUE per project — otherwise you lose clarity.


---

4. Use the Today View (create it yourself)

Create a new sheet called Today. Use this formula (Google Sheets or Excel 365+):

=FILTER(
  Actions!A2:Q,
  (Actions!G2:G = TRUE) *
  (Actions!F2:F <> "Completed")
)

Or use QUERY if in Google Sheets:

=QUERY(
  Actions!A2:Q,
  "SELECT A, C, D, H, I WHERE G = TRUE AND F <> 'Completed' ORDER BY H ASC, I ASC",
  1
)


---

5. Add Extra-Curriculars

In the Extra_Curricular tab:

Log workshops, side projects, events, anything that’s valuable but doesn’t need a project

Link to GoalID where relevant

Add a short reflection (what did you learn?)



---

6. Log Completed Items

When you finish a project or action:

1. Copy the row to the Completed_Log


2. Fill in:

ItemType = “Action” or “Project”

OriginalID

CompletionDate

Any final reflections

ArchivedDate = today’s date




You’ll now have a clean archive for:

Performance reviews

Personal retrospectives

Career storytelling



---

7. Review Tracker (Optional Use)

You can log your reviews manually or build filters that highlight:

Projects not reviewed in 30 days

Goals needing reflection

Actions without any competency logged


Use the Review_Tracker to schedule and check your own cadence.


---

8. Dashboard Ideas (optional)

You can fill the Dashboard tab with: | Metric | Formula | |--------|---------| | Active Goals | =COUNTA(FILTER(Goals!A2:A, Goals!F2:F = "High")) | | Overdue Actions | Count where DueDate < TODAY() and Status ≠ Completed | | Skills Used This Month | Pivot table on SkillUsed in Actions |

Let me know if you want help creating these formulas or pivot tables.


---

Next Steps

1. Open the file


2. Fill in 2–3 Goals, 3–5 Projects, and 5–10 Actions to get started


3. Filter for Today


4. Reflect weekly and quarterly


5. Use the Completed_Log for long-term value tracking



