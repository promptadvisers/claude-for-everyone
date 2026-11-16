# Workshop prompts

Copy the complete paragraph in each section into Claude.

## Demo · Receipts to Excel

Attach the five PDFs in 01-receipts/demo, then paste this in Claude.

```text
Read the five attached receipts and create expense_report.xlsx. For this fictional classroom dataset, all amounts are USD. Make a Receipts sheet with one row per source and columns for file name, date, vendor, total, currency and category. Make a Summary sheet with formulas that total the receipts by category and calculate a grand total. Mark unclear values for review. Create a new workbook and leave the source files alone.
```

**Check:** Five rows and a formula total of USD 177.98

## Lab 1 · Check two receipts

Use the two PDFs in 01-receipts/lab, or inspect the workbook in 01-receipts/examples.

```text
Create receipts_check.xlsx from these two receipts. For this fictional classroom dataset, both receipts are in USD. Include the source file name, vendor, date, amount and currency for each. Calculate the combined total with a formula. Flag any field you are unsure about.
```

**Check:** Two source rows, matching amounts and a formula total

## Demo · Brief from three reports

Open the project with the three short reports in 02-synthesis/inputs, or attach them in a new chat.

```text
Using only the three supplied reports, write a one-page briefing for an operations manager. Give the main finding, two supporting findings and one open question. For each factual claim, name the report and page or section. Include a short evidence table. State where the reports disagree or leave a gap.
```

**Check:** A one-page brief with claims tied to source passages

## Lab 2 · Audit the draft brief

Attach the three short reports and flawed-brief.md from 02-synthesis/lab.

```text
Check this draft against the three reports. For each factual claim, mark it as supported, contradicted or unsupported and give the report and page or section. Rewrite the weakest claim using only what the sources establish.
```

**Check:** Mark the pilot claim unsupported and replace it with a sourced statement

## Demo · Read from a connected app

Use a preconnected training workspace with the Sample Operations Brief.

```text
Find the training document titled “Sample Operations Brief” in the connected app. List its three decisions and link to the source. Ask me if you find multiple documents with that title. Leave the document unchanged.
```

**Check:** Three decisions and a link to their source

## Demo · April sales review

Attach 03-sales/inputs/april_sales.csv and paste the full prompt in Claude.

```text
Using the attached April sales CSV, first identify the columns you will use and check the number of rows. Create april_review.xlsx with source data, revenue by region and product, and the three highest-revenue dates. Use the revenue_usd column as the source of recorded revenue and formulas to aggregate it. Show the formulas and explain the grouping fields. Then create a four-slide april_review.pptx with the headline, regional results, product results and one supported recommendation. Draft a short email summary in summary_email.md. Include the same exact total in all three outputs. Leave the CSV unchanged and do not send anything.
```

**Check:** All three deliverables agree on USD 20,298,481.72

## Demo · Propose a weekly briefing

Use the cloud training note, or show the prepared proposal using the same fictional notes.

```text
Draft a recurring Monday 9:00 a.m. Toronto-time task to summarize the training project’s weekly notes into three decisions and three open questions. Use the “Weekly Operations Notes” document in the training Drive as the input. Link the source in each result. Show the proposed schedule and instructions for review. Put each result in Claude for me to review.
```

**Check:** Confirm the cadence, time zone, source and expected output before scheduling

## Demo · Build Mission Control

Start a new Claude conversation. This demo uses no starting files.

```text
Create an interactive Claude Artifact called Mission Control, a one-page 3D-style solar system explorer. Show a glowing sun and three orbiting planets: Earth, Mars, and Saturn. Clicking or selecting a planet should highlight it and show one short fact. Add Pause and Resume for the orbits. Use CSS perspective and inline graphics so it works without downloads, external libraries, or a network connection. Open the working preview beside this chat.
```

**Check:** Select Mars, read its fact, then test Pause and Resume

## Demo · Edit Mission Control

Paste this in the same conversation after the preview opens.

```text
Update this same Artifact. Start with Mars selected, and add a Reset view button that returns to Earth with the orbits paused. Keep the planet facts and the rest of the design.
```

**Check:** Mars starts selected. Reset view selects Earth and pauses the orbits
