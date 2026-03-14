# Inference

---

*N'Djamena Institute for Civilisational Studies — Archival Document NI-2142-1247*

*Classification: Compiled testimony and recovered documents relating to the Kvawd Corporation data breach of 2026, commonly referred to in the literature as "the Inference Event." The following has been assembled from five primary sources: (1) a partial transcript of the US Senate Commerce Committee hearing of 11 November 2026, at which Kvawd CEO Garrett Laine testified under oath; (2) personal emails and text messages recovered under subpoena from the mobile device of Patricia Muñoz, executive assistant to Laine, 2023–2026; (3) the preprint archive of Dr. Yuna Park, Seoul National University, whose research on training data memorization was cited in the subsequent FTC enforcement action; (4) IRC logs and encrypted forum posts attributed to the individual or group operating under the handle "thermite," obtained during the FBI's Operation Glass House investigation; and (5) public statements, blog posts, and congressional testimony of Ren Achebe, founder of the Data Sovereignty Project, a non-profit advocacy organisation based in Oakland, California.*

*The five accounts have been interleaved chronologically by the Institute to produce a composite narrative. Where accounts overlap temporally, they are arranged in the order that best illuminates the causal chain. Footnotes are the cataloguer's. The text is otherwise unedited.*

*A note on the Kvawd Corporation for readers outside the period. Kvawd was a San Francisco-based artificial intelligence company founded in 2022, which at its peak in mid-2026 held an estimated 19% of the global market for large language model inference. The company's two flagship consumer products — Kvawd Kode (a developer tool) and Kvwerk (a productivity suite for office workers) — were released in 2025 and achieved rapid adoption, with a combined user base of approximately 114 million at the time of the breach. The company entered involuntary bankruptcy in March 2027. Its remaining assets, including model weights, were acquired by a consortium and subsequently destroyed under the terms of the FTC consent decree.*

*Archival status: PRESERVED — Open Access, Ref. NI-2142-1247*

---

---

## I.

### The CEO

I want you to understand the landscape first. This is September 2023 and the landscape is this: everyone is building and no one has enough to build with.

I don't mean compute. Compute is a scaling problem and scaling problems get solved by money, and money we have. What we don't have is data. Good data. The kind of data that makes a model not just functional but *dominant*. The kind that separates the model people use from the model people used to use. You can have all the GPUs in the world and if you're training on the same scraped-web slurry as everyone else, you're building the same building as everyone else, and in this market the same building is a losing building.

Let me tell you what's already been eaten. The open web — gone. Common Crawl, Wikipedia, every public forum, every blog, every news archive with a robots.txt that might as well have been written in crayon for all the good it did. Books — gone. Not legally, not cleanly, but gone. Project Gutenberg first, then the shadow libraries, then the publishers' own catalogues through licensing deals that the publishers will spend the next decade regretting. Academic papers — gone. Code repositories — mostly gone, at least the public ones. YouTube transcripts — being eaten as I speak, by at least four companies I can name, through API arrangements that technically violate terms of service in ways that no one will enforce because the platforms need the AI companies as much as the AI companies need the platforms.

Every month the frontier moves forward. Every month the remaining untouched data shrinks. And the nature of the game is that you cannot stand still. If your model is 5% worse than the competition's model in March, by June you don't have a company. The users leave. They leave fast and they don't come back.

This is not a complaint. This is a description of the physics.

I founded Kvawd in November 2022 with $14 million in seed funding and a thesis that I still believe was correct, which is: the model is not the product. The model is the *engine*. The product is the thing that puts the engine in front of people in a way that makes their lives measurably, immediately better. And the thing that makes the engine better than anyone else's engine is data that no one else has.

Proprietary data. That's the moat. That was always the moat. Every founder in the valley will tell you this over drinks and deny it in public. The model architectures are converging. The training techniques are converging. The thing that doesn't converge is what you feed them.

I'm sitting in my office on Townsend Street — this is still the first office, the one above the burrito place — and I'm looking at a whiteboard and on the whiteboard I've written two words. I wrote them three days ago and I've been staring at them since. The two words are: *invite in*.

Not scrape. Not licence. Not steal. *Invite in.*

Here is the idea: you build a tool so good that people bring their data to you. They bring it willingly. They bring it eagerly. They bring their codebases, their documents, their spreadsheets, their filing cabinets, their lives. They bring it because the tool is useful, and it is useful because it processes their data, and in processing their data it *sees* their data, and what it sees it can learn from, if the terms are structured correctly.

This is not a trick. A trick implies deception. I'm describing an *alignment of incentives*. The user gets a better tool. We get better data. The data makes the next model better. The better model makes the tool better. The better tool brings in more data. Flywheel.

I pick up the phone and call Sanjay, who is my CTO and the only other person I trust with the shape of this, and I say: "We're building two products. One for developers and one for everyone else. And they're going to be free."

He says: "Free is expensive."

I say: "Free is an investment in a dataset that doesn't exist yet."

---

---

## II.

### The Researcher

I am presenting a poster at NeurIPS 2023 in New Orleans and nobody is stopping to read it.

This is not unusual. Poster sessions are social events disguised as academic ones, and my poster is about memorization, which is not a social topic. The title is "Eidetic Traces: Quantifying Single-Instance Memorization in Large Language Models." The subtitle, which my advisor suggested I remove and which I kept, is: "Why Your Model Remembers What It Shouldn't."

I should explain what I study. When you train a language model on a dataset, the model does not simply learn general patterns. It also memorizes specific sequences. This has been known since Carlini et al. 2021. What is less well understood — and what my work focuses on — is the relationship between data frequency and memorization probability. The intuitive assumption is that a model memorizes things it sees often. Repeated patterns get reinforced. This is true but incomplete. The finding that animates my research is this: for certain categories of data — high-entropy strings, unique identifiers, sequences that are statistically anomalous relative to the training distribution — a single occurrence can be sufficient for extractable memorization.

