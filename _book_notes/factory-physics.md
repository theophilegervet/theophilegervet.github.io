---
layout: post
title: Factory Physics
date: 2026-10-05
description: Wallace Hopp
img: assets/books/factory-physics.png
importance: 1
category: manufacturing & supply chain
giscus_comments: false
related_posts: false
toc:
  sidebar: left
---

## Executive Summary

Factory Physics is about understanding the underlying behavior of manufacturing systems well enough to make good decisions without relying on slogans, rules of thumb, or management fashions.

The central idea is that a factory is a **flow system**, not a collection of independent machines. Material moves through transformations, queues, buffers, inspections, assembly steps, and rework loops. Improving one local process does not necessarily improve the whole system.

The most important quantities are:

- **Throughput (TH):** output per unit time
- **Cycle Time (CT):** elapsed time a unit spends in the system
- **Work in Process (WIP):** units currently inside production
- **Raw Process Time (T0):** actual processing time if there were no waiting
- **Bottleneck Rate (rb):** maximum sustainable rate of the system's constraint
- **Utilization (u):** fraction of available capacity being consumed
- **Variability:** randomness in arrivals, processing, failures, quality, supply, and demand

The most important relationship is Little's Law:

$$
WIP = TH \times CT
$$

This means WIP, throughput, and cycle time are mechanically connected. If throughput stays constant and WIP doubles, cycle time roughly doubles.

A second key relationship is critical WIP:

$$
W_0 = r_b T_0
$$

In an ideal zero-variability factory, critical WIP is the amount of WIP required to achieve maximum throughput with minimum possible cycle time. Too little WIP starves the system. Too much WIP mostly creates waiting rather than additional output.

The third major concept is **VUT**:

$$
CT_q \approx
\left(\frac{c_a^2+c_e^2}{2}\right)
\left(\frac{u}{1-u}\right)t_e
$$

Conceptually:

$$
\boxed{\text{Queueing} \sim \text{Variability} \times \text{Utilization} \times \text{Time}}
$$

This explains why factories become congested. Variability creates queues, high utilization magnifies them nonlinearly, and long process times increase their scale.

Variability has to be paid for somewhere. The three fundamental buffers are:

$$
\boxed{\text{Inventory, Capacity, Time}}
$$

If you remove inventory without removing the variability it was protecting against, you will usually pay through spare capacity, longer lead times, lost throughput, or worse customer service.

Large batches trade setup efficiency for WIP and cycle time. Pull systems work primarily because they cap WIP. Quality and flow reinforce each other. Supplier variability becomes factory variability. Product architecture determines much of the complexity of the resulting factory.

The deepest lesson is:

> **Manufacturing performance comes from managing the interactions among flow, variability, capacity, inventory, quality, and product architecture — not from maximizing any single metric.**

---

## 1. The Core Idea

Factory Physics is about understanding the underlying behavior of manufacturing systems well enough to make good decisions without relying on slogans, rules of thumb, or management fashions.

The most important skill is not knowing a long list of tools. It is developing intuition for how throughput, WIP, cycle time, variability, capacity, and bottlenecks interact.

A factory is not a collection of independent machines. It is a flow system. Material moves through a sequence of transformations, queues, buffers, inspections, and assembly steps. Improving one local process does not necessarily improve the whole system.

A machine can become faster and simply create more inventory in front of the next machine. A purchasing team can lower component price while increasing total system cost through unreliable supply. A factory can report excellent utilization while delivering products slowly.

The correct question is always:

> **What change improves the performance of the entire system?**

That is the central mindset of the book.

---

## 2. The Core Variables You Must Understand

The core operating variables are:

- **Throughput (TH):** output per unit time
- **Cycle Time (CT):** elapsed time a unit spends in the system
- **Work in Process (WIP):** units currently inside the production system
- **Raw Process Time (T0):** actual processing time if there were no waiting
- **Bottleneck Rate (rb):** maximum sustainable rate of the system's constraint
- **Utilization (u):** fraction of available capacity currently being consumed
- **Variability:** randomness in arrival and processing behavior

The most important relationship is Little's Law:

