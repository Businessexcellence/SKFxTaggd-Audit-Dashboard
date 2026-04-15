# SKF Recruitment Audit Dashboard

## Project Overview
- **Name**: SKF Recruitment Audit Dashboard
- **Goal**: Interactive dashboard to visualize and analyze recruitment audit quality data for SKF Automotive and SKF Industrial divisions
- **Platform**: Cloudflare Pages with Hono framework

## Features
- **Dual Account Authentication**: Separate password-protected access for SKF Auto (`Skfauto@321`) and SKF Industrial (`Skfind@123`)
- **5 Dashboard Views**: Overall, Monthly, Yearly, Recruiter Performance, Parameter View
- **Deep AI Insights**: Automated analysis displayed between filters and charts
- **Trend Analysis**: Accuracy score trends over time in Overall view
- **Cascading Multi-Select Filters**: Year, Month, Week, Recruitment Stage, Parameter, Recruiter
- **Chart.js with Data Labels**: All charts have clearly visible pre-rendered data labels
- **SKF Branded Theme**: Light theme based on SKF website colors (blue/teal)
- **Responsive Design**: Works on desktop and tablet

## Dashboard Views

### 1. Overall View
- KPI cards: Accuracy, Population, Audited, Pass Rate, Failures, Error %
- Accuracy Score Trend (line chart)
- Pass/Fail/NA Distribution (doughnut)
- Accuracy by Recruitment Stage (bar)
- Error % Trend Over Time (line)
- Detailed audit data table

### 2. Monthly View
- Monthly accuracy comparison (grouped bar)
- Monthly sample count (bar)
- Monthly error trend (line)
- Monthly breakdown table

### 3. Yearly View
- Yearly accuracy by stage (grouped bar)
- Yearly pass/fail distribution (pie)
- Population vs sample comparison (bar)
- Yearly summary table

### 4. Recruiter Performance
- Recruiter average audit score (bar)
- Recruiter score by parameter (radar)
- Recruiter monthly trend (multi-line)
- Recruiter detail table

### 5. Parameter View
- Parameter-wise accuracy (horizontal bar, color-coded)
- Parameter error % comparison (bar)
- Parameter pass rate (doughnut)
- Parameter detail table

## Data Architecture
- **Source**: Two Excel files (SKF Auto, SKF Industrial)
- **Sheets**: Audit Count (main metrics) + Recruiter Performance
- **Storage**: Data embedded in TypeScript module (no database needed)
- **API Endpoints**:
  - `POST /api/auth` - Authentication
  - `GET /api/data/audit?account=auto|industrial` - Audit data
  - `GET /api/data/recruiter?account=auto|industrial` - Recruiter data

## Tech Stack
- **Backend**: Hono framework on Cloudflare Workers
- **Frontend**: Vanilla JS + Tailwind CSS (CDN) + Chart.js + chartjs-plugin-datalabels
- **Icons**: Font Awesome 6
- **Font**: Inter (Google Fonts)

## URLs
- **Sandbox**: https://3000-{sandbox-id}.sandbox.novita.ai
- **Production**: Deploy to Cloudflare Pages

## Deployment
- **Platform**: Cloudflare Pages
- **Build**: `npm run build` (Vite SSR build)
- **Deploy**: `npm run deploy`
- **Status**: Active (Development)
- **Last Updated**: 2026-04-15
