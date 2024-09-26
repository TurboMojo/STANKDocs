---
layout: page
title: STANKResponse
permalink: /STANKResponse/
nav_order: 8
---

The STANKResponse class ties together your Fellers and the other systems in STANK.  It defines the conditions necessary for a Feller to respond to a Stank.  Each Feller may have their own set of STANKResponses or they may be shared, if you want Fellers to react the same way to the same smells.

STANKResponse defines an event system to which all active components of STANK subscribe for each Feller.  STANKResponseParticles, STANKYLeg, and STANKResponseAudio all subscribe to this event system and, where appropriate, compare the triggered response with the response configured in their inspectors then play, depending on if they match.

Utilization of STANKResponses in custom scripts depends on inheriting from STANKResponseListener and implementing the ISTANKResponse interface.  This will include your script in the STANKResponse system and allow you to drive custom behaviors in response to olfactory stimulus.  You should call your custom code from the ProcessThreshold() method provided by ISTANKResponse.
