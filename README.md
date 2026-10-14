NyayaVerse — Citizen-Centric Justice Workflow Prototype
> **PromptWars prototype | Demo mode | Human-reviewed workflow support**
Live demo: https://nyayaverse-promptwars.floot.app  
Public judgment used as a reference example: State of Maharashtra v. Dr. Praful B. Desai (Supreme Court of India, 1 April 2003)
NyayaVerse is a prototype for making case handoffs and source-to-claim review more traceable. It provides a structured workspace to record sources, enter claims that need checking, flag items for human review, manage follow-up tasks, and review an activity trail.
Important: This is a demonstration workflow, not an official court system, legal advice, an evidence-authentication service, or a production case-management platform. It does not connect to court databases or verify the truth of a claim. Its current claim checks are deterministic demo rules (including keyword/source and date checks), not a live AI model.
---
Problem statement
Case-related work can be difficult to hand over clearly when a summary contains claims but the receiving person cannot quickly see the source behind each claim, which details remain unverified, or what follow-up is still open. Information may be spread across documents, notes, evidence registers, and separate task lists. A handoff can therefore lose context and make human review harder.
Problem statement: How might we help justice-sector stakeholders trace report claims back to recorded source material, make missing or uncertain information visible, and hand over outstanding work with clearer accountability—without replacing professional judgment?
Gaps this prototype targets
These are workflow gaps the prototype is designed to explore, not claims that every existing court platform lacks these capabilities:
Claim-to-source visibility: a claim and its supporting source details should be reviewable together.
Uncertainty visibility: missing source details or possible date/value conflicts should prompt review instead of being presented as verified facts.
Handoff continuity: open follow-ups should be visible to the next person handling the case.
Action accountability: a checklist and activity history can help users see what has been recorded or marked complete.
Plain-language case workspace: a structured view can help non-technical users navigate records and outstanding steps.
Transparent automation: automated checks should explain their limited basis and leave decisions to a responsible human.
The prototype does not establish that a claim is true, authenticate evidence, determine guilt or innocence, calculate legal outcomes, or guarantee a legally valid handoff.
Reference case used in the demo
The app's sample workspace references the public Supreme Court judgment:
Case: State of Maharashtra v. Dr. Praful B. Desai
Court: Supreme Court of India
Decision date: 1 April 2003
Public judgment: https://indiankanoon.org/doc/560467/
The judgment considered whether witness evidence in a criminal trial could be recorded through video conferencing, and the Court permitted video conferencing subject to applicable conditions and safeguards.
The public judgment is used as an educational reference for the demo workspace. The evidence-register entry, claims, tasks, activity events, and checklist are demo-created workflow records, not official court records or a complete reproduction of the judgment. Please consult the linked judgment itself for the authoritative text.
Features
Case workspace with a sample public-judgment reference
Evidence/source register for recording source details
User-entered claims and deterministic demo checks
Review cues for missing source details and possible conflicts
Follow-up/action checklist
Activity history for workflow events
Case navigation and workspace summaries
Responsive layout rules for mobile and larger screens
Clear demo-mode and human-review disclaimers
Browser-local demo persistence (see limitations below)
Stakeholders
Potential users and reviewers include:
Investigators / evidence reviewers: record source references and identify information needing follow-up.
Police or investigation teams: hand over case-related notes and outstanding actions with more context.
Lawyers and legal researchers: review which claims have recorded source references and which require checking.
Court and administrative staff: understand the status of workflow tasks (not to replace official court systems).
Victims, accused persons, and their representatives: potential beneficiaries of clearer, accountable processes; the prototype is not a public case portal.
Judges and judicial officers: any use would require formal review and safeguards; this prototype does not make judicial decisions.
NGOs / legal-aid and support organisations: potential workflow stakeholders where appropriate and authorised.
These are intended stakeholder groups, not confirmed users or institutional partners.
How to use the demo
Open the live demo.
Review the case workspace and its demo-mode disclaimer.
Open Evidence register to inspect the recorded source details. In an authorised test, add a source record and include its title/reference, relevant date, and description.
Open Claim verification and enter a claim from material you are permitted to use. Add the corresponding source details where available.
Run the demo check and read its explanation. Independently compare the claim with the original source; do not treat a keyword match as proof.
Open Action checklist, review outstanding follow-ups, and mark a task complete only when appropriate for the demonstration.
Open Activity history to review the recorded workflow events.
Refresh and reopen the workspace to test browser-local persistence on the same browser/device.
Use only public or synthetic material in demonstrations. Do not enter confidential, sensitive, or real case data.
Technical approach
Frontend: TypeScript / React-style page and component structure generated and hosted through Floot.
Styling: CSS modules and shared CSS.
Demo verification: deterministic rules; no external AI model call is made.
Persistence: browser `localStorage` for this demo; data is local to the browser/device and is not a shared, central case database.
Tests: project typecheck and selected automated helper specs were run during development.
The complete runnable source and dependency versions should be reviewed in the project export before building or deploying outside Floot. Floot's generated component library and runtime may be required; this README alone is not a standalone deployment recipe.
Validation status
Last recorded development checks:
Typecheck: passed
Selected automated tests: 4 spec files passed, 0 failed
Published site HTTP response: 200 in a prior check
Google PageSpeed mobile snapshot supplied during testing: Performance 97, Accessibility 89, Best Practices 100, SEO 90
The PageSpeed scores are a point-in-time result and may vary. The accessibility report flagged insufficient foreground/background contrast and a missing root HTML `lang` attribute. Contrast CSS and `lang="en"` handling were updated afterward, and typecheck/tests passed; the updated accessibility score and a full cross-device end-to-end browser test have not yet been independently confirmed. Do not represent the app as fully WCAG-compliant based on these checks alone.
Limitations and responsible use
Not an official court service and not integrated with eCourts, police, or court databases.
Not legal advice; not a substitute for lawyers, investigators, judges, or other authorised professionals.
Demo checks are not a factual truth detector, legal analysis engine, or evidence-authentication system.
A “supported” result only indicates a match under limited demo rules; it does not prove that the claim is true.
Local browser storage is not suitable for sensitive case information or multi-user collaboration.
No production-grade authentication, access control, audit integrity, encryption, retention policy, or institutional security review is claimed.
Do not enter real confidential case data. Verify all material against original sources and follow applicable law and institutional policies.
Reproducibility / setup
This project was built and published through Floot. To reproduce or self-host it:
Export/download the complete project source from the project owner's Floot workspace.
Inspect the exported project instructions, dependency manifest, and build scripts.
Install the dependencies using the package manager and lockfile supplied with the export.
Run the project's documented development command.
Run typecheck and the available tests.
Verify the responsive layout and keyboard/screen-reader behaviour at multiple viewport sizes.
Configure an appropriate secure backend and access controls before considering any use with real case information.
Exact commands are intentionally not guessed here because the exported project manifest and lockfile need to be checked first.
Suggested evaluation checklist
[ ] Create and switch between cases
[ ] Add/edit a source record and verify it persists after refresh
[ ] Run a claim check and inspect the explanation
[ ] Test missing-source and possible-conflict cases
[ ] Complete a follow-up and inspect activity history
[ ] Check keyboard navigation and visible focus
[ ] Check colour contrast, labels, and screen-reader names
[ ] Test phone, tablet, laptop, and desktop layouts
[ ] Re-run PageSpeed/Lighthouse after any code changes
[ ] Confirm no confidential data is used in the demo
Credits and links
Live prototype: https://nyayaverse-promptwars.floot.app
Reference judgment: https://indiankanoon.org/doc/560467/
Hosting / builder: Floot
Challenge context: PromptWars x Creative Community VVITU — AI for Better Living & Smarter Communities
---
Built as a student innovation prototype to explore more traceable, human-reviewed justice workflows.
