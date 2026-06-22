# Salesforce Pipeline Hygiene Dashboard
## Project Summary

Built a Salesforce pipeline hygiene workflow to help Sales Ops identify at-risk opportunities, forecast cleanup issues, and deal-review priorities before an executive forecast call.

This project includes custom Opportunity fields, filtered list views, Salesforce reports, and a dashboard designed to turn messy CRM data into a cleaner leadership review process.

## The Friday Forecast Fire Drill

It is late Friday afternoon. The week is almost over. Slack is quiet. Everyone is mentally halfway to the weekend.

Then the VP of Sales drops this message:

> “I have a pipeline review with the CFO Monday morning. Salesforce says we have enough pipeline, but I do not trust the forecast. Can you tell me which deals are real, which ones need cleanup, and where the risk is hiding?”

Translation:

The spreadsheet vibes are bad. The forecast is shaky. The CFO is about to ask very reasonable questions in a very unreasonable tone.

This Salesforce workflow was built to help Sales Ops quickly identify pipeline risk, forecast cleanup issues, and deal-review priorities before leadership walks into a Monday forecast call.

---

## Business Problem

The pipeline looked healthy on the surface, but the underlying Salesforce data had several red flags:

* Opportunities with overdue close dates
* Deals marked as forecastable even though the stage did not support that confidence
* Weak or missing next steps
* High-value deals sitting too early in the sales cycle
* Opportunities that needed manager review before being trusted in the forecast

The issue was not just “bad data.” The real issue was forecast confidence.

Leadership did not need another generic opportunity list. They needed a practical workflow that answered:

* Which deals need review?
* Why are they risky?
* Which opportunities are creating the most pipeline exposure?
* What should Sales Ops and sales leaders clean up before the CFO call?

---

## Objective

Build a Salesforce pipeline hygiene workflow that helps Sales Ops flag and review risky opportunities before forecast discussions.

The workflow needed to support:

* Opportunity-level risk tracking
* Forecast cleanup visibility
* List views for fast deal review
* Reports for leadership-level analysis
* A dashboard that summarizes the biggest pipeline hygiene issues


## Key Results

- Flagged **5 opportunities** for forecast review
- Identified **$1.44M in forecast cleanup pipeline**
- Surfaced **4 at-risk opportunities** totaling **$1.015M**
- Highlighted forecast risk tied to overdue close dates, stale activity, high-value early-stage deals, and forecast category mismatch
- Created a repeatable Sales Ops workflow for reviewing pipeline hygiene before executive forecast calls

---

## Salesforce Configuration

To make pipeline risk visible inside Salesforce, I created custom Opportunity fields designed around real Sales Ops review behavior.

Custom fields included:

- **Pipeline Risk Status:** Classifies an opportunity as Healthy, Needs Review, or At Risk.
- **Next Step Quality:** Identifies whether the next step is clear, weak, missing, or needs an update.
- **Risk Reason:** Explains why the opportunity needs attention.
- **Forecast Review Needed:** Flags opportunities that should be reviewed before the forecast call.
- **Sales Ops Notes:** Documents cleanup notes, forecast concerns, and manager follow-up actions.

---

## Opportunity Risk Configuration

The example below shows a deal marked as **Commit** while still in **Qualification**. That mismatch creates forecast risk because the deal is being treated as more reliable than the actual sales stage supports.

This is exactly the type of issue Sales Ops should catch before a CFO forecast review.

![Opportunity Risk Fields](opportunity-risk-fields.png)

---

## Sample Pipeline Scenario

I created a small set of sample NimbusAI opportunities to simulate a messy sales pipeline.

The sample opportunities included:

* Overdue close dates
* Stale activity
* Forecast category mismatches
* High-value early-stage opportunities
* Deals requiring manager review
* One healthy opportunity used as a control record

This allowed the Salesforce workflow to separate healthy pipeline from opportunities needing cleanup.

---

## List View 1: Forecast Cleanup Needed

The **Forecast Cleanup Needed** list view surfaces opportunities where the Forecast Review Needed checkbox is selected.

This gives Sales Ops a fast working queue for deals that need attention before leadership uses the pipeline in a forecast conversation.

![Forecast Cleanup Needed List View](forecast-cleanup-list-view.png)

---

## List View 2: At-Risk Opportunities

The **At-Risk Opportunities** list view narrows the focus even further by showing only opportunities where Pipeline Risk Status is marked as At Risk.

This gives managers a cleaner view of the deals most likely to create forecast problems.

![At-Risk Opportunities List View](at-risk-opportunities-list-view.png)

---

## Report 1: At-Risk Pipeline by Rep

The **At-Risk Pipeline by Rep** report groups at-risk opportunities by Opportunity Owner and summarizes the pipeline amount tied to those deals.

In a real sales org, this would help leadership quickly understand which reps or teams have the most forecast exposure.

In this Developer Edition build, the sample opportunities are owned by one user, but the report structure is built the same way it would be used in a live revenue organization.

![At-Risk Pipeline by Rep Report](at-risk-pipeline-by-rep-report.png)

---

## Report 2: Forecast Cleanup Needed by Risk Reason

The **Forecast Cleanup Needed by Risk Reason** report groups flagged opportunities by the reason they need cleanup.

This turns a messy pipeline review into a cleaner leadership conversation:

Instead of saying, “We have a bunch of questionable deals,” Sales Ops can say:

* This amount is tied to high-value early-stage opportunities
* This amount is tied to forecast category mismatch
* These deals need manager review
* These deals are stale or overdue

That is a much better conversation than everyone staring at Salesforce and pretending the vibes are fine.

![Forecast Cleanup by Risk Reason Report](forecast-cleanup-by-risk-reason-report.png)

---

## Dashboard: NimbusAI Pipeline Hygiene Dashboard

The final dashboard brings the workflow together.

It gives sales leadership a quick view of:

* Forecast cleanup exposure by risk reason
* At-risk pipeline by opportunity owner
* The specific deals behind the risk

The goal is simple: make the pipeline easier to inspect before the CFO asks uncomfortable questions with a spreadsheet open.

![Salesforce Pipeline Hygiene Dashboard](salesforce-pipeline-hygiene-dashboard.png)

---

## What This Workflow Helps Sales Ops Do

This Salesforce workflow helps Sales Ops and sales leadership:

* Identify risky opportunities before forecast calls
* Separate healthy pipeline from cleanup-needed pipeline
* Spot forecast category mismatches
* Review weak or missing next steps
* Create a repeatable pipeline hygiene process
* Improve forecast confidence before executive review

---

## Tools Used

* Salesforce Developer Edition
* Salesforce Opportunity object
* Custom Opportunity fields
* Salesforce list views
* Salesforce reports
* Salesforce dashboards
* GitHub for documentation and portfolio presentation

---

## Skills Demonstrated

This project demonstrates hands-on ability to:

* Configure custom Salesforce fields
* Build opportunity-level pipeline hygiene logic
* Create operational list views for Sales Ops workflows
* Build Salesforce reports with filters, groupings, and summaries
* Create a leadership dashboard from Salesforce reports
* Translate messy CRM data into actionable forecast review insights
* Document a business workflow in a clear, portfolio-ready format

---

## Key Takeaway

A forecast does not fall apart on Monday morning. It usually starts falling apart weeks earlier through stale activity, unrealistic close dates, weak next steps, and deals being forecasted more confidently than they should be.

This Salesforce workflow helps catch those issues before the forecast call turns into a crime scene.

The goal was not just to build fields, reports, and dashboards.

The goal was to build a practical Sales Ops workflow that helps leadership trust the pipeline before they have to defend it.