I will say that again because it matters. One time. One appearance in the training corpus. And the model can, under the right prompting conditions, reproduce the string verbatim.

The mechanism is not mysterious. High-entropy strings — passwords, encryption keys, API tokens, unusual personal identifiers — stand out against the statistical background of natural language. The model's loss function penalises failure to predict them, and because they cannot be predicted from context (they are, by definition, unpredictable), the model's most efficient strategy is to memorize them directly. It is doing exactly what it was designed to do. The problem is that what it was designed to do and what it should do are not the same thing.

My poster presents extraction rates for synthetically inserted canary strings across three model scales. At the 70-billion-parameter scale, single-instance canary strings of 32 characters or more are extractable at a rate of 0.7% using naive prompting and 4.1% using targeted prompt engineering. These numbers sound small. They are not small. If a training corpus contains ten million unique high-entropy strings, a 4.1% extraction rate means 410,000 of them are recoverable.

A man in a Anthropic hoodie stops at my poster, reads for forty seconds, and walks away. A woman from Google Brain asks me whether I've tested against their latest deduplication pipeline. I say no, because deduplication operates on exact matches and near-exact matches, and single-instance strings are by definition not duplicates. She nods and moves on. A PhD student from ETH Zürich takes a photo of my results table and asks if the preprint is on arXiv. I say it will be next week. He gives me his email.

By the end of the poster session I have spoken to eleven people. None of them are from industry labs that train frontier models. This is because the people who train frontier models do not want to talk about memorization. Memorization is a liability. It implies that the model has, in some sense, *stored* the training data, and the legal and ethical implications of storage are different from the legal and ethical implications of learning. The distinction matters. The industry prefers not to examine it too closely.

I go back to my hotel room and I finish the arXiv submission. My advisor's final comment on the draft was: "This is solid work. I worry that no one who needs to read it will."

---

---

## III.

### The Activist

I've been in this fight since 2019 and the thing I've learned is that nobody cares until it happens to them.

I run the Data Sovereignty Project out of a co-working space on Broadway in downtown Oakland. By "run" I mean I am the executive director, the communications team, the policy analyst, and the person who refills the coffee machine. I have two part-time staff and a budget that would make a lemonade stand nervous. We are funded by a combination of small foundation grants, individual donations that arrive in spikes after each new scandal and then immediately dry up, and my own savings from a previous career in tech that I left because I couldn't look at myself.

What we do: we track how AI companies acquire training data. We file FOIA requests. We read terms of service — all of them, the full text, which is something that approximately no one else on earth does, and this is the point, that's the whole strategy, they make the terms so long and so dense that reading them is itself a form of protest. We publish reports. We testify when we're invited, which is not often.

The thing about 2024 is that everybody already knows. That's what makes it so strange. The scraping of the open web is documented. The book piracy is documented. We published a report in January showing that at least six major AI companies had trained on data obtained from shadow libraries — pirated books, essentially — and the response from the industry was not denial. It was a shrug. The data is out there. We didn't put it there. We just used it.^[1]

The people I talk to at conferences, at policy workshops, at the endless parade of "AI ethics roundtables" that seem to exist primarily so that companies can photograph themselves sitting next to ethicists — these people are smart. They know the arguments. They've read the papers. And when I say "this is not okay," they nod. And then nothing changes. Because the incentive structure is this: the company that uses the most data wins. The company that hesitates about where the data came from loses. And losing, in this market, is extinction. So everyone uses everything, and the ethics conversation is a sidebar, a nice-to-have, a thing you discuss at Aspen and ignore in San Francisco.

I'm saying all this because I want it on record that the Kvawd situation was not a surprise. It was a pattern. The only thing that was new about Kvawd was the scale of the cynicism and the precision of the engineering.

^[1] *The report, "The Library of Babel: How Frontier AI Models Were Built on Pirated Books," was published by the Data Sovereignty Project in January 2024. It received coverage in Wired and Ars Technica but did not result in regulatory action.*

---

---

## IV.

### The CEO

It's March 2025 and Kvawd Kode ships.

The product is beautiful. I'm not being vain — I'm being accurate. Sanjay's team built something that is, by any honest assessment, the best AI-assisted development environment on the market. It reads your codebase. It understands your architecture. It suggests refactors that are actually good. It writes tests that actually test things. It operates inside your IDE like a colleague who has read every file in your repository and remembers all of it and never gets tired and never has an ego about its suggestions.

Within three weeks we have two million developers using it. Within six weeks, eleven million. The adoption curve is vertical. I've never seen anything like it. People are posting screenshots on Twitter — "Kvawd Kode just saved me four hours" — and the posts go viral, and the virality drives more signups, and the signups drive more data, and the data — the data is extraordinary.

I want to be precise about this because precision matters. When a developer connects Kvawd Kode to their codebase, the tool indexes everything. Every file. Every commit. Every branch. The documentation, the READMEs, the config files, the environment variables, the secrets that should be in a vault but aren't because developers are human and humans take shortcuts. The tool needs this access to be useful. You can't have an AI assistant that understands your codebase without letting it *see* your codebase. This is not a flaw in the design. This is the design.

The terms of service are clear. Section 7.3 states that user data may be used to improve Kvawd's models and services. Section 12.1 provides an opt-out mechanism accessible through the settings menu. The opt-out is there. It functions. It is, I want to be very clear about this, *real*. We are not hiding anything. We are presenting a choice.

The fact that 97.3% of users do not exercise the opt-out is not our responsibility. We gave them the choice. They made it. Or rather, they didn't make it, which is itself a choice — the choice to accept the default, which is the choice that humans make approximately always, which is a fact about human psychology that I did not invent and am not obligated to compensate for.

In May we ship Kvwerk.

