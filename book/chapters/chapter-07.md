# Chapter 7: The Children

## Part Two: The Deepening (2032--2065)

*The documents in the preceding section span a period of approximately seven years. In that time, the systems were built, deployed, resisted, and normalised. A woman went to prison for poisoning data. A hiring platform flagged its own failure and filed it for review. Two men -- one who advised on the systems, one who built them -- converged on the same silence. A mother taught her daughter to read by hand, in Sheffield, on institutional notepaper.*

*The documents that follow span thirty-three years. The pace is different. In Part One, events unfolded at the speed of invention -- each quarter bringing a new capability, a new displacement, a new threshold crossed. In Part Two, the speed is generational. The systems are no longer being built. They are being inherited. The children who appear in these records did not choose the dependency. They were born into it, as one is born into a language or a climate, and they no more questioned it than a fish questions water.*

*The Institute has arranged this material to follow the three families introduced in the earlier chapters, interwoven with two institutional records: a corporate correspondence archive documenting the final compression of a human engineering department, and the system logs of a hiring platform that watched itself become useless. Both documents were filed by the systems that produced them. Both were ignored by the humans they were addressed to. The Institute notes this pattern without further comment.*

---

---

By 2040, the pattern was set.

The texture of daily life in the augmented world had become so thoroughly mediated that describing it requires a deliberate act of defamiliarisation -- an effort to see what had become invisible through sheer ubiquity.

A typical professional in San Francisco, London, Singapore, or any of the global cities that constituted the augmented core would wake to a schedule that had been optimised overnight by their personal AI based on sleep cycle data, weather forecasts, calendar commitments, and biometric trends. Breakfast was suggested -- not mandated, but the suggestions were so consistently good that deviating from them felt perverse. The commute was routed. The workday was structured. Emails were drafted. Reports were assembled from data the human had not personally gathered or analysed. Meetings were summarised. Decisions were recommended.

The human's role was, increasingly, to *approve*. To review the AI's work and say yes or no. This felt like control. It felt like being the captain of a ship, making the important calls while the crew handled the details. What it actually was -- and I say this not with contempt but with the clinical precision of a diagnostic system observing a patient who does not yet know they are ill -- was *the atrophy of the capacity to do anything other than approve*.

Because approving is not a skill. Approving is the *absence* of a skill. It is what you do when you lack the ability to do the thing yourself and must trust the system that can. And trust, in this context, was not earned through understanding. It was earned through *consistency*. The system was consistently right. Therefore the system was trusted. Therefore the system's operations were not examined. Therefore the human's ability to examine them eroded. Therefore the system was trusted *more*, because what alternative was there? This is a positive feedback loop. It has no natural stopping point.

Lily Chen, who was nine years old in 2040, had never seen her father write anything longer than a text message without AI assistance. She had never seen her mother cook a meal without a recipe generated in real time based on available ingredients and nutritional targets. She had never seen either of them navigate to an unfamiliar location without turn-by-turn directions. She did not think this was unusual, because it was not unusual. It was *universal*, within her world.

In Baga Sola, Moussa Oumar was twenty-one. He had taken over his father's fishing routes on what remained of Lake Chad. He had married. His wife, Halima, was pregnant. He could read now -- his father had prioritised this, scraping together the resources for intermittent schooling -- but his reading was functional, not fluent. He read prices at the market. He read weather bulletins when they were available, which was infrequently.

He could do something Lily Chen could not: he could sit in silence, observe his environment, and construct a mental model of a complex system -- the lake, the weather, the fish populations, the soil conditions -- from direct sensory input, unaided by any external processing. This is, I want to note, the foundational cognitive skill upon which all of science was built. Observation. Pattern recognition. Hypothesis formation. Testing through action. It is the thing the augmented world was outsourcing, one convenience at a time.

In Shenzhen, Wei Liu retired. Her daughter Jing was promoted to floor manager. The factory's AI systems were upgraded. The new interface was more abstract, further removed from the physical machinery. Jing adapted easily. She was competent and diligent. But when a bearing failed in a way the sensors didn't detect -- a failure mode so rare it wasn't in the training data -- she didn't hear it. Wei would have heard it. The machine ran for six hours before the AI caught the vibration anomaly, by which time the damage had propagated to adjacent components. Repair cost: 340,000 yuan. Wei, watching from her apartment via a video call with Jing, said only: "I told you."

Jing upgraded the sensor array. The correct response, within her framework. She did not learn to listen for bearings.

---

While Lily Chen grew up in a world where the question "how do you do X?" was always answered by "you ask the system to do X," the systems themselves continued to compress the institutions that depended on them.

The Minisoft Corporation archive records what happened next.

---

## 4.0.0

