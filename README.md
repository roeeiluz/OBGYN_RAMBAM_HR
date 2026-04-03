# OBGYN HR - Rambam

A comprehensive HR management dashboard for the **Department of Obstetrics & Gynecology at Rambam Health Care Campus**.

Built as a single-page application (`index.html`) with no build step or dependencies — just open in a browser.

## Features

### Home (AI Assistant)
- Chat interface for querying resident data
- Ask about any resident by name — stage, rotation, syllabus progress, time remaining
- Pre-built suggestions for common queries (ending soon, external rotations, syllabus gaps, department summary)

### Staffing Overview
- Full staffing board: specialists, residents, vacant positions, candidates
- Department breakdown (OB, GYN, Fertility)
- Approved positions tracking with slot controls
- Doctor cards with status indicators (Kupah, leaving, staying, rotation, military service, maternity)
- Inline editing for each doctor's details and rotation plan

### Training Analysis
- **Rotation timeline** — visual bar chart of each resident's rotation history and plan
- **Status board** — current rotation/absence status for all residents
- **Stage A/B tracking** — exam status management for all residents

### Procedure Syllabus
- Per-resident progress across all required procedure categories
- Cesarean section tracking (first/repeat/total)
- Filter by completion level (complete, partial, below 50%)

### Feedback System
- **Quick feedback** — short written feedback with topic selector (clinical, surgical, teamwork, etc.)
- **Periodic feedback** — self-assessment or supervisor evaluation with star ratings across multiple categories
- **Procedure feedback** — per-procedure evaluation with independence level and performance rating

### Tools
- **Residency Plan for Scientific Council** — generates a formal DOCX document with:
  - Auto-populated resident data (name, ID, start date)
  - Gender-aware Hebrew text
  - Calculated 12-semester rotation schedule based on start date
  - Basic sciences exemption option (reduces to 11 semesters)
  - Document date set to generation day
  - Signed by department head
- **Report Generation** — summary, progress, syllabus, rotation, and vacancy reports

## Data

- Resident and specialist data is baked into the HTML with full rotation plans and procedure counts
- Optional sync with Google Sheets via Apps Script API
- Shlav (exam) data persisted in browser localStorage

## Tech Stack

- Single HTML file, zero build tools
- Vanilla JavaScript
- CSS custom properties for theming
- [docx.js](https://github.com/dolanmiri/docx) (CDN) for DOCX generation
- Google Fonts (Heebo)

## Usage

```
open index.html
```

Or serve locally:

```
python3 -m http.server 8080
```

## License

Internal use — Rambam Health Care Campus.
