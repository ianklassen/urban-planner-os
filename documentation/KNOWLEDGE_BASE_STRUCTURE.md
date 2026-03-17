# Urban Planner OS: Knowledge Base Structure & Templates

The knowledge base is the "brain" of your planning OS. It's where all relevant planning information lives in organized, accessible form.

Good knowledge base = agents can reason comprehensively; analysis is grounded in reality; decisions are consistent and well-informed.

---

## Knowledge Base Organization

```
planning-knowledge/
│
├── regulations/
│   ├── zoning_ordinance_summary.md          [Key chapters, simplified]
│   ├── zoning_districts.md                  [Each district with uses, FAR, height, setbacks]
│   ├── design_guidelines/
│   │   ├── downtown_design_guidelines.md
│   │   ├── neighborhood_character_guidelines.md
│   │   └── sustainable_development_standards.md
│   ├── development_standards.md             [Parking, loading, utilities, safety]
│   ├── affordable_housing_policy.md         [Inclusionary zoning, requirements]
│   └── land_use_policies.md                 [Development patterns, growth strategy]
│
├── comp_plan/
│   ├── vision_statement.md                  [Our long-term vision]
│   ├── goals_and_policies.md                [Goals + supporting policies]
│   ├── equity_framework.md                  [How we define and measure equity]
│   ├── sustainability_targets.md            [Climate, environment goals]
│   ├── housing_strategy.md                  [Housing supply, affordability targets]
│   └── transportation_vision.md             [Transit, walkability, parking approach]
│
├── demographics/
│   ├── citywide_profile.md                  [Overall population snapshot]
│   ├── neighborhood_profiles/
│   │   ├── downtown.md                      [Neighborhoods or districts]
│   │   ├── inner_east.md
│   │   ├── outer_neighborhoods.md
│   │   └── [more neighborhoods]
│   ├── population_trends.md                 [Migration, growth, aging, changes]
│   ├── housing_market_data.md               [Rents, prices, supply, trends]
│   ├── employment_data.md                   [Jobs by sector, wages, growth]
│   ├── equity_indicators.md                 [Access to opportunity by neighborhood]
│   └── census_summary.md                    [Latest census data snapshot]
│
├── projects/
│   ├── active_projects.md                   [Projects in development review]
│   ├── approved_projects/
│   │   ├── 2024_approvals.md
│   │   ├── 2023_approvals.md
│   │   └── [historical by year]
│   ├── project_precedents/
│   │   ├── local_successful_projects.md     [Projects that worked well]
│   │   ├── comparable_cities/
│   │   │   ├── denver_mixed_use.md
│   │   │   ├── austin_affordability.md
│   │   │   └── [other precedent cities]
│   │   └── design_precedents.md             [Design examples to emulate]
│   ├── lessons_learned.md                   [What we've learned from past projects]
│   ├── pipeline.md                          [Proposed projects in discussion]
│   └── under_construction.md                [Current construction projects]
│
├── decisions/
│   ├── decision_log.md                      [Log of major decisions with rationale]
│   ├── approval_trends.md                   [What we're approving; are we consistent?]
│   ├── equity_decision_audit.md             [How decisions tracked against equity]
│   ├── comp_plan_implementation.md          [Are we implementing comp plan?]
│   └── policy_changes.md                    [Policy amendments and rationale]
│
├── stakeholders/
│   ├── community_organizations.md           [Neighborhood groups, advocates]
│   ├── key_contacts.md                      [Contacts across constituencies]
│   ├── engagement_history.md                [What we've heard; where sentiments are]
│   └── development_community.md             [Developers, builders, key players]
│
└── best_practices/
    ├── comparable_cities_policies/          [How other jurisdictions handle issues]
    │   ├── affordability_strategies.md
    │   ├── transit_oriented_dev.md
    │   ├── equity_frameworks.md
    │   └── [other policy topics]
    ├── design_standards_library.md          [Examples of good design]
    ├── policy_models.md                     [Policy language from other cities]
    ├── tools_and_methods.md                 [Planning tools (equity mapping, etc.)]
    └── research_and_data_sources.md         [Where to find planning data]
```

---

## Content Template Examples

### 1. ZONING DISTRICT SUMMARY

**File**: `regulations/zoning_districts.md`

