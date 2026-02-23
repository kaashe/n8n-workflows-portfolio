# Medical Call Agent – AI-Powered Insurance Claim Status Inquiry

## Overview
This n8n workflow automates outbound calls for checking insurance claim status on behalf of patients. It integrates with  UltraVox AI  and  Plivo  to create calls, handle answers, track call status, and provide call summaries. The workflow is designed for medical or insurance support teams.

---

## Features
- Start calls via webhook with dynamic phone numbers and call modes.
- AI-powered voice assistant handles interactions with insurance representatives.
- Integrates with  UltraVox AI  for intelligent call automation.
- Uses  Plivo  for call connection, recording, and transcription.
- Provides call lifecycle events:
  - Call started
  - Call answered
  - Call status updates
  - Call hangup
- Returns detailed call summary including call duration, recording URL, call cost, and metadata.


## Workflow Nodes
1.  Start Call Webhook  – Receives call requests via HTTP POST.
2.  Workflow Configuration  – Sets call metadata (phone number, call mode, timestamp).
3.  Create UltraVox Call  – Initiates AI-driven call.
4.  Extract UltraVox Details  – Extracts call ID, join URL, and answer URL.
5.  Make Plivo Call  – Connects the call using Plivo API.
6.  Respond Success  – Confirms call initiation.
7.  Answer URL Webhook  – Handles call answer events from Plivo.
8.  Extract Answer Details  – Extracts answered call data.
9.  Return XML to Plivo  – Streams AI audio to Plivo.
10.  Call Hangup Webhook  – Handles call termination.
11.  Extract Hangup Data  – Extracts hangup metadata.
12.  Get Ultravox Call Data  – Fetches UltraVox messages.
13.  Merge Call Data  – Combines call data from hangup and UltraVox.
14.  Return Call Details  – Sends detailed call summary back.
15.  Call Answered Webhook  – Receives answered call notifications.
16.  Respond Call Answered  – Confirms call answered.
17.  Call Status Webhook  – Receives call status updates.
18.  Extract Status Data  – Extracts status info.
19.  Respond Status Update  – Confirms status update.


## Usage

### 1. Import Workflow
1. Open n8n.
2. Click  Import  →  Import from JSON .
3. Select `medical-call-agent.json`.

### 2. Configure Credentials
-  Plivo  – HTTP Basic Auth credentials for call handling.
-  UltraVox AI  – HTTP Basic Auth credentials for AI calls.
- Keep API keys secure and avoid committing them to GitHub.

### 3. Trigger a Call
Send a POST request to your n8n webhook:

```http
POST /start-call
Content-Type: application/json

{
  "phoneNumber": "+1234567890",
  "callMode": "human",
  "sessionId": "optional-session-id",
  "timestamp": "2026-02-23T12:00:00Z",
  "callerId": "Agent123"
}