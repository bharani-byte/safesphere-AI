# SafeSphere AI

SafeSphere AI is an AWS-ready public safety intelligence demo for hackathons. It combines live-style incident reports, community risk signals, and an AI triage layer to help teams detect urgent events, prioritize response, and create action plans.

## What It Does

- Scores public safety incidents by urgency, confidence, and impact.
- Converts raw reports into response playbooks.
- Shows a command dashboard for city, campus, venue, or enterprise safety teams.
- Includes an AWS architecture that can be deployed with serverless services.

## Demo

Open `web/index.html` in a browser. No build step is required.

## Hackathon Pitch

**Problem:** Safety teams receive fragmented reports from calls, sensors, social updates, cameras, and staff messages. Important incidents can be delayed or mis-prioritized.

**Solution:** SafeSphere AI centralizes signals, scores risk, summarizes the situation, and recommends immediate response actions.

**AWS Fit:**

- Amazon API Gateway receives incident reports.
- AWS Lambda runs triage and enrichment.
- Amazon Bedrock powers natural-language summaries and response recommendations.
- Amazon DynamoDB stores incidents and risk history.
- Amazon SNS sends alerts to responders.
- Amazon Location Service maps hotspots and zones.
- Amazon QuickSight can provide executive reporting.

## Repository Structure

```text
safesphere-ai/
  web/
    index.html
    styles.css
    app.js
  lambda/
    triage.js
  docs/
    aws-architecture.md
    pitch.md
```

## Local Usage

1. Open `web/index.html`.
2. Select a sample incident.
3. Adjust incoming report details.
4. Click `Run AI Triage`.

## Deploy Idea

For a production AWS version:

1. Host `web/` on Amazon S3 with CloudFront.
2. Create an API Gateway endpoint for incident submissions.
3. Deploy `lambda/triage.js` as a Node.js Lambda function.
4. Store results in DynamoDB.
5. Replace the mock summarizer with Amazon Bedrock.

## Judging Highlights

- Clear social impact.
- Strong AWS serverless alignment.
- Working interactive demo.
- Explainable risk scoring.
- Easy path from prototype to production.
