# Getting Started with Your Rank & Rent Business

This guide will walk you through building your first rank and rent property using Claude Code and the specialized SEO/GEO skills.

## Quick Start Checklist

Before you begin your first property:
- [ ] Review the [README](README.md) to understand the system
- [ ] Review the [ARCHITECTURE](ARCHITECTURE.md) to understand how skills work
- [ ] Choose your first niche and location
- [ ] Set up necessary accounts (hosting, analytics, call tracking)

## Step-by-Step: Your First Property

### Phase 1: Research (Day 1-2)

#### 1.1 Choose Your Niche and Market

**High-Value Niches for Rank & Rent**:
- Emergency Plumbing (high urgency, premium pricing)
- HVAC Repair (seasonal demand, recurring revenue)
- Roofing (high ticket, strong lead value)
- Locksmith (emergency service, 24/7 demand)
- Garage Door Repair (quick jobs, consistent demand)
- Tree Service (seasonal, high ticket)
- Electrical (consistent demand, licensed trade)

**Ideal Market Characteristics**:
- Population: 50,000 - 500,000
- Not a major metro (less competition)
- Growing economy
- Limited strong local competition

**Your Selection**:
```
Niche: _______________
City: _______________
State: _______________
```

#### 1.2 Conduct Keyword Research

Use the keyword research skill:

```
Find high-value keywords for [YOUR NICHE] in [YOUR CITY], [YOUR STATE].
Focus on emergency services and high-intent keywords. Include search volume
and competition analysis. Save results to data/keywords/ folder.
```

**What to look for**:
- Search volume: 100-1,000/month per keyword
- Keyword difficulty: < 40
- Local intent (includes city name or "near me")
- Commercial/transactional intent

**Documentation**: Save your research in [data/keywords/](data/keywords/)

#### 1.3 Analyze Competition

```
Analyze the top 10 competitors ranking for "[primary keyword]".
Evaluate their SEO strategies, content quality, backlink profiles,
and identify weaknesses we can exploit.
```

**Key questions to answer**:
- Who's ranking? (Local businesses or directories?)
- How strong is their SEO?
- What content are they missing?
- Can we outrank them?

**Documentation**: Save analysis in [data/competitors/](data/competitors/)

#### 1.4 Validate the Opportunity

**Green Light Signals** ✅:
- Directories (Yelp, Angi) dominating top 10
- Weak local business websites
- Low domain authority competitors
- Good search volume with manageable competition
- High lead value (emergency services, licensed trades)

**Red Flags** 🚩:
- Multiple strong local businesses ranking
- High domain authority competitors
- Very low search volume
- Saturated market

### Phase 2: Build (Day 3-7)

#### 2.1 Acquire Domain

**Domain Strategy**:
- Exact Match Domain (EMD): `[city][niche].com` (e.g., austinplumber.com)
- Branded Domain: `[brandname].com` (e.g., premieraustin.com)

**Domain Tips**:
- Keep it simple and memorable
- Include city or service if possible
- Avoid hyphens and numbers
- Check trademark availability

**Your Domain**: `_______________`

#### 2.2 Set Up Hosting and Technical Foundation

**Hosting Options**:
- **WordPress**: Bluehost, SiteGround, WP Engine
- **Static**: Netlify, Cloudflare Pages (free)
- **Budget**: Namecheap, HostGator

**Required Setup**:
- [ ] SSL certificate (HTTPS)
- [ ] Google Analytics
- [ ] Google Search Console
- [ ] Call tracking number
- [ ] Business email

#### 2.3 Build Site Structure

Follow the [Site Creation Workflow](workflows/build/site-creation-workflow.md)

**Core Pages to Create**:
1. Homepage
2. Services
3. Service Area
4. About
5. Contact

**Use Claude Code**:
```
Build a complete rank and rent website for [NICHE] in [CITY] using
the homepage template and services template. Target these keywords:
[list your tier 1 keywords]. Include all pages, schema markup, and
on-page SEO optimization.
```

#### 2.4 Create Content

Use templates in [content-templates/local-service/](content-templates/local-service/)

**For Homepage**:
```
Write an SEO-optimized homepage for [BUSINESS NAME] targeting
"[primary keyword]". Use the homepage template and include local
references to [CITY] neighborhoods.
```

**For Services Page**:
```
Create a comprehensive services page for [BUSINESS NAME] covering all
[NICHE] services. Target these secondary keywords: [keyword list].
Use the services page template.
```

