# Urban Planner OS: Setup & Implementation Guide

Ready to build your own Urban Planner Operating System? This guide walks you through getting started in phases.

---

## Prerequisites

**Technical**:
- Access to Cursor IDE (or Claude API/web interface)
- Ability to create/edit text files
- Basic file organization skills
- GitHub account (optional, but recommended for version control)

**Planning knowledge**:
- Familiarity with your zoning code
- Copy of your comprehensive plan
- Some recent development approvals to use for testing

**Time commitment**:
- Phase 1 (Essential): 15-20 hours over 2-3 weeks
- Phase 2 (Intermediate): 15-20 hours over 2-3 weeks
- Phase 3 (Advanced): Ongoing, 5-10 hours/week

**Success likelihood**: If you follow this guide and actually build it (don't just read), you'll have a working system that saves your planning team 20+ hours per month.

---

## Phase 1: Foundation (Weeks 1-2)

### Week 1: Rules Framework

**Goal**: Codify your planning DNA—what you care about, what the law requires

**Step 1.1: Extract Your Zoning Code Summary** (2-3 hours)

1. Open your zoning ordinance
2. Read through and extract key districts you use most
   - What zones exist? R-1? R-4? D? C? M?
   - For each zone: What uses allowed? FAR? Height? Setbacks? Parking? Key design standards?
3. Create file: `regulations/zoning_districts.md`
4. Use template from Knowledge Base Structure document above
5. **Don't copy entire code**—just key info that agents need for analysis
   - Use: "R-4 allows apartments, duplexes, townhomes; FAR 3.0, height 8 stories"
   - Don't copy: Entire "Use Table, Section 23.47.100, as amended by Ordinance 2018-067..."
6. Spend maybe 30 minutes per zone you commonly use

Example: If your city has 5 main zones, spend 2.5 hours extracting summaries.

**Step 1.2: Extract Comp Plan Goals** (2-3 hours)

1. Open your comprehensive plan
2. Read through; identify 5-7 major goals
   - Housing goal?
   - Equity goal?
   - Sustainability goal?
   - Walkability goal?
   - Economic development goal?
3. For each goal:
   - What's the vision? (1-2 sentences)
   - What are specific targets? (40% affordability? Net-zero by 2035?)
   - What policies support this goal? (List 3-5)
4. Create file: `comp_plan/goals_and_policies.md`
5. Use template from Knowledge Base Structure doc above
6. Again: Summarize, don't copy entire document

**Step 1.3: Build Your Rules Framework** (3-4 hours)

1. Create file: `RULES_FOR_YOUR_CITY.md`
   - Copy the Rules Framework template above
   - Adapt each section to your jurisdiction:
     - Regulatory rules from your zoning code
     - Strategic rules from your comp plan
     - Process rules from your charter/procedures
     - Values rules from your community character/comp plan
2. Write 5,000-10,000 words total (not overly long; just enough to guide analysis)
3. Make rules testable (not vague)
   - Good: "All residential projects 50+ units must include 20% affordable housing"
   - Bad: "Projects should consider housing affordability"
4. Include examples from your jurisdiction
5. Have a colleague review for accuracy

**Deliverables by end of Week 1**:
- ✓ Zoning districts summary (key zones, simplified)
- ✓ Comp plan goals & policies (extracted key goals)
- ✓ Rules framework (Regulatory, Strategic, Process, Values rules for your city)

**Time check**: 7-10 hours. You're on track.

---

### Week 2: Knowledge Base Foundation

**Goal**: Build minimum knowledge base so agents have context to reason from

**Step 2.1: Current Demographic Snapshot** (2 hours)

1. Gather data:
   - Latest census data (population, age, income, race, housing)
   - Current housing market data (rents, prices, vacancy, affordability)
   - Employment data (unemployment, wages, job growth by sector)
2. Create file: `demographics/citywide_profile.md`
3. Use template from Knowledge Base Structure
4. Include:
   - Current population (total, density)
   - Age, income, race distribution
   - Housing (owner vs. renter, avg price/rent, affordability)
   - Employment (unemployment, median wage, growth)
5. Don't overthink; good-enough data is fine for now
   - Can use Census data even if 2-3 years old
   - Can use Zillow or CoStar for housing data
   - Can use Bureau of Labor Statistics for employment

**Step 2.2: Neighborhood Profiles** (3-4 hours)

1. Identify 3-5 key neighborhoods/districts
   - Probably: downtown, inner neighborhoods, outer neighborhoods, specialty areas
2. For each, create a profile using template from Knowledge Base Structure
   - Current demographics (population, income, housing, employment)
   - Trends (how is neighborhood changing?)
   - Opportunity analysis (what's strong? what's missing?)
   - Equity assessment (is neighborhood equitable?)
   - Planning implications (what should we do here?)
3. Spend 45-60 minutes per neighborhood
4. Use best available data (census, your own GIS data, market reports, local knowledge)
5. Profiles don't need to be perfect; they need to be useful for agents

**Step 2.3: Affordability & Equity Policy** (1-2 hours)

1. Locate and extract:
   - Your inclusionary zoning policy (if you have one)
   - Your equity goals (from comp plan, council resolutions, etc.)
   - Any affordability targets you've committed to
2. Create files:
   - `regulations/affordable_housing_policy.md` (extract key requirements)
   - `comp_plan/equity_framework.md` (how you define equity; what you're measuring)
3. Make explicit:
   - What % affordability is required? At what income levels? For how long?
   - What does "equity" mean in your jurisdiction?
   - What opportunity gaps are you trying to close?
   - How will you measure success?

**Step 2.4: Active Projects List** (1 hour)

1. List current projects in development review (at least 5, up to 15)
2. Create file: `projects/active_projects.md`
3. For each project include:
   - Name and location
   - Developer/applicant
   - What's proposed (units? Uses? Height? Affordability?)
   - Current status (preapp? In review? Pending decision?)
4. This becomes your testing ground for agents

**Step 2.5: Decision Log Template** (30 minutes)

1. Create file: `decisions/decision_log.md`
2. Use template from Knowledge Base Structure
3. Add 1-3 recent major decisions (approvals or denials)
4. For each, document:
   - What was requested
   - What was the planning analysis
   - Why did you approve/deny
   - What conditions were imposed
   - What outcomes are you tracking
5. This becomes your decision history; increasingly valuable over time

**Deliverables by end of Week 2**:
- ✓ Citywide demographic profile
- ✓ 3-5 neighborhood profiles
- ✓ Affordability and equity policy files
- ✓ Active projects list
- ✓ Decision log with 1-3 decisions

**Time check**: 7-10 hours. Still on track. Total Phase 1: ~15-20 hours.

---

## Phase 2: Skills & Testing (Weeks 3-4)

### Week 3: Set Up Cursor & First Skill

**Goal**: Get system running in Cursor; test with real projects

**Step 3.1: Set Up Cursor Environment** (1-2 hours)

1. If using Cursor IDE:
   - Create new project folder `urban-planner-os`
   - Organize subfolders matching knowledge base structure:
     ```
     urban-planner-os/
     ├── rules/
     │   ├── RULES_FOR_YOUR_CITY.md
     │   └── regulatory_summary.md
     ├── knowledge/
     │   ├── regulations/
     │   ├── comp_plan/
     │   ├── demographics/
     │   ├── projects/
     │   └── decisions/
     └── skills/
     ```
   - Copy all files from Phase 1 into appropriate folders
   - Create `.cursor/rules` or similar (check Cursor documentation for exact structure)

2. If using Claude web/API:
   - Create a master system prompt that includes:
     - All rules (rules/RULES_FOR_YOUR_CITY.md)
     - Knowledge base summary (demographics, comp plan, zoning)
     - Available skills (list of skills you can trigger)
   - Keep this prompt available for copy/paste

3. Test basic setup:
   - Try a simple query: "What are the zoning requirements for downtown?"
   - System should reference rules/zoning and answer accurately
   - If it does, setup works

**Step 3.2: Implement Development Review Skill** (2-3 hours)

1. Create file: `skills/DEVELOPMENT_REVIEW.md` or equivalent
2. In the file, write the full Development Review skill (from SKILLS_CATALOG above)
   - Include: Purpose, Trigger, Input, Process (steps), Output format
   - Make it detailed enough that an LLM can execute it
3. Test with one active project:
   - Copy/paste project description
   - Invoke: `@devreview [project description]`
   - System executes skill and generates Development Review report
4. Review output:
   - Does it capture the right issues?
   - Are recommendations sound?
   - Missing anything?
5. Iterate:
   - If output needs refinement, adjust skill description and try again
   - After 2-3 iterations, skill should be solid

**Deliverables by end of Week 3**:
- ✓ Cursor or API environment set up with rules and knowledge base
- ✓ Development Review skill working with test projects
- ✓ Understand the workflow (how to invoke skills, what output looks like)

**Time check**: 3-5 hours.

### Week 4: Agents & Operationalization

**Goal**: Get agents working; build routine for using the system

**Step 4.1: Set Up Development Review Agent** (2 hours)

1. Create file: `agents/DEVREVIEW_AGENT.md` (or similar)
2. From AGENTS_DEFINITIONS above, extract Development Review Agent definition
3. Set up "trigger":
   - How will this run? Option A: Manual (planner runs it on each project)
   - Option B: Scheduled (runs weekly on all new projects)
   - Option C: Integrated (developer portal auto-submits projects)
   - Start with manual (Option A) or weekly batch (Option B)
4. Set up routing:
   - Where does output go? Email? Shared drive? Project management system?
   - Who gets notified?
5. Document the workflow:
   - "When new project comes in, planner runs `@devreview [project]`"
   - "Agent generates report; staff reviews recommendations"
   - "Use as basis for planning staff analysis"

**Step 4.2: Build Equity Audit Routine** (1-2 hours)

1. Create file: `agents/EQUITY_AUDITOR_AGENT.md`
2. Set up monthly equity audit:
   - First Monday of month: Run equity audit on all approvals from previous month
   - Use Equity Impact Analysis skill (from SKILLS_CATALOG)
   - Generate report: "What % was affordable? Are we on track for comp plan goal?"
3. Document:
   - Who runs it? (Could be rotating planner, could be automatic)
   - What data is needed? (List of approvals from month)
   - What output? (Email report? Spreadsheet? Dashboard?)
   - What's the decision threshold? ("If <15% affordability, trigger policy review conversation")

**Step 4.3: Build Approval Tracking Spreadsheet** (1-2 hours)

1. Create simple tracker:
   - Columns: Project name, location, units approved, % affordable, affordability level, decision date
   - Rows: All approvals in past 12 months
2. This becomes data for equity audits, comp plan monitoring
3. You can automate later, but start manual
4. Use for: "Are we meeting comp plan goals? What are we building?"

**Step 4.4: Document Your Workflow** (1 hour)

1. Create file: `OPERATING_PROCEDURES.md`
2. Document how you'll use the system:
   - Development Review Skill: "When project arrives, run devreview"
   - Community Engagement Synthesis: "When comment period closes, run synthesis"
   - Equity Audit: "First Monday of month, run equity review"
   - Decision Log: "After approval/denial, document in decision log with rationale"
3. Make it simple enough that planning staff (not just you) can execute
4. Include templates, examples, step-by-step

**Step 4.5: Trial Run with One Real Project** (1-2 hours)

1. Pick one active project
2. Run through full workflow:
   - Run Development Review skill → read output
   - Consider community engagement (if past that stage)
   - Use output to inform planning analysis
   - Make planning recommendation
   - Document decision in decision log with rationale
3. Reflect:
   - Did the system help? How?
   - What was missing?
   - What can improve?
   - Would your team use this?

**Deliverables by end of Week 4**:
- ✓ Development Review Agent implemented and tested
- ✓ Equity Audit routine documented
- ✓ Approval tracking spreadsheet started
- ✓ Operating procedures documented
- ✓ One real project completed using system

**Time check**: 5-7 hours. Total Phase 2: ~10-15 hours.

---

## Phase 3: Expansion & Optimization (Month 2+)

After Phase 1 & 2, you have a working system. Now expand and refine.

### Skills to Add Next:
1. **Community Engagement Synthesis** (useful if you have major projects with lots of comment)
2. **Equity Impact Analysis** (formalize what equity audit does)
3. **Housing Impact Analysis** (if housing is major planning issue)
4. **Comprehensive Plan Monitor** (quarterly check: are we implementing comp plan?)
5. **Policy Review** (when you want to revisit a policy)

### Agents to Add Next:
1. **Equity Auditor** (once you have routine down)
2. **Community Engagement Coordinator** (if volume justifies)
3. **Comp Plan Monitor** (after you have 6 months of approvals)

### Knowledge Base to Deepen:
1. Add more neighborhood profiles (eventually all neighborhoods)
2. Collect precedent projects (local, national) with analysis
3. Build design examples library (good design, what to emulate)
4. Expand decision log (historical decisions; pattern analysis)
5. Add policy models (how other cities handle challenges you face)

### Metrics to Track:
1. **System use**: How often are planners using it? Which skills/agents most used?
2. **Time savings**: Is it actually saving time? By how much?
3. **Quality**: Is analysis better? Decisions more consistent?
4. **Equity**: Is it helping you achieve equity goals?
5. **Community satisfaction**: Are stakeholders perceiving improvements?

---

## Phase 4: Integration & Automation (Month 3+)

Once system is mature:

1. **Integrate with project management system**
   - Auto-submit projects to agents
   - Store reports in project folder
   - Track approvals/denials

2. **Create public-facing dashboard**
   - What have we approved recently?
   - How are we tracking on comp plan goals?
   - What % is affordable?
   - This increases accountability, transparency

3. **Build decision support for elected officials**
   - Summarize planning issues
   - Show tradeoffs
   - Help decision-makers understand planning implications

4. **Expand to regional planning**
   - If you're part of regional coordination, share knowledge base across jurisdictions
   - Learn from peers

---

## Troubleshooting & Common Issues

### "The system is giving bad recommendations"

**Solution**:
- Check rules: Are they clear? Accurate?
- Check knowledge base: Is information current? Complete?
- Check skill definition: Is process well-defined?
- Feedback loop: Iterate on prompt/rules until output improves

### "Planners aren't using it"

**Solution**:
- Make system easy to access (not buried in shared drive)
- Show results early (quick wins build adoption)
- Integrate with existing workflows (don't create new work)
- Get feedback: Why aren't they using it? What would make it useful?

### "System is missing context"

**Solution**:
- Expand knowledge base (what information does it need?)
- Create new skills (what analysis are you doing manually that could be systematized?)
- Refine rules (is there important guidance agents should follow?)

### "We don't have all the data the system suggests"

**Solution**:
- Start with good-enough data
- Improve iteratively (add new data sources as you go)
- Use proxies (example: if you don't have detailed income data, use census data)
- Document gaps: "We don't track X; would like to add in Year 2"

---

## Success Stories to Track

Document wins:

1. **Time saved**: "Used Development Review agent on [project]; took 30 min instead of 4 hours"
2. **Better decisions**: "Equity analysis flagged displacement risk; led to better community benefits"
3. **Consistency**: "Same zoning question now answered consistently vs. variably"
4. **Quality**: "Development Review output informed staff analysis; staff said recommendations were excellent"
5. **Accountability**: "Decision log shows clear rationale for approval; community can see we applied rules consistently"
6. **Learning**: "Pattern analysis showed we're not meeting affordability goal; led to policy discussion"

Share these wins with your team and elected officials. They justify continued investment.

---

## Conclusion: You're Building a Planning Institution

By the end of Phase 2 (about 4 weeks of work), you'll have:
- Clear rules documenting your jurisdiction's planning values
- Knowledge base grounding analysis in reality
- Working development review skill
- Equity audit routine
- Decision documentation practice

By end of Phase 3 (another 4-8 weeks), you'll have:
- Multiple skills handling common planning tasks
- Agents proactively monitoring and alerting
- Operating procedures ensuring consistency
- Evidence that system is helping

This is a planning institution: durable, consistent, accountable, learning-oriented.

Good luck. Feel free to adapt; make it your own.
