---
layout: page
title: STANKYLeg
permalink: /stankyleg/
nav_order: 7
---

**STANKYLeg**

STANKYLeg is the module that handles animations for STANK.  It uses Mecanim by default and builds a custom layer containing any animations defined in your STANKResponses, if they exist, and triggers them when appropriate.

No modifications need to be made to your AnimatorController.  STANKYLeg is designed as a fully automatic system that plays your animations when they should play without being intrusive into the rest of your workflow.

If you're using an animation system other than Mecanim, you can derive a custom script from STANKResponseListener and implement the ISTANKResponse interface to tie your script into the STANKResponse event system and ensure the ProcessThreshold() method is included in your script.
