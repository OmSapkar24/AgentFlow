# AgentFlow Documentation

## Overview

AgentFlow is an automated job application system that streamlines the job search and application process.

## Project Structure

```
AgentFlow/
├── src/                  # Core application code
│   └── agentflow.py     # Main automation logic
├── dashboards/           # Streamlit dashboard
│   └── app.py           # Dashboard application
├── data/                 # Data files
│   └── sample_jobs.json # Sample job listings
├── docs/                 # Documentation
│   └── README.md        # This file
└── README.md             # Main project README
```

## API Reference

### AgentFlow Class

The main class for automated job application workflow.

#### Methods

##### `fetch_jobs(keywords: List[str], location: str = None) -> List[Dict]`

Fetch job listings from various sources.

**Parameters:**
- `keywords`: List of job search keywords
- `location`: Optional location filter

**Returns:**
- List of job dictionaries

##### `optimize_resume(job_description: str, base_resume: str) -> str`

Optimize resume for specific job description.

**Parameters:**
- `job_description`: Target job description
- `base_resume`: Base resume content

**Returns:**
- Optimized resume content

##### `auto_apply(job: Dict, resume: str, cover_letter: str = None) -> bool`

Automatically apply to a job.

**Parameters:**
- `job`: Job dictionary with application details
- `resume`: Resume content
- `cover_letter`: Optional cover letter content

**Returns:**
- True if application successful, False otherwise

## Dashboard

The Streamlit dashboard provides a visual interface for tracking application statistics.

### Running the Dashboard

```bash
streamlit run dashboards/app.py
```

### Features

- Application metrics (total, pending, interviews, rejections, offers)
- Recent applications table
- Settings configuration

## Roadmap

### Phase 1: Foundation (Current)
- [x] Project structure setup
- [x] Basic AgentFlow class skeleton
- [x] Streamlit dashboard framework
- [x] Sample data structure

### Phase 2: Core Features
- [ ] Implement job fetching from multiple sources
- [ ] Resume optimization using AI/ML
- [ ] Auto-apply functionality for supported platforms
- [ ] Database integration for tracking applications

### Phase 3: Enhanced Features
- [ ] Multi-platform support (LinkedIn, Indeed, Glassdoor, etc.)
- [ ] Cover letter generation
- [ ] Interview scheduling integration
- [ ] Email notifications
- [ ] Advanced analytics and reporting

### Phase 4: Advanced Features
- [ ] Machine learning for job matching
- [ ] Salary negotiation assistance
- [ ] Career progression tracking
- [ ] API for third-party integrations

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

TBD