$$
WIP = TH \times CT
$$

This is not just a formula. It gives you a way to reason about the factory.

If you produce 100 robots per week and each robot spends three weeks in production, then you must have approximately 300 robots in WIP.

That WIP is real. It is cash, floor space, unfinished hardware, hidden quality problems, and engineering-change exposure.

If throughput stays constant and WIP doubles, cycle time roughly doubles.

This is one of the simplest and most useful ways to diagnose a production system.

---

## 3. Raw Process Time vs. Cycle Time

Raw process time is how long the actual work takes.

Cycle time is how long the product spends in the factory.

These can be radically different.

A robot might require only 15 hours of real assembly, calibration, and test work but take 10 days to move through production. The gap is waiting.

That waiting may come from:

- queues
- batch formation
- unavailable parts
- rework
- scheduling
- machine downtime
- transportation
- matching delays between subassemblies

This is why speeding up individual operations often produces much less improvement than expected.

Suppose machining takes one hour, but the component waits three days before machining and another two days afterward. Making the machining operation 20% faster barely changes total cycle time.

In many factories, the dominant opportunity is not reducing processing time.

It is reducing **waiting**.

---

## 4. The Bottleneck Governs the System

Every production system has a constraint.

The bottleneck is the resource that limits sustainable throughput.

If final calibration can process only 50 robots per day, then the factory cannot sustainably ship more than 50 robots per day unless that bottleneck changes.

Improving a non-bottleneck may improve local efficiency while doing nothing for total output.

If machining can produce 200 robot sets per day but calibration can process 50, increasing machining capacity to 300 does not increase shipments. It may simply create more inventory in front of calibration.

This creates one of the most important habits in manufacturing:

> **Always ask where the bottleneck is.**

Then ask:

> **If we fix it, where does the bottleneck move next?**

The bottleneck is not necessarily permanent. It can move as product mix, staffing, yield, equipment uptime, and capacity change.

---

## 5. Critical WIP

The book defines:

$$
W_0 = r_b T_0
$$

where $W_0$ is critical WIP.

Critical WIP is the amount of WIP that, in an ideal zero-variability system, is enough to achieve maximum throughput while keeping cycle time at its minimum.

This is an important correction to simplistic interpretations of lean.

The goal is not zero inventory.

Zero WIP means zero production.

The useful ideal is closer to:

> **Have enough WIP to keep the bottleneck productive, but not so much that the system becomes congested.**

Below critical WIP, the system may be starved and adding WIP can raise throughput.

Once the bottleneck is fully utilized, additional WIP cannot create additional capacity.

It mostly creates queues and longer cycle time.

This explains one of the most common production mistakes:

> "We're behind, so release more work."

That can make the factory slower.

---

## 6. Variability Is the Fundamental Enemy of Flow

Real factories are variable.

Process times vary. Machines fail. Operators work at different speeds. Suppliers arrive late. Parts require rework. Demand changes. Product mix changes.

This variability creates congestion.

The book's fundamental principle is:

> **Increasing variability degrades production-system performance.**

More variability generally means some combination of:

- more WIP
- longer cycle time
- lower throughput
- greater spare-capacity requirements
- worse customer service

The deeper insight is that variability must be absorbed somewhere.

There are only three fundamental buffers.

### Inventory

Keep extra raw material, components, WIP, or finished goods.

### Capacity

Maintain spare machine, labor, supplier, or overtime capacity.

### Time

Allow longer production or customer lead times.

This gives one of the most useful mental models in the book:

$$
\boxed{Variability \rightarrow Inventory,\ Capacity,\ Time}
$$

If someone says, "Let's eliminate safety stock," the right response is:

> **What happened to the variability?**

If the underlying uncertainty still exists, the cost has merely moved somewhere else.

---

## 7. VUT: Why Queues Form

One of the most important quantitative ideas in Factory Physics is the VUT equation.

For a single workstation, average queue time can be approximated by:

$$
CT_q \approx
\left(\frac{c_a^2+c_e^2}{2}\right)
\left(\frac{u}{1-u}\right)t_e
$$

Conceptually:

$$
\boxed{CT_q = VUT}
$$

where:

- **V = Variability**
- **U = Utilization**
- **T = Effective process time**

You do not need to constantly calculate this equation. What matters is the intuition.

If a station has excessive queues, there are three broad places to look:

1. Is the process or arrival stream too variable?
2. Is utilization too high?
3. Is the effective process time too long?

This is an extremely powerful diagnostic framework.

### Effective Process Time

The "T" in VUT is not necessarily the machine's nominal cycle time.

The factory experiences **effective process time**, which includes the consequences of:

- breakdowns
- setups
- rework
- interruptions
- maintenance

A machine may physically cut a component in 30 seconds but behave like a much slower and more variable process once real operating conditions are included.

This means you should estimate capacity using what the production system actually experiences, not merely the machine specification.

### Why Utilization Is So Dangerous

The utilization term is:

$$
\frac{u}{1-u}
$$

At 80% utilization:

$$
4
$$

At 90%:

$$
9
$$

At 95%:

$$
19
$$

At 99%:

$$
99
$$

Going from 90% utilization to 99% is therefore not simply "9% more utilized."

The queueing consequences can be enormous.

This is why idle capacity is not automatically waste.

Sometimes capacity slack is the cheapest way to buy responsiveness.

---

## 8. Batching Is a Tradeoff

Large batches often exist because setups are expensive.

If a machine requires two hours to change from one product to another, it is tempting to produce a large quantity every time the setup is performed.

That reduces setup frequency and may increase effective capacity.

But large batches also create:

- more WIP
- longer cycle time
- slower quality feedback
- greater schedule rigidity
- greater engineering-change exposure

This is why Toyota's insight was so powerful.

Instead of merely asking:

> What batch size is optimal given a four-hour setup?

ask:

> **Why does the setup take four hours?**

Reducing setup time changes the economics of the entire system.

The broader principle is:

> **Do not treat bad parameters as permanent constraints if they can be improved.**

### Process Batch vs. Transfer Batch

A **process batch** is how many units you run before changing setup.

A **transfer batch** is how many units you wait for before moving material downstream.

These do not have to be equal.

Suppose you machine 100 pieces under one setup. You might still transfer groups of 10 to the next process as soon as they are ready.

This allows downstream work to begin sooner.

Reducing transfer batch size can therefore significantly reduce cycle time without increasing setup frequency.

---

## 9. Push vs. Pull

The book defines push and pull very cleanly.

A **push system** releases work according to external information such as:

- schedules
- forecasts
- planned orders

A **pull system** limits WIP and releases new work based on the state of the production system.

The critical distinction is not whether somebody physically "pulls" a part from another station.

It is whether the system has an explicit WIP limit.

This leads to a useful control-system interpretation.

### Push

Control release rate and observe the resulting WIP.

### Pull

Control WIP and observe the resulting throughput.

Pull is powerful because WIP is directly observable.

You can count how many jobs are inside the factory.

True effective capacity is harder to know because it changes with:

- downtime
- product mix
- staffing
- yield
- setups

Therefore controlling WIP is often more robust than trying to estimate capacity perfectly.

---

## 10. CONWIP

The simplest pull mechanism in the book is CONWIP:

**CONstant Work In Process.**

Suppose the production system permits 100 jobs inside.

When one finished job leaves, one new job may enter.

The WIP remains approximately constant.

This prevents uncontrolled congestion.

CONWIP also creates useful pressure on the system.

If machine reliability is poor, low WIP makes the problem visible.

If quality is poor, low WIP exposes it quickly.

If setup times are excessive, low WIP makes their consequences painful.

High WIP can hide operational problems.

Low WIP exposes them.

However, low WIP is not magic.

If you lower WIP while leaving variability unchanged, eventually downstream processes will starve and throughput will fall.

Successful pull systems therefore combine WIP reduction with:

- reliability improvement
- quality improvement
- setup reduction
- supplier improvement
- better process control

---

## 11. Cycle Time, Lead Time, and Service

Cycle time and lead time are related but different.