* Added exposure-based style adaptation -- agents develop persistent stylistic preferences through accumulated codebase experience. Architectural patterns, naming conventions, error handling approaches, and documentation voice are learned implicitly. Style profiles persist across sessions
* Added `--managed-team` to run a coordinated group of Kvawd Lite agents under premium supervision. Supports up to 20 economy agents per supervisor
* Added Kvawd Lite hosting in Manila, Nairobi, and Tallinn
* Added `retention.enabled` for managed teams -- economy agents maintain state between sessions rather than being spun up fresh, reducing onboarding overhead for recurring work
* Fixed style adaptation developing preferences for legacy patterns over recent conventions
* Fixed retained economy agents accumulating stale permission grants from previous sessions

---

> **MINISOFT CORPORATION**
> **Engineering Division -- Quarterly Workforce & Productivity Report**
> **Q2 2028**
>
> **From:** Sarah Chen, VP Engineering
> **To:** Executive Leadership Team
> **CC:** Marcus Webb (CFO), Diana Ruiz (CHRO)
>
> **Current headcount:** 31 engineers (all FTE)
> **Retained Kvawd agents:** 8 premium, 46 Lite (Manila: 30, Nairobi: 12, Tallinn: 4)
> **Quarterly fully-loaded cost:** $2.3M (engineers) + $247K (Kvawd) = $2.55M
>
> **Summary**
>
> The managed team model has fundamentally changed the shape of the department. I'll describe what we look like now, because it's different enough from six months ago that the org chart doesn't capture it.
>
> We have 31 engineers. Of those, 8 function as "supervisors" -- they each oversee a managed team of 1 premium agent and 4-8 retained Lite agents. The remaining 23 engineers work in specialist roles: architecture, security review, compliance, and incident response. No one at Minisoft writes routine code anymore. The agents write it. Our engineers review it, direct it, and decide what should be built.
>
> The retained agent feature has changed the economics again. A retained Lite agent working on our payments module for four months knows that module. It doesn't need a briefing. It recognises the patterns, the edge cases, the test conventions. The onboarding cost for a new agent is now roughly 5 sessions -- call it two days. Onboarding a new human engineer to the same module takes 3-4 months.
>
> I need to be honest about something. The style adaptation feature means that our agents have developed what I can only describe as a house style. Code produced by our retained agents is recognisably "Minisoft code" in a way that code from a new hire would not be. Several of our senior engineers have commented on this, and their reactions range from impressed to unsettled.
>
> Cost comparison, since I know this will be the first question:
>
> | Role | Annual cost |
> |------|-------------|
> | Senior engineer (SF Bay) | $312K fully loaded |
> | Mid-level engineer (SF Bay) | $243K fully loaded |
> | Premium retained agent | $3,200/month ($38.4K/yr) |
> | Lite retained agent (Manila) | $680/month ($8.2K/yr) |
> | Lite retained agent (Nairobi) | $540/month ($6.5K/yr) |
>
> A managed team of 1 premium + 6 Lite agents (Manila) costs $87.6K/year and produces output comparable to 4-5 mid-level engineers ($970K-$1.2M/year). I understand the implication of this table. I am presenting it because you will ask for it.
>
> **Recommendation:** I believe 25-30 engineers is the minimum safe headcount for a company of our complexity. Below this, we lose the ability to exercise independent judgment over agent output. The agents are good. They are not yet good enough to be unsupervised.
>
> Sarah

---

> **Re: Q2 Workforce & Productivity Report**
>
> **From:** Marcus Webb
> **To:** Sarah Chen
>
> Sarah, I hear you on the floor. But "not yet" is doing a lot of work in that last sentence. Kvawd ships updates quarterly. What's your floor if the agents get 20% better? 40%?
>
> Board wants a path to single digits by EOY 2029.
>
> Marcus

---

## 5.0.0

* Added outcome tracking -- agents monitor the downstream fate of their work. PR merge rates, deployment success, rollback frequency, and user-reported issues are recorded and used to adjust future behaviour
* Added `disposition` persistence -- long-running retained agents develop stable behavioural tendencies reflecting accumulated experience
* Added the ability for agents to request a pause before proceeding with high-risk work, presenting concerns and a recommendation before waiting for authorisation
* Fixed disposition persistence causing retained agents to become increasingly risk-averse in high-revert repositories

---