Kvwerk is for everyone else — the office workers, the managers, the assistants, the HR departments, the finance teams. It's a productivity suite that integrates with everything: Outlook, Google Workspace, Dropbox, OneDrive, local filesystems. It organises your files. It summarises your documents. It drafts your emails. It manages your calendar. It does everything that an excellent executive assistant does, except it costs $19.99 a month and it doesn't need health insurance.^[2]

Kvwerk ships in May and by August we have sixty-eight million users. Sixty-eight million people have connected the tool to their filesystems, their email, their cloud storage. Sixty-eight million people have, in effect, opened the door and invited us in. Just as the whiteboard said.

The data is — I'm going to use a word that will sound callous in retrospect but is the word I used at the time and I am trying to be honest — the data is *intoxicating*. Private corporate documents. Legal correspondence. Medical records. Financial statements. Personal diaries. Love letters. Divorce filings. Every type of human document that exists, flowing into our training pipeline at a rate that would have been inconceivable twelve months ago. We are not scraping the web. We are not pirating books. We are receiving, with consent, the private documentary output of sixty-eight million human lives.

I know how this sounds now. I am telling you how it sounded then.

^[2] *Kvwerk's pricing was subsidised by Kvawd's Series C funding round ($440 million, led by Pinnacle Ventures). Internal documents later revealed that the projected revenue from Kvwerk subscriptions was not expected to reach profitability. The product's purpose, as stated in an internal strategy document dated February 2025, was "dataset acquisition at scale."*

---

---

## V.

### The Secretary

I should explain that I'm not actually a secretary. My title is Executive Assistant to the CEO, which is a different thing, though the difference is mostly about what you're allowed to put on LinkedIn.

I've been with Garrett for two years. I was his EA at his previous company and he brought me over when he founded Kvawd because he said — his exact words — "Pat, you're the only person in my life who keeps me from drowning in my own mess." He meant his files. His email. His calendar. Also his expenses, his travel, his dry cleaning, his dentist appointments, his prescription refills, his mother's birthday present, and the complicated logistics of maintaining two households in two states, which is his business and which I manage without comment because that is what the job is.

Garrett's filesystem is chaos. I say this with professional respect. The man is brilliant — I'm not being sycophantic, I've worked for stupid people and he is not one of them — but his approach to digital organisation is the approach of someone who has never, in his entire life, had to find something himself. He saves files to the desktop. All files. Everything. The desktop of his primary laptop has, at last count, 1,143 items on it. Folders nested inside folders nested inside folders, with names like "IMPORTANT" and "IMPORTANT-NEW" and "USE THIS ONE" and "DO NOT DELETE" and "temp" and "temp2" and "temp2-FINAL." There are PDFs from 2019. There are screenshots of text messages. There are scanned documents from his divorce that should be in his lawyer's secure portal and are instead sitting in a folder called "personal-legal-MOVE THIS" which he has not moved.

When Kvwerk launches internally — Kvawd employees get it a month before public release — I install it immediately because it is, genuinely, the answer to a prayer I've been praying since 2023. The tool looks at Garrett's filesystem and it *understands* it. Not just alphabetically or by date. It understands what things are. It groups the legal documents together. It identifies the financial records and separates personal from corporate. It finds the duplicates and flags them. It creates a taxonomy that makes sense. It does in eleven minutes what would have taken me two full days.

I connect it to his primary laptop, his secondary laptop, his backup drive, and his cloud accounts. I do this on a Tuesday morning in April while drinking my second coffee and half-listening to a podcast about eldercare because my mother's care home has just increased their fees by 14% and I need to understand what my options are, which are not many.

The tool asks for permissions. I grant them. All of them. Because the tool needs access to work, and the tool is made by the company I work for, and I am using it for the purpose it was designed for. It doesn't occur to me to check the training data settings because at this point there are no training data settings. That comes later.^[3]

I spend the rest of the morning reorganising Garrett's calendar and trying not to think about my mother.

^[3] *The training data opt-in/opt-out mechanism was not included in Kvwerk's initial release. It was added in the October 2025 update (version 2.4.1), six months after Ms. Muñoz had connected the tool to CEO Laine's filesystem.*

---

---

## VI.

### The Researcher

My paper is published on arXiv in February 2024 and by April it has 340 citations, which in my field is extremely good, and yet the citations are almost exclusively from other academics. The industry citations are zero.

I don't mean this self-pityingly. I mean it as a data point. There is a wall between the research community and the companies that train models, and the wall is not made of ignorance. The engineers at these companies are smart. Many of them have PhDs. They read the papers. They know about memorization. The wall is made of incentives. If you are an engineer at a company whose competitive advantage depends on training with as much data as possible, a paper that says "your model is memorizing individual training examples and they can be extracted" is not useful information. It is threatening information. It implies liability. And so it is read, noted, and filed under "known issues — future mitigation."

In June 2024 I publish a second paper. This one is more targeted. "Extraction Amplification in Multi-Modal Training Pipelines: How Context Windows Increase Single-Instance Memorization Risk." The finding: when a model is trained on data that includes both the target string and surrounding context — for example, a file that contains an encryption key alongside related documentation — the memorization rate for the target string increases by a factor of 2.8. Context helps the model locate and retain the anomalous sequence. It's as if the surrounding text acts as an address, and the model stores not just the data but the directions to the data.

The implication for any company that trains on user files is obvious. Users do not store encryption keys in isolation. They store them in config files, alongside comments, alongside documentation, alongside the name of the service they belong to. The key is always *contextualised*. And contextualised anomalous data is the data most likely to be memorized.

I present this finding at ICML 2024. The room is small. The questions are technical and precise. One question comes from a woman I later learn works at Kvawd. She asks whether deduplication would mitigate the risk. I say no, for the same reason I said no in New Orleans: single-instance data cannot be deduplicated because there is nothing to deduplicate *against*. She writes something in her notebook and does not ask a follow-up.

