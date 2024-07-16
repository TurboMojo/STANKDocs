---
layout: page
title: STANKEye
permalink: /stankeye/
nav_order: 5
---

STANKEye is a system that utilizes multiple components for various behaviors.  It's responsible for displaying visual parts of STANKResponses, such as particle systems and icons.  The base STANKEye script should be attached to your Feller gameobject and any of the system's other scripts must be attached as a child of the Feller.

**STANKResponseParticles**

STANKResponseParticles is the STANKEye module that plays particle systems when STANKResponses are triggered.  You can use the Prefab or attach the STANKResponseParticles component to any Particle System.  It only needs to be configured with a STANKResponse association and made a child of the Feller.

**STANKResponseAudio**

STANKResponseAudio is very similar to STANKResponseParticles.  Just attach it to an AudioSource that's also a child of your Feller and configure it with a STANKResponse.
