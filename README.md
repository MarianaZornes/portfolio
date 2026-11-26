# Mariana Zornes — Project Portfolio

Media and artifacts from projects on my resume. Code for school projects stays
private per Georgia Tech's academic policies — this repo shows the work itself:
gameplay, art, and results.

---

## 🧵 LOOM — Runtime Rule Synthesis for Text Games
**The full project is public → [MarianaZornes/LOOM](https://github.com/MarianaZornes/LOOM)**

A 9,000-line Python roguelike where an LLM writes new game rules at runtime and a
deterministic validator decides which ones hold. 46 tests, 7-experiment reproducible
harness; validator ablation: 0% of attacks land with validation on vs. 100% of
worlds broken with it off.

![Forging a new verb at runtime](loom/forge.png)
*`hum` didn't exist until the player typed it — a rule is proposed, validated clause-by-clause
against the live world, installed, and immediately re-binds to objects in other rooms.*

---

## 🤖 Killer Robot — 3D Unity Action Game (5-person team)
Single-level 3D action game: escape a factory of hostile robots. Built for Georgia
Tech's Video Game Design course. My contributions: modeled, rigged, and animated the
RoboDog enemy (one of two core enemy types), authored the explosion VFX and
destructible barrel assets, and built the ExplodingBarrel hazard system in C# —
radius-based damage with distance falloff, rigidbody knockback, and chain detonation.

| | |
|---|---|
| ![Title](killer-robot/title.jpg) | ![Rules](killer-robot/rules.jpg) |
| ![Obstacles](killer-robot/obstacles.jpg) | ![Enemies](killer-robot/enemies.jpg) |
| ![Boss fight](killer-robot/boss-fight.jpg) | ![Victory](killer-robot/victory.jpg) |

**Gameplay clips:**

![Laser obstacles](killer-robot/lasers.gif)
![Boss fight](killer-robot/boss.gif)

![Exploding barrels](killer-robot/barrels.gif)
*The final-level barrel field — my ExplodingBarrel hazard system (radius damage with falloff, knockback, chain detonation).*

*(Captured from the team's playthrough video; team code repo is private.)*

---

## 🐕 RoboDog — 3D Character Art
The enemy character I modeled, rigged, and animated for Killer Robot, in Blender.

![Walk cycle](robodog/walk-cycle.gif)

![Rig](robodog/rig.jpg)
*Armature and IK setup — the mesh, rig, and animation clips shipped in the final enemy prefabs.*

Source file: [`robodog/RoboDog.blend`](robodog/RoboDog.blend)

---

## 🏔️ Procedural Terrain Generation — Game AI coursework
Hierarchical PCG node graph generating three visually distinct biomes — mountain,
desert dunes, canyon — from a single Perlin noise field, with trapezoid region
partitioning and smooth crossfade transitions. Jagged multi-octave peaks with rock
spires; rolling dunes with ripple detail and crest sharpening; plateau canyons carved
with subtractive cuts. Scored 100/100. *(Code private.)*

| | |
|---|---|
| ![Mountain biome](terrain/mountain.jpg) | ![Desert dunes biome](terrain/desert.jpg) |
| ![Canyon biome](terrain/canyon.jpg) | ![Biome transitions overview](terrain/overview.jpg) |

*Mountain · desert dunes · canyon · crossfade transitions between all three.*

---

## 🎨 Computer Graphics — Software Renderers (Fall 2026, in progress)
Renderers written from scratch in Java, no graphics APIs: a recursive ray tracer
with reflection, refraction, soft shadows, depth of field, motion blur, and
triangle-mesh rendering; a rasterization pipeline with flat and smooth shading;
and implicit-surface modeling (blobby surfaces, sweeps, twists). *(Code private.)*

| | |
|---|---|
| ![Refractive bunny in a mirror](graphics/raytrace-glass-bunny.jpg) | ![Mesh + reflective spheres](graphics/raytrace-bunny-spheres.jpg) |
| ![Depth of field](graphics/raytrace-depth-of-field.jpg) | ![Textured + reflective scene](graphics/raytrace-gt-logo.jpg) |
| ![Smooth-shaded Stanford bunny](graphics/shaded-bunny.jpg) | ![Implicit-surface linked tori](graphics/implicit-linked-tori.jpg) |

*Ray-traced glass bunny and mirror · reflective spheres · depth of field · texture
mapping · smooth shading · implicit surfaces.*

---

## 🧠 Knowledge-Based AI — Agents (Fall 2026, in progress)
A semester of classical AI agents in Python, no ML libraries: an **ARC-AGI agent**
using generate-and-test over extract → reorient → recolor rule pipelines — every
candidate rule must reproduce all training pairs exactly before it may predict —
solving **79 of the 400 public ARC-AGI training tasks** (78 on the first prediction).
Plus smaller agents: a semantic-network state-space solver, a means-ends block-world
planner, a sentence-reading QA agent, case-based classification/diagnosis agents,
and minimax game players. *(Code private.)*

![ARC agent solving public tasks](kbai/arc-agent.png)
*Three solved tasks — symmetry repair, mirror tiling, and learned color mapping —
run on the public ARC-AGI training set.*

---

## 🧪 HCI / UX Research — Household Calendar Redesign (Fall 2026, in progress)
A full design-lifecycle research project: needfinding survey (n = 24), heuristic
evaluation of Google Calendar's event flow, three low-fidelity prototypes tested
with 16 interviewees, and a medium-fidelity combined design evaluated with paired
t-tests against the originals. The problem: shared calendars remember *when*, but
not *who* or *what's needed* — so the redesign gives every event an owner, an
acknowledgement state, and a bring list that surfaces in the reminder.

![Creating the event](hci/prototype-create.jpg)
![The week view with handoff states](hci/prototype-week.jpg)
![Handoff and reminder moments](hci/prototype-moments.jpg)

*Final medium-fidelity prototype — owner field and bring list at creation; assigned /
seen / accepted states visible in the week grid; the two notification moments that matter.*

---

## 📈 Machine Learning — Optimization & Uncertainty Study
*"Optimization and Uncertainty on Forest Cover Type: Dissecting Training
Interventions on a Fixed PyTorch Backbone"* — CS 7641, scored 101/100 after update.
Four pre-registered hypotheses tested on a fixed PyTorch MLP (Covertype, 7-class,
heavily imbalanced): randomized optimization (RHC / SA / GA) of the final layer,
seven Adam-family optimizer ablations, and five regularizers — every claim
evaluated across three seeds with full compute accounting. Headline finding: RO
cut the validation objective 13–15% yet never improved test Macro-F1 — a clean
demonstration of loss–decision dissociation. *(Report available on request.)*

![Randomized optimization of the final layer](ml/randomized-optimization.png)
![Optimizer ablations](ml/optimizer-ablations.png)

*RHC / SA / GA search trajectories and the compute-for-transfer trade-off; seven
optimizers under a fixed 12,000-update budget — momentum-family speed vs. Adam's
self-limiting stability.*

---

## ⚙️ Software Engineering — JobCompare6300 (4-person team)
An Android app for entering, weighting, and ranking job offers, built across four
deliverables in Georgia Tech's Software Development Process course: requirements
and use cases, UML design, SQLite schema, JUnit tests, and a working APK, all on a
shared Git workflow. Team grade 100/100; my solo Android project in the same
course scored 94/100. *(Code private.)*

![Use case model](sdp/use-case-model.png)

| My UML design | Team's final design |
|---|---|
| ![My class design](sdp/my-class-design.png) | ![Team class design](sdp/team-class-design.png) |

*Each member designed independently, then the team converged on a final architecture —
use-case model and both stages shown.*

---

📍 More: [github.com/MarianaZornes](https://github.com/MarianaZornes) · [LinkedIn](https://www.linkedin.com/in/mariana-zornes-98561256)
