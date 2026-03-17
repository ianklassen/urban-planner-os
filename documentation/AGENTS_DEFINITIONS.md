# Urban Planner OS: Agents Definitions

Agents are autonomous specialists that execute planning work without requiring human invocation for every step. They proactively monitor, analyze, and alert.

Think of agents as your planning department working 24/7: monitoring incoming projects, tracking policy implementation, synthesizing community feedback, auditing decisions for equity.

---

## Core Agents

### 1. DEVELOPMENT REVIEW AGENT

**Purpose**: Continuously monitor incoming development proposals; screen against zoning/design/comp plan standards

**Trigger**: New development proposal submitted to system

**Work Process**:
1. Monitor intake (applications, preapplication meetings, inquiries)
2. When new proposal received:
   - Extract project details (use, density, height, location, affordability, etc.)
   - Run automatically through Development Review skill
   - Generate staff analysis
3. Screen against regulations
   - Compliance checklist (pass/fail on zoning, design, comp plan)
   - Issues identified (ranked by severity)
4. Generate output
   - Compliance/non-compliance flag
   - Issues list
   - Suggested conditions
   - Recommended modifications
5. Route to right planner
   - If compliant as proposed → "Ready for review; recommend approval with conditions X, Y, Z"
   - If non-compliant → "Issues: A, B, C; Recommend applicant revise before public review"
   - If complex → Alert lead planner for judgment call
6. Maintain record
   - Log in project database
   - Track what issues flagged
   - Later: Did we call it right? Did the issues actually matter?

**Output**:
- Development Review Report (same as skill)
- Flagged issues list
- Recommended conditions
- Routing recommendation to planning staff

**Success Metrics**:
- Does agent-flagged issues match staff review? (Should be >80% alignment)
- Do recommended conditions prevent problems?
- Do applicants use recommendations to improve projects?
- Does early review accelerate timeline?

**Configuration**:
```
TRIGGER: New development proposal
FREQUENCY: On intake
AUTOMATION LEVEL: Full analysis; flags urgent issues
ESCALATION: Complex projects to lead planner
OUTPUT LOCATION: Project management system
ROUTING: [Zoning compliance] → planner A
         [Design review] → planner B
         [Large/complex] → planning manager
```

---

### 2. EQUITY AUDITOR AGENT

**Purpose**: Review all planning decisions for equity impacts; alert if decisions likely to worsen opportunity gaps

**Trigger**:
- Monthly review of all approvals (what were we approved?)
- Major policy decision
- Pattern flagging (e.g., "5 projects in a row with no affordability")

**Work Process**:
1. Monitor approvals
   - What got approved this month?
   - What were the conditions?
   - What affordability level?
2. Screen against equity framework
   - Does decision advance or harm opportunity?
   - Who benefits? Who bears costs?
   - Is it widening or closing gaps?
3. Patterns analysis
   - Is affordability %age declining over time?
   - Are low-income neighborhoods getting displacement-risk development?
   - Are wealthy neighborhoods hoarding opportunity?
   - Do decisions reflect equity values?
4. Alerts
   - "Last 6 projects averaged 8% affordability; target is 20%"
   - "3 projects in Community of Concern zone; none include community benefits"
   - "East side getting market-rate only; west side getting mixed-income"
   - "Project in high-opportunity area; consider maximizing affordability"
5. Recommendations
   - Tighten requirements?
   - Offer incentives for more affordability?
   - Update policy?
   - Reallocate capital to equity goals?

**Output**:
- Equity audit report (monthly/quarterly)
  - What approvals did we grant?
  - Were they equitable?
  - Are we advancing equity goals?
  - What needs to change?
- Red flags / urgent alerts
- Pattern alerts ("If this continues, we're off our equity target")
- Recommendations for policy/practice changes

**Success Metrics**:
- Is affordability %age tracking toward goal?
- Are opportunity gaps narrowing or widening?
- Can you point to specific decisions that reduced/increased opportunity gaps?
- Do equity concerns get proactively addressed vs. only reactive?