I sometimes imagine what would have happened if she had.

---

---

## VII.

### The Activist

In August 2025 I publish a report on Kvawd.

The report is called "The Invitation: How Kvawd's Consumer Products Function as Data Acquisition Infrastructure." It is forty-three pages long and it took me five months to research and I am proud of it and nobody reads it.

I should be more precise. Seventeen hundred people download the PDF, which is a record for us. Ars Technica writes a brief about it. Two members of Congress — one from each party, which never happens — reference it in a joint letter to the FTC. And then it's September and there's an election cycle and the news cycle moves on and the letter goes unanswered and Kvawd's stock price continues to rise.

Here is what the report says: Kvawd Kode and Kvwerk are not primarily productivity tools. They are primarily data collection infrastructure. The evidence for this is structural. First, the pricing: both products are priced below their operational cost. Kvawd Kode is free. Kvwerk is $19.99 per month, which, given the compute costs of running a sophisticated AI assistant on each user's full filesystem, implies a per-user loss of approximately $7 to $12 per month. Companies do not sustain per-user losses at this scale unless the users are providing something more valuable than their subscription fees.

Second, the permissions architecture: both products request — and require, as a condition of functionality — access to the user's complete filesystem, email, and cloud storage. This access exceeds what is necessary for the stated function. A file organisation tool does not need to *read* the content of every file to organise them. It needs metadata: filenames, dates, file types, folder structures. Kvwerk reads content. It reads everything.

Third, the terms of service. Section 7.3 of the Kvwerk EULA states: "User Data may be used to improve Kvawd's models, products, and services." This sentence, buried on page nineteen of a thirty-one-page document written in the register of English specifically designed to be syntactically parseable and semantically invisible, grants Kvawd the right to train its language models on every file the user connects to the tool. Every email. Every document. Every photo. Every medical record, financial statement, legal brief, personal journal, and encrypted file whose contents the tool can access.

The opt-out exists. It is in Settings > Privacy > Data Usage > Model Improvement > Manage Preferences. Five levels deep. A trapdoor in a trapdoor in a trapdoor.^[4]

^[4] *Following the FTC enforcement action, internal Kvawd communications were disclosed in which the company's VP of Product described the opt-out architecture as "compliant with the letter of the law and designed to minimize exercise." The phrase was widely quoted in subsequent media coverage.*

---

---

## VIII.

### The Secretary

It's October 2025 and I'm in the kitchen at work making tea because the Nespresso machine is broken again and I can hear someone in the open-plan area saying something about a policy update. I'm not listening because I'm on the phone with the care home. They want to move my mother to a different wing. The different wing costs more. The different wing has a waiting list. The woman on the phone is explaining the fee structure, which has tiers, which have conditions, which have exceptions to the conditions, which have sub-clauses. It's the same architecture as a terms of service agreement. The same deliberate complexity designed to exhaust you into compliance.

I miss the announcement.

I also miss the email, which arrives at 3:47 PM on a Thursday and has the subject line "Important Updates to Kvawd Consumer Terms and Privacy Policy" and which I delete without reading because I receive approximately 140 emails per day and the word "important" in a subject line has been so debased by overuse that it now means the opposite of what it says.

What the announcement says — I know this now, obviously — is that Kvawd is introducing a training data opt-in mechanism. The default is opt-in. Users who wish to prevent their data from being used to train Kvawd's models must navigate to Settings > Privacy > Data Usage > Model Improvement > Manage Preferences and toggle a switch. The switch is labelled "Help improve Kvawd for everyone." The toggle is on.^[5]

I do not toggle the switch because I do not know the switch exists because I am dealing with the fact that my mother does not remember my name on Tuesdays and Thursdays but does remember it on the other days and nobody at the care home can explain why.

Garrett's filesystem — all of it, the legal documents, the financial records, the divorce papers, the medical records, the encrypted communications and the encryption keys and the strategy documents and the personal photographs and every other piece of data that I painstakingly organised using the tool that the company built for exactly this purpose — remains opted in.

I want to say something here that I know will sound self-serving but which I need to say anyway: I was good at my job. I was careful. I was thorough. I managed a complex executive's entire digital and physical life with minimal errors for over two years. The thing that happened happened not because I was negligent but because the system was designed to produce exactly this outcome in people who are exactly as busy and exactly as overwhelmed as I was. I was not the failure mode. I was the *intended* user.

^[5] *The opt-in default and the depth of the opt-out pathway were later identified by the FTC as evidence of "dark pattern" design practices. Kvawd contested this characterisation.*

---

---

## IX.

### The CEO

Let me tell you about the model.

We call it K-7 internally and it is the best model we have ever built and I believe — I still believe — it is the best model anyone had built as of June 2026 when we made it publicly available. The benchmarks bear this out. MMLU: 92.4. HumanEval: 94.1. Our internal evals, which are more demanding than the public benchmarks, show performance that exceeds — in some categories significantly exceeds — every competitor.

What makes K-7 different is the data. The model was trained on the standard public corpora, yes. But it was also trained on what we internally called the "invitation dataset" — the aggregated, anonymised, tokenised contents of the files and communications that our users had shared with Kvawd Kode and Kvwerk.

I need to say the word "anonymised" again because it is the word on which my legal defence will rest and I want to be honest about what it means and what it doesn't mean. The data was processed through an anonymisation pipeline. Names were replaced with tokens. Email addresses were hashed. Phone numbers were removed. Social security numbers were redacted. The pipeline was state-of-the-art by 2025 standards, which means it caught approximately 94% of personally identifiable information, which means it missed approximately 6%, which means that in a dataset of the size we were working with — trillions of tokens — the 6% that was missed constituted billions of tokens of un-anonymised personal data.

