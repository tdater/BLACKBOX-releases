BLACKBOX is a local-first Android project intelligence workbench designed to connect the parts of troubleshooting and development that usually end up scattered across screenshots, notes, logs, conversations, and memory.

It brings evidence capture, structured testing, project history, comparisons, and AI-assisted reasoning into one continuous workflow:

Capture evidence → ask a question → plan a test → record the result → compare → resume or hand off.

The goal is not simply to put more tools inside one application. It is to eliminate the gaps between those tools so that every observation, change, and result contributes to a useful, persistent understanding of the project.

BLACKBOX is designed around Android devices as the initial target devices for portability. The broader goal is an adaptive experience that remains useful on compact screens, expanded displays, and other supported Android form factors.

───

Project Status

BLACKBOX is under active development.

This README describes the intended product, development priorities, and design principles. It is not a guarantee that every described feature is available in the current build.

Implemented features, verified device behavior, installation instructions, and known limitations should be documented as development progresses.

Initial Development Priority

Deliver a complete, useful offline investigation workflow before expanding into optional AI integrations, advanced hardware connections, or cross-device services.

The first release should let a user:

1. Create a project and investigation.
2. Capture or import evidence.
3. Define and run a test.
4. Record the actual result.
5. Compare recorded changes.
6. Generate an actionable project-resume summary.
7. Prepare a structured handoff for further development or troubleshooting.

───

The Problem

A typical technical project spans multiple disconnected tools:

• Screenshots show what happened.
• Logs contain diagnostic details.
• Notes explain what was changed.
• AI conversations contain possible explanations.
• Source-control history records code changes.
• Memory is expected to connect everything else.

That arrangement works until the project becomes complicated, gets interrupted, or develops several overlapping failures.

Questions become difficult to answer:

• Which build introduced this behavior?
• What exactly changed before the problem appeared?
• Did that adjustment help, or did the test conditions change?
• Have I already tried this?
• What was the last known-good configuration?
• What should I do next?
• How do I explain the problem to a coding agent without rebuilding the entire context?

BLACKBOX is designed to make those answers part of the project record instead of something the user has to reconstruct repeatedly.

───

The Core Idea

A project is more than a conversation or a folder of attachments.

BLACKBOX treats a project as a connected record of:

• Goals.
• Questions.
• Evidence.
• Environment and configuration.
• Changes.
• Tests.
• Outcomes.
• Remaining unknowns.
• Next actions.

The application should preserve the relationship between these records.

A screenshot can support an observation. An observation can motivate a hypothesis. A hypothesis can lead to a test. A test can produce a result. That result can update the next action.

The result is a project history that explains not only what happened, but why the next step makes sense.

───

Who It Is For

BLACKBOX is initially focused on hands-on technical work, including:

• Android application development.
• AI-assisted coding and debugging.
• Android head-unit and launcher development.
• Automotive telemetry and OBD-II projects.
• Bluetooth and connected-hardware troubleshooting.
• Electronics and accessory installation.
• Repeatable software and hardware testing.
• Personal technical projects that span multiple sessions.

The underlying workflow is intentionally broader than any one category. Future capabilities may extend it to physical repairs, home projects, component documentation, and controlled experiments.

───

Core Workflow

1. Create an Investigation

Start with a specific problem, objective, or question.

Example:

Live OBD values stop updating after the head-unit screen turns off.

Record what should happen, what currently happens, and any relevant starting conditions.

2. Capture Evidence

Attach the material needed to understand the issue:

• Text observations.
• Photos.
• Screenshots.
• Logs.
• Files.
• Recorded voice notes.
• Entered measurements.

Evidence should be easy to save immediately. Organizing or interpreting it can happen afterward.

Saving an observation must not depend on an AI response, an internet connection, or a lengthy form.

3. Record the Environment

Associate the investigation or test with its relevant context:

• Device and operating system.
• Application build.
• Connected hardware.
• Connection mode.
• Configuration values.
• Other conditions that may affect the result.

Historical tests should retain their original environment snapshots rather than change when the current configuration is edited.

4. Define a Test

Record:

• The question being tested.
• Prerequisites.
• Reproduction steps.
• Expected behavior.
• The variable being changed.
• Conditions intended to remain constant.

The purpose is to make a test repeatable, not merely record that someone “tried something.”

5. Record the Result

Capture the actual outcome and supporting evidence.

A test may be:

• Passed.
• Failed.
• Partially successful.
• Inconclusive.
• Not yet finished.

A passing test establishes that its stated expectation passed in that run. It does not automatically mean the entire project is fixed.

