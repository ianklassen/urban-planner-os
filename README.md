# Urban Planner Operating System

Welcome! You're looking at a complete blueprint for building an AI-augmented operating system for urban planners.

This is inspired by the PM Operating System but adapted specifically for planning work.

---

## What Is This?

An operating system that helps planning teams work smarter by giving AI comprehensive context about your jurisdiction. Instead of starting fresh for each analysis, your OS provides:

- **Rules**: Your planning values, regulations, and goals (applied to every decision)
- **Skills**: Standardized planning tools (development review, equity analysis, feedback synthesis, etc.)
- **Agents**: Autonomous specialists that monitor projects, track comp plan implementation, audit equity
- **Knowledge Base**: Organized planning information (zoning, comp plan, demographics, decisions, precedents)

**Result**: Faster, more consistent, more equitable planning decisions grounded in data and values.

---

## Files in This Package

### 1. **URBAN_PLANNER_OS_GUIDE.md** - START HERE
Complete overview of the system:
- Philosophy and how it works
- Core components (Rules, Skills, Agents, Knowledge Base)
- Deep dives on agents with specific examples
- Integration with Cursor IDE
- Success metrics

*Read this first to understand the vision.*

---

### 2. **RULES_FRAMEWORK.md**
Your planning DNA: what you care about, what the law requires, how decisions should be made.

**Sections**:
- **Regulatory rules**: Zoning, design standards, affordability mandates (from your code)
- **Strategic rules**: Land use vision, housing goals, climate targets (from comp plan)
- **Process rules**: Public engagement, decision documentation, equity assessment
- **Values rules**: Community character, livability, environmental stewardship

**How to use**: Adapt the template to your jurisdiction. Extract from your zoning code, comp plan, and community values. This becomes the "system prompt" your OS uses.

*This is the first thing you'll build in Phase 1.*

---

### 3. **SKILLS_CATALOG.md**
Specialized planning tools that you or agents can invoke.

**Core skills included**:
- Development Review: Analyze proposals against zoning, design, comp plan
- Community Feedback Synthesis: Process 100s of comments into themes
- Impact Analysis: Housing, equity, fiscal impacts
- Policy Review & Drafting: Analyze and improve policies
- Demographic Profile: Population snapshots and trends
- Scenario Planning: Compare alternative futures

**How to use**:
- Each skill has: Purpose, Trigger, Input, Process (steps), Output format
- Customize skills for your jurisdiction
- Add new skills as you discover planning workflows that could be systematized

*Build 2-3 core skills in Phase 2; expand to 8-10 over time.*

---

### 4. **AGENTS_DEFINITIONS.md**
Autonomous specialists that execute planning work.

**Core agents included**:
- Development Review Agent: Screens incoming projects automatically
- Equity Auditor: Monthly audit of decisions against equity goals
- Community Engagement Coordinator: Monitors and synthesizes feedback
- Comprehensive Plan Monitor: Tracks implementation toward goals
- Trend Analysis: Alerts on market/policy shifts
- Design Review Specialist: Deep design analysis

**How to use**:
- Each agent has: Purpose, Trigger, Process, Output, Success metrics
- Start with Development Review Agent (most immediately useful)
- Build toward 4-6 core agents
- Customize agents for your specific planning challenges

*Start with 1-2 agents in Phase 2; expand in Phase 3.*

---

### 5. **KNOWLEDGE_BASE_STRUCTURE.md**
Organized repository of planning information.

**Structure**:
```
planning-knowledge/
├── regulations/ (zoning, design guidelines, policies)
├── comp_plan/ (goals, policies, equity framework, sustainability targets)
├── demographics/ (population, neighborhoods, trends, equity indicators)
├── projects/ (active projects, approvals, precedents, lessons learned)
├── decisions/ (decision log, approval trends, equity audits, comp plan tracking)
├── stakeholders/ (community organizations, contacts, engagement history)
└── best_practices/ (comparable city policies, design examples, tools)
```

**Content templates included**:
- Zoning district summary template
- Neighborhood profile template
- Comp plan goal summary template
- Decision log template

**How to use**:
- Populate with information from your zoning code, comp plan, demographics, recent approvals
- This is ongoing work (expanded over months/years)
- Start with essentials in Phase 1; expand in Phase 2+

*Phase 1: ~30% full (zoning, comp plan summary, current demographics). Phase 3+: expand to 80%+ coverage.*

---

### 6. **SETUP_AND_IMPLEMENTATION_GUIDE.md**
Step-by-step implementation across 4 phases.

**Phase 1 (Weeks 1-2): Foundation**
- Extract zoning code summary
- Extract comp plan goals
- Build rules framework
- Create demographic snapshot
- Add neighborhood profiles
- Document affordability and equity policies
- List active projects

