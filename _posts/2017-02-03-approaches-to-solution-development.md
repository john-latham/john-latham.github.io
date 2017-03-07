---
title:  "Approaches to solution development"
author: John Latham
categories: CRM
header:
  overlay_image: /assets/images/feature-leeds.jpg
  caption: "Photo credit: Rory 89 (Own work) [CC BY-SA 4.0 (http://creativecommons.org/licenses/by-sa/4.0)], via Wikimedia Commons"
redirect_from: /approaches-to-solution-development
---

How might councils approach development of technical solutions with a view to collaboration and re-use?

* TOC
{:toc}

# Background

Leeds City Council have joined with members of LocalGov Digital to discuss their common challenges and develop a joint approach to building and procuring the systems with which citizens interact, often referred to as CRM (Customer Relationship Management).

The objective is to do a better job of meeting the needs of the citizen for a given amount of technology spend and associated implementation and support effort.

There is a belief that  the 'monolithic' and proprietary nature of these systems is part of the problem, leading to long initial implementation, problematic integration with other systems and painful upgrade/replacement cycles, and that alternative approaches may deliver cheaper, open and more flexible systems.

What routes are there to the commissioning/development/composition of replacement systems?

This post briefly offers some alternative approaches to solving the technology problems from the perspective of an engineer, assuming a wider context of user needs-driven process such as the [Local Government Digital Service Standard](http://localgovdigital.info/localgov-digital-makers/outputs/local-government-digital-service-standard/standard/).

# Service-requirements first approach

- Define the customer interactions that need to be supported
- Define the scope of the system, what's inside and outside the “system boundary”
- Consider the requirements for UX consistency with other services used (at least provided by the same Council) 
- Define non-functional requirements (e.g preference for on-premise vs cloud hosting, availability of skilled staff to implement, support and extend the solution)
- Buy or build components to meet the requirements (or a single product, in the old way of doing things)

This is an approach used in a traditional IT procurement. It seems logical. Why wouldn't we want to fully determine the requirements first? The problem is that we're eliciting a wishlist without giving people any steer about what's easy or hard.

People get psychologically anchored to requirements that aren't strictly necessary. Do we really need a full audit trail of every change to a record? Do forms really need to work offline?

It's also difficult to draw the system boundary. Where do we stop?

# Capabilities-first approach

- Look for components in the market (and those in use or latent in the Council) that offer compelling capabilities and can be easily integrated together with each other and with existing systems
- Rapidly formulate a service using these components
- If a component doesn't exist or doesn't have the right integration options, try to bend the solution around it or use an integration platform to glue things together
- Engage service users (public) early, fine-tune, add and replace components to improve user experience
- As a last resort, build components from scratch

This is a more pragmatic approach, "go to war with the army we have (or can assemble at short notice)" philosophy.

Examples:
- How could we re-imagine our bulky waste collection service using GOV.UK design patterns and “Government as a Platform” (GaaP) components (Verify, Notify, Pay, webchat)?
- How could we compose a Mental Health Assessment tool using only cloud-based components, so that it may be re-used by other Councils with minimal IT involvement?

# Product-first approach

- Take an existing product which is working well in a Council, supports most of the capabilities/service requirements and is unencumbered by re-use restrictions (open source or Council-owned) but perhaps isn’t yet ready for re-use or re-composition.
- Adapt the product to make it more suitable for re-use
- Re-compose the product in a new environment, taking into account local requirements

Examples:
- How could we reverse-engineer the Leeds case management solution, replacing all Leeds-specific parts with minimally-functional off the shelf components?
- How could we adapt the Monmouthshire case management solution such that it can be re-hosted by other Councils, applying their own branding and business rules?
- How could we extract the Housing Benefit/Council Tax Reduction form from the Better Off benefits advice platform?
