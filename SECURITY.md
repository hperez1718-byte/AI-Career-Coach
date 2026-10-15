# Security and privacy

## API keys

- Never commit a `.env` file or paste an API key into an issue, pull request, or screenshot.
- The app loads a `.env` file only from its own project folder. Copy `.env.example` to `.env` for local use.
- For a public hosted deployment, do not ask visitors to enter API keys into an untrusted deployment. Prefer local downloads with each user running the app themselves, or use a protected server-side key with appropriate authentication, rate limits, and a budget.

## Resume data

Resumes and job descriptions are sent to Google's Gemini API when users run an AI feature. Do not use student or applicant data unless you have permission and your organization's privacy policy permits it.

## Reporting a vulnerability

Please do not post security issues containing secrets or personal data publicly. Contact the repository owner privately through GitHub instead.