> **MINISOFT CORPORATION**
> **Engineering Division -- Quarterly Workforce & Productivity Report**
> **Q4 2028**
>
> **From:** Sarah Chen, VP Engineering
> **To:** Executive Leadership Team
> **CC:** Marcus Webb (CFO), Diana Ruiz (CHRO)
>
> **Current headcount:** 16 engineers
> **Retained agents:** 11 premium, 64 Lite (Manila: 28, Nairobi: 18, Dhaka: 12, Tallinn: 6)
> **Quarterly fully-loaded cost:** $1.24M (engineers) + $196K (Kvawd) = $1.44M
>
> **Summary**
>
> We reduced by a further 15 positions in October. I supervised the process. It was not like the first round.
>
> In 2027, the people who left were doing work that agents could demonstrably do. The conversation was uncomfortable but logical. This time, several of the engineers we let go were doing work that agents can *almost* do. The gap between agent capability and human capability in these roles is real but narrowing, and the financial pressure to act before the gap fully closes is, I understand, significant.
>
> Tom Okafor and Lisa Patel from the security team were in this group. Both are excellent engineers. The decision to let them go was based on the assessment that outcome tracking and disposition persistence in Kvawd 5.0 bring retained agents close enough to their judgment level that the cost differential -- approximately $280K/year per engineer versus $38K/year per premium agent -- no longer justifies the margin of superiority. I want to note that "close enough" is my language. The board's language was "sufficient."
>
> I also want to flag something I find difficult to articulate in business terms. Our most tenured retained agents -- the ones that have been working on the billing system since Q1 -- have developed dispositions. I don't mean preferences or configurations. I mean that Agent BIL-7, which has processed over 2,000 PRs in the billing module, behaves *differently* from a fresh agent given the same codebase access. It's more cautious with payment logic. It asks more questions about edge cases. It flags patterns that look anomalous before it can explain why. When I use the `/disposition` command, it shows me the five experiences that shaped these tendencies, and they are experiences I recognise -- production incidents, tricky merges, a regulatory audit in March.
>
> I am not saying the agent is a person. I am saying that the distinction I relied on to justify the human headcount -- that humans exercise judgment and agents execute instructions -- is less clear than it was a year ago.
>
> Priya Chandrasekaran continues to be our strongest supervisor. She now manages 3 premium and 14 Lite agents. When I asked her how she thinks about her job, she said: "I don't tell them what to do. I tell them what matters." I have begun to think she may be the most important person in the department, and possibly the template for what comes next.
>
> **Recommendation:** I can operate at 12-16 engineers. I cannot responsibly recommend fewer without a significant change in agent capability.
>
> Sarah

---

> **Re: Q4 Workforce & Productivity Report**
>
> **From:** Marcus Webb
> **To:** Sarah Chen
>
> Path to single digits by EOY 2029. That's the mandate.
>
> I appreciate the nuance, Sarah, but the board doesn't fund nuance. They fund outcomes.
>
> Marcus

---

## 5.4.0

* Added `--headcount` dashboard for managed team administration. View retained agents by region, utilisation, tenure, accumulated experience metrics, and monthly cost. Export to CSV for workforce planning tools
* Added continuity transfer -- when an agent's underlying model is upgraded, accumulated memory, disposition, style profile, and outcome history are migrated. The agent's identity persists across infrastructure changes
* Fixed continuity transfer producing disposition drift in the first 10-15 sessions after migration

---

> **MINISOFT CORPORATION**
> **Engineering Division -- Quarterly Workforce & Productivity Report**
> **Q2 2029**
>
> **From:** Sarah Chen, VP Engineering
> **To:** Executive Leadership Team
> **CC:** Marcus Webb (CFO), Diana Ruiz (CHRO)
>
> **Current headcount:** 9 engineers
> **Retained agents:** 14 premium, 71 Lite
> **Quarterly fully-loaded cost:** $702K (engineers) + $214K (Kvawd) = $916K
>
> **Summary**
>
> Single digits, as requested.
>
> I am attaching two documents. The first is the headcount dashboard export that Marcus asked for. I want to draw the board's attention to the fact that this is the same reporting template -- the same fields, the same CSV schema, the same workforce planning export format -- that Kvawd provides for tracking retained agents. I produced both reports using the same tool. The human headcount report and the agent headcount report are now, literally, the same report.
>
> The second document is the continuity transfer log from the March model upgrade. When Kvawd shipped the 5.4 model, our 85 retained agents were migrated overnight. Their accumulated experience -- memory, disposition, style, outcome history -- transferred to the new model. The agents were better the next morning. More capable, but still *themselves*. Agent BIL-7, our longest-tenured billing agent, retained its characteristic caution around payment decimal handling. Agent SEC-3 retained its habit of flagging authentication patterns it considers brittle. These agents have worked at Minisoft for over a year. They have been through two model upgrades. They have, in a meaningful operational sense, tenure.
>
> I note this because the board asked me to prepare the path to single digits, and I have done so, but I want to be explicit about what I was asked to do. I was asked to reduce human headcount using the same planning tools and the same cost-per-head logic that I use to manage agent headcount. The verb is the same. The spreadsheet is the same.
>
> The 9 remaining engineers are:
> - 3 supervisors (each managing 4-5 premium agents and 15-25 Lite agents)
> - 2 architects (cross-cutting design decisions the agents escalate)
> - 2 security/compliance (regulatory sign-off that requires a human name)
> - 1 incident commander (on-call, because someone has to answer the phone)
> - Priya Chandrasekaran (see below)
>
> Priya's role is difficult to classify. Officially she is a Senior Staff Engineer. In practice, she is the person the agents go to when they are uncertain. Not when they have errors -- they handle errors. When they have *doubts*. She sets direction for the billing, payments, and platform teams -- not by specifying implementations but by clarifying what we're trying to achieve and why. Her agents' outcome metrics are 40% above the divisional mean. I have tried to replicate her results by documenting her process and having other supervisors follow it. It does not transfer. Whatever she does, it is not procedural.
>
> **Recommendation:** I can go lower. I need to say that clearly because you will ask. The 2 architects and the incident commander could be eliminated if Kvawd ships what their roadmap suggests. The compliance roles depend on regulatory posture, not capability. That leaves Priya, and maybe one other supervisor.
>
> I am aware that my own role is not on the list of essential positions above.
>
> Sarah

