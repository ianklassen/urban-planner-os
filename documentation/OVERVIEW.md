# Urban Planner Operating System

## Overview

The Urban Planner OS is an AI-augmented operating system designed to accelerate planning work by giving LLMs comprehensive shared context about a city, region, or planning domain. It integrates fragmented planning knowledge (zoning codes, demographic data, community feedback, regulatory frameworks, precedents) into a unified system where AI agents can reason holistically about planning decisions.

**Built for**: Planners, planning departments, urban design teams, community planners, regional planning organizations
**Tech Stack**: Cursor IDE + Claude (or compatible LLM), with optional MCP tool integrations
**License**: MIT (adapt as needed)

---

## Core Philosophy

Urban planning is inherently contextual and interconnected. Planners must simultaneously consider:
- Regulatory constraints (zoning, design guidelines, state/federal law)
- Data realities (demographics, traffic, land use, environmental conditions)
- Stakeholder needs (residents, businesses, developers, equity communities)
- Strategic direction (comprehensive plans, policy frameworks)
- Precedent & best practices (comparable projects, design standards)

The OS gives LLMs this full context, enabling them to:
- Synthesize complex information automatically
- Catch conflicts and unintended consequences
- Generate higher-quality analysis faster
- Reduce manual context-switching
- Maintain consistency across decisions
- Track reasoning over time

---

## System Architecture

### 1. **Rules** - Persistent Guidance
Applied to every interaction. Define your jurisdiction's planning DNA.

**Core rule categories:**
- **Regulatory**: Zoning code, design guidelines, development standards
- **Strategic**: Comp plan priorities, equity frameworks, climate goals
- **Process**: Public engagement protocols, decision-making criteria, approval workflows
- **Values**: Sustainability standards, livability metrics, community priorities

**Example Rules**:
- "All proposals must be evaluated against equity criteria: Will this increase or decrease access to opportunity for historically marginalized communities?"
- "Mixed-use development is preferred in commercial corridors per Comp Plan 2030"
- "All residential projects must include 15% affordable units per inclusionary zoning policy"

Rules ensure every analysis is grounded in your jurisdiction's context and values.

### 2. **Skills** - On-Demand Capabilities
Specialized planning tools callable by users or agents.

**Core Skills for Urban Planners**:

#### Development Review (DevReview)
- Analyze development proposals against zoning, design guidelines, comp plan
- Identify compliance issues, design concerns, conditions needed
- Generate staff reports or recommendation memos

#### Comprehensive Plan Analysis
- Assess how proposals align with long-term vision
- Identify conflicts with stated policies
- Suggest modifications to achieve plan intent
- Track cumulative impacts of decisions on plan goals

#### Impact Analysis
- Traffic/mobility impact assessment
- Housing impact analysis (supply, affordability, displacement)
- Environmental impact screening
- Economic impact analysis
- Equity impact assessment (who benefits/bears burden?)

#### Community Feedback Synthesis
- Process public comment (100s to 1000s of comments)
- Identify themes, concerns, and opportunities
- Categorize by topic, sentiment, stakeholder group
- Generate summary reports highlighting key issues

#### Policy Review & Drafting
- Analyze existing policies for gaps, conflicts, outdated language
- Draft policy language aligned with best practices
- Cross-reference with related policies
- Flag unintended consequences

#### Demographic Analysis
- Analyze census/demographic data for neighborhoods
- Identify trends: growth, aging, gentrification risk
- Create profiles of current/future populations
- Support equitable planning decisions

#### Precedent Research
- Find comparable projects/policies (locally and nationally)
- Analyze what worked, what didn't, why
- Adapt best practices to local context

#### Scenario Planning
- Develop alternative futures for neighborhoods/corridors
- Model different zoning, density, use mix scenarios
- Analyze impacts of each scenario
- Support data-driven planning conversations

### 3. **Agents** - Autonomous Specialists
Persistent assistants that execute planning work.

**Core Agents**:

