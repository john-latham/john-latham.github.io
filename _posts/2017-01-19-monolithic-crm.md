---
title: Alternatives to monolithic CRM
date: 2017-01-19 00:00:00 Z
categories:
- CRM
author: John Latham
header:
  overlay_image: "/assets/images/feature-leeds.jpg"
  caption: 'Photo credit: Rory 89 (Own work) [CC BY-SA 4.0 (http://creativecommons.org/licenses/by-sa/4.0)],
    via Wikimedia Commons'
redirect_from: "/monolithic-crm"
---

Expensive, awkward to integrate, confusing for users?

* TOC
{:toc}

# Background

Leeds City Council have joined with members of LocalGov Digital to discuss their common challenges and develop a joint approach to building and procuring the systems with which citizens interact, often referred to as CRM (Customer Relationship Management).

There is a suspicion that  the 'monolithic' and proprietary nature of these systems is part of the problem, leading to long initial implementation, problematic integration with other systems and painful upgrade/replacement cycles, and that alternative approaches may deliver cheaper, open and more flexible systems.

The objective is to do a better job of meeting the needs of the citizen for a given amount of technology spend and associated implementation and support effort.

The working group is ambivalent at the outset about whether the answer lies in better market engagement, co-funding development of new solutions, or better exploiting the solutions already in place.

# What's the problem?

A monolithic product is composed of inseparable parts. In the CRM context, all functions of the governing customer-interaction (forms, notifications, authentication, visual styles etc) are part of a single software product from a single supplier.

This brings internal challenges, such as the time taken to migrate selected services into the solution and the risks associated with relying on a single  supplier for many critical transactions.

There are also important effects on user experience where different Council services present different features depending on which product they were implemented in. This isn't purely an issue of aesthetics or consistent navigation.

A product may offer a sign-in solution to allow users to maintain a "citizen account" with the council. This may offer benefits to the user in terms of following up, but equally offers the Council a "single view of the customer".  When the system is introduced alongside anonymous services this isn't initially problematic. The Council can promote "My *Council name*" for new transactions in Contact360, and the others will continue as before without identity.

The major issue comes when the Council wants to implement another solution that requires or offers identity and which does not integrate out of the box with Contact360. "My *Council name*" is taken already - there can't be two of them.

This is perfectly executed vendor lock-in, in which the choices are typically (a) use the same platform for all services regardless of fit, or (b) pay the vendor to integrate with an open identity solution (Verify, Okta, auth0 etc).

# What's the alternative?

An alternative is to compose customer-interacting services by integrating smaller distinct components.

This is not a new idea. It has roots in aspects of the Unix philosophy first articulated in 1978.

> Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features".

*Doug McIlroy, The Bell System Technical Journal*

Example components in the CRM layer might be:

- Web-based forms
- Identity
- Analytics
- Notifications
- Web chat
- Standards may be used where appropriate to reduce integration costs and ensure consistency of user experience.

For instance, the Identity Provider may support standard mechanisms for authentication and authorization such as OpenID, OAuth2, or SAML.

The forms service may comply with specific WCAG accessibility standards, use well-researched patterns from the GOV.UK Service Manual, and follow a standard visual style imposed by the Council.

Other services are typically designed for easy integration (analytics, web chat) so can be selected purely on features and price.

# Why have vendors not offered integration-friendly solutions?

Whilst there are cynical commercial reasons to offer solutions which are expensive to integrate and difficult to replace, vendors targeting the UK public sector have some justification for offering monolithic solutions. When the sale is business-led rather than IT-led, a solution which is presented as having fixed costs and not requiring effort from/engagement with IT is more appealing and appears less risky. This is evidenced by the proliferation of "no-code" and "low-code" offerings which are often followed up with integration and customisation services when the limits of configuration are reached.
 
Besides which, there's no point in developing an integration-friendly product if there exist few complementary products with which to integrate.

# Sub-critical mass of UK public-sector appropriate solutions

Outside public sector, the "API economy" is well-established. Time to market is critical; vendors focus innovation on a narrow area of functionality. Typically supplied as “cloud services”, products require no on-premise management and are automatically upgraded and hardened to resist security threats. This reduces implementation costs and total cost of ownership. Customers leverage API integrations to complete the solutions. Lower-level “platform as service” (PaaS) offerings are built on to provide higher-value “software as a service” (SaaS) products.

Many of these products are developed by US companies primarily targeting US private sector customers. Consequently, these products often do not meet the strict requirements of the UK public sector who have greater statutory obligations than the typical private sector SaaS customer.

For instance, in early 2015 LookingLocal evaluated eight Forms as a Service (FaaS) products with significant market presence share (not specifically in UK public sector) which are designed to allow non-programmers to develop forms capability. Of those eight, only two claimed to be compliant with section 508 (as US Federal govt standard) or the W3C Web Content Accessibility Guidelines (WCAG). The remaining two products stored data outside the EU, and neither of those were signed up to the Safe Harbour Privacy Principles in force at the time to regulate EU-US data transfers.

# Recent developments in the API economy

Some services are not sensitive to data governance or accessibility issues, either because they hold no sensitive data (e.g. Analytics) or because they have no end-user interface (e.g. push messaging middleware).

There are signs that as the API economy matures, vendors will increasingly focus on issues of importance to government customers (like data governance) to differentiate their offerings. For instance Dropbox, the leading provider of consumer- and SME-oriented cloud storage, started trialling EU data hosting in mid-2016 for business and education customers with 250 seats or more, and expect to roll this out to smaller customers in future. *([Box](https://box.com) offers EU hosting already, and is available in GCloud).*

The UK Government Digital Service (GDS) is developing reusable services as part of its Government as a Platform (GaaP) strategy. For instance: Verify for identity and Notify for SMS notifications/transactions. Whilst their initial focus has been on central government, these offerings are starting to become available to local authorities and this availability is expected to improve in 2017.

# What to do where no solutions exist in the market?

It is not necessary to rely wholly on off-the-shelf cloud solutions to achieve the goal of a loosely-coupled CRM infrastructure.

Consistent signalling of integration requirements to existing vendors in the UK public sector market, through both informal pre-sales channels and formal procurement requirements, ought to focus minds on the importance of making products easier to integrate and reconfigure over time.

Where vendors are not stepping up to offer solutions, public bodies may co-fund the development of products or offer their own solutions to each other through [sharing of code and solution designs](./sharing).