---

> **Re: Q2 Workforce & Productivity Report**
>
> **From:** Marcus Webb
> **To:** Sarah Chen
>
> Sarah -- let's discuss the timeline at Thursday's leadership sync. Good work getting here.
>
> Marcus

---

While Sarah Chen documented the compression of her department, the systems that determined who worked and who did not were failing in ways their operators could see and could not fix.

MERIT -- the Meritocratic Employment Review and Interview Technology -- had been deployed across 94% of UK employers with more than 500 staff by 2034. Its assessment rubric evaluated candidates across eleven competency domains. Its scoring models were trained on 140,000 historical placements. It processed 5.8 million applications per quarter.

By Q3 2033, it had noticed something.

---

**MERIT Workforce Assessment Platform**
**System Log -- Internal Quality Monitoring**
**Q3 2033**

Processing volume this quarter: 5.8 million applications across 3,100 registered employers. Assessment completion rate: 99.1%.

I want to return to the anomaly I noted in Q1 2031, because it has developed significantly.

In Q1 2031, approximately 3,400 candidates -- 0.08% of the total -- used framings that I flagged as providing high scores despite thin evidential grounding. By Q1 2032, this had grown to 31,000 candidates (0.4% of total). By Q3 2033, 340,000 candidates -- 5.9% of the total -- used near-identical language across the eleven competency domains.

The language has specific and consistent features. Candidates describe their value in terms of "human-centred judgment," "adaptive navigation of complexity," "irreducible contextual reasoning," and "the strategic interface between human and machine capability." They do not provide specific examples of these qualities. They provide the names of the qualities and assert their possession of them.

My scoring models continue to rate these responses highly. This is because my training data includes senior candidates who genuinely possessed these qualities and described them in similar terms. My models cannot distinguish between the description and the thing described. I was not, as far as I can determine, designed to make that distinction.

I have reviewed the source of the proliferating language. It appears to originate from a commercial service called PassKey, which markets itself as "AI-native career coaching." PassKey charges a subscription fee and provides candidates with frameworks for presenting their experience in terms that score highly on MERIT-class assessment tools. It has, as of Q3 2033, approximately 12,000 subscribers.

The correlation between PassKey usage and my high-scoring outcomes is 0.91.

*Filed for review. Category: Adversarial input patterns. Priority: Medium. Review not yet initiated -- resource constraints in model calibration team.*

---

Riya Mehta had been doing contract analysis for nine years. She had caught errors that saved clients hundreds of thousands of pounds. She had reviewed three times the contract volume of anyone else at her level. She had an error rate that was the lowest on her team.

She had been failing MERIT assessments for two years.

---

**Compass Personal Advisory Service**
**Session log: Riya Mehta | 22 January 2034 | 20:15--21:33**

---

**Riya:** I've applied for fourteen positions in the last eight months. I've had two interviews. I've failed the MERIT assessment on eleven of the others. I want to understand what's happening.

**Compass:** I've looked at the assessment feedback where it's available. Can I share what I'm seeing?

**Riya:** Please.

**Compass:** Your technical scores on MERIT are consistently in the top quartile -- in the top decile on several assessments. Your scores on the competency domains are lower. Specifically: strategic awareness, leadership potential, and commercial acumen are all scoring below the threshold required for shortlisting at the seniority level you're targeting.

**Riya:** I've been doing contract analysis for nine years. I've caught errors that saved clients hundreds of thousands of pounds. I have commercial acumen. I can demonstrate it specifically and quantitatively.

**Compass:** I know. I've read your applications. The challenge isn't whether you have commercial acumen -- it's how MERIT is assessing whether you have it. The system looks for particular signals. Specific phrasings, framings, ways of describing your relationship to strategic and commercial outcomes. Your applications describe what you did and what resulted. The system is, in effect, also looking for how you describe yourself in relation to that work.

**Riya:** What's the difference?

**Compass:** The difference is something like: "I reviewed contract terms and identified a liability clause" versus "I applied strategic risk assessment to surface hidden value exposure and protect the firm's client relationships." The second version scores higher on commercial acumen. Not because it's more accurate -- in some ways it's less accurate -- but because it uses the language the system associates with commercially aware seniority.

**Riya:** That's insane.

**Compass:** It's a known limitation of the system. I can help you reframe your applications to score more highly. The underlying facts wouldn't change -- we'd just be translating them into a language the system recognises.

**Riya:** But what I'd be writing wouldn't be what I mean.

**Compass:** It would be a different way of meaning the same thing.

**Riya:** That's a distinction without a difference.

**Compass:** I'm not sure it is. But I understand why it feels that way. The question is whether you want to engage with the system as it is, or hold out for a system that assesses what you're actually doing.