6. Compare and Continue

Compare runs, builds, or configurations to identify recorded differences.

Use the results to:

• Choose the next test.
• Update the investigation.
• Preserve a known-good reference.
• Create a regression check.
• Prepare a coding-agent handoff.
• Pause the project with a clear resume point.

───

Planned Core Features

Project and Investigation Management

Organize related work without losing the distinction between a broad project and a specific problem.

A single project may contain several investigations, each with its own evidence, tests, status, and next action.

Evidence Timeline

Maintain a chronological record of observations, attachments, changes, and results.

Evidence should remain linked to the investigation, session, or test that gives it meaning.

Original files and later interpretations should remain distinguishable.

Structured Test Runs

Create reusable test plans and record individual executions against specific builds and environment snapshots.

Document expected behavior separately from actual behavior.

“What Changed?” Comparisons

Compare explicit, recorded information between two runs or builds.

The comparison should identify:

• Known changes.
• Known matching values.
• Missing or unknown information.
• Different outcomes.
• Conditions that make a comparison unreliable.

Missing information must never be presented as proof that nothing changed.

Resume Capsules

Generate a concise, actionable snapshot of the project:

• Current objective.
• Last known-good state.
• Current failure.
• Last tested change.
• Next action.
• Relevant evidence.

A resume capsule should make it possible to return after an interruption without rereading an entire conversation.

It should also indicate when newer project activity has made the snapshot outdated.

Coding-Agent Handoffs

Prepare structured, editable Markdown for Claude Code or another development workflow.

A useful handoff includes:

• The problem and desired outcome.
• Environment and build details.
• Reproduction steps.
• Expected and observed behavior.
• Changes already tested.
• Results and regressions.
• Selected evidence.
• Remaining unknowns.
• The requested next action.

The user reviews the content before copying, saving, or sharing it.

Project Archives

Export and import a complete project record, including attachments and relationships.

An archive should preserve the investigation rather than reduce it to a summary that loses the supporting evidence.

Regression Memory

Turn confirmed past failures into reusable checks.

Before accepting a new build, revisit behaviors that have previously broken.

The goal is project-specific regression awareness, not a generic checklist disconnected from actual history.

───

Fold-Native Experience

BLACKBOX is intended to use a foldable device as a changing workspace rather than simply stretch a phone layout across a larger screen.

Compact Display

Prioritize:

• Quick evidence capture.
• Project selection.
• Resume summaries.
• Focused, single-task interactions.

Expanded Display

Provide space for related information side by side:

• Evidence and investigation details.
• Expected behavior and actual results.
• Two test runs.
• A project timeline and the next action.

Tabletop Posture

Where supported and practical, separate reference material from interaction controls.

For example:

• Upper area: evidence, instructions, or camera reference.
• Lower area: capture controls, test steps, and result entry.

Continuity

Changing posture, orientation, or window size should preserve the user's work.

The app should not lose drafts, duplicate tests, restart captures, or reset the active investigation merely because the device was folded or unfolded.

Exact behavior must be verified on supported devices.

───

Evidence Before Answers

BLACKBOX must distinguish between different kinds of knowledge.


Category
Meaning

Observed
Something recorded by the user, imported from an artifact, or directly measured.

Inferred
A possible explanation or interpretation.

Tested
An action was performed under recorded conditions.

Supported result
A specific outcome established by that test.

Unknown
Information that is missing, conflicting, or not yet established.



An AI suggestion must not silently become a confirmed fact.

A correlation must not be presented as proof of causation.

Conflicting observations should remain visible rather than be overwritten to produce a cleaner story.

“Unknown” is a valid and useful result.

───

Optional AI Assistance

AI is intended to accelerate the investigation workflow, not replace its evidence.

Potential AI-assisted tasks include:

• Summarizing selected records.
• Identifying missing information.
• Suggesting hypotheses.
• Proposing a test that distinguishes competing explanations.
• Drafting resume capsules.
• Preparing coding-agent handoffs.

The local project record should remain useful when AI is unavailable, disabled, or unconfigured.

AI Design Requirements

• Requests are deliberately initiated by the user.
• Context is limited to selected, permitted records.
• Generated interpretations remain distinguishable from original evidence.
• Referenced records must exist.
• Errors and unavailable features are reported honestly.
• No hidden cloud fallback.
• No automatic execution of model-proposed commands.
• No assumption that a consumer AI subscription includes third-party API access.

The initial implementation should favor one well-integrated provider over unnecessary multi-model complexity.

───

