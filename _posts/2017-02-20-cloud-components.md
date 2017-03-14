---
title: Cloud components
date: 2017-02-20 00:00:00 Z
categories:
- CRM
author: John Latham
header:
  overlay_image: "/assets/images/feature-leeds.jpg"
  caption: 'Photo credit: Rory 89 (Own work) [CC BY-SA 4.0 (http://creativecommons.org/licenses/by-sa/4.0)],
    via Wikimedia Commons'
redirect_from: "/cloud-components"
---

What are the opportunities for UK local authorities to develop solutions from cloud components? What are the challenges? Who is doing it already?

I am interested in the reuse of successful technology solutions between UK local authorities.

This is partly inspired by the [LocalGov Digital](http://localgovdigital.info/) network, which I've recently joined via 
its Slack channel, but also by the history of Looking Local which has been run as a traded service by Kirklees Council 
since around 2006 to help spread the costs of technology development.

**What are we doing?**

Looking Local makes heavy use of cloud services to build and host its products. The most important of these is Amazon Web Services, on which we run around 50 virtual web servers (Apache Tomcat) 
and a number of database servers.

In addition to AWS our products have the following SaaS dependencies: Contentful (API-first content management), elastic.co (website search), Esendex (push messaging), Github (software change management), Google Cloud Platform (real-time databases and big data), and Travis (continuous integration).

We also rely on a cloud of supporting SaaS applications to support the products and our team: AppFigures (monitoring uptake of our smartphone apps), Atlassian OnDemand (issue tracking), Dropbox (internal file sharing), Google for Work (e-mail), Slack (team comms), and UptimeRobot (availability monitoring).

We are in the business of developing software and are lucky to have a talented team of software engineers, but we try to 
write as little code as possible so that the code we do write is better. We rely on a deep stack of [free software](https://www.gnu.org/philosophy/free-sw.en.html) components 
to help us write less code, but we also look first for a SaaS (software-as-a-service) solution before 
hitting the keyboard to develop something new. This *constructive laziness* is a powerful productivity pattern.

**What looks promising?**

Some parts of the CRM layer are already well-supported with SaaS solutions targeted at UK local public sector, e.g. [GOSS Forms](https://www.digitalmarketplace.service.gov.uk/g-cloud/services/7930072465972187) and [FirmStep AchieveForms](https://www.digitalmarketplace.service.gov.uk/g-cloud/services/7538519155506750), although it's not clear whether these are fine-grained and open enough to be considered cloud components, or simply monolithic software which is sold as a service.

GOV.UK is developing SaaS solutions in its *Government as a Platform* initiative: Verify, Pay, and Notify being prime examples. These are becoming available to local government (albeit slowly).

Box, one of the leading corporate cloud file storage vendors, has several interesting features that make it a candidate for this cloud composition model. Box is EU-hosted, on G-Cloud and the security/data governance looks good. They recently announced [support for custom metadata](https://docs.box.com/blog/add-custom-metadata-to-a-file) and workflow (the [Relay](https://www.box.com/collaboration/relay-workflow) product, currently in beta, generally available in mid-2017). These capabilities have the potential to move the Box offering from simple cloud file storage to something closer to a full EDRMS solution, but with all the webhooks and APIs required to knit it together with other components.

At the extreme end of SaaS adoption, all solution components are rented SaaS, and integration between these products is configured *within* these products. 
This requires each product to have appropriate native "connectors", e.g. compatible webhooks.
For instance, we can have Userlike (a SaaS chat platform) post incoming conversations to Slack, so that team members do not need to keep Userlike open through their working day in order to provide responsive support.

Where a native connector does not exist, we can use an _integration platform as a service_ (IPaaS) to link products together.

At the lighter "no code" end of the IPaaS spectrum, typically targeted at consumers and SMEs, are services from [Zapier](https://zapier.com/) and [Workato](https://www.workato.com/).

At the heavier end the lead offerings are the likes of Mulesoft Anypoint Platform, Dell Boomi, SnapLogic, Informatica, and Jitterbit Harmony (source: Gartner's [2016 Magic Quadrant For Integration Platform-As-A-Service](https://www.gartner.com/doc/reprints?id=1-31XRY2I&ct=160325&st=sb)). Also noteworthy is [Adaptris Cirrus](http://www.adaptris.com/pages/products-and-services/cirrus), based in the UK and identified by Gartner as a "challenger" (executes well enough to be a serious threat to the leading vendors). *Note: this is not an endorsement of Gartner's analysis.*

Microsoft is a late entrant to this space with BizTalk Services and Logic Apps, which may be useful to councils with experience of on-premise Biztalk Server who want to move to IPaaS or assist others to do so.

**Who is doing this?**

UK local authorities are (like other organisations) trying to find the balance between renting SaaS solutions, managing licensed software on premise or in their own datacentres and developing their own software. They have mostly the same statutory requirements as each other but have different resources available.

One borough council is planning to replace their monolothic CRM solution with a collection of cloud services:

> That's what we're trying to achieve: Box for storage / access, O365 for document editing, Salesforce / web based LOB, Okta for SSO to join them all together.

I'd love to hear from other councils integrating cloud components into their solutions.

**What are the limitations and risks?**

SaaS enables easier integration *in principle* since the software is securely hosted on the public internet. It does not, however, guarantee open or easily integrated. Compare search results for [AchieveForms api](https://www.google.ie/search?q=AchieveForms+api&gws_rd=cr) and [Typeform api](https://www.google.ie/search?q=AchieveForms+api&gws_rd=cr). The first takes you to a dead link which redirects to the Firmstep home page, the second to comprehensive documentation and examples. Unfortunately Typeform is not targetting UK public sector, they have only a weak commitment to accessibility and no plans to provide services outside of the US. (Maybe AchieveForms has excellent API documentation; I couldn't find it.)

Many SaaS solutions, particularly at the cheaper "no code" end of the spectrum, are targeted primarily at businesses. Government is not like business, it has different and much more varied statutory obligations with which all public servants strive to comply. A business can mostly ignore the needs of those at the margins of society if it chooses to; these are often the state's "best customers". Even where businesses have strict obligations to society, compliance is sometimes a risk-reward calculation (see [Ford Pinto](https://en.wikipedia.org/wiki/Ford_Pinto) controversy).

Evidence of this inadequacy can be found in poor or absent compliance with accessibility guidelines and US-hosted solutions which require cross-border transfers of personal data.

So we should look for components amongst the best that private sector SaaS providers can offer, and embrace government SaaS initiatives (GOV.UK GaaP) where they bear fruit, but [plan](./approaches-to-solution-development) for when these solutions are absent or immature. 

How does SaaS change the implementation and support effort? 

Cloud software is upgraded continuously by the supplier. Whilst these upgrades are almost always backwards-compatible, features do get deprecated and withdrawn. Whole 
services get decommissioned typically with 12 months or less notice, and when this happens there is no way to extend, 
it's a race to migrate off the platform before your data is deleted.

[Parse.com](https://en.wikipedia.org/wiki/Parse_(company)), a *mobile-backend-as-a-service* provider acquired by Facebook in 2013, announced shutdown in Jan 2016 for Jan 2017. The [Parse platform](https://parseplatform.github.io/)  was released as open-source and several companies stepped up to provide hosting. This was a relatively happy ending.

Nonetheless, the dynamic nature and more fine-grained nature of SaaS offerings represents something of a treadmill. As soon as you've finished one piece of integration you'll need to look afresh at the marketplace to evaluate new products and new features of existing products, and to check for deprecation of existing products and features.
