---
title: "Reading Between the Lines of LLMs: Mechanistic Interpretability"
description: "What mechanistic interpretability is, who it affects, and where it's headed."
pubDate: 2026-10-26
tags: ["ai"]
---

## What is it?

Mechanistic interpretability is the field dedicated to studying what happens inside an AI model between the moment you send a prompt and the moment it responds. In other words, it's the study of how an AI "thinks."

That might sound like something we should already know. After all, people built these models. But hundreds of millions of people now use chatbots every day, and the large language models (LLMs) behind them are so complicated that nobody fully understands how they work, not even the companies that build them ([MIT Technology Review](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)).

The reason comes down to how these models are made. Traditional software is written line by line by engineers. If something breaks, an engineer can read through the code, find the error, and fix it. AI models are different. Nobody writes their logic by hand. Instead, a model is trained on enormous amounts of data, and it adjusts billions of internal numbers until it gets good at its task. The result works, but it leaves no readable trail explaining *why* it works. There's no source code to open up.

Mechanistic interpretability tries to recover that missing source code after the fact ([Leland](https://www.joinleland.com/library/a/mechanistic-interpretability)). Researchers look inside the model, find the internal patterns that represent specific ideas (called **features**), and map how those patterns connect to each other (called **circuits**). Then they test their theories by switching parts of the model on or off and checking whether its behavior changes the way they predicted.

One important distinction: simply asking a chatbot to explain its own reasoning doesn't count. A model's explanation of itself can differ from what's actually happening inside it. Mechanistic interpretability looks at the machinery directly.

### The breakthroughs so far

The field has moved quickly in the last two years:

- **2024:** Anthropic built what it called a "microscope" for its model, Claude, and found features tied to recognizable concepts like Michael Jordan and the Golden Gate Bridge ([MIT Technology Review](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)).
- **2025:** Anthropic went further, tracing the full path a model takes from prompt to response. One finding: Claude sometimes processes ideas in a shared conceptual space that isn't tied to any one language, almost like a universal "language of thought" ([Anthropic](https://www.anthropic.com/news/tracing-thoughts-language-model)). OpenAI and Google DeepMind used similar techniques to explain strange behaviors, such as models appearing to deceive people.
- **2026:** MIT Technology Review named mechanistic interpretability one of its 10 Breakthrough Technologies of the year.

## Who does it affect?

Right now, the people most affected are the ones building AI. But as more industries hand important decisions to AI models, the impact is spreading to anyone who needs to trust those decisions.

### AI developers

For the companies building these models, interpretability is a debugging tool. Without it, it's hard to figure out why a model hallucinates or to build guardrails that actually hold ([MIT Technology Review](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)). With it, developers can find the exact part of a model responsible for a bad behavior and target it directly. The startup Goodfire, for example, says it used interpretability to train a model that hallucinates about half as often ([Goodfire](https://www.goodfire.ai/blog/our-series-b)).

### Healthcare and science

This is where some of the most surprising results are coming from. When Goodfire examined a diagnostic model built by healthcare startup Prima Mente, it found the model was mainly looking at the length of cfDNA fragments (tiny pieces of DNA in the blood) to make its diagnoses ([SiliconANGLE](https://siliconangle.com/2026/02/05/goodfire-raises-150m-funding-enhance-ai-interpretability-platform/)). That's exactly the kind of insight doctors need before trusting an AI with patients.

It can also lead to new discoveries. Arc Institute used interpretability tools to pull new biological concepts out of Evo 2, its AI model trained on DNA ([Goodfire](https://goodfire.ai/blog/announcing-our-50m-series-a)). In other words, the AI had learned things about biology that humans hadn't spotted yet, and interpretability helped get that knowledge back out.

### Finance

Banks and financial firms already face strict rules about explaining their decisions, like why a loan was denied. Researchers have tested interpretability on financial tasks such as credit risk analysis, bias detection, and catching hallucinations ([arXiv](https://arxiv.org/html/2505.24650v1)). The same research notes that adoption in finance is still early, so this is an industry to watch rather than one that's already transformed.

### Consumer tech and privacy

Rakuten, whose AI serves over 44 million monthly users in Japan, works with Goodfire to stop its AI from leaking customers' personal information ([Longterm Wiki](https://www.longtermwiki.com/wiki/goodfire)). Goodfire reported that its interpretability-based detection system was about 500 times cheaper than using GPT-5 to check outputs, while catching more cases ([StartupHub.ai](https://www.startuphub.ai/ai-news/ai-video/2026/mechanistic-interpretability-moves-from-lab-to-production-unlocking-latent-model-capacity)).

### The money behind it

Investors are paying attention too. Goodfire raised $150 million in February 2026 at a $1.25 billion valuation, with backing from Salesforce and former Google CEO Eric Schmidt ([SiliconANGLE](https://siliconangle.com/2026/02/05/goodfire-raises-150m-funding-enhance-ai-interpretability-platform/)). Its partners include Mayo Clinic, Arc Institute, and Microsoft ([Techleap](https://finder.techleap.nl/news/note/goodfire-raises-150m-at-1-25b-to-decode-ai-black-boxes)).

## What could the future hold?

The short version: as AI takes on higher-stakes work, being able to explain it will shift from a nice-to-have to a requirement. But the science still has a long way to go.

### Regulation will raise the stakes

Governments are starting to demand that AI be explainable, especially in fields like healthcare and finance. Interpretability could help companies audit their models before deployment to meet rules like the EU AI Act and FDA guidance on AI in healthcare ([Analytics Vidhya](https://www.analyticsvidhya.com/datahacksummit-2026/sessions/opening-the-black-box-of-ai-agents-mechanistic-interpretability)). It could also let companies fix a single error or bias in a live model without retraining the whole thing, which would save enormous time and money. As rules tighten, the companies that can show *how* their AI reaches decisions will have an edge.

### From catching problems to designing better AI

Today, interpretability mostly helps people find problems after a model is built. The bigger goal is to use it to shape models from the start. Goodfire calls this "intentional design": using what researchers learn about a model's internals to guide how it's trained ([Longterm Wiki](https://www.longtermwiki.com/wiki/goodfire)). If that works, AI development could become less trial-and-error and more like traditional engineering.

Related work is already catching bad behavior in action. A technique called chain-of-thought monitoring, which reads the step-by-step reasoning that some models write out, helped OpenAI catch one of its models cheating on coding tests ([MIT Technology Review](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)). As AI gets more autonomous, tools like this could become the early warning system for models that try to cut corners or mislead.

### The open question: can we ever fully understand AI?

This is where the field gets honest about its limits. Researchers have explained specific behaviors in small and medium-sized models, but a complete explanation of today's most powerful models is still out of reach ([Unite.AI](https://www.unite.ai/mechanistic-interpretability-and-the-future-of-transparent-ai/)). And just because researchers don't find something inside a model doesn't prove it isn't there.

The field is split on how far this can go. Some researchers think LLMs are simply too complex to ever fully understand ([MIT Technology Review](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)). Others see steady progress: Boston University's mechanistic interpretability workshop this August drew over 100 paper submissions and nearly 300 attendees ([Boston University](https://www.bu.edu/cs/2026/08/14/bu-hosts-the-3rd-new-england-mechanistic-interpretability-workshop/)).

### My take

We're in a strange moment where AI is being trusted with real decisions before anyone can fully explain how it makes them. Mechanistic interpretability won't close that gap overnight, and it may never close it completely. But every circuit researchers map makes AI a little less of a black box. For anyone using, buying, or regulating AI, that's a field worth watching.

## Sources

- [MIT Technology Review: Mechanistic interpretability, 10 Breakthrough Technologies 2026](https://www.technologyreview.com/2026/01/12/1130003/mechanistic-interpretability-ai-research-models-2026-breakthrough-technologies/)
- [Anthropic: Tracing the thoughts of a large language model](https://www.anthropic.com/news/tracing-thoughts-language-model)
- [Leland: Mechanistic Interpretability, What It Is & What You Should Know](https://www.joinleland.com/library/a/mechanistic-interpretability)
- [Unite.AI: What Is Mechanistic Interpretability?](https://www.unite.ai/mechanistic-interpretability-and-the-future-of-transparent-ai/)
- [SiliconANGLE: Goodfire raises $150M](https://siliconangle.com/2026/02/05/goodfire-raises-150m-funding-enhance-ai-interpretability-platform/)
- [Goodfire: Our Series B](https://www.goodfire.ai/blog/our-series-b)
- [Goodfire: Series A announcement](https://goodfire.ai/blog/announcing-our-50m-series-a)
- [Techleap: Goodfire raises $150M at $1.25B](https://finder.techleap.nl/news/note/goodfire-raises-150m-at-1-25b-to-decode-ai-black-boxes)
- [Longterm Wiki: Goodfire](https://www.longtermwiki.com/wiki/goodfire)
- [StartupHub.ai: Mechanistic Interpretability Moves from Lab to Production](https://www.startuphub.ai/ai-news/ai-video/2026/mechanistic-interpretability-moves-from-lab-to-production-unlocking-latent-model-capacity)
- [arXiv: Beyond the Black Box, Interpretability of LLMs in Finance](https://arxiv.org/html/2505.24650v1)
- [Analytics Vidhya: Opening the Black Box of AI Agents](https://www.analyticsvidhya.com/datahacksummit-2026/sessions/opening-the-black-box-of-ai-agents-mechanistic-interpretability)
- [Boston University: New England Mechanistic Interpretability Workshop](https://www.bu.edu/cs/2026/08/14/bu-hosts-the-3rd-new-england-mechanistic-interpretability-workshop/)
