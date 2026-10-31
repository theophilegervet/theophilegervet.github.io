---
layout: post
title: Toyota Production System
date: 2026-10-05
description: Taiichi Ohno
img: assets/books/toyota-production-system.png
importance: 2
category: manufacturing & supply chain
giscus_comments: false
related_posts: false
toc:
  sidebar: left
---

## Executive Summary

The Toyota Production System is built around one objective: **produce exactly what customers need, with the minimum resources, by continuously eliminating waste**.

TPS was developed for an environment of high product variety, changing demand, and limited resources, where traditional mass production tends to create excess inventory and cost. Its two pillars are **Just-in-Time**, which means making only what is needed, when needed, in the quantity needed, and **jidoka**, which means stopping when an abnormality occurs so defects and problems cannot continue unnoticed.

Flow, kanban, production leveling, standard work, quick changeovers, visual management, and Five Whys all support those two pillars.

---

## 1. Produce to Demand, Not Capacity

A factory should not produce simply because machines and workers are available. If customers need 100 units and the factory makes 120, the extra 20 are not productivity; they are overproduction.

The fundamental reversal in TPS is that **demand determines production**, rather than production capacity determining output.

> **Produce what is needed, not what is possible.**

---

## 2. True Efficiency Means Lower Cost

More output is useful only if customers need it. If 10 workers can produce 120 units but demand is only 100, the goal is not to produce 120. The better improvement is to reorganize the work so fewer resources can produce the required 100.

TPS therefore distinguishes true efficiency from apparent efficiency. Increasing local output can look productive while increasing total system cost.

> **True efficiency means producing the required output with fewer resources.**

---

## 3. Capacity Contains Hidden Waste

Ohno's core productivity model is:

$$
\boxed{\text{Present Capacity} = \text{Useful Work} + \text{Waste}}
$$

A line may appear fully occupied while much of its capacity is consumed by overproduction, waiting, transportation, over-processing, inventory, unnecessary motion, and defects.

Productivity improves by removing this waste, not by making people work harder.

---

## 4. Overproduction Is the Most Dangerous Waste

Ohno treats overproduction as especially harmful because it hides other problems. Producing ahead creates inventory, which then requires storage, handling, transportation, tracking, and often more labor. It also hides waiting and delays the discovery of defects.

A system full of inventory can therefore appear productive while actually containing large amounts of waste.

> **Overproduction makes a weak system look healthy.**

---

## 5. Flow Comes Before Pull

Traditional factories often organize around departments or machine types. TPS instead tries to organize production around the **sequence of the product**, allowing material to move from one operation to the next with as little waiting and inventory as possible.

Flow reduces WIP, transportation, handoffs, lead time, and the ability of problems to remain hidden. Ohno is clear that kanban works poorly if it is placed on top of a disconnected batch-production system.

> **Establish flow before trying to control production with pull.**

---

## 6. Pull: Consumption Triggers Replenishment

Traditional production pushes goods forward according to schedules. TPS reverses that logic. The downstream process takes only what it needs, and the upstream process replaces only what was consumed.

The key principle is simple:

> **Do not produce because you can. Produce because downstream actually needs replenishment.**

This is the core logic of pull and Just-in-Time.

---

## 7. Kanban Is a Control Mechanism

Kanban communicates what is needed, how much is needed, and when replenishment is authorized. Its purpose is to prevent uncontrolled production and make pull operational.

Kanban is not the Toyota Production System itself. It works only when the underlying system already has reasonably stable flow, standard work, production leveling, and reliable quality.

> **Kanban controls pull; it does not create a good production system by itself.**

---

## 8. Reduce Buffers to Expose Problems

Inventory protects production from machine failures, poor quality, long setups, supplier problems, and process instability. But the same inventory also hides those problems.

TPS deliberately reduces buffers so weaknesses become visible. The logic is:

> **Reduce the buffer → expose the problem → solve the root cause → reduce the buffer again.**

Low inventory is therefore not the ultimate objective. **Stronger processes are the objective.**

---

## 9. Jidoka: Stop Abnormalities

Ordinary automation means a machine can run by itself. Jidoka means a machine or worker can recognize an abnormal condition and stop the process.

The purpose is not merely to stop defects. Stopping makes the abnormality visible and forces the organization to investigate why it occurred and prevent recurrence.