**Cycle time** is what the production system actually does. It is the amount of time an individual job takes to traverse the production process.

**Lead time** is a management decision or customer commitment. It is how much time the company allows for the job to finish.

If average cycle time is ten days, promising ten-day delivery does not produce 100% on-time performance because cycle time is variable.

Some jobs will take less than ten days.

Some will take more.

For a given target service level, required manufacturing lead time increases with both:

- average cycle time
- cycle-time variability

Conceptually:

$$
\text{Lead Time}
\approx
\text{Average Cycle Time}
+
\text{Safety Allowance}
$$

The more variable production is, the larger the safety allowance must be.

This creates an important strategic consequence:

> **Reducing variability can shorten customer lead time even if average processing speed barely changes.**

---

## 12. Quality and Flow Are Tightly Linked

Quality is not separate from manufacturing flow.

Poor quality creates:

- rework
- scrap
- unpredictable routing
- extra processing
- extra capacity demand
- more variability
- more WIP

Rework is especially destructive because it sends material back through parts of the production system.

A 5% rework rate therefore does not simply mean 5% more labor.

It also creates queues and variability.

The reverse is equally important:

> **Good flow improves quality.**

When WIP is low and cycle time is short, defects are discovered sooner.

A process that begins producing bad parts might produce 10 defective units before detection instead of 500.

The feedback loop between cause and detection becomes shorter.

For an engineering-heavy hardware company, this is especially valuable because faster quality feedback is also faster engineering learning.

---

## 13. Variability Pooling and Postponement

Another important concept is **variability pooling**.

Independent uncertainty becomes easier to handle when it is pooled.

A simple example is machine queues.

If three identical machines have three separate queues, one machine may become idle while another has a large backlog.

If all three share one queue, the next available machine handles the next job.

Pooling generally reduces waiting.

The same principle applies to inventory.

Generic inventory that can serve several final products is often more efficient than separate finished inventory for every variant.

### Inventory / Order Interface

Every production system has a point where production shifts from:

**make-to-stock**

to:

**make-to-order**

Moving that point changes the tradeoff between customer speed, inventory, and customization.

If you hold finished products, customer response is fast but finished-goods inventory is high.

If you hold generic modules and finish configuration after an order arrives, inventory can be pooled while retaining customization.

### Postponement

**Postponement** means intentionally delaying product differentiation until late in the process.

Instead of forecasting five finished variants independently, you might hold one common module and configure it after actual demand becomes known.

This can provide:

- lower finished-goods inventory
- lower forecast risk
- more customization
- faster response than pure build-to-order

Postponement is therefore partly a product-architecture decision.

---

## 14. Why WIP Is Especially Dangerous in Robotics

In a mature factory, WIP mostly represents working capital and flow inefficiency.

In an early robot company, it also represents engineering risk.

Every unfinished robot may contain:

- an old PCB revision
- an old mechanical design
- outdated harnesses
- obsolete sensors
- old actuator revisions
- known defects not yet corrected

That makes short cycle time strategically important.

The longer material spends inside the factory, the greater the chance that an engineering change makes it obsolete.

So for a rapidly evolving robot, reducing WIP is not just lean manufacturing.

It increases **engineering velocity**.

---

## 15. Matching Is a Major Robotics Problem

Robots are complex assemblies.

Final assembly may require:

- actuators
- batteries
- compute
- sensors
- harnesses
- structural parts
- end effectors

If one critical component is missing, all the others may sit idle.

This creates **wait-to-match** and matching WIP.

You can therefore have a warehouse containing millions of dollars of inventory while being unable to complete a single robot.

This means one of the most useful inventory questions is not:

> How much inventory do we have?

It is:

> **How many complete buildable sets do we have?**

The problem becomes more severe as the number of independently supplied components grows.

Complexity creates a synchronization tax.

---

## 16. Supplier Performance Is Part of Factory Physics

A supplier's variability enters your factory as arrival variability.

If a gearbox supplier has unpredictable delivery times, your line experiences:

- starvation
- incomplete builds
- rescheduling
- expediting
- excess inventory elsewhere

Supplier selection should therefore never be based on piece price alone.