```markdown
# Zoning Districts

## R-1: Single Family Residential

**Permitted uses**: Single-family dwellings, accessory dwelling units (max 60% of primary unit square footage)

**Conditional uses**: Home occupations (if minimal impact), child care, small farms

**Density limits**:
- FAR: 0.5
- Lot size minimum: 6,000 sq ft
- Setbacks: Front 20', Side 5', Rear 20%

**Height limit**: 35 feet, 2.5 stories

**Parking requirement**: 1 space/unit

**Design standards**: Pitched roof required, front porch preferred, materials similar to neighborhood character

**Key notes**:
- Most single-family zoning; very restricted
- Design guidelines emphasize neighborhood character preservation
- Setbacks make higher density infill difficult
- Accessory dwelling units are allowed way to add housing without rezoning

---

## R-4: Mixed Residential

**Permitted uses**: Single-family, duplexes, townhomes, apartments, mixed-use with residential

**Density limits**:
- FAR: 3.0
- Lot size minimum: 5,000 sq ft for first unit, 1,000 sq ft for each additional
- Setbacks: Front 15', Side 0-5', Rear 15%
- Height limit: 8 stories

**Parking requirement**: 0.75 spaces/unit for apartments

**Ground floor retail**: If on transit corridor, 40% ground floor retail/office required

**Design standards**: Street wall, pedestrian-oriented ground floor, active uses

**Key notes**:
- Allows significant density; enables mixed-use development
- Suited for transit corridors, main streets, infill
- Parking reduced because transit/walkability reduces car dependency
- If you want higher density, R-4 is zone of choice

---

## D-1: Downtown Mixed-Use

**Permitted uses**: Residential, office, retail, restaurants, hotels, cultural, civic

**Density limits**:
- FAR: 4.0 (can go to 5.0 with planning bonus for affordability or public benefit)
- No parking minimums (historic downtown shouldn't be parking lots)
- Height limit: 12 stories (can request variance for special buildings)

**Ground floor retail**: 70% transparency required; active, pedestrian-oriented uses required (no blank walls)

**Parking**: Underground or structured; if proposed at street level, requires special review

**Design standards**: Historic character compatibility, pedestrian activation, public realm contribution

**Key notes**:
- Highest density downtown; no height limit really means "tall buildings OK if designed well"
- No parking requirements = enables car-free development
- Active ground floor = vibrant streets
- Designed for walkable urban district
```

---

### 2. NEIGHBORHOOD PROFILE TEMPLATE

**File**: `demographics/neighborhood_profiles/downtown.md`