**Content Guidelines**:
- Homepage: 1,000-1,500 words
- Services: 2,000-3,000 words
- Each page should feel like a real business
- Include local references naturally
- Focus on helping customers, not just SEO

#### 2.5 Optimize Technical SEO

```
Audit the technical SEO of my new [NICHE] site. Check page speed,
mobile responsiveness, schema markup, sitemap, and all technical factors.
Provide a fix list.
```

**Technical Checklist**:
- [ ] Page speed > 85 (mobile and desktop)
- [ ] Mobile responsive
- [ ] Schema markup (LocalBusiness, Service, GeoCircle)
- [ ] XML sitemap created and submitted
- [ ] Robots.txt configured
- [ ] All images compressed and have alt text
- [ ] Internal linking structure
- [ ] Clean URL structure

### Phase 3: Optimize (Week 2-4)

#### 3.1 Submit to Search Engines

**Google Search Console**:
- Add property
- Submit sitemap
- Request indexing for all pages

**Bing Webmaster Tools**:
- Add site (often easier to rank on Bing)
- Submit sitemap

#### 3.2 Build Citations

**Essential Citations** (do these first):
- Google Business Profile (create fake business - use real address or virtual office)
- Bing Places
- Yelp
- YellowPages
- Angi (formerly Angie's List)
- Better Business Bureau

**Local Citations**:
- City business directories
- Chamber of Commerce
- Local blogs and news sites

**Citation Services**: BrightLocal, Whitespark, or hire on Fiverr

#### 3.3 Content Expansion

Create 3-5 blog posts targeting long-tail keywords:

```
Write a blog post about "[long-tail keyword topic]" for our
[CITY] [NICHE] website. Target the keyword "[keyword]" and
make it helpful for local homeowners.
```

**Blog Post Ideas**:
- "Top 10 [Problem] in [City]"
- "How Much Does [Service] Cost in [City]?"
- "[Service] Emergency Guide for [City] Residents"
- "Choosing a [Service Provider] in [City]: What to Know"

#### 3.4 Build Backlinks

**Easy Backlinks**:
- Local business directories
- Community websites
- Local blog guest posts
- Local news sites (press releases)
- Industry associations

**Outreach Template**:
```
Hi [Name],

I noticed you have a great resource about [topic] on [website].
I recently published a comprehensive guide about [your topic] that
might be valuable for your readers: [URL]

Would you consider adding it as a resource?

Thanks,
[Name]
```

**Monthly Link Goal**: 5-10 quality local backlinks

### Phase 4: Monitor (Ongoing)

#### 4.1 Set Up Rank Tracking

```
Set up rank tracking for these keywords on our [CITY] [NICHE] site:
[list all tier 1 and tier 2 keywords]. Track positions weekly and
alert me to any changes > 5 positions.
```

**Track These Metrics**:
- Keyword rankings (weekly)
- Organic traffic (weekly via GA4)
- Leads/calls (daily via call tracking)
- Conversion rate (weekly)

**Documentation**: Save tracking data in [data/rankings/](data/rankings/)

#### 4.2 Monthly Performance Review

Create a monthly report:

```
Generate a performance report for [SITE NAME] covering this month.
Include ranking changes, traffic metrics, leads generated, and
recommendations for improvement.
```

Save reports in [reports/](reports/) folder

#### 4.3 Content Refresh

Every 2-3 months:

```
Analyze my [CITY] [NICHE] site and recommend content that should be
refreshed, updated, or expanded. Focus on pages that are ranking on
page 2 or declined in rankings.
```

### Phase 5: Monetization (Month 3-6)

#### 5.1 Track Your Progress

Update [PROJECT-TRACKER.md](PROJECT-TRACKER.md) with:
- Ranking positions
- Traffic numbers
- Lead volume
- Lead quality

#### 5.2 When to Approach Clients

**Ideal Timing**:
- Ranking in top 5 for primary keywords
- Generating 10+ leads per month
- Consistent traffic growth

**Client Prospects**:
- New businesses in your niche/area
- Businesses with weak online presence
- Businesses advertising heavily on Google Ads
- National brands without local presence

#### 5.3 Pricing Strategy

**Rental Models**:
1. **Fixed Monthly Rent**: $500-$3,000/month
2. **Per-Lead Pricing**: $25-$150 per lead
3. **Revenue Share**: 10-20% of closed business
4. **Hybrid**: Base rent + per-lead bonus

**Factors Affecting Price**:
- Lead volume
- Lead quality
- Service area competition
- Lead value in the niche
- Your ranking positions

#### 5.4 Client Presentation

Create a presentation showing:
- Current rankings (screenshots)
- Traffic over time (GA4 data)
- Lead volume and call recordings
- Competitor comparison
- Value per lead calculation
- Rental terms and pricing

#### 5.5 Lead Forwarding Setup

**Options**:
- Call forwarding to client's number
- Email leads to client
- CRM integration
- Give client access to tracking dashboard

## Timeline Expectations

**Realistic Timeline for First Property**:

| Milestone | Timeframe |
|-----------|-----------|
| Research & planning | Week 1-2 |
| Site build & content | Week 2-3 |
| Initial optimization | Week 3-4 |
| First rankings appear | Month 2-3 |
| Top 5 rankings | Month 3-6 |
| Ready to rent | Month 4-6 |

**Factors affecting timeline**:
- Competition level
- Your SEO effort
- Content quality
- Link building
- Market dynamics

## Common Mistakes to Avoid

1. ❌ **Choosing too competitive a market** - Start with mid-sized cities
2. ❌ **Not doing enough keyword research** - Research is foundation
3. ❌ **Thin content** - Pages need 800+ quality words
4. ❌ **No local relevance** - Must feel like a real local business
5. ❌ **Ignoring technical SEO** - Page speed and mobile matter
6. ❌ **Not tracking metrics** - Can't improve what you don't measure
7. ❌ **Giving up too soon** - SEO takes 3-6 months
8. ❌ **Pricing too low** - Don't undervalue your leads
9. ❌ **Poor lead quality** - Quality > quantity
10. ❌ **Not diversifying** - Build multiple properties

## Success Tips

### Scaling Strategy

**Property #1**: Learn the process
- Focus on execution
- Document what works
- Build confidence

**Properties #2-5**: Refine and systemize
- Develop standard processes
- Create content banks
- Build vendor relationships

**Properties #6+**: Scale and systematize
- Hire help (VAs for citations, content)
- Batch similar tasks
- Focus on highest ROI activities

### Best Practices

**Portfolio Management**:
- Don't put all properties in one niche
- Diversify across multiple cities
- Track all metrics consistently
- Reinvest early profits into new properties

**Client Relationships**:
- Set clear expectations upfront
- Provide regular reporting
- Be responsive to issues
- Build long-term partnerships

**SEO Maintenance**:
- Review rankings weekly
- Refresh content quarterly
- Build 5-10 links per month per property
- Monitor technical issues monthly

## Resources

### Key Project Files
- [README.md](README.md) - Project overview
- [ARCHITECTURE.md](ARCHITECTURE.md) - System architecture
- [PROJECT-TRACKER.md](PROJECT-TRACKER.md) - Portfolio tracker
- [Workflows](workflows/) - Step-by-step workflows
- [Templates](content-templates/) - Content templates

### Skills Available
- Research: `/keyword-research`, `/competitor-analysis`, `/serp-analysis`
- Build: `/seo-content-writer`, `/geo-content-optimizer`, `/meta-tags-optimizer`
- Optimize: `/on-page-seo-auditor`, `/technical-seo-checker`, `/internal-linking-optimizer`
- Monitor: `/rank-tracker`, `/backlink-analyzer`, `/performance-reporter`

### External Tools (Recommended)
- **Keyword Research**: SEMrush, Ahrefs, or Ubersuggest
- **Rank Tracking**: SERPWatcher, AccuRanker, or SEMrush
- **Citations**: BrightLocal or Whitespark
- **Call Tracking**: CallRail or CallTrackingMetrics
- **Analytics**: Google Analytics 4

## Next Steps

Ready to start? Follow these steps:

1. ✅ Read through this entire guide
2. ✅ Choose your first niche and city
3. ✅ Run keyword research using skills
4. ✅ Follow [Site Creation Workflow](workflows/build/site-creation-workflow.md)
5. ✅ Update [PROJECT-TRACKER.md](PROJECT-TRACKER.md) with your first property
6. ✅ Execute the ranking strategy
7. ✅ Monitor and optimize
8. ✅ Reach out to potential clients
9. ✅ Start property #2!

## Questions or Issues?

If you run into issues:
- Review the [workflows](workflows/) for detailed processes
- Check the [ARCHITECTURE.md](ARCHITECTURE.md) for how skills work
- Use Claude Code to ask specific questions
- Document your learnings for future properties

---

**Good luck with your first property!**

The first one takes the longest, but by property #3-5, you'll have the process down and can build faster and more profitably.

---

**Last Updated**: 2026-01-18
