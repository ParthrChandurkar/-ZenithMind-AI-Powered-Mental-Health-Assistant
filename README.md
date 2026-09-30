# ZenithMind Mental Health Assistant

ZenithMind is a web application for self-reported mood and stress tracking, guided mental-wellness activities, therapist appointment workflows, and community interaction. It includes Gemini-backed conversational features, MongoDB persistence, and optional Google Fit and Zoom integrations.

ZenithMind is an educational wellness project. It is not a diagnostic tool, medical device, crisis service, or substitute for qualified professional care.

## Features

- JWT-based user, therapist, and administrator flows
- Mood, stress, sleep, activity, nutrition, and progress tracking
- Gemini-backed chat and reflection features
- Therapist profiles, appointments, and meeting integration
- Memory, arithmetic, sequence, and word games
- Socket.IO community rooms and presence counts
- Optional Google Fit data synchronization

## Architecture

The React client communicates with an Express API. Express applies security middleware and role checks before calling route controllers and services. MongoDB stores users, wellness logs, chat sessions, appointments, tokens, and game scores. Socket.IO handles realtime rooms. Gemini, Google Fit, and Zoom are accessed through backend routes when their credentials are configured.

The repository also contains optional Python mood-prediction scripts under `server/` and `realtime/`; they are separate from the primary Node.js API.

## Tech Stack

- React, Create React App, React Router, Bootstrap, and Recharts
- Node.js, Express, Socket.IO, Helmet, and Mongoose
- MongoDB
- JWT authentication
- Google Gemini API
- Google Fit OAuth and Zoom server-to-server OAuth integrations
- Jest and React Testing Library configuration

## Getting Started

Prerequisites: Node.js 18 or newer, npm, and MongoDB. External features require their respective provider credentials.

Install frontend and backend dependencies:

```bash
npm install
cd server
npm install
cd ..
```

Copy the example environment files:

```powershell
Copy-Item .env.example .env
Copy-Item server\.env.example server\.env
```

The frontend requires API and Socket.IO base URLs. The backend example documents MongoDB, JWT, CORS, Gemini, Google Fit, Zoom, and administrator configuration. Any `REACT_APP_*` value is embedded into the browser bundle, so secrets belong in the backend environment only.

Start the API from `server/`:

```bash
npm run dev
```

Start the frontend from the repository root in another terminal:

```bash
npm start
```

The frontend defaults to `http://localhost:3000`; the API defaults to `http://localhost:7000`.

## Testing

Frontend checks use the scripts defined in the root `package.json`:

```bash
npm test
```

Review `server/package.json` for the currently supported backend scripts before adding backend automation.

## Limitations and Safety

- Self-reported wellness data is subjective and incomplete.
- Generated responses may be inaccurate or inappropriate and require user judgment.
- Third-party features depend on provider availability, OAuth approval, and user consent.
- A real deployment would require a formal privacy review, secure secret management, HTTPS, monitoring, data-retention controls, and a clearly implemented crisis-response experience.

