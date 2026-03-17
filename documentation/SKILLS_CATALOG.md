# Urban Planner OS: Skills Catalog

Skills are specialized planning tools that users or agents can invoke. Each skill takes specific input and produces specific output.

Think of skills as your planning team's playbook: standardized ways of analyzing, designing, or communicating about planning work.

---

## Core Skills for Urban Planners

### 1. DEVELOPMENT REVIEW

**Purpose**: Analyze a development proposal against regulations, comp plan, design standards

**Triggers/Invocation**:
- User: "Analyze this development proposal"
- Agent: When new proposal enters system

**Input**:
- Project description (use, units, height, FAR, parking, etc.)
- Location (address, zoning district, neighborhood)
- Images/plans (if available)
- Project team's proposal document

**Process**:
1. Extract key project parameters
2. Check zoning compliance
   - Use permitted? ✓/✗
   - Density within envelope? ✓/✗
   - Height within limit? ✓/✗
   - Setbacks correct? ✓/✗
   - Parking ratios OK? ✓/✗
3. Check design compliance
   - Street frontage? ✓/✗
   - Ground floor activation? ✓/✗
   - Context sensitive? ✓/✗
   - High quality design? ✓/✗
4. Check comp plan alignment
   - Supports land use vision? ✓/✗
   - Contributes to housing goals? ✓/✗
   - Supports transit/sustainability? ✓/✗
5. Equity analysis
   - Affordability level? Market/workforce/deeply affordable?
   - Who will live/work here?
   - Gentrification risk?
   - Community benefit?
6. Summary recommendation
   - Approvable as-is? / Approvable with conditions? / Recommend changes?

**Output**:
```
DEVELOPMENT REVIEW REPORT
Project: [Name]
Applicant: [Name]
Location: [Address] - [Zone]

COMPLIANCE SUMMARY
Zoning:           [Pass/Fail] - [Issues if any]
Design Standards: [Pass/Fail] - [Issues if any]
Comp Plan:        [Pass/Fail] - [Issues if any]

DETAILED FINDINGS
[For each non-compliance: What's the issue? Why does it matter? How to fix?]

EQUITY ANALYSIS
[Current affordability in area: X% at <60% AMI]
[Project affordability: Y% at Z% AMI]
[Assessment: Contributes to goal? / Underperforms? / Risk of displacement?]
[Recommendation: Increase affordability? Community benefits?]

RECOMMENDED CONDITIONS
[List specific conditions to address issues and fulfill plan intent]

STAFF RECOMMENDATION
Recommend [APPROVAL / APPROVAL WITH CONDITIONS / DENIAL]
Rationale: [1-2 sentences on why this supports planning goals]
```

---

### 2. COMMUNITY FEEDBACK SYNTHESIS

**Purpose**: Process 10-1000 community comments into clear themes and recommendations

**Triggers**:
- User: "Synthesize these public comments"
- Agent: When comment period closes

**Input**:
- Public comments (emails, survey responses, meeting notes, social media)
- Project description (for context)
- Any prior community feedback on similar issues

**Process**:
1. Extract all comments
2. Parse into individual opinions/concerns
3. Categorize by topic
   - Safety/traffic/parking
   - Environment
   - Housing/affordability/displacement
   - Design/character
   - Economic impact
   - Process/engagement
   - Support/opposition
   - Other
4. Identify stakeholder groups
   - Residents in/near impact area
   - Business community
   - Affordable housing advocates
   - Environmental advocates
   - Faith community
   - Youth
   - Seniors
   - Other
5. Analyze by group: What does each group want?
6. Assess sentiment
   - % supportive / opposed / conditional
   - Intensity of concern
   - Underlying values/fears
7. Identify "dark horse" insights
   - Rare but important concerns (only 3 people mentioned, but critical)
   - Common ground between opposing groups
   - Constructive suggestions
8. Synthesize into themes
9. Translate themes into implications for decision

