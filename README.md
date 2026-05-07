# github-copilot-pbi-demo

Sample PBIX and prompts to do end-to-end semantic modeling with GitHub Copilot.

## Demo Goal

Show how to use GitHub Copilot plus prompt files in this repo to accelerate semantic model development in Power BI.

## Demo Flow

1. Start with a PBIX file.
2. Save the file as a PBIP project.
3. Explore the semantic model files in the PBIP folder.
4. Run prompt-driven updates to:
	- create relationships
	- create measures
	- generate descriptions
	- clean up the semantic model
5. Validate results in Power BI Desktop.

## Prerequisites

- Power BI Desktop
- A sample report and semantic model in PBIX format
- This repository cloned locally
- GitHub Copilot enabled in VS Code

## Step-by-Step Demo Script

### 1. Save PBIX as PBIP

In Power BI Desktop:

1. Open your PBIX file.
2. Select File > Save As.
3. Choose Power BI Project (*.pbip).
4. Save to a current folder.

Result: your model is now represented as files and folders you can inspect and edit. The original PBIX is still present if you need to roll back.

### 2. Explore PBIP Semantic Model Files

In VS Code:

1. Open the PBIP project folder.
2. Locate semantic model artifacts (tables, measures, relationships, and metadata files).

### 3. Create Relationships with Prompt

Use [prompts/1. create relationships.yaml](prompts/1.%20create%20relationships.yaml).

Ask Copilot to apply the prompt against the semantic model files and generate relationship definitions.

Expected outcome:

- Missing relationships are created.
- Relationship directions/cardinality are aligned to model intent.

### 4. Create Measures with Prompt

Use [prompts/2. create measures.yaml](prompts/2.%20create%20measures.yaml).

Ask Copilot to generate DAX measures in the model files based on the prompt guidance.

Expected outcome:

- Standard business KPIs are added.
- Measure naming follows consistent conventions.

### 5. Add Descriptions with Prompt

Use [prompts/3. create descriptions.yaml](prompts/3.%20generate%20descriptions.yaml).

Ask Copilot to add human-readable descriptions for tables, columns, and measures.

Expected outcome:

- Metadata becomes self-documenting.
- Field usage is easier for report authors and consumers.

### 6. Clean Semantic Model with Prompt

Use [prompts/4. clean semantic model.yaml](prompts/4.%20clean%20semantic%20model.yaml).

Ask Copilot to apply cleanup rules (for example: remove unused artifacts, normalize naming, and improve organization).

Expected outcome:

- Cleaner model structure.
- Better maintainability and readability.

### 7. Validate in Power BI Desktop

1. Reopen or refresh the PBIP project in Power BI Desktop.
2. Confirm relationships, measures, and descriptions appear as expected.
3. Run a quick report check using key visuals.