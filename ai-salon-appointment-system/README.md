# An AI-powered conversational booking assistant built using n8n and Google Calendar integration.

## 🎯 Problem Statement
Manual appointment booking in service-based businesses results in:
Scheduling conflicts
Double bookings
Staff dependency on phone coordination
Limited booking hours
Businesses require a 24/7 automated booking assistant capable of:
Conversational interaction
Real-time availability checking
Conflict prevention
Automated confirmation


## 🚀 Solution Overview
This workflow implements a tool-augmented AI scheduling assistant that:
Interacts with users via chat
Maintains conversational memory
Checks real-time availability
Prevents overlapping bookings
Creates confirmed calendar appointments
The system leverages AI decision logic combined with Google Calendar API orchestration.



## 🏗 Workflow Architecture
1. Chat Trigger – Receives incoming booking messages
2. AI Agent – Acts as a virtual salon scheduling assistant
3. Memory Buffer – Maintains conversational state
4. Calendar Availability Tool – Fetches existing events
5. Time Slot Validation Logic – Prevents overlap
6. Appointment Creation – Books validated slot
7. User Confirmation – Returns booking details