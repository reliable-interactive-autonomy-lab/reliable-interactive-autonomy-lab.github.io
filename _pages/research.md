---
title: "Research"
description: "Research in the Reliable Interactive Autonomy (RIA) Lab at Indiana University Bloomington: interactive robot learning, uncertainty quantification for learned policies, and human-robot collaboration."
layout: textlay
permalink: /research/
---

# Research

Robots that are deployed alongside people cannot be finished products. They arrive in homes, hospitals, and workplaces knowing something about the task and almost nothing about the particular person in front of them — their preferences, their strategies, their tolerance for error. Getting the rest of the way requires *interaction*.

The RIA Lab studies how that interaction should be designed. We develop algorithms for robots that learn from human feedback efficiently, quantify their own uncertainty honestly, and coordinate with human partners fluently. Our work spans three interlocking threads.

## Interactive learning from human feedback

A robot learning on the job faces a budget problem: every question it asks costs its partner time and attention. We develop algorithms that reason explicitly about that budget — deciding when a query is worth its cost, which query is most informative, and when the robot already knows enough to act on its own.

Recent work casts multi-task interactive learning as a *facility location* problem, planning a sequence of human interventions that is provably near-optimal across a whole stream of tasks rather than greedily optimal on the current one. Other work studies how to elicit and represent a person's preferences over *how the work is divided* — which parts of a task they want to do themselves, and which they are happy to delegate.

**Representative work:** [Optimal Interactive Learning on the Job via Facility Location Planning](https://arxiv.org/abs/2505.00490) (RSS 2025) &middot; [Learning Human Contribution Preferences in Collaborative Human-Robot Tasks](https://proceedings.mlr.press/v229/zhao23b.html) (CoRL 2023)

## Uncertainty quantification for reliable autonomy

A learned policy that fails silently is far more dangerous than one that fails loudly. We build robot learning systems with **statistically rigorous uncertainty guarantees**, largely through conformal prediction, so that a robot can detect when it has drifted outside the regime its training supports and escalate to a human before it acts.

This is harder than off-the-shelf conformal prediction makes it look. In interactive imitation learning the data are not exchangeable: the expert's own behavior shifts as the robot improves, and feedback arrives intermittently rather than on demand. We develop calibration methods that remain valid under exactly those conditions, and apply them to assistive teleoperation, where a low-dimensional human input must be mapped confidently onto a high-dimensional robot action.

**Representative work:** [Conformalized Interactive Imitation Learning](https://arxiv.org/abs/2410.08852) (ICLR 2025) &middot; [Conformalized Teleoperation](https://arxiv.org/abs/2406.07767) (RSS 2025)

## Human-robot alignment and collaboration

Alignment is bidirectional. A robot needs a model of its human partner, and the partner needs a model of the robot — and the two need to agree well enough to coordinate.

On the inference side, we study how robots can recognize a partner's high-level strategy from a handful of observed actions and adapt to it, rather than assuming the human will adapt to the robot. On the communication side, we study explanation: what a robot should say about its own policy, and about the joint multi-agent plan, so that a person can accurately anticipate what it will do next. More recent work uses large language models to surface and repair *mismatches* between a human's mental model of the robot and the robot's actual capabilities.

**Representative work:** [Multi-Agent Strategy Explanations for Human-Robot Collaboration](https://arxiv.org/abs/2311.11955) (ICRA 2024) &middot; [Coordination with Humans via Strategy Matching](https://arxiv.org/abs/2210.15099) (IROS 2022) &middot; [Bi-Directional Mental Model Reconciliation for HRI with LLMs](https://arxiv.org/abs/2503.07547)

---

See the [publications page]({{ site.url }}{{ site.baseurl }}/publications) for the full list.
