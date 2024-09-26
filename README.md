---
title: Smell Tracking and Notification Kit
layout: home
nav_order: 1

---

![STANKBanner_large](https://github.com/user-attachments/assets/63b7e7c0-bc70-4f98-a3f3-3e6e43e3b913)

Smell Tracking and Notification Kit is a plugin for Unity that allows developers to add a sense of smell to their game.  STANK enables characters and NPCs to be aware of smells and respond to them in a variety of ways depending on the perceived pungency of the smell.  The goal of STANK is to enable game designers to craft fresh, new, immersive gameplay experiences using olfactory sensory perception to drive stimulus responses.

The primary working units of STANK are [Fellers]({{site.baseurl}}{% link Fellers.md%}), [Smellers]({{site.baseurl}}{% link smeller.md%}), [Stanks]({{site.baseurl}}{% link stank.md%}) and [STANKResponses]({{site.baseurl}}{% link stankresponse.md%}).  These classes establish the sensory perception system that drives all other behaviors.  Fellers are your characters, whether it's the player or NPCs.  Fellers can smell things and be aware of them.  Smellers smell.  They emit odors that can be perceived by Fellers.  Stanks are how the smells are defined.  STANKResponses define a pungency threshold at which to trigger the response.

The connection between Fellers and Stanks is a [STANKResponse]({{site.baseurl}}{% link stankresponse.md%}).  It defines a perceived pungency threshold for a Stank for a Feller and triggers an event system which is used by supporting components in the Feller's hierarchy.  These components can trigger any custom code, but included components make it easy to play particle systems, visual effect graphs and sound effects, display icons, and more.

STANKResponses define a system that can trigger anything on a Feller.  At this time, STANK supports audio sources, particle systems, and HUD icons.  They use a custom event system that can trigger any custom behaviors.
