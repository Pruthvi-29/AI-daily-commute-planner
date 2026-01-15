# AI-Powered Daily Commute Planner

An AI-driven automation that plans the optimal daily commute route using
real-time weather and air quality data.

## What This Project Does

Every day at 5:00 AM, the system:

- Fetches live weather and air quality data (Meteosource API)
- Reads available routes from Google Sheets
- Selects the best route based on weather and AQI
- Creates a Google Calendar event
- Sends an email with route and conditions

## Tech Stack

- n8n (Cloud)
- Large Language Model (OpenRouter / Gemini)
- Meteosource API (Weather + AQI)
- Google Sheets API
- Google Calendar API
- Gmail API

## AI Agent Design

- Model-agnostic prompt
- Tool-based data dependency (no hallucination)
- Trigger-driven execution
- Rule-based decision logic

## Decision Logic

- Rain or thunderstorm → safer / covered route
- Poor AQI → shorter, less exposed route
- Good weather & AQI → scenic route
- No suitable route → notify user only

## Testing Strategy

- Manual Trigger for development
- Schedule Trigger for production
- Execution logs for validation

## Screenshots

See the screenshots folder for workflow, execution, email, and calendar output.

## Notes

- API keys and credentials are not included
- Workflow JSON can be imported into n8n