#### Development Review Agent
- Monitors incoming development proposals
- Automatically screens against zoning/design standards
- Flags issues early to planning staff
- Suggests conditions/modifications
- Generates initial staff analysis

#### Equity Auditor Agent
- Reviews all planning decisions for equity impacts
- Asks: Who benefits? Who bears the burden? Why?
- Tracks whether planning is reducing/increasing opportunity gaps
- Alerts on decisions that may worsen equity outcomes

#### Community Engagement Coordinator
- Tracks public feedback across channels (meetings, surveys, online portals)
- Synthesizes themes from 100+ comments into actionable summary
- Identifies stakeholders and their positions
- Suggests engagement strategies based on feedback themes
- Generates meeting summaries and next steps

#### Comprehensive Plan Monitor
- Tracks how individual decisions accumulate toward plan goals
- Alerts if series of decisions contradicts comp plan intent
- Suggests policy adjustments to steer toward goals
- Maintains running record of plan implementation progress

#### Trend Analysis Agent
- Monitors market data, census updates, policy changes (state/federal/regional)
- Identifies emerging opportunities and challenges
- Alerts planning team to shifts in housing market, tech, climate, etc.
- Flags when assumptions underlying current policies may be outdated

#### Design Review Specialist
- Deep analysis of development proposals from design perspective
- Evaluates against design guidelines, context sensitivity, urban design principles
- Suggests design improvements aligned with community character
- Can compare to comparable projects for quality benchmarking

### 4. **Knowledge Base** - Shared Context
Organized repository of planning information that agents reference.

**Core Knowledge Domains**:

```
knowledge/
├── regulations/
│   ├── zoning_ordinance.md
│   ├── design_guidelines/
│   ├── development_standards.md
│   └── land_use_policy.md
├── comp_plan/
│   ├── vision_statement.md
│   ├── goals_and_policies.md
│   ├── equity_framework.md
│   └── sustainability_targets.md
├── demographics/
│   ├── neighborhood_profiles.md
│   ├── census_data/
│   ├── population_trends.md
│   └── equity_indicators.md
├── projects/
│   ├── active_projects.md
│   ├── precedents/
│   ├── lesson_learned.md
│   └── pipeline.md
├── stakeholders/
│   ├── community_organizations.md
│   ├── key_contacts.md
│   └── engagement_history.md
├── decisions/
│   ├── decision_log.md
│   ├── major_approvals/
│   ├── policy_changes.md
│   └── outcomes.md
└── best_practices/
    ├── comparable_cities.md
    ├── design_precedents.md
    ├── policy_models.md
    └── tools_and_methods.md
```

**What to include**:
- Full or summarized text of ordinances/guidelines
- Key comp plan passages, not full documents
- Current demographic/market data (updated annually)
- Active project descriptions and decisions
- Historical decisions and rationale
- Links to external resources (state requirements, climate commitments, etc.)
- Lessons learned from past projects
- Examples of excellent design in your jurisdiction

---

## The Context Graph - Memory & Learning

Over time, the OS builds a **decision and reasoning history** that becomes increasingly valuable.

**What it tracks**:
- Major planning decisions made
- Reasoning behind each decision
- Outcomes: Did the decision achieve intended goals?
- How decisions interconnect (proposal A impacts comp plan goal B, which enables project C)
- Trends: Are we implementing the comp plan? Moving toward equity goals?
- What worked: Which policies generated good outcomes? Which missed?

**Why it matters**:
- Future decisions can reference past reasoning ("We chose this approach in 2024 because...")
- Pattern recognition: "We've approved 5 projects with similar concerns—time for policy change?"
- Accountability: Clear record of why decisions were made
- Learning: Next comp plan update grounded in actual implementation experience

---

## Getting Started: Implementation Guide

### Phase 1: Setup (Week 1-2)

1. **Fork/clone PM Operating System** (or set up manually in Cursor)
   - Structure files like PM OS
   - Adapt for planning domain

