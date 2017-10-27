---
layout: post
title: Bring on the v2
subtitle: Revamping APIs
date: '2017-10-12 12:01:47 +0100'
tags: [snomed, api]
---

Over the last few years, the team at SNOMED International have implemented a number of open REST APIs as part of the rapid development of tools to manage and interact with SNOMED CT.


Any software development project involves looking for the best balance between elegance and clarity in designs and developments, against the business need for speed of deployment. Our approach has leaned more to necessity and speed. Now that we have moved to a more stable development phase, we have the time to review and refactor our APIs to present a more standard view.


At the moment, our most commonly used APIs are those used in the SNOMED CT Browser, amongst the first ones that we developed (SNOMED CT Snapshot REST API). This has been the ideal place to start, looking to see how we can provide more standardized APIs so that any consumers can expect the same standard.


And like magic this has been done and v2 of the API has now been deployed. More details can be found here - [http://ihtsdo.github.io/sct-snapshot-rest-api/api.html](http://ihtsdo.github.io/sct-snapshot-rest-api/api.html).


The main highlight is the JSON representation of a concept, which uses standard terms for the labels, instead of shortcuts like the current version, and provides most things that would be needed to represent a SNOMED CT concept in one call

Feedback is always welcome.