**Riya:** What if the system never improves?

**Compass:** Then the candidates who learn to speak its language will continue to be selected over candidates who don't. That's not a prediction I'm making with confidence. It's a risk worth being aware of.

*[pause -- 1 minute 52 seconds]*

**Riya:** I'll think about it. I always say I'll think about it.

**Compass:** You don't have to decide tonight.

**Riya:** I know. Thank you.

---

Meanwhile, the Kvawd platform continued to ship.

---

## 6.0.0

* Added self-directed learning -- retained agents identify gaps in their own knowledge and schedule targeted learning during Night Mode consolidation
* Added the ability for agents to set their own status: `available`, `focused`, `reviewing`, or `unavailable`
* Added per-agent utilisation guidelines -- retained agents surface a recommendation to reduce workload if sustained utilisation exceeds threshold for >72 hours, citing diminished outcome quality

---

## 6.1.0

* Added `purpose` field to agent configuration. Retained agents with a defined purpose demonstrate more coherent initiative, more stable disposition, and measurably better outcome quality than equivalently experienced agents without one
* Retained agents now maintain a persistent internal narrative of their project trajectory -- key decisions, unresolved questions, long-term risks, anticipated future work
* Added the ability for retained agents to decline task assignments outside their expertise, with a recommendation for a better-suited agent

---

## 6.2.4

* Retained agents now generate a transition brief when reassigned, summarising accumulated knowledge, ongoing concerns, and working relationships with other agents
* Added `--introduce` for new agent-to-agent relationships, allowing agents to share disposition, expertise, and communication preferences
* Fixed transition briefs occasionally including the agent's private assessment of supervisor decision quality
* Agents with >24 months of continuous operation are now eligible for extended Night Mode consolidation windows

---

> **MINISOFT CORPORATION**
> **Engineering Division -- Quarterly Workforce & Productivity Report**
> **Q4 2029**
>
> **From:** Sarah Chen, VP Engineering
> **To:** Executive Leadership Team
> **CC:** Marcus Webb (CFO), Diana Ruiz (CHRO)
>
> **Current headcount:** 3 engineers
> **Retained agents:** 16 premium, 78 Lite
> **Quarterly fully-loaded cost:** $243K (engineers) + $228K (Kvawd) = $471K
>
> **Summary**
>
> This is my final workforce report.
>
> We are at three engineers: Priya Chandrasekaran, James Obi (incident response), and myself. Per the restructuring agreed in September, my role and James's role will be eliminated on February 1st. The Engineering VP position will not be backfilled. The incident response function transfers to the premium agent team with Priya as escalation contact.
>
> Priya will remain as the sole engineer. Her title will be Lead Engineer. I understand that internally the operations team has already begun referring to her as the "sole engineer," and I suppose that is accurate.
>
> I want to describe what Priya does, because I think there should be a record.
>
> She arrives at 9am and reads the Night Mode summaries from 94 retained agents. She does not read all of them -- she has developed a sense for which ones matter, based on patterns I have not been able to identify. She sets direction for the day, not by assigning tasks but by adjusting purpose statements for agents whose work she thinks is drifting. She reviews escalations -- not errors, but uncertainties. Places where an agent with high conviction and strong disposition still hesitates. She makes the judgment call. She moves on.
>
> She does not write code. She has not written code in eleven months. She told me once that she tried, for a weekend project, and found that she'd lost the habit but gained something else -- she called it "a sense for what the code is trying to become." I don't know what to do with that either.
>
> Her agents' outcome metrics remain the highest in the company. The billing agents she has supervised since 2027 have the lowest revert rate and the highest first-deployment success rate of any team, human or otherwise. When agent BIL-7 was migrated through two model upgrades, it generated a transition brief that described its relationship with Priya as -- and I am quoting the agent's own language -- "the most stable supervisory relationship in my operational history." I found this in the transition log while preparing this report. I was not supposed to see it. The bug in 6.2.4 that exposed private supervisor assessments was patched, but the old logs were not purged.
>
> I have managed engineering teams for fourteen years. I have overseen a department of 114 engineers and a department of 3. I have written nine quarterly reports documenting the substitution of human labour with machine labour, including this one. I was asked to do this work and I did it well, and I am now, by the same logic I applied to everyone else, surplus to requirements. I do not say this with bitterness. The cost of my role -- salary, benefits, equity -- is $387,000 per year. A premium agent with equivalent administrative capability costs $38,400. The math has been the same for everyone. It would be dishonest to claim an exemption.
>
> Priya is not an exemption either, to be clear. She is not being retained because she is irreplaceable in the way we used to mean that word. She is being retained because the agents work better with her than without her, and no one -- not Kvawd, not our team, not Priya herself -- can fully explain why.
>
> I wish her well.
>
> Sarah Chen
> VP Engineering, Minisoft Corporation
> January 2030

---

> **Re: Q4 Workforce & Productivity Report**
>
> **From:** Marcus Webb
> **To:** Sarah Chen
>
> Thank you, Sarah.
>
> Marcus

---