Allowing production to continue through an abnormal condition may preserve short-term output, but it creates larger downstream waste.

> **Detect the abnormality, stop, understand the cause, and prevent recurrence.**

---

## 10. Make Problems Visible

TPS tries to make the difference between normal and abnormal conditions obvious. Andon, kanban, standard work, inventory limits, and visual controls all serve this purpose.

The faster a problem becomes visible, the faster it can be addressed. Hidden problems persist because the organization can continue operating around them.

> **Problems that are visible can be improved. Problems that remain hidden become part of the system.**

---

## 11. Production Leveling / Heijunka

If downstream production swings sharply between high and low demand, upstream processes need extra equipment, labor, capacity, and inventory to absorb those peaks.

Production leveling smooths both the quantity and mix of production so those fluctuations do not amplify as they move upstream.

Ohno describes the objective as:

> **Lower the mountains and raise the valleys.**

Leveling makes low-inventory pull systems much more practical because upstream processes face a more stable pattern of demand.

---

## 12. Small Lots Require Fast Changeovers

Large batches are often justified by long setup times. Traditional thinking accepts the setup time and compensates by producing more each time the machine is changed over.

TPS attacks the opposite variable: **reduce the setup time**.

Shorter changeovers make smaller lots economical, which enables better leveling, lower inventory, faster response, and greater product variety.

> **Do not design the whole production system around a bad constraint before asking whether the constraint itself can be improved.**

---

## 13. Takt Time: Demand Sets the Rhythm

Takt time translates customer demand into the required production pace.

$$
\boxed{
\text{Takt Time}
=
\frac{\text{Available Production Time}}
{\text{Required Customer Quantity}}
}
$$

If 480 minutes are available and customers require 40 units, takt is 12 minutes per unit.

The important idea is not the calculation itself. It is that **the customer determines the pace of production**.

---

## 14. Standard Work Creates the Baseline

Standard work defines the current best known way to perform a process. Ohno emphasizes three elements: **cycle or takt time, work sequence, and standard inventory**.

Without a standard, it is difficult to tell whether a condition is abnormal or whether an improvement actually made the process better. But the standard should never become permanent.

> **Standardize, improve, then re-standardize.**

Standardization and continuous improvement depend on each other.

---

## 15. Five Whys: Solve Causes, Not Symptoms

Restarting a failed process does not necessarily mean the problem has been solved. Five Whys pushes investigation beyond the immediate symptom toward the underlying mechanism that allowed the failure to occur.

The number five is not the important part. The important habit is refusing to stop at the first plausible explanation.

> **A repair restores production. A root-cause countermeasure prevents recurrence.**

---

## 16. Go See the Real Process

Ohno strongly favors direct observation of the production floor. Reports can tell management that something went wrong, but the actual process shows where material waits, where workers struggle, where inventory accumulates, where defects begin, and what workarounds people have created.

> **Facts at the process are more valuable than assumptions made from a distance.**

This plant-first mindset is foundational to TPS problem solving.

---

## 17. Availability Is More Important Than Utilization

TPS distinguishes between how much a machine is actually running and whether it is ready to run when needed.

A machine should not produce unnecessary goods merely to remain busy. What matters is that it is reliable, maintained, and available when demand requires it.

> **Ready when needed is better than always running.**

Maximum utilization can create overproduction, so idle capacity is not automatically waste.

---

## 18. Stable Flow Beats Local Speed

A machine that runs extremely fast may simply create a queue in front of the next process. Local speed is therefore not the same as system productivity.

Ohno's tortoise-and-hare analogy captures this idea: steady, synchronized production is often more efficient than bursts of output followed by waiting.

> **Optimize the flow of the whole system, not the speed of individual resources.**

---

## 19. Flexible Manpower

A strong production system must remain economical when demand falls. This requires multi-skilled workers, flexible work combinations, teamwork, and layouts that allow staffing to change with required output.

Increasing productivity while volume is rising is relatively easy. The harder test is reducing the resources required when volume declines.

> **A strong system scales resources with demand.**

---

## 20. Muda, Mura, and Muri

TPS attacks three related conditions: **muda** is waste, **mura** is unevenness, and **muri** is overburden.

These reinforce one another. Uneven production creates periods of overload, overload creates instability and defects, and organizations then add buffers to protect themselves, creating more waste.