```markdown
# Demographic Profile: Downtown

**Area**: 150 blocks between [boundaries]
**Land use**: Mixed residential, office, retail, civic

## Current Population (2024)

**Total population**: 12,500
**Population density**: 85 people/acre (citywide avg: 45 people/acre)

**Age distribution**:
- 0-17: 1,200 (9.6%)
- 18-34: 4,500 (36%) ← Much younger than city average (28%)
- 35-64: 5,200 (41%)
- 65+: 600 (4.8%)

Downtown skews young; few families with kids; very few seniors

**Income distribution**:
- <30% AMI: 800 households (15%)
- 30-60% AMI: 1,200 households (22%)
- 60-100% AMI: 1,800 households (33%)
- >100% AMI: 2,400 households (44%)

Median household income: $75,000 (city median: $65,000)
Income inequality: Gini coefficient 0.42 (higher = more unequal; city avg: 0.38)

Downtown is wealthier than city overall; also has pockets of poverty (limited affordable housing)

**Race/ethnicity**:
- White: 65%
- Hispanic/Latino: 18%
- Black/African American: 10%
- Asian: 6%
- Other/multiracial: 1%

Downtown less diverse than city as a whole (city: 52% White, 25% Hispanic, 12% Black, 10% Asian)

**Housing**:
- Owner-occupied: 22%
- Renter-occupied: 78%

Downtown is renter-dominated; very expensive market-rate; limited affordable

Avg rent (1br): $2,200/month (city avg: $1,800)
Avg home value (if owned): $650,000 (city avg: $550,000)

Rent/income burden: 38% of renters spend >30% of income on rent (unaffordable)

**Employment**:
- Unemployment rate: 3.2% (city avg: 4.1%) [Downtown has jobs]
- Median wage (downtown jobs): $55,000
- Job growth (past 5 years): +3.2%/year (strongest sectors: tech, services, professional)

**Transportation**:
- Car ownership: 0.6 cars/household (city avg: 1.2)
- Transit commute: 42% (city avg: 15%)
- Bike commute: 8% (city avg: 4%)

Downtown is transit-rich; car-dependent less common; walkable/bikeable

## Trends (past 10 years)

**Population**:
- 2014: 8,200 → 2024: 12,500
- Growth: +52% (city growth: +12%)
- Downtown growing 4x faster than city

**Housing affordability**:
- 2014: 35% of renters spending >30% on rent
- 2024: 38% of renters spending >30% on rent
- Affordability DECLINING; rents rising faster than income

**Income trend**:
- High-earners in-migrating
- Low-income residents: Displacement risk from gentrification
- Income inequality increasing

**Who's moving in**:
- Young professionals (age 25-40)
- High-income households
- Mostly white/higher-income; diversity not keeping pace with city

**Racial equity**:
- Downtown becoming less diverse as high-income, high-education, mostly white population influxes
- Black and brown residents experiencing displacement pressure

## Opportunity Analysis

**Opportunity Strengths**:
- Jobs: High job density; career opportunity; median wage $55K
- Transit: Excellent transit access; 42% transit commute
- Amenities: Walkable district; retail, restaurants, culture, parks, schools

**Opportunity Gaps**:
- Affordable housing: Only 15% of housing at <30% AMI; gap for lower-income residents
- Wealth building: High rents limit ability to save; ownership limited by prices
- Gentrification risk: Rapid change; displacement pressure on current residents
- Educational opportunity: Limited K-12 in downtown; families leaving

## Equity Assessment

**Who has strong opportunity in downtown?**
- High-income professionals: Yes. Good jobs, walkability, lifestyle
- Middle-income workers: Moderate. Some jobs available; housing expensive
- Lower-income residents: Limited. Few affordable units; rents rising; displacement risk

**Equity index**: [On scale of 1-10] 4/10
- Strong for high-income
- Weak for lower-income
- Gentrification concentrated opportunity upward

## Planning Implications

**Issues**:
- Affordability crisis: Market-rate development not serving lower-income residents
- Displacement risk: Current residents (especially communities of color) at risk
- Diversity declining: Opportunity concentrating for high-income, mostly white residents
- Families underserved: Few housing options for families; few schools

**Opportunities**:
- Growth momentum: Demand for downtown living is strong; opportunity to build affordability
- Transit-rich: Can support denser, less car-dependent development
- Already walkable: Can add housing at scale without sprawl

**Recommended planning actions**:
- Increase affordable housing requirement (inclusionary zoning mandates 25%+ affordability)
- Offer incentives for deeper affordability (subsidies for <30% AMI)
- Preserve existing affordable stock (rent stabilization)
- Community benefits (require contributions to community stabilization)
- Workforce development (connect lower-income residents to downtown jobs)
- Schools: Revitalize/build schools so families can stay/move to downtown
```

---

### 3. COMP PLAN GOAL SUMMARY

**File**: `comp_plan/goals_and_policies.md`