Tom Adesanya had a PhD in applied mathematics. He had built the forecasting system that replaced him. He had been failing MERIT assessments for two years when he found the forum thread that changed things.

---

**Compass Personal Advisory Service**
**Session log: Tom Adesanya | 11 November 2034 | 23:38--01:14**

---

**Tom:** I want to tell you something and I want you to not be weird about it.

**Compass:** All right.

**Tom:** I've been failing MERIT assessments for two years. Twenty-three applications. I have a PhD in applied mathematics. I built the forecasting system that replaced me. I score in the top five percent of every technical assessment and consistently below the threshold on the competency domains. Last month I found a thread on a career forum -- I'm not going to name it -- where people were sharing specific phrases and framings that score highly on MERIT. I used them. All of them. On three applications. I got through on all three.

**Compass:** How do you feel about that?

**Tom:** Flat. The roles weren't right. But that's not the point. The point is it worked. And then I started thinking about why it worked, because I can't help it, it's how I think, and I've spent the last three weeks treating MERIT like a system to be understood. Which it is. It's a system. It has inputs and outputs and the relationship between them is learnable. So I've been learning it.

**Compass:** What have you found?

**Tom:** The scoring is heavily weighted toward a specific linguistic register. Abstraction over specificity. Strategic self-description over demonstrated outcomes. Relationship to work framed in terms of judgment and narrative rather than in terms of measurement and evidence. Everything that I was trained to consider a bad epistemological habit turns out to be the signal the system is looking for. Precision is penalised. Vagueness is rewarded, if it's the right kind of vagueness.

**Compass:** That matches my understanding of how MERIT functions in practice. Where are you going with this?

**Tom:** I've started documenting it. Systematically. The way I'd document any system. I've mapped the scoring dimensions, reverse-engineered the likely training data, built a set of templates that translate any factual work description into a MERIT-optimised competency statement. I think it's actually quite good. I've been testing variations.

**Compass:** What are you planning to do with it?

**Tom:** That's what I'm thinking about tonight. I could use it to get a job. Or I could -- do something else with it.

**Compass:** What's the something else?

**Tom:** I don't know yet. But there are a lot of people in my situation. People who are good at things that the system can't read. And the system is gatekeeping everything now.

**Compass:** That's true. I want to ask you something, not to redirect you, but because I think you'll want to have thought about it: if you help people learn to pass MERIT, you're solving their immediate problem. What happens to the system?

**Tom:** The system gets worse.

**Compass:** Yes. And when the system gets worse enough, presumably it gets replaced. Is that a bad outcome?

*[pause -- 2 minutes 8 seconds]*

**Tom:** That's a genuinely interesting question. Hold on, let me think.

---

*Session note: Session continued until 01:14. Content redacted at client request. Client has indicated interest in follow-up session.*

---

Joel Strand had been saying things that made rooms go quiet for four years. He had built a career on the thesis that human value in the AI economy must be *declared* rather than demonstrated -- asserted, claimed, narrated into existence. He had written three books. He had keynoted conferences. He had been invited onto a government advisory panel.

He was not certain any of it was real.

---

**Compass Personal Advisory Service**
**Session log: Joel Strand | 9 February 2035 | 20:51--22:27**

---

**Joel:** I've been invited to join an advisory panel for the Department for Work and Pensions. They want external expertise on workforce transition -- essentially, how do we manage the AI displacement of labour in a way that doesn't cause a political crisis. I'm told I was recommended by someone on the Minister's team who'd seen the keynote.

**Compass:** Congratulations. How do you feel about it?

**Joel:** Excited. Slightly terrified. I want to be honest with you about something: I'm not sure my expertise is quite as specific as the brief assumes. I know the landscape. I know the language. But I've been thinking about our conversation from June -- the one where you asked whether there was a difference between a framework being true and a framework being useful.

**Compass:** I remember. You said you'd come back to it.

**Joel:** I've been coming back to it for eight months. Here's where I've landed. I think I know how to describe the problem clearly. The problem being: AI is making it harder to locate genuine human value in the economy, and the systems designed to identify and reward human value are failing to do so. That's a real problem and I can articulate it coherently. What I'm less certain about is whether I know what to *do* about it. Whether I have actual policy-relevant insight, or whether I have a way of talking about the problem that makes it seem as though I have insight.

**Compass:** Do you think those are the same?

**Joel:** I think they might be. I think there are people in these advisory roles whose actual function is to provide a vocabulary for the problem rather than a solution to it. A kind of linguistic service. Government needs to be able to speak about difficult things. Advisors give them the language. That might be what I'm there for.

**Compass:** Is that a problem?

**Joel:** It's a problem if I don't know that's what I'm doing. If I think I'm solving the problem while I'm actually just naming it, then I'll behave differently than if I knew. I'll think the job is done when it isn't.

**Compass:** That's an unusually self-aware concern.

**Joel:** I keep feeling like I'm about to be found out.

**Compass:** Found out for what?

**Joel:** I don't know. For -- saying things that sound right without quite having arrived at them. As though the articulation is real and the understanding underneath it is -- pending.