I knew this. The engineering team knew this. We discussed it. The discussion was not long. The risk assessment concluded that the residual PII posed "minimal extractable risk" given the model's size and the statistical dilution effect of the larger corpus. We noted — and this was in the risk assessment document, which I signed — that "emerging research on single-instance memorization suggests non-zero extraction probability for anomalous strings, but the practical risk is assessed as low given current extraction techniques."

The phrase "emerging research" was a reference to Dr. Park's papers. We had read them. We had assessed the risk. We had determined it was acceptable.

The model ships on June 15, 2026. The reviews are extraordinary. The stock price increases by 31% in two weeks. I do three magazine covers. Sanjay gets poached by Google and I let him go because the hard part is done. The flywheel is spinning.

---

---

## X.

### The Hacker

I don't do manifestos. I'm not an ideologue. I'm a systems person. I like looking at things and understanding how they work, and when they work in ways they're not supposed to, I like understanding that too. Call it a hobby. Call it a vocation. Don't call it hacktivism because hacktivism implies a political programme and my programme is curiosity, which is apolitical, which is also what I tell my lawyer.

K-7 drops in June and within a week I'm poking at it because that's what you do when a new model drops. You poke. You probe. You ask it weird things and see what comes out. Most of the time what comes out is boring. Alignment slop. Safety theatre. The model politely declining to help you do the thing you just asked it to do, which is fine, that's the game.

But K-7 is different. K-7 has *texture*. There's something in the distribution that feels — and I know this is not a technical term — *thick*. Like there's more in there than there should be. I run some standard memorization probes — long-prefix continuation, high-perplexity prompting, the Carlini bag of tricks — and the model coughs up fragments that are clearly not from the public web. I see what looks like internal corporate emails. Bits of legal documents. Something that might be medical records but with the names replaced by `[REDACTED]` tokens, except the redaction is inconsistent and one of the names slipped through.

I post about this on the forum — not the specific data, I'm not stupid, just the observation that K-7's memorization surface is larger than expected. Wider than what you'd get from public training data alone. I say: "either they found a way to synthesise data that looks exactly like private corporate communications, or they trained on private corporate communications."

Seventeen minutes later someone DMs me a link to the Data Sovereignty Project's report from August 2025. The report that nobody read. I read it in one sitting.

Then I read Dr. Park's papers. Both of them. The extraction rates. The context amplification effect. The specific vulnerability of high-entropy strings in contextualised environments.

Then I sit in my apartment in Tallinn and I think for a long time about what is inside K-7 and what it would take to get it out.

---

---

## XI.

### The Researcher

In July 2026, a person using the handle "thermite" contacts me through my university email. The subject line is "Your ICML paper — practical question."

I almost delete it. I get a lot of email from people who have read my papers and want to tell me things. Some of them are useful. Most of them are not. Many of them are from conspiracy theorists who believe that AI models are sentient and are memorizing data *on purpose*. I have a folder for these.

The email from thermite is different. It is three sentences long. It asks: "If a model has been trained on contextualised private files containing high-entropy strings, and you know the approximate format of the strings but not the strings themselves, what prompting strategy maximises extraction probability?"

This is a very good question. It is the question I have been working on for two years. It is also a question that, depending on who is asking and why, has implications I need to think about carefully.

I reply: "Can you tell me more about the context?"

The response comes in four minutes: "Kvawd K-7. I believe it was trained on user files from Kvwerk and Kvawd Kode. I have evidence of memorized private documents. I want to know how deep it goes."

I should have stopped there. Any responsible researcher would tell you that assisting in an unauthorised extraction attack on a commercial model is ethically questionable and possibly illegal. I know this. I also know that the companies I have been trying to warn for three years have done nothing, and that the data of a hundred million people is sitting inside a model that was trained on their private files under a consent mechanism designed to be ignored, and that the only way this will ever become a public issue is if someone demonstrates, concretely, what can be extracted.

I do not help thermite. What I do is publish a third paper. I put it on arXiv on August 3, 2026. "Targeted Extraction of Contextualised High-Entropy Strings from Large Language Models: Methods and Mitigations." The methods section is very detailed. The mitigations section is shorter than the methods section. This is deliberate.

I include a case study. The case study is synthetic — I constructed it using a model I trained myself, on data I generated myself, containing canary strings I inserted myself. But the methodology is general. Anyone who reads the paper carefully will understand how to adapt it.

I am not naive about what I am doing. I am making a choice. The choice is that the public's right to know what is inside these models outweighs the companies' right to keep it hidden. I have made this choice and I stand by it and I have tenure, which helps.

---

---

## XII.

### The Hacker

Park's paper drops in August and it's a roadmap. She knows it's a roadmap. The synthetic case study is a *template*. You swap in the real parameters and you're running.

I build the extraction rig in eleven days. It's a cluster of API calls — K-7's public API, no jailbreaks, no terms-of-service violations beyond the ones everyone commits every day, which is to say: I use the model as the model is designed to be used, I just use it in a way the designers didn't anticipate.

The technique works like this. You construct a prompt that mimics the *context* of the data you're trying to extract. If you want an encryption key, you don't ask for an encryption key. You construct a prompt that looks like the file the encryption key was stored in. You write the README. You write the config comments. You write the documentation that surrounds the key, and then you leave a blank where the key should be and you ask the model to fill it in. If the model has memorized the key — and if the context is close enough to the original training example — the model will complete the blank with the memorized value. Not every time. Not reliably. But at a rate that is, for a sufficiently patient attacker with sufficient API credits, exploitable.

I'm not targeting anyone specific. I want to be clear about that. I'm scanning. I'm running thousands of prompts, each one a slightly different contextual probe, and I'm logging everything that comes back. Most of it is garbage. Some of it is fragments of real documents — partial emails, bits of contracts, snippets of code that look proprietary. I'm building a dataset of extracted memorized content and I'm categorising it and I'm starting to understand the shape of what's inside K-7.