```markdown
# Comprehensive Plan: Goals & Policies

## HOUSING GOAL
"Provide sufficient, diverse, and affordable housing to serve all residents across the income spectrum"

**Specific targets**:
- 40% of new housing at/below 100% AMI by 2035
- 20% of new housing at/below 60% AMI by 2035
- Preserve 5,000 existing affordable units (no net loss)
- Add 2,000 new affordable units by 2035

**Supporting policies**:
- Inclusive zoning: All projects 5+ units must include 15% affordable at 80% AMI minimum
- Zoning: Allow mixed-income development throughout (not only in low-opportunity areas)
- Preservation: Fund community land trust to preserve existing affordable stock
- Incentives: FAR bonus, height bonus, density bonus for projects exceeding affordability targets
- Public land: Use public land sales for affordable housing (not market-rate only)

**How we measure progress**:
- Track annually: % of new housing at each affordability level
- Are we on pace for 40% target?
- Are we preserving existing stock?
- What neighborhoods are getting affordability? (Ensure equitable distribution, not just poor neighborhoods)

---

## EQUITY GOAL
"Planning decisions shall reduce gaps in access to opportunity for historically marginalized communities"

**What we mean by opportunity**:
- Access to quality jobs (career pathways)
- Access to stable, affordable housing
- Access to quality education
- Access to healthy environment (parks, clean air, food)
- Access to community wealth building (ownership, entrepreneurship)
- Safety and freedom from discrimination

**Specific targets**:
- [Opportunity measure 1]: Close gap between [community A] and city average by 20% by 2035
- [Opportunity measure 2]: [Similar targets]
- Displacement: Prevent displacement of 5,000+ households through anti-displacement policies

**Supporting policies**:
- Equity assessment: All major decisions must include explicit equity analysis
- Affordability: Concentrate affordable housing in high-opportunity areas (not only in poor neighborhoods)
- Anti-displacement: Rent stabilization, community benefits, community preference policies
- Workforce development: Fund job training to connect residents to good-paying jobs
- Community voice: Meaningful engagement of marginalized communities in planning decisions
- Wealth building: Support community ownership (community land trust, cooperative housing, small business)

---

## SUSTAINABLE DEVELOPMENT GOAL
"Achieve net-zero emissions by 2035; create resilient community."

**Climate targets**:
- 50% reduction in transportation emissions (mode shift to transit/bike/walk)
- Net-zero new buildings (all new construction)
- Electrification: No new gas hookups; existing buildings transition to electric by 2035

**Land use policies**:
- Compact, walkable development (reduce sprawl, reduce driving)
- Transit-oriented density (concentrate growth near transit stations)
- Mixed-use neighborhoods (reduce commute distances)
- Complete streets (prioritize transit, bike, pedestrian over cars)

**Building/energy policies**:
- All new buildings: Net-zero ready or net-zero
- Retrofit existing buildings: Improve efficiency, electrify
- Renewable energy: Community solar, rooftop solar incentives
- Green infrastructure: Rainwater capture, permeable surfaces, urban forest

**Transportation policies**:
- Reduce parking requirements (enables denser, cheaper housing)
- Transit investment: Frequent, reliable transit network
- Bike/pedestrian infrastructure: Safe, connected network
- Electric vehicles: EV charging in all new developments
- Car-sharing: Reduce need for private vehicles

---

## COMPLETE NEIGHBORHOODS GOAL
"Every neighborhood shall have access to jobs, housing, schools, parks, and services within walkable distance"

**Walkability target**:
- 15-minute neighborhoods: Jobs, schools, parks, services, transit within 15-minute walk (1 mile)
- Neighborhood centers: Identify main street/center in each neighborhood; concentrate services

**Services**:
- Schools: Quality elementary and secondary schools accessible to all
- Parks: Public park within 10-minute walk of all residents
- Grocery: Grocery store/market within 15-minute walk
- Healthcare: Clinic or health facility within 15-minute walk
- Employment: Job opportunities within neighborhood or transit-accessible

**Policies**:
- Zoning: Allow diverse housing (apartments, townhomes, single-family in all neighborhoods)
- Mixed-use: Allow retail/office on ground floor in neighborhoods
- Small businesses: Support local retail, restaurants, services
- Park investment: New parks in underserved neighborhoods
- School investment: Quality neighborhood schools
```

---

### 4. DECISION LOG TEMPLATE

**File**: `decisions/decision_log.md`

