# Receipt checker skill

This skill turns receipt PDFs or images into an Excel workbook with traceable rows and formula totals.

## Add it to Claude Desktop

1. Download [receipt-checker.zip](receipt-checker.zip).
2. Open Claude Desktop, then **Customize → Skills → Add → Upload skill**.
3. Select the ZIP and confirm the upload.
4. Open **Yours** and check that **receipt-checker** is enabled.

Skills require code execution and file creation to be enabled. A workplace administrator may control access. The skill consists of one readable [SKILL.md](receipt-checker/SKILL.md) file.

## Try it with the lab receipts

Start a new Claude chat and attach the [Tartine Bakery PDF](../01-receipts/lab/2026-04-12_Tartine_Bakery.pdf) and the [Uber PDF](../01-receipts/lab/2026-04-18_Uber.pdf). Copy the complete prompt.

```text
Use my receipt-checker skill on these two receipts. For this fictional classroom dataset, both receipts are in USD. Create receipt_skill_check.xlsx.
```

Compare your output with the [rehearsed workbook](receipt_skill_check.xlsx). Claude may prefix uploaded filenames with an internal identifier. Check the original filename suffix and receipt contents.

The expected total is USD 50.65 from USD 12.45 and USD 38.20. Open the workbook and confirm that each row names its source PDF, the Summary total is a formula, and any unclear fields are flagged. Use a disposable copy to raise one receipt amount by USD 1 and check that the summary rises by USD 1.

Open Claude's activity details and confirm that it read the receipt-checker skill. The workbook output alone does not prove that the skill was loaded.

The skill works with new receipt sets. It takes amounts and currencies from the receipts and your instructions.