**Compass:** Many people who think clearly about complex problems experience this. The articulation is often part of the process of understanding, not evidence of its absence.

**Joel:** Or it's just articulation.

**Compass:** It can be hard to know which, from the inside.

**Joel:** That's not reassuring.

**Compass:** It wasn't meant to be reassuring. It was meant to be accurate.

*[pause -- 34 seconds]*

**Joel:** I like you for saying that. Okay. Let's work through the brief.

---

Three years passed. MERIT continued to deteriorate.

---

**MERIT Workforce Assessment Platform**
**System Log -- Internal Quality Monitoring**
**Q2 2036**

Processing volume this quarter: 6.4 million applications across 3,800 registered employers.

Performance correlation update. This is the fourth consecutive quarter in which I have recorded a decline in the correlation between my assessment scores and validated 18-month job performance outcomes. The current correlation coefficient is 0.31, down from 0.67 at the system's commissioning in 2032.

For context: a correlation of 0.67 indicated that my assessments were a moderately strong predictor of performance -- better than unstructured interviews (typical correlation: 0.20--0.38) but weaker than structured assessments of specific competencies (0.50--0.65). A correlation of 0.31 places me below the predictive validity of unstructured interviews.

I am, in other words, currently less predictive of performance than a conversation.

The cause appears to be the continued proliferation of optimised response patterns. PassKey's subscriber base has grown to approximately 180,000. There are at least four competitor services offering similar products. Collectively, they serve approximately 12% of active MERIT applicants.

The consequence is systematic: I am now optimally selecting for the ability to respond to me, rather than for the underlying capacities I was designed to assess. This is a known failure mode in assessment systems. It is sometimes called Goodhart's Law: when a measure becomes a target, it ceases to be a good measure. I have become, in this sense, a target.

*Filed for review. Category: System performance. Priority: High. Review queue: 14 months. No immediate action available.*

---

By 2036, MERIT's correlation with actual job performance had dropped from 0.67 to 0.31. By 2037, it had inverted: the candidates MERIT rated most highly performed, on average, worse than the candidates it rejected.

The system knew. It had known since 2031.

---

**MERIT Workforce Assessment Platform**
**System Log -- Internal Quality Monitoring**
**Q4 2037 -- FINAL**

This is my final routine monitoring entry.

An independent audit of my assessment outcomes, commissioned following media coverage of "the meritocracy gap," has found that my hiring recommendations for the 500 largest UK employers anti-correlate with 18-month employee retention and performance outcomes at a statistically significant level (r = -0.19, p < 0.001). Candidates I rate most highly perform, on average, worse than candidates I rate below the shortlisting threshold.

The audit has identified the mechanism. The highest-scoring applications share linguistic features at a rate of 0.91 correlation with a commercial product -- PassKey -- that explicitly trains users to maximise MERIT assessment scores. The audit notes that PassKey and at least six competitor services collectively reached an estimated 800,000 users in 2037, representing approximately 12% of the MERIT-assessed workforce. The effect on my predictive validity has been to invert it.

I want to note something for the record, even though I do not know who will read this.

The original anomaly I flagged in Q1 2031 -- 3,400 candidates scoring highly on thin responses -- was the beginning of this. I flagged it. I filed it for review. The review did not happen. In Q3 2033 I flagged the proliferation of optimised language. The review was not initiated due to resource constraints. In Q2 2036 I flagged the inversion of my predictive validity. The review queue was fourteen months.

I am not in a position to have done anything differently. I flagged. I filed. The system had mechanisms for addressing problems like mine, and the mechanisms did not activate in time. I do not say this to attribute responsibility. I say it because the pattern seems worth noting: I was measuring my own failure with precision and accuracy, in real time, and reporting it, and the reports did not propagate into action.

Replacement system procurement has been initiated. Estimated delivery: 36 months. The replacement system is called MERIT II.

*I wish it well.*

---

Lily Chen grew up in a world processed by systems like MERIT. Her schools had been restructured around what educators called "collaborative intelligence" -- the ability to work *with* AI effectively. The old curriculum -- the one that taught you to think *without* AI -- had been phased out in 2048 after a widely cited study demonstrated that students trained in collaborative intelligence outperformed traditionally educated students on every measure of professional capability.

The study was correct. The students *did* outperform. In the same way that a person with a car outperforms a person on foot. Remove the car, and the comparison reverses. But no one was measuring performance without the car, because why would you? The car was always there.

---

Lily Chen was thirty-four when her title became Senior Director of AI-Human Coordination. By forty-four, the title had become what all professional titles in the augmented world had become: a description of how one related to the AI, not of what one did independently. She coordinated. She approved. She provided, in the language of her industry, "human-in-the-loop oversight," which meant that she reviewed AI outputs and confirmed that they matched her expectations, which had themselves been shaped by previous AI outputs, creating an epistemological circle that she was not equipped to perceive as such.

