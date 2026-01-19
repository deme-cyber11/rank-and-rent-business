# Keyword Research Workflow

## Objective
Identify high-value, low-competition keywords for rank and rent opportunities in local service niches.

## Prerequisites
- Target niche selected (plumbing, roofing, HVAC, locksmith, etc.)
- Target geographic location(s)
- Basic understanding of service area

## Step-by-Step Process

### 1. Define Research Parameters

**Input Required**:
```
Service Type: [e.g., "emergency plumber"]
City: [e.g., "Austin"]
State: [e.g., "TX"]
Radius: [e.g., "30 miles"]
```

**Claude Prompt**:
```
Research keywords for {SERVICE_TYPE} in {CITY}, {STATE}. Focus on high-intent,
local service keywords with commercial intent. Include:
- Primary service keywords
- Emergency/urgent variations
- Neighborhood-specific terms
- Service-specific long-tail keywords
```

### 2. Gather Seed Keywords

**Primary Keywords**:
- `{city} {service}` (e.g., "austin plumber")
- `{service} {city}` (e.g., "plumber austin")
- `{service} near me`
- `emergency {service} {city}`

**Long-tail Variations**:
- `24 hour {service} {city}`
- `best {service} in {city}`
- `affordable {service} {city}`
- `{service} {neighborhood}`

### 3. Analyze Competition & Opportunity

**Metrics to Track**:
- Search volume (monthly searches)
- Keyword difficulty (0-100 scale)
- Current ranking sites
- Local pack presence
- Ad competition level

**Ideal Rank & Rent Keywords**:
- Search volume: 100-1,000/month
- Keyword difficulty: < 40
- High commercial intent
- Local results dominated by directories (not strong local businesses)

### 4. Categorize Keywords

**By Intent**:
- **Transactional** (ready to buy): "emergency plumber austin", "hire plumber austin"
- **Commercial** (comparing options): "best plumber austin", "plumber austin reviews"
- **Informational** (research): "how much does plumber cost austin"

**By Priority**:
- **Tier 1** (Primary targets): High volume + low competition + high intent
- **Tier 2** (Secondary): Medium volume + medium competition + high intent
- **Tier 3** (Long-tail): Low volume + low competition + specific intent

### 5. Document Research

**Output Format**:
Save to: `data/keywords/{niche}-{city}-keywords.json`

```json
{
  "research_date": "2026-01-18",
  "niche": "plumbing",
  "location": {
    "city": "Austin",
    "state": "TX"
  },
  "keywords": [
    {
      "keyword": "emergency plumber austin",
      "search_volume": 480,
      "difficulty": 32,
      "intent": "transactional",
      "tier": 1,
      "notes": "High urgency, premium pricing"
    }
  ],
  "opportunities": [
    "austin plumber near me - weak directory competition",
    "24 hour plumber austin tx - only 2 strong local competitors"
  ],
  "recommendations": "Focus on emergency keywords first. Build content around neighborhoods: Westlake, Downtown, North Austin"
}
```

## Claude Skill Command

```
Find high-value keywords for {service} in {city}, {state}.
Analyze search volume, competition, and local intent.
Save results to data/keywords/ folder.
```

## Success Metrics

- ✓ 20+ relevant keywords identified
- ✓ At least 5 Tier 1 opportunities found
- ✓ Competition analysis completed
- ✓ Keywords categorized by intent and priority
- ✓ Research documented in JSON format

## Next Steps

After completing keyword research:
1. Move to [Competitor Analysis Workflow](./competitor-analysis-workflow.md)
2. Validate market opportunity
3. Begin content planning based on Tier 1 keywords

## Tips for Rank & Rent

- **Prioritize emergency/urgent keywords**: Higher lead value
- **Look for directory dominance**: Easier to outrank Yelp/Angi than established local businesses
- **Check local pack**: If Google Maps has weak results, big opportunity
- **Seasonal keywords**: Some services peak seasonally (HVAC summer/winter)
- **Avoid brand keywords**: Focus on generic service terms

## Common Mistakes to Avoid

- Targeting keywords that are too competitive (difficulty > 50)
- Ignoring local intent modifiers
- Focusing only on high volume without considering commercial intent
- Not researching neighborhood-specific terms
- Overlooking mobile "near me" searches

---

**Estimated Time**: 30-60 minutes per niche/location
**Recommended Tools**: SEMrush, Ahrefs, Google Keyword Planner
**Skill Used**: `/keyword-research`