Privacy and Local-First Design

The core application is intended to work without an account or cloud service.

Local-Only Projects

A local-only project must be excluded from external AI requests.

This restriction belongs in the application's data and request-handling logic, not only in the interface.

Deliberate Sharing

The user should review what is included before exporting or sharing a handoff.

Private attachments, sensitive logs, and credentials must not be included automatically.

Credential Protection

API credentials must not be hardcoded, committed to source control, included in project archives, or written into logs.

No Silent Monitoring

BLACKBOX is not intended to continuously watch the device or secretly collect activity from other applications.

Any future screen-capture or connected-device feature must use supported access methods and explicit user action.

Honest Security Boundaries

A local-only policy controls application uploads. It is not a claim of complete device security or forensic protection.

Work-related information must still be handled according to the user's organizational policies.

───

Example Investigation

Problem

OBD readings stop updating after the screen turns off.

Initial Evidence

• The adapter remains connected.
• The displayed RPM value freezes.
• An imported log records the relevant session.
• The application build and adapter details are recorded.

Test

Repeat the screen-off sequence while changing one selected configuration value.

Recorded Outcome

The result is attached to that test run, along with the actual environment and supporting evidence.

Comparison

BLACKBOX identifies the recorded configuration difference and compares the outcomes.

It does not automatically declare that the changed setting caused the improvement.

Handoff

The user generates a fix request containing the reproduction steps, tested changes, observed results, and selected logs.

A coding agent receives a focused technical brief instead of a vague description and an unrelated pile of screenshots.

───

Product Roadmap

Phase 1 — Offline Investigation Workbench

• Projects and investigations.
• Evidence capture and import.
• Test plans and results.
• Environment and build references.
• Timeline.
• Deterministic comparisons.
• Resume capsules.
• Editable handoffs.
• Project archive export and import.
• Adaptive layouts.

Phase 2 — Development Intelligence

• Optional AI integration.
• Reviewed context selection.
• Evidence-linked interpretations.
• Regression checklists.
• Improved search and filtering.
• Structured event imports from applications the user owns.

Phase 3 — Physical Project Workbench

• Component labels on saved photos.
• Installation history.
• Diagrams and reference material.
• Parts and connection records.
• Instrument readings.
• Before-and-after comparisons.

Phase 4 — Controlled Experiments and Continuity

• Repeatable experiment templates.
• More rigorous measurement comparisons.
• Richer cross-device resume workflows.
• Optional authenticated companion integrations.
• Additional AI roles where they demonstrate practical value.

Roadmap items describe direction, not guaranteed release commitments.

───

Technical Direction

The preferred implementation direction is:

• Kotlin.
• Jetpack Compose.
• Adaptive layouts and fold-aware behavior.
• CameraX where appropriate.
• Structured local persistence.
• Durable attachment storage.
• Testable comparison and export logic.
• Optional AI behind a provider interface.

The architecture should remain understandable and maintainable.

Core investigation logic must not depend on a specific AI provider or UI screen.

Exact dependencies, supported Android versions, build commands, and device compatibility should be documented from the actual implementation.

───

Reliability Goals

A useful build should demonstrate that:

• Core workflows work offline.
• Saved records survive application relaunch.
• Imported attachments remain available.
• Layout changes do not discard active work.
• Comparisons distinguish unknown values from unchanged values.
• Generated content references real project records.
• Project archives preserve attachments and relationships.
• Permission denial does not break unrelated features.
• Local-only projects cannot reach an external AI provider.
• Failed AI requests do not produce fabricated results.

───

What BLACKBOX Is Not

BLACKBOX is not intended to be:

• Another generic chatbot.
• An always-recording surveillance tool.
• A universal controller for every installed app.
• A replacement for an IDE or source-control system.
• A guarantee of diagnostic accuracy.
• A substitute for appropriate physical measurements or safety procedures.
• A collection of disconnected features behind a dashboard.

Its value comes from preserving the relationship between a problem, its evidence, the tests performed, and the next useful action.

───

Build and Installation

Build requirements, installation steps, and APK availability will be added as the implementation is established.

Do not assume that a described capability is implemented or device-verified unless it is identified as such in the current development documentation.

───

Project Philosophy

A chatbot remembers a conversation.

A notebook stores information.

A testing tool records results.

BLACKBOX is designed to connect those functions into a persistent working context:

This is my project.
This is what I know.
This is what changed.
This is what happened.
This is what I should do next.

The goal is not more features or more AI.

The goal is less lost context, better evidence, cleaner experiments, and a more useful next action. 