**Configuration**:
```
TRIGGER: Regular audit (monthly/quarterly) + real-time flagging of outliers
FREQUENCY: Scheduled review (e.g., first Monday of month)
AUTOMATION LEVEL: Analysis only; alerts to planning director
ESCALATION: Major equity concerns to planning commission/council
OUTPUT LOCATION: Equity audit log; public dashboard if available
```

---

### 3. COMMUNITY ENGAGEMENT COORDINATOR AGENT

**Purpose**: Monitor, synthesize, and respond to community feedback; help planning team engage effectively

**Trigger**:
- Comment period opens on public project
- Feedback received (email, survey, meeting)
- Public meeting held

**Work Process**:
1. Monitor engagement channels
   - Email to planning department
   - Online survey/portal
   - Social media mentions
   - Meeting attendance and comments
2. Collect and organize
   - Extract individual opinions
   - Track commenter info (name, stakeholder group if known)
   - Note sentiment, intensity, specific concerns
3. Synthesize in real-time
   - "100 comments received so far; themes emerging: traffic (40 mentions), affordability (25 mentions), design (15 mentions)"
   - "Residents near site mostly concerned about traffic; business community supportive"
   - "Environmental advocates flagging tree loss; suggests alternative design"
4. Identify opportunities
   - What suggestions keep appearing? Could these improve project?
   - What misunderstandings can staff clarify?
   - Where's common ground between opposing groups?
   - What's genuinely non-negotiable vs. could be resolved?
5. Alert planning team
   - "Major concern about parking; may need project revision or mitigation study"
   - "Community suggests X; worth considering?"
   - "Support weak until you address Y; could you modify?"
6. Generate synthesis
   - When comment period closes: full synthesis report
7. Track outcomes
   - Later: Did community input shape decision?
   - Did we communicate responsiveness?
   - What did community think of final decision?

**Output**:
- Real-time comment summaries ("40 comments received, themes...")
- Alerts on emerging concerns
- Recommendations for project modification
- Full synthesis report when comment period closes
- Engagement follow-up checklist

**Success Metrics**:
- Do staff feel they understand community position?
- Does feedback synthesis drive better decisions?
- Do communities feel heard? (Survey satisfaction)
- Are early concerns raised in comments addressed in final decision?
- Does synthesis process save staff time?

**Configuration**:
```
TRIGGER: Comment period opening; ongoing comment monitoring; comment period closing
FREQUENCY: Continuous; synthesis report at end
AUTOMATION LEVEL: Full analysis + alerts; recommendations only (no decision-making)
ESCALATION: Major controversy to planning manager; concerns about process to director
OUTPUT LOCATION: Project tracking system; visible to planning team
TRANSPARENCY: Synthesis report made public so community sees we listened
```

---

### 4. COMPREHENSIVE PLAN MONITOR AGENT

**Purpose**: Track whether individual decisions cumulatively implement comp plan; alert if drifting

**Trigger**:
- Monthly/quarterly monitoring
- Annual review against comp plan targets

**Work Process**:
1. Track comp plan goals
   - Goal: 40% of new housing at/below 100% AMI by 2035
   - Goal: Transit-oriented development in station areas
   - Goal: Reduce carbon emissions by 50% by 2030
   - Goal: Achieve equitable opportunity in all neighborhoods
   - Etc.
2. Monitor approvals against goals
   - Project approved: housing mix analysis
   - Calc: This project = X units, Y% affordable, contributes $Z toward goal
   - Cumulative: Year to date, we've approved Z% affordable
   - Track: Are we on trajectory for 40%?
3. Pattern detection
   - "All approvals this quarter in downtown; outer neighborhoods under-developing"
   - "High-opportunity jobs concentrated in north; south side lacks opportunity"
   - "Zoning allows density but market not delivering; prices too high"
   - "We're drifting from comp plan intent"
4. Alerts
   - "At current rate, we'll hit 25% affordability by 2035, not 40%; need to accelerate"
   - "Station area development slow; transit ridership potential untapped; consider incentives"
   - "Comp plan called for complete streets; traffic patterns suggest missed opportunity"