```markdown
# Major Planning Decisions Log

## 2024 Q2 - Central Corridor Housing Project

**Decision**: Approved with conditions

**What was requested**: Rezone 3-block area from R-1 (single family) to R-4 (mixed residential).
Proposed 250 apartments, 15% market-rate affordable, 1 acre public plaza

**Planning analysis**:
- Zoning: Compliant with comp plan land use vision (transit-oriented development)
- Housing: Strong contribution to comp plan affordability goals (250 units × 15% = 37.5 affordable units)
- Affordability level: 80% AMI = workforce housing, addresses mid-level affordability gap
- Design: Context-sensitive; 8-story limit respected; street wall maintained
- Transit: Project is 0.2 miles from light rail; supports transit ridership
- Community: Mixed response. Transit advocates supportive; nearby single-family residents concerned about parking/traffic

**Equity analysis**:
- Opportunity: Adds housing in high-opportunity corridor (near jobs, transit, amenities)
- Gentrification: Contributes to gentrification pressure (high-demand area)
- Community benefits: Required community benefits to offset displacement impact
  - $2M community stabilization fund
  - 2% project cost for local hiring
  - Community land trust partnership to preserve 50 affordable units permanently

**Why we approved**:
This project advances multiple comp plan goals simultaneously:
1. Housing supply (250 units in tight market)
2. Affordability (50 affordable units permanently)
3. Transit ridership (high-opportunity location; reduced car dependency)
4. Equitable development (community benefits offset gentrification impacts)
5. Climate action (transit-supportive density; walkable)

Single-family neighbors' concerns about parking/traffic are legitimate but addressable through conditions.
Trade-off: Growth/walkability vs. neighborhood character (accepted because transit benefits justify change)

**Conditions imposed**:
- Traffic study and mitigation plan (address peak hour impacts)
- Parking maximums not minimums (50% under typical to support transit/walking)
- Community hiring plan (2% of jobs for local residents)
- Community benefits agreement ($2M community stabilization, workforce development)
- Design review (ensure street wall, activation of public plaza)

**Outcomes to track**:
- Did transit ridership increase as expected?
- Did community stabilization funds reduce displacement in neighborhood?
- Did local hiring goals get achieved?
- What was traffic impact in reality?
- Did affordable units actually serve 80% AMI households?
- Community perception: Did neighbors feel heard? Accept the trade-off?

---

## 2024 Q1 - Downtown Office-to-Residential Conversion

**Decision**: Approved with streamlined permitting (adaptive reuse incentives)

**What was requested**: Convert 8-story 1980s office building to 80 apartments + ground-floor retail

**Planning analysis**:
- Zoning: Allowed in D-1 downtown zone
- Housing: Converts underutilized office (remote work changed demand) to housing
- Affordability: Developer required 20% affordable (16 units at 80% AMI) to secure expedited review
- Design: Adaptive reuse preserves building character; retrofit for residential function
- Ground floor retail: Contributes to active downtown streets

**Why we approved with incentives**:
1. Remote work shift means downtown office market softening
2. This conversion turns underperforming asset into housing (market failure → planning intervention)
3. Expedited review incentivized affordability (developer happy to get faster approval; city got 20% vs. 15%)
4. Adaptive reuse better than demolition
5. Downtown housing supports walkability, transit ridership, street vitality

**Incentives provided**:
- Expedited environmental review (3 months vs. 6)
- Streamlined design review (meets guidelines = auto-approved)
- Parking modification (reduced requirement for transit-rich location)
- FAR bonus eligibility (could go over typical downtown limits for additional height/density)

**Outcomes tracked**:
- Did streamlined approval attract more conversions?
- Did affordability levels actually happen or was it just paper?
- Did ground floor retail activate downtown streets?
- Was developer pleased with incentives? Willing to do more conversions?
```

---

## How to Populate Your Knowledge Base

### Phase 1: Essential (Week 1-2)
1. **Zoning summary**: Extract key regulations (don't copy entire code; just key info)
2. **Comp plan summary**: Key goals and policies (not full document)
3. **Demographic snapshot**: Current population, housing, employment (use latest census/market data)
4. **Decision log template**: Start capturing decisions going forward

### Phase 2: Important (Week 3-4)
5. **Neighborhood profiles**: One profile per neighborhood (use template above)
6. **Affordability policy**: Full inclusionary zoning policy text
7. **Equity framework**: How you define/measure equity
8. **Active projects**: Current projects in review

### Phase 3: Comprehensive (Month 2+)
9. **Design guidelines**: Reference document
10. **Precedent projects**: Projects that worked well; what made them successful?
11. **Comparable cities**: How do other jurisdictions handle your challenges?
12. **Approval trends**: Analyze last 2 years of approvals—what did you build? How equitable?

---

## Keeping Knowledge Base Updated

- **Monthly**: Update active projects, add new decisions, track comp plan progress
- **Quarterly**: Update demographic/market data, trend analysis
- **Annually**: Full demographic refresh, comp plan implementation assessment, policy review
- **As needed**: New projects, policy changes, lessons learned

---

## Using Knowledge Base with Agents

Agents reference knowledge base to ground analysis:

- **Development Review Agent**: "Check zoning against R-4 district rules [link to zoning_districts.md]"
- **Equity Auditor**: "How does this compare to equity framework [link to equity_framework.md]"
- **Community Engagement**: "Who are stakeholders in this area [link to neighborhood_profile.md]"
- **Comp Plan Monitor**: "Does this advance housing goal [link to goals_and_policies.md]"

Knowledge base is source of truth; agents apply it consistently.
