---
title: ScanStation Show and Tell - 6th Feb - Q&A
date: 2017-02-08 00:00:00 Z
categories:
- ScanStation
author: Rhea Cunio
header:
  overlay_color: "#8681bf"
excerpt: Yesterday LookingLocal and Kirklees Council hosted their third ScanStation
  Show and Tell day, which saw 15 local authorities making a visit to Kirklees to
  see the ScanStation platform up close and hear about its implementation at the council.
---

Yesterday LookingLocal and Kirklees Council hosted their third ScanStation Show and Tell day, which saw 15 local authorities making a visit to Kirklees to see the ScanStation platform up close and hear about its implementation at the council.
 
ScanStation is Kirklees Council’s new self-serve document scanning platform which is helping to reduce queues and create a more efficient customer contact centre. The platform consists of a touch screen, tablet-enabled app enabling customers to self-scan documents to support a range of government services, e.g. housing benefit, council tax reduction, disabled travel passes and blue badges. As a combined software and furniture solution, ScanStation ensures quality images every time, can integrate with any back-end system and is a simple, accessible customer-focused solution.
 
Our Show and Tell sessions are designed to be as interactive as possible, giving delegates the freedom to ask as many questions as they like and really get under the skin of the technology.
 
Below are a few of the key questions and answers from the day that we wanted to share:

Q: In regards to the integration into back office systems, is that via an API?

>Yes, full integration would require a suitable API. In the case of Kirklees a web service was built to allow scanned proofs to be imported into their Generic Import Module (GIM) within Northgate. From there they are passed through to Anite for processing.
 
Q: Have you encountered any bugs or issues with ScanStation?
>Before ScanStation went live there were a couple of issues with internet connectivity. However, this was purely a location-based issue. LookingLocal will advise each local authority to have strong enough WiFi capability in place prior to implementation. You can read about other lessons learnt during the development of the platform here.
 
Q: Is there a possibility for high error rates?
>There is always the potential that the customer uses the wrong claim reference which could result in the wrong evidence being attached to the wrong file. However, this could happen with postal evidence. When some form of the process includes human involvement there is always room for mistakes. However, we believe the risk of any back office mistakes are now significantly reduced.
 
Q: When the tablet screen goes to timeout - does that take you back to the beginning?
>Yes - after a certain amount of inactivity the tablet screen logs the customer out and you are taken back to the login screen. Kirklees configured the app like this for security reasons. However, you can preconfigure this time-out period depending on your preferences. Images that are scanned are stored in a temporary cache and so are completely wiped from the device once submitted (or time-out occurs), again for security reasons.
 
Q: Where does the address data come from?
>In the case of Kirklees, the customer address data comes from their Local Land and Property Gazetteer (LLPG) - although other lookups such as Google Maps Geocoding API can also be used.
 
Q: Do you consolidate the images into one document?
>Yes, into a multi-page PDF file.
 
Q: Isit easy for the back office to match claims?
>We’ve found that with the use of ScanStation back office staff are more than happy with the quality of scanned documents and we’ve found that everything has been indexed by the system correctly.
 
# Statistics from ScanStation’s implementation at Kirklees

- The average customer scans 3-4 documents and takes on average 3.4 mins to complete the whole process - from logging in to submitting all scanned docs
- Near on 100% of customers have channel shifted to the online self-serve approach with only 1% needing some sort of assistance from a floor-walker
- Customers have rated the platform 9/10

The results are fantastic and this is why Kirklees are keen to share this technology with other local authorities who want to diminish queues and create a more efficient customer contact centre.

This event was very popular and did sell out. We have therefore added a second event date for the 10th March and again this is filling up quickly. You can register for the next ScanStation Show and Tell day [here](here).

Alternatively, if you would like a local briefing of the product please email [scanstation@lookinglocal.gov.uk](mailto:scanstation@lookinglocal.gov.uk).

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