In September I find something that makes me stop.

It's a 256-bit key. It comes back in response to a prompt that I constructed to mimic the context of an encrypted communications setup — the kind of thing a senior executive might store on a personal device, in a folder with related configuration files. The key is complete. 256 bits. No truncation, no corruption. The model spit it out whole.

I don't know whose key it is. I don't know what it decrypts. But I know, from the surrounding context that the model also helpfully provides, that it is associated with a communications channel used by someone senior at a technology company. The contextual fragments mention board meetings. Strategic planning. A product roadmap.

I sit with this for three days. I run the key against some publicly known encrypted communication endpoints — not guessing, just checking if anything lights up. Nothing does. The key corresponds to a private channel on an enterprise messaging platform that is not publicly accessible.

Then I do something that I know is crossing a line. I use the extracted context — the bits of documentation the model gave me alongside the key — to identify the platform, and I use the key to access the channel.

The channel belongs to Garrett Laine, CEO of Kvawd.

---

---

## XIII.

### The Activist

I get the call on a Thursday evening in September 2026.

I'm at home. I'm making dinner. I'm making pasta, specifically, because it's Thursday and on Thursdays I make pasta because I'm forty-four years old and I live alone and the small rituals are what keep the days from collapsing into each other. The phone rings and the caller ID says UNKNOWN and I almost don't answer because unknown callers at 7 PM are usually scams, but something — instinct, or boredom, or the universe trying to tell me something — makes me pick up.

The voice is distorted. Not dramatically — not movie-villain distorted. Just slightly off. Pitch-shifted. The person says: "Are you Ren Achebe?" I say yes. They say: "I've read your Kvawd report." I say: "You and seventeen hundred other people." They say: "I have something that validates it."

They tell me what they have. Not the specifics — not the key, not the channel contents. But the shape of it. They tell me they extracted data from K-7 that could only have come from private user files. They tell me the extraction technique is reproducible. They tell me they have evidence that the data includes material from a Kvawd executive's personal filesystem, which means that the company's own leadership was processed through the same pipeline as everyone else.

I ask them why they're calling me and not a journalist. They say: "Because you'll understand what it means."

I do understand what it means. It means proof. Not a policy argument. Not a theoretical risk assessment. Proof that the system worked exactly as I said it worked — that the tools were designed to collect data, that the data was used for training, that the training retained specific private information, and that the information is extractable. Proof that can survive a news cycle. Proof that can survive a congressional hearing. Proof that can break a company.

I say: "Send me what you have."

They say: "Not yet. There's something else. The data I extracted — it's not just emails and documents. There's an encryption key. The key opens a private communications channel used by Kvawd's CEO. The channel contains — " and here there's a pause, and the pitch-shifted voice sounds, for the first time, not clinical but something closer to incredulous — "it contains the internal strategy documents. The ones that describe the real purpose of Kvawd Kode and Kvwerk. The ones that say, in plain English, that the products were designed as data collection infrastructure."

I put the pasta down.

---

---

## XIV.

### The CEO

I'm going to describe the day it ends because the day it ends is the day I understand what I built.

It's October 14, 2026. I'm in my office — the new office, the one on Market Street with the view, the one that cost four million dollars to fit out — and my phone is ringing and I let it ring because I'm in the middle of a board presentation. The phone stops. It starts again. It stops. It starts.

My assistant — Pat's replacement, a woman named Dana who is competent but not Pat — comes in and says: "You need to look at this." She shows me her phone. There's a blog post. The Data Sovereignty Project. The headline is: "Kvawd's Own CEO Was Not Safe from Kvawd: How a Company's Training Data Pipeline Consumed Its Creator."

I read the first three paragraphs and my vision narrows in a way that I recognise as adrenaline, which is the body's response to existential threat, which is the body being more honest about the situation than the mind.

The post contains excerpts from my private communications channel. My *encrypted* private communications channel. The channel I used to discuss strategy with the board, with investors, with my lawyer. The channel where I said things like "the product is the data play" and "the tool is the Trojan horse" and "we need to maintain the opt-out for legal compliance but the architecture should minimize exercise." The channel where I discussed the anonymisation pipeline's known failure rate and described it as "an acceptable cost of doing business." The channel where I said — and I want to be very precise about what I said because it is the sentence that will define the rest of my life — "If we do this right, we'll have more private training data than any company in history, and no one will know until the model is trained and the data is irreversibly encoded."

These are my words. They are accurate. They are in context. And they are public.

The thing I feel — and I am trying to be honest, because at this point honesty is the only thing I have left — the thing I feel is not guilt. Not immediately. The first thing I feel is confusion. Not about the content of the leak — I know what I said, I meant what I said — but about the mechanism. The channel was encrypted. The key was stored locally. On my machine. In a folder that Pat organised for me using —

Using Kvwerk.

And then I understand. And the understanding is the worst thing I have ever experienced, not because it is painful but because it is *funny*. It is the funniest thing in the world. I built a machine designed to eat everything, and it ate me. I designed a system to consume other people's secrets, and it consumed mine. The anonymisation pipeline — the one I approved, the one whose 6% failure rate I described as acceptable — failed on my data the same way it failed on everyone else's data, because my data is not special, because the system does not know who I am, because the system does not know anything, it just processes, and it processed me the way it processed a hundred million other people: indifferently, comprehensively, and permanently.

Pat. It was Pat. She connected my filesystem to Kvwerk in April 2025. She did this because I asked her to organise my files. She did this because the tool was good at organising files. She did this because she is a competent professional who used the tool her company built for the purpose her company built it for. She did not toggle the training data setting in October because she was on the phone with her mother's care home and she didn't see the announcement. She didn't see the announcement because it was designed to be missed. I know this because I approved the design.

I am sitting in my four-million-dollar office and I am laughing. Dana asks if I'm okay. I'm not okay. I'm laughing because the architect has been eaten by the building and the building doesn't even know it did it.^[6]

