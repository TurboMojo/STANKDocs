---
layout: page
title: Getting Started
permalink: /gettingstarted/
nav_order: 2
---

**Getting Started**

The basic workflow for STANK consists of four parts:

- [Feller]({{ site.baseurl }}{% link Fellers.md %}) - characters or NPCs that can smell stanks and have responses to them
  
- [Smeller]({{ site.baseurl }}{% link smeller.md %}) - objects that smell
  
- [Stank]({{ site.baseurl }}{% link stank.md %}) - the smells that things that smell smell like
  
- [STANKResponse]({{ site.baseurl }}{% link stankresponse.md %}) - Defines a threshold for a Stank on a Feller and data necessary to drive behaviors in response to the perceived pungency of a Stank.
  

1. To get started, create a new Stank either from the STANKBank window in the Tools menu or the STANK context menu in the project window.
  
2. If you have a character set up, add the Feller prefab from the STANK/Prefabs folder as a child of your character.
  
3. Create a STANKResponse from the STANK context menu in the project window or from STANKBank.
  
4. Configure the STANKResponse with a Stank and a pungencyThreshold.
  
5. Add the Smeller prefab from the STANK/Prefabs folder as a child to any object you want to be smelled and add the STANK you created earlier to the Stank field for the Smeller.
  
6. Adjust the radius of the smeller to define how far away it should be smelled by Fellers.
  
7. Adjust the Pungency curve to define how the stank's pungency varies with distance from the Smeller.
  
8. If you wish this Smeller's radius to expand over time, enter a value greater than 0 to the Expansion Rate field. This will expand the Smeller's radius at a rate of X meters per second over the lifetime of the Smeller.
  
9. If you wish to display particle systems that denote this smeller's presence, add them to the StankLinesEmitters list and check the ShowStankLines checkbox.
  

At this point, you have the necessary elements in place to detect and react to Stanks. However, you're not actually triggering any behaviors yet. STANKResponse uses an event system to trigger behaviors in response to the threshold being reached. You'll need to utilize some built-in scripts or write your own that can take advantage of this system to trigger response behaviors.

To trigger particle systems, create a particle system gameobject and add it to the scene as a child of your Feller gameobject. Add the STANKResponseParticles component and assign the STANKResponse that should trigger it.

To trigger sound effects, follow a similar pattern. Create an AudioSource gameobject positioned appropriately in your hierarchy and add the STANKResponseAudio component to it. Add the appropriate STANKResponse to the inspector field.

Now, whenever your Feller gets within sufficient range of a Smeller for the Smeller's Pungency to exceed the STANKResponse's pungencyThreshold, the particles and sound effects configured to use that STANKResponse will play.
