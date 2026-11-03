# AGENTS.md: Project Proposal (Design, Build, Ship, MPCS 51238)

**Due:** Tuesday, November 3, 2026, 5:30 PM (submitted in Google Classroom)
**Deliverable:** One static HTML page (no framework, no build step), hosted on Vercel from the student's own account, plus its GitHub repo.

## Ground rules for the agent

- **This is the student's proposal, not the agent's.** A one-shot submission is graded incomplete. The agent asks, researches, challenges, and drafts from what the student says. It does not invent ideas, user quotes, or decisions.
- Ask questions **one at a time**. Push back on vague answers.
- **Don't write proposal content until the interview (Step 3) is finished.**
- Never make up user-interview content. Quotes come from the student's notes, in the interviewees' own words.
- Use free tiers only. Don't add payment methods. Set usage limits and spending alerts.
- Keep the page simple: someone should understand the idea in a minute. Cut filler.

## Who does what

| Step | Student does / decides | Agent does |
|---|---|---|
| 1. Choose what to build | Brings candidate ideas and picks one | Asks questions about each idea, one at a time, to find which one the student is most excited about |
| 2. Choose focus | Picks Holistic Journey, Design, Systems, or AI, and says why | Explains what going deep on each focus would look like for this idea, then recommends one |
| 3. Agent interview | Answers questions about the problem, the user, the smallest v1, what's out, and how they'll know it works | Interviews the student and challenges vague answers. Searches the web for APIs, similar products, and data sources |
| 4. Talk to users | **Interviews 3 or more real people** (in person or on a call) and writes down what they said, in their words | Writes 5 questions about how people handle the problem today, without pitching the idea. Later organizes the notes the student provides |
| 5. Scope the roadmap | Approves the weekly plan and decides what's in v1, what waits for v2, and what's out | Proposes a breakdown, challenges the scope, and names the riskiest part to build first |
| 6. Write and publish | **Reads every line** and edits it into their own words. Logs into Vercel and GitHub (their accounts) | Drafts `index.html` from the student's answers, sets up git, and runs the deploy commands once the student is logged in |
| Final check | Answers quiz questions | Quizzes the student on the proposal: who it's for, what's in v1, and how it works |
| Submit | Submits the Vercel URL and GitHub URL in Google Classroom | (nothing) |

## Plan / progress

- [x] **Step 1: Ideas.** Student lists ideas. Agent asks about each one. Student picks one.
- [x] **Step 2: Focus.** Student picks a focus and gives the reason.
- [ ] **Step 3: Interview.** Cover the problem, the user, the smallest v1, what's out, success criteria, and research (APIs, competitors, data). *Done: user, v1, success test (the student is keeping only the v1 test), building research. Remaining: what's out, the v2 scope.*
- [ ] **Step 4: User interviews.** Agent writes the questions. Student runs 3 or more interviews and pastes notes. *(Schedule these early, since the deadline is tomorrow.)*
- [x] **Step 5: Roadmap.** Dates: Nov 10 start, Nov 17 v1 (works end to end), Nov 24 no class, Dec 1 v2 at the fair.
- [x] **Step 6: Tech stack.** Stack, MCP servers, and CLIs, with the reason each fits the idea. Cover free-tier limits and spending alerts for each service.
- [ ] **Step 7: Draft page.** Write `index.html` (single static file). The student reviews and rewrites it.
- [x] **Step 8: Publish.** Create the GitHub repo, then deploy to Vercel from the student's account (not an anonymous deploy, which expires).
- [ ] **Step 9: Quiz and submit.**

## Page must cover (assessment checklist)

- [ ] One-line description: the problem and the user
- [ ] Users: who they are and what they told you
- [ ] Focus (Holistic / Design / Systems / AI) and why
- [ ] Roadmap: each week, what's in v1 (Nov 17), and what's in v2 (Dec 1)
- [ ] Tech stack, MCP servers, and CLIs, and why they fit
- [ ] Static HTML on Vercel, with a GitHub repo

## Decisions log

_(The agent records the student's decisions here as they're made.)_