**Phase 2 (Weeks 3-4): Skills & Testing**
- Set up Cursor or API environment
- Implement Development Review skill
- Test with active projects
- Set up Development Review Agent
- Build equity audit routine
- Document operating procedures

**Phase 3 (Month 2+): Expansion**
- Add more skills
- Build more agents
- Expand knowledge base
- Track metrics

**Phase 4 (Month 3+): Integration**
- Integrate with project management
- Create public dashboard
- Expand to regional coordination

*Follow this guide step-by-step. You don't need to understand everything upfront; build iteratively.*

---

## Quick Start (TL;DR)

1. **Read** URBAN_PLANNER_OS_GUIDE.md (15 min) to understand the vision
2. **Adapt** RULES_FRAMEWORK.md to your jurisdiction (3-4 hours)
3. **Start building** KNOWLEDGE_BASE following templates (2-3 hours)
4. **Follow** SETUP_AND_IMPLEMENTATION_GUIDE Week 1-2 (10-15 hours)
5. **Test** Development Review skill with a real project (2-3 hours)

**Total: ~30-40 hours to get a working system (spread over 3-4 weeks)**

---

## Customization

This is a **template**, not a product. You will customize:

- **Rules**: Adapt to your zoning code, comp plan, values
- **Skills**: Add domain-specific planning tools you need
- **Agents**: Build for your most pressing planning challenges
- **Knowledge Base**: Populate with your data, projects, decisions

The system gets smarter as you feed it more information.

---

## Who Is This For?

- **Planning directors/managers**: Want to improve planning quality and consistency
- **Planning departments**: Want to automate routine analysis and free up time for judgment
- **Urban designers**: Want better design review process
- **Equity officers**: Want to systematically audit decisions for equity impacts
- **Policy teams**: Want to model policy changes and track implementation
- **Community planners**: Want better engagement and feedback synthesis
- **Regional planners**: Want to coordinate planning across jurisdictions

---

## Technology

**Minimum**: Claude (via web) + your planning documents + text editor
**Better**: Cursor IDE + your planning documents
**Advanced**: Cursor + custom MCPs for your data + integration with GIS/project management

You don't need expensive infrastructure. Start with what you have.

---

## Success Metrics

Track these to know if the system is working:

1. **Speed**: Development review takes 30 min instead of 4 hours ✓
2. **Consistency**: Similar projects analyzed same way; rules applied uniformly ✓
3. **Quality**: Staff spends less time on research, more on judgment ✓
4. **Equity**: Can demonstrate decisions reducing/increasing opportunity gaps ✓
5. **Learning**: Decision log shows planning rationale; next comp plan informed by outcomes ✓
6. **Accountability**: Community can see why decisions were made ✓

---

## Next Steps

1. **Read URBAN_PLANNER_OS_GUIDE.md** (understand the vision)
2. **Start Phase 1** (follow SETUP_AND_IMPLEMENTATION_GUIDE)
3. **Build RULES_FRAMEWORK for your city** (extract from your code/comp plan)
4. **Populate initial KNOWLEDGE_BASE** (demographics, zoning, comp plan)
5. **Test Development Review skill** with active projects
6. **Iterate and expand**

---

## License

MIT - Use, modify, share freely. Consider sharing back improvements so other jurisdictions benefit.

---

## Questions?

This is a comprehensive guide, but not every detail. As you build:
- Start simple (don't try to do everything at once)
- Test with real work (don't just read; build)
- Iterate (first version won't be perfect; that's OK)
- Document as you go (your future self will thank you)
- Share learnings (other planners facing same challenges)

---

## Document Quick Reference

| Document | Purpose | Read When | Time |
|----------|---------|-----------|------|
| **URBAN_PLANNER_OS_GUIDE.md** | System overview & vision | First | 15-20 min |
| **RULES_FRAMEWORK.md** | How to codify your planning DNA | Building rules | 1-2 hours |
| **SKILLS_CATALOG.md** | Available planning tools | Implementing skills | 1-2 hours |
| **AGENTS_DEFINITIONS.md** | Autonomous specialists | Implementing agents | 1-2 hours |
| **KNOWLEDGE_BASE_STRUCTURE.md** | Information organization | Building knowledge base | 30-60 min |
| **SETUP_AND_IMPLEMENTATION_GUIDE.md** | Step-by-step implementation | Ready to build | 2-3 hours |
| **README.md** (this file) | Navigation guide | First or when confused | 10 min |

---

## Connect with Others Building Planning OS

As you build your Urban Planner OS:
- Share what you learn
- Share your rules/skills back to planning community
- Connect with other jurisdictions building similar systems
- The more of us do this, the better planning becomes

**Happy planning!**
