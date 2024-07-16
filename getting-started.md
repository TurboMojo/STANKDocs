---
layout: page
title: Getting Started
permalink: /gettingstarted/
nav_order: 2
---

Getting Started

The basic workflow for STANK consists of three parts: 

- Fellows - characters or NPCs

- Stanks - the smells to be smelled

- STANKReactions - Defines a threshold for a Stank on a Feller and data necessary to drive behaviors in response to the level of a Stank detected.

Each Feller can have any number of STANKReactions defined for each Stank.

To get started, create a new Stank either from the STANKBank option in the Tools menu or the STANK context menu in the project window.

If you have a character set up, add the Feller prefab from the STANK/Prefabs folder as a child of your character.  

Create a STANKResponse from the STANK context menu in the project window.

Configure the STANKResponse with a Stank and a pungencyThreshold.

Add the Smeller prefab from the STANK/Prefabs folder as a child to any object you want to be smelled and add the STANK you created earlier to the Stank field for the Smeller.

Adjust the radius of the smeller to define how far away it should be smelled by Fellers.

Adjust the Pungency curve to define how the smell's intensity varies with distance from the Smeller.

If you wish this Smeller's radius to expand over time, enter a value greater than 0 to the Expansion Rate field.  This will expand the Smeller's radius at a rate of X meters per second over the lifetime of the Smeller.

If you wish to display particle systems that denote this smeller's presence, add them to the StankLinesEmitters list and check the ShowStankLines checkbox.

At this point, you have the necessary elements in place to detect and react to Stanks.  However, you're not actually triggering any behaviors yet.  STANKResponse uses an event system to trigger behaviors in response to the threshold being reached.  You'll need to utilize some scripts that can take advantage of this system to trigger particle systems or sound effects.

To trigger particle systems, create a particle system gameobject and position it appropriately in your character's gameobject hierarchy.  Add the STANKResponseParticles component and assign the STANKResponse that should trigger it.

To trigger sound effects, follow a similar pattern.  Create an AudioSource gameobject positioned appropriately in your hierarchy and add the STANKResponseAudio component to it.  Add the appropriate STANKResponse to the inspector field.

Now, whenever your Feller gets within sufficient range of a Smeller for the Smeller's Pungency to exceed the STANKReaction's pungencyThreshold, the particles and sound effects configured to use that STANKReaction will play.