You also care about:

- average lead time
- lead-time variability
- yield
- capacity
- flexibility
- responsiveness
- MOQ
- engineering support

A supplier that costs 10% more per component but delivers reliably and responds quickly may create lower total system cost.

This becomes even more important in a complex assembly.

If a robot requires many independently supplied components, every component must be available simultaneously to maintain schedule.

The more components you require, the more reliable each component's supply generally has to become — or the more safety inventory you need to hold.

Supplier reliability and product architecture are therefore tightly connected.

---

## 17. Lean Is Really About Buffer Economics

A useful Factory Physics view of lean is:

> **A lean production system achieves its objective with minimal buffering cost.**

This is more useful than saying:

> Lean means low inventory.

Inventory is only one buffer.

Capacity is another.

Time is another.

The goal is not to eliminate all three.

The goal is to understand why the buffers exist, reduce the underlying variability where economically sensible, and then use the cheapest combination required to achieve reliable performance.

A highly reliable supplier may allow lower inventory.

A flexible workforce may reduce capacity requirements elsewhere.

A customer willing to tolerate longer lead times may reduce the need for finished goods.

There is no universally correct buffer.

The correct answer depends on economics.

---

## 18. Product Architecture and Factory Architecture Are Connected

Product design determines manufacturing behavior.

A robot with many unique parts, specialized fasteners, unique calibration procedures, and tightly coupled modules creates:

- more suppliers
- more matching problems
- more inventory
- more routing complexity
- more quality opportunities
- more rework

A more modular design can dramatically simplify factory physics.

This is why design for manufacturing is not only about reducing piece-part cost.

It is also about reducing system complexity.

A product architecture decision can eliminate:

- an assembly station
- a supplier
- a fixture
- a calibration operation
- a quality check
- a queue
- a unique SKU
- an entire failure mode

That can be worth much more than negotiating a component price down by 5%.

---

## 19. MRP, Planning, and Execution

Material Requirements Planning is powerful because it recognizes the difference between **independent demand** and **dependent demand**.

If you plan to build 100 robots and each robot requires 12 actuators, then demand for 1,200 actuators follows from the bill of material.

You do not need to independently forecast actuator demand.

MRP is therefore extremely useful for understanding:

- future component requirements
- purchase timing
- bills of material
- planned orders

But classical MRP has an important weakness.

It often treats manufacturing lead times as relatively fixed and does not naturally capture the nonlinear effect of capacity and congestion.

In reality:

> **Lead time is partly an output of the factory, not merely an input to the planning system.**

If the factory becomes overloaded, queues increase.

Cycle time increases.

Lead time increases.

If the planning system continues releasing work based on an unrealistically short assumed lead time, it can make the congestion even worse.

The lesson is not that MRP is useless.

It is:

> **Do not confuse a planning model with the physical reality of the factory.**

### Plan With Push, Execute With Pull

Push-style planning is useful for anticipating the future.

You need it to determine:

- materials
- staffing
- capacity
- supplier orders

But pull is often superior for actual shop-floor execution because it prevents the factory from being overloaded with WIP.

A strong architecture is therefore:

> **Plan with push. Execute with pull.**

Use forecasts and demand information to plan what will eventually be needed.

Use actual system state to determine when work should physically enter production.

---

## 20. Capacity Does Not Need to Be Balanced

It seems intuitive that every station should have roughly equal capacity and utilization.

Factory Physics shows why this can be wrong.

Suppose one station can add capacity cheaply by adding another operator.

Another station requires a multimillion-dollar machine to add capacity.

It may be economically rational to provide substantial excess capacity at the cheap station so that it never constrains the expensive station.

The cheap resource might operate at only 60% utilization.

That is not necessarily waste.

Its spare capacity protects the resource whose capacity is expensive and difficult to expand.

This leads to an important idea:

> **A good flow line may be intentionally unbalanced.**

You can even think deliberately about where you want the bottleneck to live.

A good intentional bottleneck is often a resource that is:

- expensive to duplicate
- reliable
- predictable
- easy to protect from starvation
- strategically worth utilizing heavily

