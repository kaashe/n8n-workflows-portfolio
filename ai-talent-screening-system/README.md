# AI CV Screening & Human Approval Pipeline

## 🎯 Problem Statement
Recruitment teams spend significant time manually reviewing CVs before shortlisting candidates. This leads to delays, inconsistency in evaluation, and scalability limitations.


## 🚀 Solution Overview
This workflow automates the initial screening of CVs stored in Google Drive using AI-powered evaluation while maintaining a human approval checkpoint.

Built using n8n, this system combines document ingestion, AI analysis, structured parsing, and email-based approval gating.



## 🏗 Workflow Architecture
1. Manual Trigger
2. Google Drive PDF Search
3. Batch Processing
4. File Download
5. PDF Text Extraction
6. AI Evaluation (LangChain Agent)
7. Structured JSON Output Parsing
8. Gmail Approval Workflow