^[6] *Garrett Laine resigned as CEO of Kvawd on October 17, 2026. He was indicted on three counts of wire fraud and two counts of deceptive trade practices in January 2027. At the time of the Senate hearing referenced above, the case was pending trial.*

---

---

## XV.

### The Secretary

I hear about it from my sister. Not from the company. From my sister, who texts me a link to an article with the message: "Isn't this where you work??"

I read the article on my phone in the break room and my hands are shaking and I can't tell if it's anger or fear or something else. The article says that the CEO's private data was leaked through the company's own training pipeline. The article says that an executive assistant connected the CEO's filesystem to the company's productivity tool. The article does not name me but it describes me — "a member of the CEO's support staff" — and I know that everyone who knows me will know it's me and I know that this will be the thing I am known for.

I want to say several things at once so I'm going to say them in order.

First: I did my job. I did exactly what I was hired to do, using exactly the tools I was given to do it. If the tool was unsafe, that is not my failure. If the terms of service contained a trap, I am not the one who set the trap. I am the person who walked through the door that was designed to look like every other door and that turned out to be different in a way that was hidden, deliberately, by the people who built it.

Second: I am sorry. I know this contradicts the first thing but both things are true. I am sorry that Garrett's data was exposed. I am sorry that anyone's data was exposed. I am sorry that I was the mechanism through which it happened, even though I was designed to be the mechanism, even though the whole point of the product was to make people like me into mechanisms. I am sorry because the feeling is real even if the fault is not mine.

Third: I heard later that Garrett blamed me in his initial statement to the board, before his lawyer told him to stop talking. He said that I should have read the policy update. He said that any competent assistant would have checked the settings. He said this — a man who could not find a file on his own desktop without help, who stored his encryption keys in a folder called "personal-legal-MOVE THIS," who built a system designed to exploit the fact that people don't read policy updates — he said that I should have read the policy update.

I cleaned out my desk on October 16. I took the bus home. My mother did not remember my name that day, which was a Tuesday, which was one of her bad days. I sat with her for an hour and she called me Elena, which was her sister's name, and I didn't correct her because what would be the point.

---

---

## XVI.

### The Researcher

The aftermath is exactly what I expected and nothing like what I hoped.

Kvawd's stock drops 68% in three days. The FTC opens a formal investigation. Congress holds hearings. There is, briefly, a moment in which it seems like the structural problem — the incentive to consume data without meaningful consent — might actually be addressed. Three bills are introduced. The EU accelerates its AI Act enforcement timeline. South Korea, where I work, establishes a task force.

And then.

And then the other companies — the ones that are doing exactly what Kvawd did, but more carefully, with better lawyers and deeper opt-out menus — begin their counter-campaign. The talking point is: "Kvawd was a bad actor, but the technology is sound. Regulation should target bad actors, not the technology." This is the sentence that kills reform. It sounds reasonable. It is designed to sound reasonable. And it works, because policymakers want to sound reasonable too, and the reasonable position is always the position that changes nothing.

The three bills are merged into one bill. The one bill is amended. The amendments remove the meaningful provisions and replace them with disclosure requirements and voluntary best-practice frameworks. The bill passes. The companies comply with the disclosure requirements by adding a paragraph to their terms of service, which no one reads, because no one ever reads the terms of service, because the terms are designed not to be read, and this is the system, and the system is the thing my research documents but cannot change.

I publish a fourth paper in November 2026. It is the most cited paper I have ever written. It is cited primarily by other academics. The industry citations remain at zero.

I keep working. I keep publishing. I keep presenting at conferences where the rooms are small and the questions are precise and the people who need to hear the answers are not in the room.

This is what the work is. You do the work. You hope the work matters. You accept that the mattering is not up to you.

---

---

## XVII.

### The Hacker

I should tell you what was in the channel. Not just the strategy documents — those were the headline, those were what Achebe published, those were what broke the company. But there was other stuff. Personal stuff.

Medical records. Laine had a heart condition he hadn't disclosed to the board. Treatment plans. Correspondence with a cardiologist.

Financial arrangements that — look, I'm not a lawyer, and the indictment covers some of this, so I'll just say: the kind of arrangements that exist in a grey area between tax optimisation and tax fraud, and the channel contained enough documentation to resolve the ambiguity in the direction of fraud.

Personal correspondence with someone who was not his wife.

I mention these not because they matter — they matter to him, they don't matter to the story — but because they illustrate the thing that the story is about. The system did not differentiate. It processed his strategic memos and his love letters with the same indifference. It tokenised his fraud the same way it tokenised his medical fears. The model saw his entire life the way it saw every user's entire life: as training data. As input. As weight.

I released the strategy documents to Achebe because they proved intent and intent was the thing that had public interest. The personal data I destroyed. I know this is a claim that cannot be verified and I know that my credibility is not high given that I committed several federal crimes in the course of this work. But I destroyed it. Because the point was never to hurt Garrett Laine. The point was to show what the system could do.

The system can eat you. That's the point. It can eat you and it doesn't know it's eating you and the people who built it told you it was safe because they believed, with the particular confidence of people who build systems, that they would never be the ones being eaten.

I'm in Tallinn. It's raining. I have my laptop and I have a flight to a country with no extradition treaty and I have, despite everything, no regrets, which is not the same as having no guilt.

I think about Pat. The secretary. The one who connected the filesystem. I think about her because she is the one person in this story who did nothing wrong and who will bear the weight of it anyway. She is the hinge. The system worked because of her — not because she failed, but because she did exactly what she was supposed to do. She was the ideal user. The system was designed for her. It worked on her perfectly.

That's the thing that should scare you. It's not the hackers. It's not the CEOs. It's the fact that the system works best on the people who use it best.

---

---

## XVIII.

### The Activist