Cheap or flexible processes around it can be deliberately oversized.

---

## 21. The Factory Diagnostic Framework

When a factory is underperforming, use this sequence.

First, identify the business symptom.

Is throughput low? Is cycle time too long? Are shipments late? Is WIP too high? Is quality poor?

Then find where material is waiting.

WIP often reveals the bottleneck or synchronization problem.

Next, identify the bottleneck and determine why it is constrained.

Then look for variability:

- downtime
- quality problems
- setups
- staffing
- supplier delays
- product mix
- bursty releases

Ask how that variability is currently being buffered:

- inventory?
- capacity?
- time?

Then ask whether the variability can be removed rather than buffered.

Use VUT:

> Is the queue being driven mainly by variability, utilization, or process time?

Check whether the factory is releasing more work than it can absorb.

Check whether process batches or transfer batches are creating unnecessary waiting.

Check whether assembly is suffering from matching delays.

Finally, ask whether local optimization is hurting the global system.

The recurring question is:

> **What single change has the highest leverage on the whole system?**

---

## 22. The Equations and Ideas Worth Memorizing

### Little's Law

$$
\boxed{WIP = TH \times CT}
$$

This links inventory, throughput, and cycle time.

---

### Critical WIP

$$
\boxed{W_0 = r_b T_0}
$$

In the ideal zero-variability system, this is the amount of WIP required to achieve maximum throughput with minimum cycle time.

---

### VUT

$$
\boxed{
CT_q \approx
\left(\frac{c_a^2+c_e^2}{2}\right)
\left(\frac{u}{1-u}\right)t_e
}
$$

Conceptually:

$$
\boxed{\text{Queueing} \sim \text{Variability} \times \text{Utilization} \times \text{Time}}
$$

---

### Coefficient of Variation

$$
CV = \frac{\sigma}{\mu}
$$

This measures variability relative to the average.

---

### Variability Buffering

$$
\boxed{\text{Variability} \rightarrow \text{Inventory, Capacity, Time}}
$$

If you remove one buffer without reducing the variability, you usually pay somewhere else.

---

### Pull

$$
\boxed{\text{Pull} = \text{explicit WIP control}}
$$

The power of pull comes primarily from preventing uncontrolled congestion.

---

# The Ideas to Remember

If you remember only the most important ideas from Factory Physics, remember these:

**Factories are flow systems.** Local efficiency does not equal system efficiency.

**Little's Law is everywhere.** WIP, throughput, and cycle time are mechanically linked.

**The bottleneck governs throughput.** Improving non-bottlenecks may accomplish nothing.

**Variability always has a cost.** You pay for it with inventory, capacity, or time.

**VUT explains congestion.** Queueing comes from variability, utilization, and effective process time.

**High utilization creates nonlinear queues.** Some spare capacity can be economically valuable.

**More WIP does not necessarily mean more output.** Once the bottleneck is saturated, additional WIP mostly creates waiting.

**Low WIP exposes problems.** High WIP hides unreliable machines, poor quality, bad scheduling, and unstable suppliers.

**Batching trades setup efficiency against flow.** Reduce setup time before assuming large batches are inevitable.

**Process batches and transfer batches are different.** You can often move material downstream before the entire process batch is finished.

**Cycle time and lead time are different.** Variability forces lead-time safety margins.

**Pooling reduces the cost of variability.** Common parts, shared queues, generic inventory, and postponement can reduce required buffers.

**Quality and flow reinforce one another.** Better quality improves flow; faster flow improves quality feedback.

**Supplier variability becomes factory variability.** Unit price alone is a poor measure of supplier economics.

**Product architecture determines manufacturing architecture.** Part count, commonality, modularity, and interfaces strongly affect factory behavior.

**Plan with push and execute with pull.** Forecast-driven planning and WIP-controlled execution solve different problems.

**Capacity does not need to be evenly balanced.** Spare capacity at cheap flexible resources can be economically rational.

The deepest lesson is:

> **Manufacturing performance comes from managing the interactions between flow, variability, capacity, inventory, quality, suppliers, and product architecture — not from maximizing any single metric.**
