# System Architecture

## Overview

This Rank & Rent project leverages Claude Code with specialized SEO/GEO skills to automate the creation, optimization, and management of local service websites.

## Core Components

### 1. Claude Code Skills System

The project uses Claude's skill system for specialized AI capabilities:

```
.claude/skills/
├── seo-geo-claude-skills/     # 16 SEO/GEO tools organized by phase
├── content-creator/            # Brand voice & content frameworks
├── deal-submission/            # Business deal management
└── dev-browser/                # Browser automation
```

#### Skill Architecture

Skills are organized into four phases following the SEO methodology:

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  Research → Build → Optimize → Monitor                     │
│     │         │         │          │                        │
│     ▼         ▼         ▼          ▼                        │
│   4 skills  4 skills  4 skills   4 skills                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

Each skill is self-contained with:
- `SKILL.md` - Instructions and prompts
- `references/` - On-demand reference docs
- `assets/` - Templates and resources

### 2. Data Layer

Structured data storage for all SEO research and tracking:

```
data/
├── keywords/          # Keyword research, search volumes, competition
├── competitors/       # Competitor analysis, backlink profiles
├── rankings/          # Historical ranking data, SERP positions
└── backlinks/         # Backlink opportunities, anchor text analysis
```

**Data Format**: JSON for structured data, Markdown for reports

### 3. Content Management

Template-based content system for scalability:

```
content-templates/
├── local-service/     # Service page templates (plumber, roofer, etc.)
├── seo-content/       # Blog post templates, content frameworks
└── geo-pages/         # Location-specific page templates
```

**Template Variables**:
- `{SERVICE}` - Service type (e.g., "plumbing", "roofing")
- `{CITY}` - Target city
- `{STATE}` - Target state
- `{PHONE}` - Business phone number
- `{SCHEMA}` - Generated schema markup

### 4. Site Management

Organized tracking of site portfolio:

```
sites/
├── templates/         # Base site templates (HTML, WordPress, etc.)
├── active/           # Currently ranked and rented sites
│   ├── {niche}-{city}/
│   │   ├── site-info.json
│   │   ├── content/
│   │   ├── analytics/
│   │   └── client-info.json
└── sold/             # Sold properties (archived)
```

**Site Info Schema**:
```json
{
  "site_id": "plumber-miami-001",
  "niche": "plumbing",
  "city": "Miami",
  "state": "FL",
  "domain": "miamiplumberpro.com",
  "created": "2026-01-01",
  "ranking_date": "2026-03-15",
  "target_keywords": ["emergency plumber miami", "miami plumber"],
  "monthly_rent": 1500,
  "client": "ABC Plumbing LLC",
  "status": "rented"
}
```

### 5. Workflow Automation

Phase-based workflow templates:

```
workflows/
├── research/
│   ├── keyword-research-workflow.md
│   ├── competitor-analysis-workflow.md
│   └── market-validation-workflow.md
├── build/
│   ├── site-creation-workflow.md
│   ├── content-generation-workflow.md
│   └── technical-seo-setup-workflow.md
├── optimize/
│   ├── on-page-optimization-workflow.md
│   ├── content-refresh-workflow.md
│   └── link-building-workflow.md
└── monitor/
    ├── ranking-tracking-workflow.md
    ├── lead-tracking-workflow.md
    └── client-reporting-workflow.md
```

## Technical Stack Integration

### SEO Tools
- **Keyword Research**: Integration points for SEMrush, Ahrefs APIs
- **Rank Tracking**: Automated rank checking via APIs or scraping
- **Backlink Analysis**: Monitor backlink profiles

### Development Tools
- **dev-browser skill**: Browser automation for testing and validation
- **Site builders**: WordPress, static HTML, or modern frameworks
- **Hosting**: Cloudflare Pages, Netlify, or traditional hosting

### Analytics
- **Google Analytics**: Traffic and conversion tracking
- **Call Tracking**: Track phone call leads
- **Form Submissions**: Monitor lead generation

## Workflow Execution

### Phase 1: Research (Input → Analysis)

```
User Request: "Find opportunities for locksmith in Austin TX"
      ↓
[keyword-research] → keywords.json
      ↓
[competitor-analysis] → competitors.json
      ↓
[serp-analysis] → serp-data.json
      ↓
[content-gap-analysis] → opportunities.json
      ↓
Output: Market research report + actionable insights
```

### Phase 2: Build (Research → Content)

```
Research Data (keywords.json, opportunities.json)
      ↓
[seo-content-writer] → draft-content.md
      ↓
[geo-content-optimizer] → optimized-content.md
      ↓
[meta-tags-optimizer] → meta-tags.json
      ↓
[schema-markup-generator] → schema.json
      ↓
Output: Complete site content package
```

### Phase 3: Optimize (Content → Improvements)

```
Published Site URL
      ↓
[on-page-seo-auditor] → audit-report.md
      ↓
[technical-seo-checker] → technical-issues.json
      ↓
[internal-linking-optimizer] → link-structure.json
      ↓
[content-refresher] → refresh-plan.md
      ↓
Output: Optimization action plan
```

### Phase 4: Monitor (Site → Metrics)

```
Active Sites
      ↓
[rank-tracker] → rankings.json (daily/weekly)
      ↓
[backlink-analyzer] → backlinks.json (weekly)
      ↓
[performance-reporter] → monthly-report.pdf
      ↓
[alert-manager] → notifications (real-time)
      ↓
Output: Performance dashboard + alerts
```

## Skill Invocation

Skills are invoked through natural language commands:

**Explicit invocation**:
```
"Use keyword research skill to find plumbing keywords in Miami"
```

**Implicit invocation** (skill auto-detects based on context):
```
"Find profitable keywords for emergency locksmith in Austin"
```

Claude Code automatically:
1. Detects the appropriate skill based on task description
2. Loads relevant skill instructions
3. Executes the workflow
4. Returns structured output

## Data Flow

```
┌──────────────┐
│  User Input  │
└──────┬───────┘
       │
       ▼
┌──────────────────┐
│  Claude Code     │
│  + Skills        │
└──────┬───────────┘
       │
       ├──→ [Research Skills] → data/keywords/, data/competitors/
       │
       ├──→ [Build Skills] → content-templates/, sites/
       │
       ├──→ [Optimize Skills] → sites/active/
       │
       └──→ [Monitor Skills] → data/rankings/, reports/

```

## Scalability

The architecture supports scaling in multiple dimensions:

1. **Vertical**: Add more skills to each phase
2. **Horizontal**: Manage multiple sites in parallel
3. **Automation**: Workflow templates for repeatable processes
4. **Integration**: Connect external tools via APIs

## Security & Privacy

- No credentials stored in project (use environment variables)
- API keys managed through secure config
- Client data stored locally, encrypted if needed
- Separate folders for active vs. sold properties

## Extension Points

The architecture is designed for easy extension:

1. **Custom Skills**: Add new skills to `.claude/skills/`
2. **Templates**: Add new content templates to `content-templates/`
3. **Workflows**: Create custom workflows in `workflows/`
4. **Integrations**: Connect external tools via MCP (Model Context Protocol)

## Performance Considerations

- Skills load on-demand (lazy loading)
- Reference docs loaded only when needed
- Structured data in JSON for fast parsing
- Markdown for human-readable reports

---

**Architecture Version**: 1.0
**Last Updated**: 2026-01-18