This is why TPS combines leveling, flow, standard work, and jidoka instead of treating waste as an isolated problem.

---

## 21. Respect Human Intelligence

TPS is not fundamentally about making people move faster. It tries to eliminate meaningless work so people can contribute through judgment, problem solving, improvement, and teamwork.

Machines should perform repetitive work and detect abnormalities where possible. Human attention should be used where intelligence and judgment add value.

> **Remove meaningless work and use human capability to improve the system.**

---

## The TPS System

The core operating logic is:

> **Customer demand → takt → leveling → flow → pull**

That flow is supported by **standard work, jidoka, and visual control**, which make problems visible.

Once a problem becomes visible, the process is:

> **Problem → root cause → countermeasure → improved standard**

The system can then be tightened again, exposing the next weakness. TPS is therefore not a final state but a continuous improvement cycle.

---

## The Ideas to Remember

- **Produce what is needed, not what is possible.**
- **True efficiency means producing required output with fewer resources.**
- **Overproduction is the most dangerous waste because it hides other problems.**
- **Create flow before implementing pull.**
- **Consumption should trigger replenishment.**
- **Kanban controls pull; it is not TPS itself.**
- **Reduce buffers to expose weak processes, then fix the weakness.**
- **Jidoka means stopping abnormalities instead of allowing them to propagate.**
- **Level production so variability does not amplify upstream.**
- **Reduce setup time rather than accepting large batches as inevitable.**
- **Takt makes customer demand the clock of production.**
- **Standard work creates the baseline for improvement.**
- **Solve root causes rather than repeatedly treating symptoms.**
- **Observe the actual process instead of managing only from reports.**
- **High availability matters more than maximum utilization.**
- **Optimize total flow, not local speed.**
- **Design the system to remain efficient when demand falls.**
- **TPS is a continuous cycle of exposing weaknesses, solving them, and tightening the system again.**











# Toyota Production System — Foundations & Mental Models

## Executive Summary

The Toyota Production System (TPS) is a system for **producing exactly what customers need, with the minimum resources, by continuously eliminating waste**.

It was developed for an environment of high product variety, limited resources, and changing demand. This makes its logic very different from traditional mass production, where efficiency is often associated with large batches, high machine utilization, and maximizing output.

TPS rests on two pillars:

- **Just-in-Time (JIT):** make only what is needed, when it is needed, in the quantity needed.
- **Jidoka:** stop when an abnormality occurs so defects and process problems cannot continue unnoticed.

The rest of TPS — flow, pull, kanban, leveling, standard work, quick changeovers, visual control, and root-cause problem solving — supports these two pillars.

---

## 1. Produce to Demand, Not Capacity

The starting point of TPS is **required demand**, not available capacity. A machine being able to produce more is not a reason to produce more.

If customers need 100 units and the factory makes 120, the extra 20 are not productivity. They are overproduction.

> **Produce what is needed, not what is possible.**

This changes the definition of efficiency. The goal is not to maximize output with existing resources, but to use the minimum resources necessary to produce the required output.

---

## 2. Productivity Comes From Removing Waste

Ohno's basic productivity model is:

$$
\boxed{\text{Present Capacity} = \text{Useful Work} + \text{Waste}}
$$

A factory may appear fully occupied while large amounts of capacity are being consumed by unnecessary activity. Improvement means identifying that waste and removing it rather than asking people to work harder.

Ohno identifies seven forms of waste:

1. Overproduction
2. Waiting
3. Transportation
4. Over-processing
5. Inventory
6. Unnecessary motion
7. Defects

### Why overproduction matters most

Overproduction is especially dangerous because it **hides the other wastes**. Producing ahead creates inventory, which then requires storage, transportation, handling, tracking, and additional labor. It can also hide waiting and delay the discovery of defects.

> **Overproduction makes a weak system look productive.**

TPS therefore treats producing too early as a problem, even when everything produced will eventually be used.

---

## 3. Muda, Mura, and Muri

TPS is not only about eliminating obvious waste.

It also tries to reduce:

- **Muda:** waste
- **Mura:** unevenness or inconsistency
- **Muri:** overburden

These reinforce one another. Uneven production creates periods of overload; overload creates instability and defects; companies then add inventory and excess capacity to protect themselves, creating more waste.

