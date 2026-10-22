# Smart Campus Helpdesk – Multi-Agent AI Assistant

**Live Demo:** https://smart-campus-liev.hatchable.site?utm_source=chatgpt.com

## About the Project

Smart Campus Helpdesk is an AI-powered campus chatbot that helps students and faculty find information about college regulations, attendance, academic credits, examinations, hostel fees, and administrative procedures.

The application uses Google Gemini and Retrieval-Augmented Generation (RAG) to answer questions using available college documents.

## Features

- Student-friendly chatbot interface.
- College email login restricted to `@bitsathy.ac.in`.
- Student and Faculty role selection.
- Four specialized AI agents and one Coordinator Agent.
- Document-based question answering.
- Visual responses, including tables, bar charts, flowcharts, and timelines.
- Conversation history for follow-up questions.
- Error handling for missing information and API quota limits.

## Multi-Agent Architecture

### 1. Attendance Agent
Handles attendance requirements, examination eligibility, and condonation rules.

### 2. Academic Agent
Answers questions about curriculum, credit requirements, and degree completion.

### 3. Examination Agent
Provides examination schedules, eligibility information, arrear rules, and reappearance procedures based on available documents.

### 4. Administration Agent
Handles hostel fee information, administrative procedures, and document-submission guidance.

## Knowledge Base

The project is configured to use the following uploaded documents:

1. B.E./B.Tech. Regulations 2022 PDF.
2. Periodical Test II timetable.
3. Hostel fee notice.
4. Student database spreadsheet containing 30 sample records.

Important: The student spreadsheet contains demo data and must not be treated as the official college student database.

## Technology Stack

- AI model: Google Gemini
- Embeddings: Google embedding model
- Retrieval: Retrieval-Augmented Generation (RAG)
- Database: PostgreSQL, as configured in the project
- Frontend and hosting: Hatchable
- Knowledge sources: PDF, spreadsheet, and college documents

## Visual Answers

The chatbot can present information using:

- Tables for examination schedules and fee breakdowns.
- Bar charts for numerical comparisons.
- Flowcharts for eligibility and administrative procedures.
- Timelines for examination schedules.
- Step-by-step visual explanations.

All college-specific facts should be grounded in retrieved documents. If the required information is unavailable, the chatbot should say so rather than inventing an answer.

## How to Run the Demo

Open the deployed application:

**https://smart-campus-liev.hatchable.site?utm_source=chatgpt.com**

Sign in using an email address ending in `@bitsathy.ac.in`, select Student or Faculty, and ask a campus-related question.

## API Key Configuration

The application uses Google Gemini. Configure the API key through Hatchable's secure environment variables or secrets settings.

Required environment variable:

```env
GOOGLE_API_KEY=your_google_api_key_here
```

Never commit your real API key to GitHub or expose it in frontend code.

Get or manage your API key at [Google AI Studio](https://aistudio.google.com/app/apikey).

## Example Questions

- What is the minimum attendance percentage?
- What are the credit requirements for an ECE student?
- Show the Periodical Test II timetable as a table.
- What is the hostel fee mentioned in the uploaded notice?
- Explain the above in short.
- Show the attendance eligibility procedure as a flowchart.

Verify important answers against the relevant official source documents.

## Testing Checklist

- [ ] College email-domain validation works.
- [ ] Student and Faculty role selection works.
- [ ] Attendance answers match the regulations PDF.
- [ ] ECE credit answers are supported by the relevant curriculum section.
- [ ] Examination dates match the uploaded timetable.
- [ ] Hostel fee answers match the uploaded notice.
- [ ] Demo student records are identified as sample data.
- [ ] Follow-up questions use conversation history.
- [ ] Tables, charts, and flowcharts render correctly.
- [ ] Missing information produces a clear response.
- [ ] API quota errors are handled without fabricating answers.

## Security and Limitations

- Email-domain validation alone does not verify ownership of a mailbox.
- Do not upload real student personal information without authorization.
- Examination schedules and fee notices can become outdated.
- Document retrieval may miss relevant passages, so important answers should be checked against the source.
- AI-generated responses are not guaranteed to be correct.

## Project Status

The application is deployed on Hatchable. Verify the live application, document indexing, and answers before relying on it for official college information.