**Output**:
```
COMMUNITY FEEDBACK SYNTHESIS REPORT
Project: [Name]
Comment period: [Dates]
Comments received: [#]

OVERALL SENTIMENT
% Supportive:     X%
% Opposed:        Y%
% Conditional:    Z%
% Neutral:        A%

KEY THEMES (by frequency)
1. [Theme - X mentions]
   - Specific concern 1
   - Specific concern 2
   - What people are really worried about

2. [Theme - Y mentions]
   - Specific concern 1
   - Specific concern 2

[Etc.]

STAKEHOLDER BREAKDOWN
Residents near site (n=X):
  - Sentiment: X% support, Y% oppose
  - Top concerns: [1, 2, 3]

Affordable housing advocates (n=X):
  - Sentiment: X% support, Y% oppose
  - Top concerns: [1, 2, 3]

Business community (n=X):
  - Sentiment: X% support, Y% oppose
  - Top concerns: [1, 2, 3]

[Etc. for each stakeholder group]

COMMON GROUND ACROSS GROUPS
[Areas where different groups agree, even if they disagree overall]

CONSTRUCTIVE SUGGESTIONS
[Ideas mentioned that could improve project; not opposed by any group]
- Suggestion 1 (X mentions)
- Suggestion 2 (Y mentions)

STAFF INTERPRETATION
What the community is telling us:
[Translate concerns into planning implications]

Implications for decision:
- [Condition 1 addresses concern X]
- [Condition 2 addresses concern Y]
- [Community benefit to address concern Z]

RED FLAGS
[Concerns that suggest project may have real problems; need to address]

ENGAGEMENT QUALITY ASSESSMENT
- Were all affected communities able to participate? [Y/N]
- Did concerns get heard? [Y/N]
- Recommend follow-up with [group]?
```

---

### 3. IMPACT ANALYSIS (Multiple Types)

#### 3a. Housing Impact Analysis

**Purpose**: Understand how development affects housing supply and affordability