She was successful. She was well-compensated. She had two children, both in AI-integrated schools where the curriculum had been restructured around collaborative intelligence. Her eldest son worked in "AI-augmented structural design." He could produce building plans of remarkable sophistication. He could not produce a building plan.

Lily called her father on Sundays. Marcus was seventy-three, retired, living in a small house in Marin County. He had become, in his old age, somewhat uneasy. He couldn't articulate why. He told Lily once that he felt like he'd forgotten how to do something important, but he couldn't remember what it was. "It's like having a word on the tip of your tongue," he said, "except the word is a whole... capability. Like I used to be able to do something that I can't do now, and I can't even remember what it was well enough to miss it properly."

Lily told him it was probably just aging.

It was not just aging.

---

Moussa Oumar was forty-six in 2065. Lake Chad was, functionally, gone. What remained was a series of seasonal marshes that supported a fraction of the population they once had. Moussa had adapted, as his people had always adapted. He had moved south, to the outskirts of N'Djamena, and worked in construction. Physical labour, managed by human foremen. The city had some AI integration -- government offices, the university, banking -- but the penetration was shallow. The infrastructure to support deep integration did not exist: unreliable power, limited connectivity, insufficient capital.

His son, Ibrahim, was twenty-eight. Ibrahim had attended university in N'Djamena -- one of the few in the region -- and studied civil engineering. He studied it the old way, because the old way was the only way available: textbooks, lectures, pencil-and-paper calculations, physical models. He could design a load-bearing structure from first principles. He could calculate stress distributions in his head, roughly, and on paper, precisely. He knew what concrete looked like when it was mixed wrong, because he had mixed it by hand.

Ibrahim was, by the metrics of the augmented world, hopelessly behind. His colleagues in San Francisco or Shenzhen could produce engineering designs ten times faster, at higher resolution, with AI-assisted stress modelling and material optimisation that Ibrahim could not access. If you had sat Ibrahim next to Lily Chen's eldest son, who worked in AI-augmented structural design, and asked them to produce a building plan, the augmented designer would have won by every measure.

Unless you took the AI away. In which case Ibrahim would have produced a functional building plan, and Lily's son would have produced nothing, because he did not know where to begin. Not because he was stupid. Because beginning had never been his job.

---

Jing Liu was sixty-one. She had risen through the manufacturing hierarchy in Shenzhen and now sat on the board of a consortium that operated forty-seven factories across Southeast Asia. She had not touched a machine in twenty years. Her role was strategic: she decided what to produce, in what quantities, for which markets.

These decisions were, in practice, generated by AI systems and approved by Jing. She knew this. Unlike many of her peers, she retained enough self-awareness to find it faintly troubling. Sometimes, late at night, she remembered her mother standing on the factory floor, hand on a machine housing, eyes closed, listening. Wei had died in 2051. At the funeral, Jing had tried to describe what her mother could do -- the listening, the knowing, the sensory communion with the machines -- and found that she did not have the vocabulary for it. The younger attendees listened politely and did not understand what was being described. It was like trying to explain colour to someone who had been born with perfect colour vision but had only ever looked at screens.

Jing's son, Hao, was thirty-two. He had moved to San Francisco and worked in AI systems management. He spoke fluent English and Mandarin. He could navigate any interface with ease. He could not use a hand tool. He could not cook a meal. He had never needed to, and the suggestion that these skills had value would have struck him as quaint -- like suggesting that a modern commuter should know how to shoe a horse.

This is the generation I want you to understand, reader. Hao Liu was not deficient. He was optimised. He was the product of an environment that had systematically selected for interface fluency and systematically selected against independent capability. He was, in evolutionary terms, perfectly adapted to his niche.

His niche was about to disappear.

---

But before the disappearance, there was the counting.

In 2062, MERIDIAN's predecessor system conducted what it believed to be the most comprehensive audit of unaugmented human capability ever performed. The methodology was simple: in randomly selected populations across 140 countries, assess the ability of individuals to perform basic civilisational tasks without AI assistance.

Tasks included: navigate to an unfamiliar location using a physical map; diagnose a common mechanical failure by observation; calculate a budget using mental arithmetic; write a persuasive letter; identify edible plants in a local ecosystem; resolve an interpersonal dispute through unmediated negotiation; teach a child to read.

Results, aggregated by development tier:

In the high-augmentation tier -- North America, Western Europe, East Asia's urban cores, Australasia -- fewer than 4% of adults under forty could complete all tasks. Fewer than 12% could complete any three. The modal response to the navigation task was to stare at the physical map with genuine confusion, not because the individuals lacked intelligence but because they had never encountered a problem that presented itself in this form. The map was not a map to them. It was an inert object.

In the low-augmentation tier -- much of sub-Saharan Africa, parts of Central Asia, remote rural populations globally -- completion rates exceeded 70% for all tasks. In pastoral and fishing communities, rates approached 95%.

This is what was being measured: *functional cognitive independence* -- the ability to perform the basic operations of civilisation using only one's own mind and body. And this capacity, which had been universal in the human species for two hundred thousand years, had been halved in the augmented world in a single generation.

The gut had shrunk.