This is why TPS combines waste elimination with production leveling, standard work, and stable flow.

---

## 4. Flow Before Pull

Traditional factories often organize equipment by function: lathes in one department, drills in another, assembly somewhere else. Material moves between them in batches and waits between processes.

Toyota instead tries to arrange work according to the **sequence in which the product is made**. The aim is continuous flow with as little waiting and work-in-process inventory as possible.

Flow reduces lead time, transportation, queues, handoffs, and the ability of problems to remain hidden.

> **Organize around the flow of the product, not the utilization of individual machines.**

This is also why Ohno warns against implementing kanban before fixing the underlying production flow.

---

## 5. Just-in-Time and Pull

Just-in-Time means that each process receives the **right item, at the right time, in the exact quantity required**.

Toyota achieves this by reversing the conventional direction of production control. Instead of upstream processes producing according to a plan and pushing material forward, the downstream process withdraws what it needs. The upstream process then replenishes what was consumed.

> **Consumption triggers replenishment.**

This is the essence of pull.

The important rule is:

> **Do not produce because you can. Produce because something downstream actually needs it.**

---

## 6. Kanban Controls Pull

Kanban is the mechanism Toyota uses to communicate what should be withdrawn or replenished. It tells the process what is needed, how much is needed, and when production is authorized.

Its value comes partly from what it prevents: upstream processes cannot simply continue producing because they have free capacity.

But kanban is **not TPS itself**. It depends on a production system that already has reasonably stable flow, standard work, leveled production, and reliable quality.

> **Kanban controls a pull system; it cannot compensate for a badly designed production system.**

---

## 7. Inventory Is a Buffer That Can Hide Problems

Inventory protects production from machine failures, defects, long changeovers, supplier problems, and unstable processes. That protection is useful in the short term, but it also prevents the organization from feeling the consequences of those problems.

TPS therefore reduces buffers carefully in order to expose weaknesses.

The improvement cycle is:

> **Reduce buffer → expose problem → solve root cause → reduce buffer again**

The objective is not simply low inventory. The objective is a production system strong enough that large buffers are no longer necessary.

---

## 8. Jidoka: Stop Abnormalities at the Source

Ordinary automation means a machine can operate without constant human effort. Jidoka goes further: the machine or worker can recognize an abnormal condition and stop the process.

Without jidoka, an automated machine may produce hundreds of defective parts before anyone notices. With jidoka, the abnormality becomes visible immediately and can be investigated.

The underlying logic is:

> **Detect → stop → understand → prevent recurrence**

Stopping production may appear inefficient in the moment, but repeatedly allowing the same abnormality to continue is much more expensive.

Jidoka turns problems into improvement opportunities instead of allowing them to flow downstream.

---

## 9. Make Problems Visible

TPS deliberately makes the difference between normal and abnormal conditions easy to see. Standard work, kanban, inventory limits, andon, and other visual controls all serve this purpose.

If a process is abnormal, management and workers should be able to recognize it quickly rather than discovering it later through a report.

> **A problem must become visible before it can drive improvement.**

This is why TPS often removes the buffers and workarounds that make operations look smoother than they really are.

---

## 10. Level Production

Pull becomes difficult when demand reaches production in large peaks and valleys. If final assembly suddenly demands huge quantities of one item, every upstream process must carry enough equipment, labor, or inventory to survive those peaks.

Production leveling smooths both **quantity and product mix** so upstream processes face a more stable pattern of demand.

Ohno's idea is essentially:

> **Make the mountains lower and the valleys shallower.**

Leveling reduces the amount of excess capacity and inventory required to handle variability and makes JIT much more practical.

---

## 11. Small Lots Depend on Fast Changeovers

Large batches are often justified by long setup times. If changing a machine takes several hours, producing a large batch appears economical.

TPS does not simply accept that assumption. It asks why the setup takes several hours and works to reduce it.

Shorter changeovers allow:

- smaller batches
- lower inventory
- more frequent product changes
- better production leveling
- faster response to demand

The broader mental model is:

> **Do not design the whole system around a bad constraint before asking whether the constraint itself can be improved.**

---

## 12. Takt Time: Demand Sets the Pace

Takt time converts customer demand into the pace at which the production system must operate.

