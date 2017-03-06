---
title:  "Leeds CRM workshop - 6th Jan - meeting notes"
author: Lianne Viney
categories: crm
header:
  overlay_image: /assets/images/feature-leeds.jpg
  caption: "Photo credit: Rory 89 (Own work) [CC BY-SA 4.0 (http://creativecommons.org/licenses/by-sa/4.0)], via Wikimedia Commons"
excerpt: Leeds City Council are constantly looking to improve their offering to customers and drive efficiencies and savings.
permalink: /leeds-workshop-notes
---

* TOC
{:toc}

# Attendees

From Leeds City Council		
- Dave Maidment		
- Graham Smith
- Neil Robinson
- Adam Kane

From Looking Local
- Lianne Viney
- John Latham

# Summary of landscape
Leeds City Council are customers of the Civica Contact 360 product, which they have branded ‘My Leeds’. Leeds have successfully incorporated many Environment, Waste and Street reporting transactions into ‘My Leeds’ and work to add additional transactional services into ‘My Leeds’ continues.

Leeds City Council are constantly looking to improve their offering to customers and drive efficiencies and savings. They are embarking on a collaborative project with other like-minded Authorities to consider the opportunity to move towards a ‘lighter’, ‘loosely coupled components’ approach to building transactional portal services. As such, they have invited other authorities to join them in discussing their challenges and develop a joint approach to building and procuring systems/products which would meet this goal. The result would cheaper, more flexible systems.

# Users first
In line with the government service design principles it is important to develop requirements around the needs of real users and not around the needs of the business. Scope, requirements, features, design and functionality should all be built around tested user stories. As such we started by establishing who our principal groups of users are and the types of interactions they would expect to have with Leeds City Council systems.

Principally, users fall into one of two groups:
- Staff/partner users looking to engage with information and case management systems in order to do their day jobs and administer council services.
- Citizens looking to engage with the council in order to report, apply, and receive services.

The time available during the workshop meant that we could only scratch the surface in regards to developing user stories and further work should be considered to build on and validate these user stories.

# User stories

We carried out a brief exercise to quickly map out a handful of top level user stories:

**Benefits**
> As a Customer Service Agent I need to be able to get access to benefit claim information so that I can provide the customer with an update on their claim.
> As a citizen I want to be able to apply for Housing Benefit so that I can pay my rent.

**Council Tax**
> As a citizen I need to be able to find out how much Council Tax I owe so that I can pay my bill.

**Social Work**
> As a citizen I need to be able to request a care needs assessment so that I can arrange me care package.

**Street Reports**
> As a citizen I want to be able to report a pothole so that it will get fixed.

**Waste**
> As a citizen I want to report a missed bin collection so that my bin gets emptied.

> As a citizen I want to request a bulky waste collection so that I can get rid of my old sofa.

**Registrars**
> As a citizen I want to be able to book an appointment with a registrar so I can register the birth of my child.

# Components of transactions

Picking a few of the simplest user stories we mapped out what components each of the transactions could be made up of:

**Fly Tipping**: Forms: Mapping (GIS), Task Management, Pub/Sub/Integration/Biztalk, Analytics, UTRN, Calendaring

**Missed Bins**: Forms: Gazetteer, Push Messaging, Task Management, Pub/Sub/Integration/Biztalk, Analytics, UTRN

**Potholes**: Forms, Mapping, Task Management, Pub/Sub/Integration/Biztalk, Analytics

**Registrars**: Appointments, Audit, Push Messaging, Forms, EDRMS, Customer Database, Analytics, Gazetteer

Reference was made to the Leeds CC document "Electronic Services Delivery - Technical Architecture and Components".

Combining these 2 lists, we produced a list of components:
 
- Customer and Staff portal
- Identity and Registration
- Customer Database
- Analytics and Business Information
- Forms Solution
- Payments
- EDRMS
- Push Messaging
- Export and Data Transport
- Mapping (GIS)
- Appointments/Bookings
- Gazetteer (UPRN)
- Evidence/Proofs/Self-scanning
- Calendars/Scheduling
- Audit Trail
- Pub/Sub (Biztalk/middleware)
- Case Management/Repository of tasks

![Components diagram](/assets/images/2017-01-17-leeds-workshop-notes/components.svg)

# Wrap up and next steps

This initial pre-discovery phase is being used to establish a business case to progress any resulting proof of concept work.

Leeds have numerous back office systems which are unlikely to change and are therefore considered out of scope for this project. The likes of Capita Academy benefits system and Orchard for housing services are established within the organisation.

Above we have identified the potential individual components that Leeds might need to deliver their services and the principles by which think they could hang together. So far little work has been done to establish the ‘off the shelf’ existence or otherwise of these components. Some components may need to be developed either in house or by external suppliers.
 
It might be beneficial to do some proof of concept work by starting with simple transaction such as fly tipping and attempt to build the entire transaction using the above described principles. Any progression will be dependant on the development of a business case to do so.