- **Premise: destruction with a story.** The player is upset with the University of Chicago and wrecks a campus building. They start inside on an upper floor, break their way down floor by floor, get out, then start on the exterior walls (and maybe more buildings). Ideally it's the building where the project fair is held. It's a loose take on the building, not an exact replica. *Open: materials (see Notes).*
- **Tone: comic.** The student's reason: so administrators don't mistake it for a serious suggestion of violence. That means an empty building (no people), absurd weapons, anger played for laughs, and no official logos.
- **User: MPCS students during finals week.** The student can easily reach classmates for interviews. Questions are in `interviews.md`.
- **v1 gameplay (draft):** the 3rd floor only, with two weapons (not yet chosen). Destroy glass windows, knock over chairs, crack tables, and maybe kick down doors. 
- **v1 weapons:** a red stapler to start (an Office Space reference), and a fire extinguisher as the upgrade.
- **Scoring:** a prop has no fixed point value. *How* it's destroyed changes its score. This also fixes the destruction leaderboard's ceiling. Scoring factors: **impact force and direction**, and **total separation of parts** (how completely the prop is broken apart). "Direction" means the **angle of the hit**. A head-on hit transfers more force than a glancing one: only the part of the force pushing straight into the surface (the normal component of the impulse) counts. That force decides how much breaks off, so the angle feeds into separation through the physics. It isn't a separate bonus.
- **How a run ends (v1):** the player breaks through the door to the main stairwell. That stops the timer and leads down to the 2nd floor. The fastest-time leaderboard measures time to break that door. Destruction points are everything smashed before then. This means breakable doors are required in v1.
- **Accounts: two leaderboards.** One for fastest time and one for most destruction points. Signing in puts your runs on them.
- **Focus: Systems.** The student's reason: "I want to explore web based games and physics destruction."
- **v2 (Dec 1, fair):** more floors (2nd, 1st, lower level, connected by the stairwell) and the finale (floors and walls become breakable, and the building collapses).
- **Finale is partly faked (the student's design):** outside, the player can only attack the building's front facade. Once enough of it is destroyed, the collapse begins. Dust rises as a smokescreen while the game switches to a preset rubble scene of the destroyed building. Breaking floors and walls indoors is no longer needed, and the facade is the only structural destruction.
- **Out (confirmed by the student):** more weapons, live leaderboards on a fair screen, server-side score checks, and general polish (sound, particles, screen shake). Exception: the finale's dust cloud is in, because the scene switch depends on it.
- **Repo:** https://github.com/carnowell-uchicago/dbs-p_final_proposal (public). **Live:** https://dbs-pfinalproposal.vercel.app/ (from the student's Vercel account, auto-deploys on push). The course PDF is gitignored.
- **Title (WIP):** "MPCS Wars: The Student Strikes Back"
- **One-liner (final, approved by the student):** "MPCS students need a way to blow off steam during finals week, so this game lets them enjoy a humorous imagining of destroying Crerar Library after hours, when there are no witnesses." The student kept "no witnesses" on purpose as a joke.
- **Tech stack:** Unity 6 (Personal) web build; Vercel (Hobby) for static hosting, with a `vercel.json` for the compressed build files; **Supabase** (free) for auth and for Postgres tables of runs and leaderboards. Sign-up happens on the web page around the game, and the session is passed into Unity. Code is on GitHub. Tools: Unity CLI and MCP, Supabase MCP and CLI, Vercel CLI, git, and Playwright MCP for testing the deployed build. Free-tier note: Supabase pauses free projects after about a week of inactivity, so keep it active or wake it up before the fair.
- **Roadmap (the student approved it "for now"; they'll work through Thanksgiving):**
  - **Nov 10–17 (v1).** Day 1: an empty Unity web build deployed to Vercel. Days 1–3: a rough 3rd floor with breakable windows, chairs, tables and the stairwell door, plus physics-based scoring. Day 3: the stapler and fire extinguisher, with the door requiring the extinguisher. Day 4: sign-up and the two leaderboards. Day 5: classmate playtest.
  - **Nov 17–24.** The 2nd floor, 1st floor and lower level, reusing props. Decide whether scores are per floor or for the whole run. Fix playtest issues.
  - **Nov 24–Dec 1.** The front facade of breakable limestone blocks, the collapse trigger, the dust cloud, the rubble scene, and a full-run playtest. Then v2 at the fair.
- **Success criteria:** the v1 test only. The student declined a Dec 1 engagement target.
- **v1 success test:** a classmate can sign up, beat the 3rd floor, and their score is still on the leaderboard afterward.
- **Structural destruction comes last.** Floors and walls stay intact until the finale, because breaking them is what can bring the whole building down. Before the finale, everything breakable is furniture and fixtures. The player moves between floors through the main stairwell, reached by breaking its door.
- **Building: John Crerar Library.** The fair is in its basement (lower level).
- **Engine: Unity, exported to the web.** Chosen by the student. Their reasons: they've built Unity projects with Claude Code before, they have time, and load speed doesn't matter to them. Things that favor Unity for this game: PhysX breakable joints (`FixedJoint.breakForce`), and better polish tools (particles, audio, camera, post-processing). The agent builds through the Unity CLI and MCP. Risks to manage: garbage-collection stutter in web builds (reuse debris objects instead of creating new ones), the cost of many joints, and the server configuration Vercel needs to serve the build's compressed files.

## Notes

### Candidate ideas (Step 1)
1. **Destructible-town game.** A small town where every plank of every structure can be knocked off. The player moves through the town and finds weapons that get more destructive as they go. Rough idea: bat, then sledgehammer, then a launcher like a pitching machine, then an RPG. The weapon list isn't fixed.

### Design implications of the campus premise
- Breaking down through floors is the core mechanic: the floor is both the obstacle and the way forward. Each floor works as a level.
- Materials change from wooden planks to interior furniture and fixtures (ceiling tiles, drywall, desks, chairs, glass, whiteboards) and exterior stone or brick blocks. Floors break as slabs or tiles.
- Crerar facts (from research): 4 levels, meaning 3 above ground plus a lower level. Opened 1984, designed by Stubbins Associates, in a late-Brutalist style. The whole facade is limestone, with vertical window patterns that echo the Gothic campus. The building was later renovated for CS (Payette). The lower level has compact shelving, a computer cluster and classroom, and the Kathleen A. Zar Room (Weston Game Lab). Floor plans are mentioned on CS Discuss (discuss.cs.uchicago.edu/t/crerar-building-floor-plans/916).
- Level idea: 3rd floor, then 2nd, then 1st, then the lower level. The finale could be smashing into the basement where the fair is happening, or going outside to break the limestone walls. The student decides.
- Tone risk: "angry at the university" plus an RPG, shown at a university event. Keep it comic: no people, absurd weapons, stress-relief framing. Avoid official logos.