2. **Build your Rules** (1-2 weeks)
   - Extract key passages from zoning code
   - Summarize comp plan goals and policies
   - Document equity framework and values
   - List public engagement standards
   - ~5,000-10,000 words total

3. **Create initial Knowledge Base**
   - Zoning and design guideline summaries
   - Comp plan highlights
   - Recent demographic snapshot
   - 3-5 precedent projects with analysis
   - Decision log template

4. **Invite early users**
   - 2-3 planning staff to test
   - Gather feedback on what context is missing

### Phase 2: Agents & Skills (Week 3-4)

5. **Build first 2-3 Agents**
   - Start with Development Review Agent
   - Add Community Engagement Coordinator
   - Iterate based on staff feedback

6. **Create 3-5 Core Skills**
   - Impact Analysis
   - Community Feedback Synthesis
   - Comprehensive Plan Analysis
   - Demographic Profile Generator
   - Policy Compliance Check

7. **Test with real work**
   - Use agents/skills on active projects
   - Refine based on results

### Phase 3: Expand & Operationalize (Month 2+)

8. **Add more Agents** as needed
9. **Build Equity Auditor** (critical for values alignment)
10. **Integrate external data** (census, market data, climate data via MCPs if available)
11. **Create decision tracking** workflow
12. **Document lessons learned**

---

## Agents Deep Dive - Specific Examples

### Development Review Agent

**Trigger**: New development proposal submitted

**Process**:
1. Extract key details (location, density, use mix, height, parking, affordability, etc.)
2. Check zoning compliance
   - Is use allowed in zone?
   - Is density within zoning envelope?
   - Are parking ratios correct?
3. Check design guideline compliance
   - Street frontage, setbacks, active ground floor?
   - Context-sensitive design?
   - Design quality?
4. Check comp plan alignment
   - Does it advance comp plan goals?
   - Does it undermine any policies?
5. Flag equity concerns
   - Does it create or worsen opportunity gaps?
   - Who will live/work here? Price point?
6. Generate output
   - Compliance checklist (pass/fail on each item)
   - Issues list (ranked by severity)
   - Suggested conditions
   - Design recommendations
   - Initial staff analysis memo

**Output sample**:
```
PROJECT: 123 Main Street Mixed-Use Development
ZONING ANALYSIS: ✓ PASS
- Use (residential + retail): Permitted
- Density (120 du/acre): Within zoning envelope
- Height (8 stories): Within code limits

DESIGN ANALYSIS: ⚠ ISSUES
- Ground floor retail frontage: PASS
- Street setback: Issue - current design sets back 15 ft, guideline requires street frontage
- Pedestrian amenities: MISSING - guideline requires public plaza

COMP PLAN ALIGNMENT: ✓ PASS
- Advances transit-oriented development goal
- Adds housing in opportunity area
- Supports mixed-use corridor vision

EQUITY REVIEW: ⚠ CONCERN
- 200 units total; 0 affordable units (project doesn't trigger inclusionary zoning per size)
- RECOMMENDATION: Negotiate affordability as condition

NEXT STEPS:
1. Applicant revise ground floor setback
2. Add public plaza
3. Negotiate affordability
```

### Community Engagement Coordinator Agent

**Trigger**: Public comment period closes on major proposal

**Input**: 200+ public comments (emails, survey responses, meeting notes)

**Process**:
1. Extract all comments
2. Categorize by topic:
   - Traffic/parking concerns
   - Environmental impact
   - Affordability/displacement
   - Design/aesthetics
   - Process concerns
   - Support/opposition
   - Specific issues
3. Identify stakeholder groups:
   - Residents near site
   - Affordable housing advocates
   - Business community
   - Environmental groups
   - etc.
4. Analyze by group: What do residents want? Business community? Equity advocates?
5. Assess sentiment: How many for/against? How intense?
6. Identify constructive suggestions vs. vague opposition
7. Generate synthesis document

