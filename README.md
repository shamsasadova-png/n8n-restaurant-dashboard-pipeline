# Restaurant Daily Dashboard Pipeline (n8n)

An n8n workflow that automatically collects a restaurant's daily sales, inventory, and staff data, then uses AI to analyze it.

## Problem
Manually reviewing a restaurant's daily sales, inventory levels, and staff schedule was time-consuming, and important trends were often missed.

## Solution
An n8n workflow that runs automatically every day at a set time:
1. Pulls data from three separate Google Sheets sources (Sales, Inventory, Staff)
2. Combines them using a Merge node
3. Aggregates them into a single structure to send to the AI
4. Claude AI (Anthropic) analyzes the data — sales trends, low-inventory alerts, staff status
5. Writes the results to a dedicated "AnalysisLog" tab in Google Sheets

## Tech Stack
- n8n (workflow automation)
- Google Sheets API
- Claude API (Anthropic)

## Diagram
   ![Workflow Diagram](Screenshot%202026-09-17%20105739.png)
## Result
A fully automated report is generated every day at 9:00 AM — eliminating the need for manual analysis.
