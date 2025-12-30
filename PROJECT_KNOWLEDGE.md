# Graham County DSA Research - Knowledge Base Document

## Quick Reference

| Property | Value |
|----------|-------|
| **Repository** | https://github.com/Mnehmos/mnehmos.dsa-graham.research |
| **Primary Language** | HTML/CSS/Markdown |
| **Project Type** | Research / Website |
| **Status** | Active |
| **Last Updated** | 2025-12-29 |

## Overview

This project contains research and data analysis for Democratic Socialists of America (DSA) chapter formation in Graham County, Arizona (Legislative District 19). It provides evidence-based organizing strategy documentation for rural Arizona labor organizing, economic justice campaigns, and working-class political mobilization in a historically conservative mining region with high poverty rates and declining union membership.

## Architecture

### System Design

This is a static research repository with two primary components:
- A comprehensive research documentation system (Markdown files) containing demographic, economic, and labor statistics
- A static HTML website for public-facing chapter presence and organizing outreach
- No backend services or APIs - purely static content delivery

### Key Components

| Component | Purpose | Location |
|-----------|---------|----------|
| Main Website | Public-facing DSA chapter website with organizing information | `index.html` |
| Research Database | Comprehensive demographic, economic, and labor statistics for LD19 | `website resources/data/research-sources.md` |
| README | Project overview and key statistics summary | `README.md` |
| Website Resources | Supporting data and content for the static website | `website resources/` |

### Data Flow

```
Research Sources → Markdown Documentation → Strategic Planning
                ↓
Static Website → Public Outreach → Community Organizing
```

## API Surface

### Public Interfaces

This project does not expose programmatic APIs. It provides two primary interfaces:

