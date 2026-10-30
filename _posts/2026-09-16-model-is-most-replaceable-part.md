---
layout: post
title: The Model Is the Most Replaceable Part of the Stack
categories: [ai, enterprise, strategy]
---

The AI stack has three layers. 
Everyone is saying that the layer that the user touches is the one that matters most. And, I agree with that. 
 
At the bottom are foundation models and the infrastructure that runs them: GPUs, data centers, token pricing, and cloud compute. This layer is advancing fast. In the middle is the application layer. It sits between raw model capability and the end user. It handles workflows, evals, data access, permissions, and change management. At the top are the applications themselves. Users touch and pay for these. Value flows through all three layers. But the layer closest to the user determines what that value is worth. That layer is the application and the experience it delivers.

With last two years of rapid advancements in the models by the frotier labs, the industry keeps score on the wrong leaderboard. Model leaderboards are not product-level evaluations. Teams run their own evals after building solutions. Enterprise AI value is being decided somewhere else entirely.

Aaron Levie has made this case all summer. His enterprise posts return to the same point. AI value comes from more than model capability. Agents are embedded in mission-critical workflows. They connect to enterprise systems. They need domain-specific change management. They use multi-model tuning. They use evals. They use pricing abstractions. The model is one ingredient. **The applied layer is the product.**

Sarah Tavel said the value is in the application layer way back in 2024. The application layer owns the end user. The job is to "sell the work," not sell a model. 

Satya Nadella describes a learning loop on top of models. Human capital and token capital compound. You should be able to swap out the model without losing what you built. Benedict Evans says models commoditize like telecom carriers. Value gets captured further up the stack. 

> Andrew Ng's one-liner: `applications must in aggregate be worth more than the infrastructure they run on, because applications pay for the infrastructure.`

The honest counterweight comes from a16z's Casado and Wang. Value is accruing across every layer right now. Models. Infra. Apps. Faster creation. Faster wipeout. Don't read "applied layer wins" as "nothing else matters."

But the asymmetry is real. Swapping your model vendor is easy. It takes an afternoon. Swapping everything else is hard. It takes months.

When I am working with businesses, it takes a lot of time to meet with them and build/integrate workflows that suit their business. A new model does not fix a broken integration.

You own the evals. You wrote them for your specific tasks. They measure what matters to your customers. A new model evals do not suit your product/solution evals. You would have to rebuild them.

You own the data access. You negotiated permissions. You cleaned the data. You made the data work for the workflows. You built pipelines. A new model cannot access your data until you do that work again.

You own the change management. You trained your users. You built trust. You established governance and controls. You handled exceptions. A new model does not train your users and govern for you.

The model vendor knows nothing about your business. They sold you intelligence. You modeled, built and sold outcomes to your customers. Those are different things.

The model is cheap to replace. The integration is expensive. The evals are expensive. The data access is expensive. The change management is expensive.

That is the asymmetry. One side is a commodity. The other side is compounding value. 

> The moat is not in the model. It is in everything you wrapped around it. _-- many saying it_

Think about what breaks when you swap models. It is not the intelligence. It is the prompts you tuned. It is the evals you built. It is the data pipelines you wired. It is the permissions you negotiated. It is the users you trained. It is the exception handling you coded. The model is a commodity input. The applied layer is where the work happens. That is where the value sticks.

This is why frontier labs are racing downstream. The model alone does not capture the margin. The companies making money in AI are not the ones with the best benchmark scores. They are the ones embedded in workflows. They own the customer relationship. They make the model disappear into the product.

Your model vendor can be swapped in an afternoon. Your evals compound. Your data access compounds. Your workflow integration compounds. Your change management compounds. AI is not going to replace an experienced engineers that bring all this expertise to businesses. Go and Build the applied layer!

**References:**

1. **Aaron Levie on enterprise AI value (Aug, 2026)**
   [https://lnkd.in/p/e2ggc5dT](https://lnkd.in/p/e2ggc5dT)

2. **Sarah Tavel on 20VC — "Why the Value is in the Application Layer" (May 6, 2024)**
   [https://www.thetwentyminutevc.com/sarah-tavel](https://www.thetwentyminutevc.com/sarah-tavel)

3. **Satya Nadella — "A frontier without an ecosystem is not stable" (June 14, 2026)**
   [https://x.com/satyanadella/status/2066182223213293753](https://x.com/satyanadella/status/2066182223213293753)

4. **Benedict Evans — "Ways to think about token pricing" (July 9, 2026)**
   [https://www.ben-evans.com/benedictevans/2026/7/9/ways-to-think-about-token-pricing](https://www.ben-evans.com/benedictevans/2026/7/9/ways-to-think-about-token-pricing)

5. **EQT ThinQ — "Why AI Value Won't Just Accrue to Foundational Models" (2026)**
   [https://eqtgroup.com/thinq/technology/why-ai-value-wont-just-accrue-to-foundational-models](https://eqtgroup.com/thinq/technology/why-ai-value-wont-just-accrue-to-foundational-models)

6. **a16z Casado & Wang — "Where Value Will Accrue in AI" (May 27, 2025)**
   [https://a16z.com/podcast/where-value-will-accrue-in-ai-martin-casado-sarah-wang](https://a16z.com/podcast/where-value-will-accrue-in-ai-martin-casado-sarah-wang)
