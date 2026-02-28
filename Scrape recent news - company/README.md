# Calls fail before they even start—not because of bad pitching, but because of bad preparation.

## 🎯 Problem Statement
 Reps waste 10-15 minutes scrambling for context before every call
 Critical company news (funding, launches, press) gets missed
 Research is inconsistent across the team
 Briefings are manual, if they exist at all
 High-value meetings happen with zero preparation

 
## 🚀 Solution Overview
This workflow transforms calendar events into comprehensive pre-call briefings—automatically, every morning at 7AM.

What it does:
Scans today's calendar for customer meetings
Identifies calls/meetings with external companies
Extracts company names from event titles
Fetches latest news (funding, products, press)
elivers structured HTML briefings via email

Outcome: Every rep walks into every call fully informed—without lifting a finger.

## 🏗 Workflow Architecture
⏰ Schedule Trigger (7AM Daily)
       ↓
📅 Google Calendar (Fetch Today's Events)
       ↓
🔍 Filter Meetings (Identify "Call with" / "Meeting with")
       ↓
   ╭───────┴───────╮
   ↓               ↓
🏢 Extract      💤 No Meetings
   Company         (End)
   Name
       ↓
📰 NewsAPI (Fetch Latest News)
       ↓
📧 Format HTML Email
       ↓
✉️ Gmail (Send Briefing)