**Output sample**:
```
ENGAGEMENT SUMMARY: 123 Main Street Project

OVERALL SENTIMENT:
- 42% supportive
- 38% opposed
- 20% conditional support

TOP CONCERNS (by frequency):
1. Traffic & Parking (mentioned in 87 comments)
   - "Will add traffic on Main Street"
   - "Not enough parking for retail"
   - "Need traffic study"

2. Affordability (mentioned in 64 comments)
   - "Rents too high for current residents"
   - "Gentrification risk"
   - "Need 30% affordable units"

3. Design & Character (mentioned in 43 comments)
   - "Too tall for neighborhood"
   - "Breaks street wall on east side"
   - "Positive: good ground floor design"

STAKEHOLDER BREAKDOWN:
- Nearby residents (n=115): 35% support, 55% opposed, 10% conditional
  Key concern: Traffic and height
- Affordable housing advocates (n=28): 18% support, 64% opposed
  Key issue: No affordability
- Business owners (n=22): 86% support
  Key support: Economic activity, customers

CONSTRUCTIVE SUGGESTIONS MENTIONED:
- Do traffic study before approval
- Add loading zone for retail delivery
- Reduce height by 1 story
- Negotiate 15% affordable units instead of 30%
- Add bike parking
- Improve retail activation potential

STAFF RECOMMENDATION:
Consider project with conditions: (1) Traffic study and mitigations, (2) 15-20% affordable units, (3) reduce height to 7 stories, (4) improve east side design

ENGAGEMENT NEXT STEPS:
- Present findings to decision-makers
- Hold follow-up meeting with building team on key concerns
- Offer mediation between project team and affordable housing advocates
```

---

## Integration with Cursor IDE

**How it works in practice**:

1. **User scenario**: Planner receives new development proposal
   - Types `@urban-planner-os devreview` in Cursor
   - Pastes project details
   - OS automatically triggers Development Review Agent
   - Agent outputs analysis, issues, recommendations
   - Planner reviews and customizes

2. **Community feedback scenario**:
   - Comment period closes
   - Planner dumps 200+ comments into Cursor
   - Types `@urban-planner-os synthesize-feedback`
   - Agent synthesizes into clear report
   - Planner uses report to brief decision-makers

3. **Ongoing intelligence**:
   - Agents continuously monitor knowledge base
   - Alert planner: "Three new projects in central corridor—pattern suggests need for transit study"
   - Equity Auditor: "Last 6 approvals average 10% affordability—below comp plan equity target of 20%"

---

## Customization & Adaptation

This OS is designed to be **highly customizable** to your jurisdiction:

- **Adapt Rules** to your comp plan, ordinances, and values
- **Build domain-specific Skills** for your planning challenges
- **Populate Knowledge Base** with your city's data, projects, and history
- **Extend Agents** as you discover new needs
- **Integrate data sources** (your GIS system, housing database, etc.) via MCPs

**Key principle**: The OS learns your jurisdiction's planning style and values, then applies them consistently across analysis.

---

## Success Metrics

How do you know the OS is working?

1. **Speed**: Time to generate development review drops from 4 hours to 30 minutes
2. **Consistency**: Development decisions show fewer contradictions; equity considerations applied uniformly
3. **Quality**: Analysis catches more issues; staff spends less time on research, more on judgment
4. **Engagement**: Community feedback synthesis helps identify real concerns vs. noise
5. **Learning**: Decision log shows planning rationale; next comp plan update informed by outcomes of past decisions
6. **Equity**: Can demonstrate that planning decisions are reducing (not increasing) opportunity gaps

---

## Getting Help & Community

- Reference PM Operating System docs for technical implementation
- Adapt examples from other planning jurisdictions
- Share your rules/agents back to planning community (via GitHub)
- Test with real projects; iterate based on results

---

## Next Steps

1. **Read the detailed component guides** (Rules.md, Skills.md, Agents.md, Knowledge_Base.md)
2. **Follow the implementation guide** in Setup.md
3. **Start with Rules** – your zoning code and comp plan summaries
4. **Test with first Development Review** – see if it works for your jurisdiction
5. **Iterate** – add agents and skills as you discover what's most valuable