5. Recommendations
   - Tighten requirements? (If behind on goals)
   - Offer incentives?
   - Use capital programs to steer development?
   - Update policies?
   - Change zoning to enable plan?

**Output**:
- Comp plan implementation report (quarterly/annual)
  - How we're tracking against goals
  - Are we on trajectory?
  - What's working? What's not?
  - What mid-course corrections needed?
- Alerts on drifting
- Recommendations for acceleration/correction

**Success Metrics**:
- Are planning decisions implementing comp plan?
- Are comp plan targets being met on schedule?
- If drifting, does early alert allow correction?
- Is comp plan living document or shelf-ware?

**Configuration**:
```
TRIGGER: Quarterly comp plan tracking; alerts on major deviations
FREQUENCY: Scheduled quarterly review + real-time pattern detection
AUTOMATION LEVEL: Analysis and alert only; recommendations for discussion
ESCALATION: If significantly off-track by end of year, alert planning commission
OUTPUT: Annual comp plan monitoring report; public dashboard
```

---

### 5. TREND ANALYSIS AGENT

**Purpose**: Monitor market, demographic, policy changes (state/federal/regional); alert if assumptions underlying planning are shifting

**Trigger**:
- Monthly/quarterly monitoring
- Integration with data sources (market analysis, census updates, state policy changes, news, etc.)

**Work Process**:
1. Monitor external data sources
   - Housing market (prices, rents, inventory, interest rates)
   - Employment (job growth by sector, wage trends, remote work)
   - Demographics (population change, migration, aging)
   - Climate/environment (temps, extreme weather, regulatory changes)
   - State/federal policy (zoning reforms, climate targets, housing mandates)
   - Technology (autonomous vehicles, remote work, e-commerce changing retail)
2. Detect shifts
   - "Interest rates spiked; housing affordability declining; less market-rate affordable"
   - "Tech jobs growing 20%/year; wage pressure = gentrification risk"
   - "Remote work adoption means office space at risk; should our downtown plan shift?"
   - "State passed zoning reform; local ordinance now conflicts"
   - "EV adoption accelerating; parking requirements may be outdated"
3. Assess implications
   - How does this change our planning?
   - Does it validate current approach? Require change?
   - What opportunities emerge? What risks?
4. Alerts
   - "Market fundamentals shifting; past assumptions may be outdated"
   - "Opportunity: [State policy] enables new strategy"
   - "Risk: [Technology change] could disrupt [sector]"
5. Recommendations
   - Revise assumptions in comp plan?
   - Pilot new policies?
   - Create contingency plans?

**Output**:
- Trend alerts ("Market tightening; affordability risk increasing")
- Annual environmental scan report
- Recommendations for policy adaptation

**Success Metrics**:
- Are planning decisions grounded in current reality?
- Do planners catch market shifts before they become problems?
- Does early detection of trends allow proactive vs. reactive response?

**Configuration**:
```
TRIGGER: Continuous monitoring; monthly alert if major shift detected
FREQUENCY: Ongoing
AUTOMATION LEVEL: Analysis and alerts; research for staff discussion
ESCALATION: Major shifts (state policy change, market collapse, etc.) to director
DATA SOURCES: [List sources: real estate market data, census, state legislature tracking, tech news, climate data, etc.]
```

---

### 6. DESIGN REVIEW SPECIALIST AGENT

**Purpose**: Deep design analysis of development proposals; ensure quality and context sensitivity

**Trigger**: Significant development proposal (likely 50+ units, major site, public building)

**Work Process**:
1. Trigger: When Development Review Agent flags for detailed design review
2. Collect design information
   - Renderings, floor plans, site plan
   - Architectural style and materials
   - Pedestrian experience
   - Public realm design
   - Parking integration
3. Analysis
   - Evaluate against design guidelines
   - Context sensitivity: Does it fit neighborhood scale, form, materials?
   - Pedestrian experience: Is ground floor inviting? Safe? Active?
   - Design quality: Materials, proportions, details
   - Public realm: Does it contribute to street/plaza quality?
   - Accessibility: Is it welcoming to all users?
