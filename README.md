# Bowtie Builder Pro - DSBA 5122

## Team & Approach
- Team #: Group 2
- Members: Bobby Deasy, Sreedhar Lakamsani, Davis Martin, Will Moore, Chris Weihrauch
- Chosen Approach: Approach 1 – Build
    - Deterministic ELK-backed React + TypeScript experience with guided Builder / Story modes, inline editing, GSAP-driven preattentive cues, export-to-PNG, and strong accessibility defaults.

## Risk Story Summary
Fleet operations normally run smoothly with trained drivers, well-maintained trucks, and multiple safety barriers in place. However, several threats: impaired driving, distraction, sensor drift, mechanical faults, bad weather, and poor visibility, can erode these defenses, especially when latent issues like deferred maintenance or missed alerts accumulate. In this scenario, a missed weather warning, an uncalibrated ADAS system, and an unresolved ABS fault combined during a storm to create a near-loss-of-control event on black ice. Mitigation barriers such as radar alerts and defensive driving ultimately prevented a crash, avoiding consequences like collisions, injuries, or rollovers. The incident reveals how layered barriers can fail or hold, depending on how well the system manages risks and addresses hidden weaknesses.

## Run / View
1. `npm install`
2. `npm run dev`
3. `npm run build`
- Preview the production bundle locally with `npm run preview` once the build succeeds.
- Run unit tests via `npm run test:run` (single pass, no watch).
- Hosted prototype: https://bowtie-project.vercel.app (Story and Builder modes available with keyboard narration support).
- Scenario content lives in `src/domain/scenarios/*`; swap these files to showcase alternative risk stories.
- Visual / design token reference: `docs/design-tokens-reference.html` for color, motion, and typography mapping.

## Highlights
- Deterministic ELK-powered layout keeps the hazard centered above the knot while maintaining left/right symmetry for prevention and mitigation branches.
- Default collapsed bowtie surfaces only threats, escalation factors, hazard, top event, and consequences until a user clicks or runs the story, simplifying workshop onboarding.
- Story mode animates focus, reveals the correct path, supports arrow-key narration, and records the barrier state for playback.
- Escalation factors remain visible as yellow-striped pills with legend support, and the inspector allows inline editing of labels, tags, and risk metadata.
- Multi-select filtering chips, PNG export, keyboard shortcuts, and reduced-motion/focus-visible defaults keep the tool accessible for mixed-experience teams.

## Preattentive Attributes
- **Color** separates roles (hazard amber, threat sand, prevention green, mitigation blue, consequence red) and timeline stages (normal gray through recovery green).
- **Size and shape** emphasize hierarchy: circular top event node, larger banner hazard/top event cards, standard rectangles elsewhere.
- **Opacity and glow** direct story focus by dimming inactive nodes and applying role-colored highlights to the active branch.
- **Motion** uses short GSAP-driven pulses that respect `prefers-reduced-motion` to indicate narration steps without overwhelming participants.
- **Position** keeps prevention left, mitigation right, and escalation factors tucked along their respective sides so each pattern maps to a single meaning.

## Acknowledgement
- This is a student project developed for DSBA 5122 in collaboration with Todus Advisors.
- Built with [React Flow](https://reactflow.dev/) and [ELK.js](https://eclipse.dev/elk/)
- Inspired by bowtie methodology from risk management literature
- Developed as part of M.S. Data Science coursework