$$
\boxed{
\text{Takt Time}
=
\frac{\text{Available Production Time}}
{\text{Required Customer Quantity}}
}
$$

If 480 minutes of production time are available and customers require 40 units, takt time is 12 minutes per unit.

The important point is not the arithmetic:

> **Customer demand sets the rhythm of production.**

Production should then organize people, machines, and work around that required rhythm.

---

## 13. Standard Work Is the Baseline for Improvement

Standard work defines the best currently known way to perform a process. Ohno emphasizes three components:

- **Cycle / takt time**
- **Work sequence**
- **Standard inventory**

Without a standard, it is difficult to distinguish normal from abnormal performance or determine whether a change actually improved the process.

But a standard should not become permanent. Once a better method is discovered, the standard should change.

> **Standardize → improve → re-standardize.**

Standardization and continuous improvement therefore depend on one another.

---

## 14. Solve Root Causes, Not Symptoms

Ohno's Five Whys is a method for pushing past the immediate symptom of a problem.

A machine may stop because a fuse blew. Replacing the fuse restores production, but it does not explain why the fuse blew. Repeatedly asking why traces the failure toward the underlying mechanism.

The exact number five is not important. The mindset is.

> **Restarting the process is not the same as solving the problem.**

A good countermeasure prevents recurrence rather than repeatedly fixing the same symptom.

---

## 15. Go See the Actual Process

Ohno places enormous value on observing the production floor directly. Reports can show that a problem exists, but direct observation reveals how the problem actually happens.

The process shows where material waits, where people struggle, where workarounds occur, where inventory accumulates, and where defects originate.

> **Facts at the process are more valuable than assumptions made from a distance.**

This is central to both problem solving and the creation of good standard work.

---

## 16. Optimize the System, Not Individual Resources

A fast machine is not useful if it merely creates inventory in front of the next process. Likewise, an expensive machine does not need to run continuously simply because management wants high utilization.

Ohno distinguishes between a machine being **used constantly** and being **available whenever it is needed**. TPS prefers reliable availability over unnecessary utilization.

This is also the meaning of Ohno's tortoise-and-hare analogy: steady, synchronized production is often superior to a process that races ahead and then waits.

> **Optimize total flow, not local speed or utilization.**

---

## 17. Build Flexibility Into Labor and Capacity

TPS must remain economical when demand falls, not only when it rises. This requires workers capable of operating multiple processes, flexible work combinations, and layouts that allow staffing to change with required output.

If demand falls significantly but the same number of workers and machines are still required, the production system is not truly flexible.

The difficult form of productivity improvement is therefore:

> **Reduce the resources required when required output falls.**

This is one reason Toyota emphasizes multi-skilled workers and team-based production.

---

## 18. Respect Human Capability

TPS is not fundamentally about making people move faster. Ohno's system tries to remove meaningless work so people can contribute through judgment, problem solving, teamwork, and improvement.

Machines should perform repetitive work and detect abnormalities when possible. People should not spend their time watching machines perform normal operations or repeatedly correcting preventable failures.

The goal is to use human intelligence where it creates value.

---

## The Core TPS Logic

At the operating level:

> **Customer demand → takt → leveling → flow → pull**

The system is stabilized through:

> **Standard work + jidoka + visual control**

When an abnormality appears:

> **Problem → root cause → countermeasure → improved standard**

Then buffers can be reduced again, exposing the next weakness.

That is the core improvement loop of TPS.

---

## Key Mental Models

- **Produce what is needed, not what is possible.**
- **True productivity comes from removing waste, not increasing unnecessary output.**
- **Overproduction is dangerous because it hides other problems.**
- **Create flow before implementing pull.**
- **Consumption should trigger replenishment.**
- **Kanban is a control mechanism, not the production system itself.**
- **Use lower buffers to expose weaknesses, then solve the weaknesses.**
- **Stop abnormalities instead of allowing them to propagate.**
- **Level demand so variability does not amplify upstream.**
- **Attack setup time rather than accepting large batches.**
- **Let customer demand determine the production rhythm.**
- **Use standard work as the baseline for continuous improvement.**
- **Solve causes rather than repeatedly treating symptoms.**
- **Observe the actual process.**
- **Optimize total flow rather than local utilization.**
- **Build a system that can remain efficient when demand falls.**