#### Interface: Static Website
- **Purpose**: Public-facing website for Graham County DSA chapter presence
- **Access Method**: Direct file access to `index.html`
- **Features**:
  - Navigation menu with sections for About, Issues, Get Involved, Events, Resources
  - Responsive design with mobile-friendly layout
  - DSA branding (red #EC1F27, dark #1a1a1a color scheme)
  - Arizona-specific design elements (copper and sand color accents)
  - Call-to-action buttons for joining and contacting
- **Deployment**: Can be hosted on any static web server or GitHub Pages

#### Interface: Research Documentation
- **Purpose**: Evidence-based organizing strategy data
- **Access Method**: Direct file reading of Markdown documents
- **Data Categories**:
  - Legislative District 19 political coverage (230,476 residents, 146,048 voters)
  - Graham County demographics (38,860 population, 17.7% poverty rate)
  - Economic statistics (median income $67,326, 90% of state median)
  - Labor history (1983-1986 mine strike, union decline to 3.7%)
  - Housing data (73.77% owner-occupied, median value $179,600)
  - Employment sectors (68.46% white-collar, 31.54% blue-collar)

### Configuration

This project has no runtime configuration. All data is static content.

| Variable | Type | Default | Description |
|----------|------|---------|-------------|
| N/A | N/A | N/A | No configuration variables - static content only |

## Usage Examples

### Basic Usage

```html
<!-- Deploying the static website -->
<!-- Simply serve the index.html file from any web server -->
<!-- Example with Python's built-in server: -->
<!-- python -m http.server 8000 -->
<!-- Then navigate to http://localhost:8000/index.html -->

<!-- Key navigation structure from index.html: -->
<nav>
    <div class="nav-container">
        <a href="#" class="nav-logo">
            <span>✊</span>
            Graham County DSA
        </a>
        <ul class="nav-menu">
            <li><a href="#about">About</a></li>
            <li><a href="#issues">Issues</a></li>
            <li><a href="#join">Get Involved</a></li>
            <li><a href="#events">Events</a></li>
            <li><a href="#resources">Resources</a></li>
            <li><a href="#contact" class="nav-cta">Join DSA</a></li>
        </ul>
    </div>
</nav>
```

### Advanced Patterns

```markdown
<!-- Extracting key statistics from research-sources.md -->
<!-- This data can be used for campaign materials, presentations, etc. -->

Key Organizing Statistics for Graham County:

Population: 38,860 (2023)
Poverty Rate: 17.7% (1.4x state average)
Median Income: $67,326 (90% of state median)
Union Membership: 3.7% in Arizona (historic low)
Political Lean: R+20-30 district

Strategic Focus Areas:
1. Economic Populism - High poverty despite copper industry wealth
2. Labor Revival - Rebuild organizing after 1983-1986 strike destruction
3. Just Transition - Worker-centered climate policy for mining communities
4. Healthcare Access - Rural healthcare deserts, Medicare for All advocacy
5. Housing Justice - Company town tenant organizing in Morenci

Major Employer: Freeport-McMoRan (3,300+ workers across Morenci and Safford mines)
Labor History: 1983-1986 Arizona Mine Strike led to union decertification
```

## Dependencies

### Runtime Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| N/A | N/A | No runtime dependencies - static HTML/CSS/Markdown |

### Development Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| Git | Any | Version control for documentation and website updates |
| Web Browser | Modern (Chrome, Firefox, Safari, Edge) | Testing and viewing static website |
| Text Editor | Any | Editing Markdown and HTML content |

## Integration Points

### Works With

Standalone project - no direct Mnehmos integrations

This research repository serves as foundational data for organizing work but does not integrate with other technical projects in the Mnehmos ecosystem.

### External Services

| Service | Purpose | Required |
|---------|---------|----------|
| GitHub Pages (potential) | Static website hosting | No |
| Web Server (any) | Serving index.html publicly | No |

## Development Guide

### Prerequisites

- Git for version control
- Modern web browser for testing
- Text editor for Markdown and HTML editing
- Optional: Local web server (Python, Node.js http-server, etc.) for local testing

### Setup

```bash
# Clone the repository
git clone https://github.com/Mnehmos/mnehmos.dsa-graham.research
cd mnehmos.dsa-graham.research

# No installation steps required - static content only

# Optional: Start a local web server for testing
python -m http.server 8000
# Or using Node.js:
# npx http-server -p 8000
```

### Running Locally

```bash
# Serve the website locally
python -m http.server 8000

# Navigate to http://localhost:8000/index.html in your browser

# View research documentation
# Open README.md or website resources/data/research-sources.md in any Markdown viewer
```

### Testing

```bash
# Manual testing checklist:
# 1. Open index.html in multiple browsers (Chrome, Firefox, Safari, Edge)
# 2. Test responsive design on mobile viewport sizes
# 3. Verify all navigation links work correctly
# 4. Check color contrast for accessibility
# 5. Validate HTML structure

# No automated tests - static content project
```

### Building

```bash
# No build process required - static HTML/CSS
# Files are deployment-ready as-is

# To deploy to GitHub Pages:
# 1. Enable GitHub Pages in repository settings
# 2. Set source to main branch / root directory
# 3. GitHub will automatically serve index.html

# To deploy to any web server:
# Simply upload all files to the web server directory
```

## Maintenance Notes

### Known Issues

1. No automated data updates - Research sources must be manually updated with new census/labor statistics
2. Website has no content management system - All updates require direct HTML editing
3. No analytics tracking - Cannot measure website traffic or engagement without adding JavaScript
4. Static data from 2023-2024 - Will become outdated and require periodic refresh

### Future Considerations

1. Add Google Analytics or privacy-respecting analytics (Plausible, Umami) to track organizing outreach
2. Create a simple CMS or markdown-to-HTML pipeline for easier content updates
3. Establish quarterly research update schedule to refresh economic and labor statistics
4. Add event calendar integration for organizing events and meetings
5. Consider migrating to a static site generator (Hugo, Jekyll, Eleventy) for better maintainability
6. Add structured data markup (JSON-LD) for better search engine visibility

### Code Quality

| Metric | Status |
|--------|--------|
| Tests | None - static content project |
| Linting | None - hand-written HTML/CSS |
| Type Safety | None - no JavaScript/TypeScript code |
| Documentation | README only - no code documentation needed |

---

## Appendix: File Structure

```
mnehmos.dsa-graham.research/
├── website resources/
│   └── data/
│       └── research-sources.md   # Comprehensive research database (16KB)
├── .git/                         # Git version control
├── .gitattributes                # Git configuration
├── index.html                    # Main website (69KB) - DSA chapter homepage
├── README.md                     # Project overview and key statistics
└── PROJECT_KNOWLEDGE.md          # This document
```

---

*Generated by Project Review Orchestrator | 2025-12-29*
*Source: https://github.com/Mnehmos/mnehmos.dsa-graham.research*