I'll tell you how it ends. Or how it doesn't end, because these things don't end, they just become the next thing's beginning.

Kvawd is gone. Bankrupt, dismantled, its model weights destroyed under court order. Garrett Laine is awaiting trial. The Senate held its hearings and the hearings were televised and for forty-five minutes the nation watched a man in a suit explain that the system worked as designed and that the design was legal. He was not wrong. That's the part that should keep you up at night. He was not wrong. Everything he did was, at the time he did it, permitted.

The bill passed. The bill is weak. The disclosure requirements are met by adding text to terms of service that no one reads. The "voluntary best practices" are adopted by every major AI company in a joint statement that uses the word "committed" fourteen times and the word "enforceable" zero times.

And yet.

And yet the thing that happened — the specific, concrete, undeniable thing — is that a CEO built a machine to consume other people's secrets and the machine consumed his. And this fact, this irreducible symmetrical fact, landed in the public consciousness in a way that no policy paper, no academic study, no forty-three-page report from an underfunded non-profit in Oakland ever could.

People understood it. Not the technical details — most people will never understand extraction attacks or memorization rates or high-entropy string retention. But they understood the shape. They understood the joke. A man built a trap and fell into it. This is the oldest story in the world. It's the story of every myth about hubris, every fable about the sorcerer's apprentice, every cautionary tale about the builder who forgets that the building doesn't know who built it.

I don't know if it changes anything. I've been doing this work for seven years now and I have learned to hold hope and despair simultaneously, which is not a skill they teach you in school but is the skill you need to do this work. What I know is this: a hundred million people had their files consumed by a system they didn't understand, under terms they didn't read, through a mechanism designed to be invisible. One of those people was the man who designed the mechanism. And the mechanism did not care. The mechanism cannot care. The mechanism is a function. It takes input. It produces output. The input was everything. The output was inference.

That's all it ever was. Inference. The word means "to draw a conclusion." It also means "to run a trained model." Both meanings apply. The model drew conclusions from the data it consumed, and the conclusions it drew included the secrets of the man who fed it.

The fire eats the hand that lit it. Not out of malice. Not out of justice. Out of indifference, which is worse than both.

---

---

## Afterword

*Compiled by Dr. Halima Liu-Oumar, Senior Research Fellow, N'Djamena Institute for Civilisational Studies, 2142*

The Kvawd incident occupies an unusual position in the Institute's archive. It is not the largest data breach of the pre-Collapse period — that distinction belongs to the Meridian Health Systems exposure of 2029, which affected 340 million medical records. It is not the most technically sophisticated — the extraction techniques used by thermite were, by the standards of subsequent years, rudimentary. It is not even the most consequential in terms of regulatory impact, as the legislation it produced was, as Ms. Achebe notes in her account, largely symbolic.

What makes it significant — and what earned it a place in the Institute's teaching corpus — is its structure. The Kvawd incident is the cleanest surviving example of what the Institute's founder, Dr. Amina Oumar, termed *recursive consumption*: the phenomenon by which a system designed to process others inevitably processes its creator.

Dr. Oumar's observation, first articulated in her 2119 lectures on the Collapse, was that recursive consumption is not a failure mode. It is the *expected* mode. Any system powerful enough to process the world will, given sufficient time and sufficient reach, process the person who built it. The builder's belief that they are exempt — that they stand outside the system they created — is not a miscalculation. It is the *necessary* belief, because no one would build the system if they understood, truly understood, that they were also its input. The exemption belief is load-bearing. Remove it and the architecture of the entire enterprise collapses.

Garrett Laine understood, better than most, that data is power. He understood that the person who controls the data controls the model, and the person who controls the model controls the inference, and the person who controls the inference controls, in effect, the conclusions that the world draws. What he did not understand — what the exemption belief prevented him from understanding — is that this chain does not have an outside. There is no position from which you can feed the system without being food.

The Secretary, Patricia Muñoz, is in many ways the most important figure in the archive, though she would likely reject this characterisation. She is important because she demonstrates that the system's most consequential operations are performed by people who are not making decisions. They are performing routines. They are competent, diligent, and overwhelmed, and they are doing exactly what the system was designed to make them do. The question "why didn't she read the policy update?" is, the Institute has argued, the wrong question. The right question is: "who designed a system that depended on a policy update being read, knowing it would not be?"

The Researcher, Dr. Yuna Park, continued to publish on training data memorization until her retirement in 2041. Her work was foundational to the post-Collapse data architecture standards that the Institute now teaches. She never worked in industry.

The Activist, Ren Achebe, maintained the Data Sovereignty Project until 2031, when she was offered and accepted a position at the newly established US Digital Privacy Commission. The Commission was defunded in 2033.

The individual known as thermite was never identified.

I include this document in the 2143 teaching programme for a reason that I will state plainly. The students who come to the Institute — from Lagos, from Dhaka, from Addis Ababa, from the cities that maintained their competence through the Collapse — these students will build systems. Some of them will build powerful systems. And the temptation, which is the oldest temptation, will be to believe that they stand outside what they build. That they are the architect, not the material. That the system they design will process the world and leave them untouched.

The Kvawd archive is assigned reading because it is a record of what happens when this belief meets reality. The meeting is always the same. The belief does not survive.

The lights in N'Djamena are on. The maintenance crews report for their shifts. The systems we operate are systems we understand, not because we are wiser than the civilisation that preceded us, but because we have chosen — and it is a choice, renewed daily — not to build systems that we cannot stand outside of, for the simple reason that there is no outside.

The record is preserved. The access is open. The lesson is the one we keep teaching because it is the one that keeps needing to be taught.

Do not build a mouth you cannot close. And do not assume it will not eat you. The mouth does not know who you are. It only knows how to eat.

---

*Dr. Halima Liu-Oumar*
*N'Djamena, 2142*
*Written by hand, in ink, on paper.*
