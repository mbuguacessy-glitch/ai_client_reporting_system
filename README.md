# Automated Client Reporting System

## What this does
Automatically generates and delivers professional weekly performance
reports to all active clients every Monday at 7am. Reports include
trend analysis comparing this week to last week and specific
next-week recommendations. Zero manual report writing.

## The problem it solves
Manual report writing takes 2–4 hours per client per month.
Quality is inconsistent — rushed weeks produce thin reports.
Clients miss their reports when teams are busy. This system
produces consistent, professional reports on a fixed schedule
regardless of team workload.

## Measurable result
- Report writing time: from 2–4 hours per client → 0 minutes automated
- Reports delivered per run: [number of active clients]
- Delivery time: every Monday at 7am without fail
- Months this can run without human involvement: indefinitely

## Tools used
- n8n Cloud (workflow automation + scheduling)
- Claude API — claude-sonnet-4-5 (narrative report writing)
- Google Sheets (client metrics data source)
- Google Docs (report document creation)
- Gmail (client email delivery)
- Airtable (client list + reports audit log)

## How it works
1. Schedule trigger fires every Monday at 7am automatically
2. Airtable returns list of all active clients
3. Loop processes one client at a time
4. Google Sheets returns this week and last week metrics
5. Claude analyses both periods and writes a 5-section narrative report:
   Executive Summary, Highlights, Areas of Focus,
   Trend Analysis, Next Week Recommendations
6. Google Doc created with full report content
7.Gmail gets new Doc and emails it to the client
8. Airtable logs the sent report with date and Doc link

<img width="1339" height="617" alt="Automated_Client_Reporting System" src="https://github.com/user-attachments/assets/32f38ba8-8826-430d-afb3-55d4bf0c1904" />