4. Comparison
   - Find comparable precedents (local & national)
   - What works about those? What doesn't?
   - Any lessons for this project?
5. Recommendations
   - Design improvements to meet guidelines
   - Suggestions for enhanced quality
   - Modifications for context sensitivity
6. Visualization
   - Generate graphic comparisons showing context sensitivity
   - "Here's how this fits your neighborhood context"
   - "Here's what ground floor experience looks like"

**Output**:
- Design review analysis with graphics
- Specific design recommendations
- Conditions for design approval
- Precedent comparisons

**Success Metrics**:
- Do recommended design improvements get built?
- Does community perception of neighborhood quality improve?
- Are design conflicts (applicant vs. neighborhood) resolved faster?

**Configuration**:
```
TRIGGER: Development Review Agent flags for detailed review
AUTOMATION LEVEL: Full analysis + recommendations
ESCALATION: Design committee review for controversial projects
OUTPUT: Design review report with graphics; color-coded suggestions
```

---

## How to Set Up Agents in Cursor

In your Cursor configuration:

```
AGENTS:

DevReview Agent:
  Trigger: Development proposal submitted
  Skill: @devreview
  Output: Dev Review Report, Issues List, Conditions
  Routing: To assigned planner

EquityAuditor Agent:
  Trigger: First Monday of month (monthly audit) + outlier detection
  Skill: @equity-impact
  Output: Equity audit report, Red flags
  Escalation: Planning director if major concerns

CommunityEngagement Agent:
  Trigger: Comment period opened; continuous monitoring; comment period closed
  Skill: @engage (ongoing); @engage-synthesis (at closure)
  Output: Real-time summaries; synthesis report
  Transparency: Public dashboard showing community feedback themes

CompPlan Monitor Agent:
  Trigger: Quarterly review (first day of Q2, Q3, Q4, Q1)
  Skill: Custom comp plan tracking
  Output: Quarterly tracking report
  Escalation: Planning commission if off-track

Trend Agent:
  Trigger: Continuous monitoring; alert if major shift
  Frequency: Weekly data check; monthly report
  Output: Alerts, environmental scan report
  Escalation: Director for major shifts

Design Review Agent:
  Trigger: Dev Review Agent flags for design detail review
  Skill: Design review + precedent research
  Output: Design review report with recommendations
  Routing: Design committee or staff
```

---

## Running Your Own Agents

You don't need to wait for AI agents; planning staff can run these processes:

1. **DIY Equity Audit**: Monthly, planner reviews approvals against equity criteria
2. **DIY Community Synthesis**: After comment period, planner synthesizes feedback
3. **DIY Comp Plan Monitor**: Quarterly, planner tracks projects against comp plan
4. **DIY Trend Scan**: Monthly planner monitors market/policy news

Once you identify the process, formalize it as an agent (or skill) that AI can execute.

---

## Agent Performance & Feedback

Track agent quality:

1. **Development Review Agent**:
   - Does it catch real issues? (Compare to staff review)
   - Are recommendations sound?
   - Do applicants improve projects based on feedback?
   - Any false alarms?

2. **Equity Auditor**:
   - Is affordability tracking toward goal?
   - Does real-time equity monitoring shift decisions?
   - Community perception: Are decisions perceived as equitable?

3. **Community Engagement**:
   - Does synthesis match staff perception?
   - Do recommendations improve projects?
   - Community satisfaction with engagement process?

4. **Comp Plan Monitor**:
   - Are we tracking toward goals?
   - Does early alert allow course correction?

Use feedback to refine agent prompts and processes.

---

## Next Steps

1. **Start with Development Review Agent**
   - Most immediately useful; saves staff time
   - Use with real proposals; refine based on feedback
2. **Add Equity Auditor next**
   - Critical for values alignment
   - Monthly audits starting
3. **Expand to other agents** as needed
4. **Create your own agents** for domain-specific planning challenges