**Input**:
- Project description (# units, affordability %, price point)
- Neighborhood housing data (current supply, affordability, rents/prices, trends)

**Process**:
1. Calculate displacement risk
   - What % of new units will be affordable?
   - What's the area's current affordability?
   - Will new market-rate development raise rents (displacement)?
2. Assess supply contribution
   - How many units? Where on supply curve?
   - Is this underproduction area? Supply-constrained?
   - How many units needed vs. provided?
3. Demographic impacts
   - Who will this serve? Young professionals? Families? Seniors?
   - What income levels?
   - What household sizes?
4. Community impacts
   - Current residents: Risk of displacement?
   - How to mitigate? Community benefits? Rent stabilization?
   - Wealth building: Ownership opportunities?

**Output**:
```
HOUSING IMPACT ANALYSIS
Project: [Name]
Units: [#] [Breakdown: % 1br, 2br, 3br]
Affordability: [X% at 60% AMI, Y% at 80% AMI, Z% market]
Price point: Estimated rent/price: $X

SUPPLY CONTRIBUTION
Housing supply in [neighborhood]: [#] units, [#] affordable
Vacancy rate: [X]% (tight=<3%, balanced=3-5%, loose=>5%)
Gap: Need [#] more affordable units to serve [#] lower-income residents
This project contributes: [X] affordable units = [%] of gap

DISPLACEMENT RISK
Current residents at risk of displacement: [#] households
Gentrification trajectory: [Description of how area changing]
Risk level: [Low / Moderate / High]
Mitigation recommendations: [Rent stabilization? Community land trust? Community benefits?]

DEMOGRAPHIC IMPACT
Households this serves:
- Age profile: Who's looking for housing?
- Income profile: Who can afford it?
- Family size: How many kids?
- Current undersupply: Young professionals / families / seniors / other?

COMMUNITY BENEFIT RECOMMENDATIONS
To address gentrification risk:
- [Condition 1]
- [Community benefit 2]
- [Wealth-building opportunity 3]
```

#### 3b. Equity Impact Analysis

**Purpose**: Understand how development affects access to opportunity and equity

**Input**:
- Project description
- Neighborhood demographic and opportunity data
- Equity framework from comp plan

**Process**:
1. Define "opportunity" in your context
   - Access to jobs?
   - Access to quality schools?
   - Environmental quality?
   - Community wealth building?
   - Cultural assets?
   - Safety?
2. Assess current opportunity gaps
   - What communities face barriers?
   - What's missing in this area?
3. Analyze project through equity lens
   - Does it expand access to opportunity? For whom?
   - Does it risk deepening gaps? How?
   - Is it culturally appropriate?
   - Who was engaged in decision?
4. Identify equity conditions
   - What would make this more equitable?
   - Who else needs to benefit?

**Output**:
```
EQUITY IMPACT ANALYSIS
Project: [Name]
Location: [Neighborhood with equity profile]

OPPORTUNITY ANALYSIS
Opportunity score in this area: [Low / Moderate / High]
Gaps vs. citywide:
- Access to jobs: [Gap X]
- Access to good schools: [Gap Y]
- Environmental quality: [Gap Z]
- Community wealth: [Gap A]
- [Other gaps]

PROJECT IMPACT ON OPPORTUNITY
Does this project expand or limit opportunity?

Positive impacts:
- Creates jobs: [#] construction, [#] permanent
- Housing for [income level]: Expands affordability? ✓/✗
- Services/amenities: [Retail, parks, etc.]
- Community wealth: Ownership? Business opportunities?

Risk areas:
- Displacement: Gentrification driver? [Assessment]
- Labor: Are construction/permanent jobs accessible to local workers?
- Community voice: Was this community engaged in decision?

Net assessment: [Project expands / maintains / risks reducing opportunity]

EQUITY CONDITIONS
To ensure project contributes to equity goals:
- Community hiring: X% local, Y% from lower-income residents
- Community benefits: [Specific benefits]
- Affordability: [Levels required]
- Community engagement: [Ongoing]
- Ownership/wealth: [Opportunity for community ownership?]
```

#### 3c. Fiscal Impact Analysis

**Purpose**: Understand financial impacts on city and community

**Input**:
- Project description
- Development cost data
- City tax/fee structure
- Operations data (typical for project type)

**Process**:
1. Development impact on municipal finances
   - Tax revenue generated
   - Infrastructure costs to serve
   - Net city fiscal impact (positive/negative)
2. Cost to residents/workers
   - Rent/price point vs. local wages
   - Affordability
   - Feasibility for stated income levels
3. Community economic impact
   - Job creation (construction + permanent)
   - Business opportunity
   - Local vs. outside capital flows

**Output**:
```
FISCAL IMPACT ANALYSIS
Project: [Name]

MUNICIPAL IMPACT
Annual revenue generated: $X
- Property taxes: $Y
- Sales taxes (if applicable): $Z

Infrastructure costs: $A
Net impact: $[B] annually

Impact over project lifetime: [Positive / Neutral / Negative]

RESIDENT/WORKER AFFORDABILITY
Estimated rent: $X
Local median wage: $Y
Rent burden: [X%] of median income [Affordable if <30%]
Accessibility: [Market-rate / workforce / deeply affordable / other]

ECONOMIC DEVELOPMENT IMPACT
Job creation:
- Construction jobs: [#] [X% local hiring requirement?]
- Permanent jobs: [#] [Wage levels? Benefits?]
- Local business opportunities: [Description]

Community wealth impact:
- Opportunities for community ownership? [Y/N]
- Small business growth? [Y/N]
- Wealth extraction to outside capital? [Risk Y/N]
```

---

### 4. POLICY REVIEW & DRAFTING

**Purpose**: Analyze existing policies or draft new ones

**Triggers**:
- User: "Review zoning code section X for gaps"
- User: "Draft affordability policy for [situation]"
- Agent: Proactive review when issues arise

**Input**:
- Existing policy language (if reviewing)
- Policy intent/goals
- Comparable policies (best practices)
- Problems you're trying to solve

**Process**:
1. Review existing policy
   - What does it say?
   - What's the intent?
   - What problems is it solving?
   - What unintended consequences?
   - Where's it weak?
2. Gap analysis
   - What situations does it not address?
   - Are there contradictions with other policies?
   - Is language clear?
   - Is it enforceable?
3. Benchmark
   - How do other jurisdictions handle this?
   - What works? What doesn't?
4. Recommendations
   - Clarifications needed?
   - Stronger enforcement?
   - New provisions?

**Output**:
```
POLICY REVIEW: [Policy Name]

CURRENT LANGUAGE
[Copy of existing policy]

INTENT & CONTEXT
[What problem does this solve? Why was it adopted?]

ANALYSIS
Strengths:
- [Strength 1]
- [Strength 2]

Weaknesses:
- [Gap 1]
- [Gap 2]
- [Unintended consequence]

Enforcement challenges:
- [Issue 1]

Ambiguities:
- [Unclear provision]

COMPARATIVE ANALYSIS
Other jurisdictions addressing this:
- [City A] approach: [Description] [Works well / Has problems]
- [City B] approach: [Description]

RECOMMENDATIONS
1. [Specific amendment]
2. [Clarification]
3. [New provision]
4. [Enforcement mechanism]

Rationale: [Why these changes improve policy]

Draft language: [If recommending specific changes, provide proposed text]
```

---

### 5. DEMOGRAPHIC PROFILE GENERATOR

**Purpose**: Create snapshot of neighborhood's current and future population

**Input**:
- Neighborhood/project area
- Available demographic data (census, household survey, etc.)
- Time frame (current, projected 10 years)

**Process**:
1. Current demographics
   - Population
   - Age distribution
   - Income distribution
   - Household types (families, seniors, singles, etc.)
   - Racial/ethnic composition
   - Language spoken
   - Housing tenure (owners vs. renters)
2. Trends
   - Population growth/decline
   - Aging? Younger? Changing family structure?
   - Income trend (gentrifying? Wealth flowing out?)
   - Changing household types
   - In-migration? Out-migration? Of whom?
3. Needs assessment
   - Housing needs (affordability, size, accessibility)
   - Service needs (schools, services for seniors, etc.)
   - Economic opportunity gaps
   - Environmental health concerns
4. Projected future
   - If trends continue, what will population look like in 10 years?
   - Is current planning supporting desired future?
   - What policies/projects would shape different outcome?

**Output**:
```
DEMOGRAPHIC PROFILE: [Neighborhood]

CURRENT SNAPSHOT (as of [year])
Population: [#]
Population density: [#] people/acre

AGE DISTRIBUTION
- 0-17: [#] [%]
- 18-34: [#] [%]
- 35-64: [#] [%]
- 65+: [#] [%]

INCOME DISTRIBUTION
- <30% AMI: [#] households [%]
- 30-60% AMI: [#] households [%]
- 60-100% AMI: [#] households [%]
- >100% AMI: [#] households [%]
Median household income: $X
Poverty rate: [X]%

HOUSEHOLD TYPES
- Families with children: [X]%
- Seniors living alone: [X]%
- Families with seniors: [X]%
- Singles: [X]%

RACE/ETHNICITY & LANGUAGE
- [Race/ethnicity 1]: [X]%
- [Race/ethnicity 2]: [Y]%
- [Language other than English spoken]: [Z]%

HOUSING
- Owner-occupied: [X]%
- Renter-occupied: [Y]%
- Avg. rent: $X
- Avg. home value: $Y
- Rent/income burden: [X]% (affordable if <30%)

EMPLOYMENT & OPPORTUNITY
- Unemployment rate: [X]%
- Median wage (local jobs): $X
- Wage gap vs. citywide: [+/- Y]%

TRENDS (past 10 years)
- Population change: [+/- X]%
- Income trend: [Gentrifying / Stable / Declining]
- Housing affordability: [Improving / Stable / Declining]
- Who's moving in/out: [Demographics]
- Industry/job changes: [Description]

NEEDS ASSESSMENT
Housing needs:
- Shortage of affordable: [#] units at [income levels]
- Need for larger units (families): [#]
- Need for accessible units (seniors/disabled): [#]

Economic opportunity:
- Wage gap vs. city: $X/year
- Jobs accessible without car: [#]
- Good jobs within reach: [Y/N]

Services/amenities:
- Schools: [Quality assessment]
- Parks/recreation: [Access]
- Health facilities: [Availability]
- Grocery/food access: [Assessment]

FUTURE PROJECTION (10 years)
If trends continue:
- Population: [#] [+/- X%]
- Age profile: [Description - aging? younger?]
- Income profile: [Gentrifying? Diversifying?]
- Housing needs: [New gaps?]

Desired future:
- What should neighborhood look like?
- What policies/projects would achieve it?
- Trade-offs?

PLANNING IMPLICATIONS
Current development patterns supporting desired future? [Y/N]
What changes needed?
```

---

### 6. SCENARIO PLANNING

**Purpose**: Model different futures and compare outcomes

**Triggers**:
- User: "What if we zoned this for higher density?"
- User: "Compare these two design alternatives"
- Agent: During comprehensive planning to test different visions

**Input**:
- Base case/current situation
- Alternative scenarios (different zoning, design, uses, density)
- Evaluation criteria (housing supply, affordability, jobs, carbon, neighborhood character, etc.)

**Process**:
1. Define current baseline
   - What's allowed now? What would likely get built?
   - Impacts on housing, jobs, revenue, character, etc.
2. Define alternatives
   - Scenario A: Higher density residential
   - Scenario B: Mixed-use commercial
   - Scenario C: Preserved as-is
   - Etc.
3. Model impacts of each
   - Housing (units, affordability, type, price point)
   - Jobs (creation, types, wages)
   - Revenue (to city)
   - Transportation (traffic, parking need, transit demand)
   - Character (massing, pedestrianism, urban vs. suburban)
   - Sustainability (walkability, transit, energy)
   - Equity (who benefits? who bears costs?)
4. Compare
   - Trade-offs? Which scenario best achieves comp plan goals?
   - Which serves equity goals?
   - Which is financially feasible?
   - Which has community support?
5. Recommend

**Output**:
```
SCENARIO PLANNING ANALYSIS
Location: [Area]
Planning question: [What are we trying to decide?]

SCENARIOS ANALYZED
Scenario 1: [Name] - [Brief description]
Scenario 2: [Name] - [Brief description]
Scenario 3: [Name] - [Brief description]

COMPARATIVE IMPACTS

Housing Production
                    Scenario 1    Scenario 2    Scenario 3
Units produced      [#]          [#]           [#]
% Affordable        [X]%         [Y]%          [Z]%
Unit types          [Mix]        [Mix]         [Mix]
Est. rent/price     $X           $Y            $Z

Employment
Jobs created        [#]          [#]           [#]
Job types           [Mix]        [Mix]         [Mix]
Wages               [Level]      [Level]       [Level]

City Fiscal Impact
Tax revenue/year    $X           $Y            $Z
Infrastructure cost $A           $B            $C
Net impact          $[+/-]       $[+/-]        $[+/-]

Transportation
New vehicle trips   [#]          [#]           [#]
Transit-dependent? [Y/N]         [Y/N]         [Y/N]
Parking need        [#] spaces   [#] spaces    [#] spaces

Sustainability
Carbon footprint    [High/Med/Low] [H/M/L]     [H/M/L]
Walkability score   [Score]       [Score]       [Score]
Green space impact  [+/-]         [+/-]         [+/-]

Character Impact
Massing             [Description] [Desc]       [Desc]
Pedestrianism       [High/Med/Low] [H/M/L]     [H/M/L]
Local character     [Preserved / Changed / Lost] [etc]

EQUITY ANALYSIS
Who benefits:
Scenario 1: [Income levels, demographics]
Scenario 2: [Income levels, demographics]
Scenario 3: [Income levels, demographics]

Who bears costs:
Scenario 1: [Groups]
Scenario 2: [Groups]
Scenario 3: [Groups]

Equity ranking: [Which advances equity goals?]

RECOMMENDATION
Best scenario for [Goal 1]: Scenario X because [reason]
Best scenario for [Goal 2]: Scenario Y because [reason]
Overall recommendation: Scenario Z because [balances goals]

Trade-offs to accept: [What are we giving up?]
```

---

## Skill Implementation in Cursor

In your Cursor skills/commands:

```
@devreview [project details] - Analyze development proposal
@engage [comments] - Synthesize community feedback
@housing-impact [project] - Housing impact analysis
@equity-impact [project] - Equity analysis
@impact-fiscal [project] - Financial impact
@policy-review [policy text] - Analyze/improve policy
@demographics [neighborhood] - Population profile
@scenarios [question] [alternatives] - Compare alternative futures
```

---

## Creating New Skills for Your Jurisdiction

Your OS should evolve with new skills as you discover needs:

1. **Identify repetitive planning work**
   - "We analyze parking impacts for every project"
   - "We always need pedestrian-level analysis for downtown"
   - "We review every proposal for tree loss"

2. **Standardize the process**
   - What questions do we always ask?
   - What data do we always analyze?
   - What format do we always use for output?

3. **Codify as a Skill**
   - Write up the skill definition
   - Use it with agents/users
   - Refine based on feedback

4. **Document & share**
   - Other jurisdictions probably need the same thing
   - Share your skills back to planning community
