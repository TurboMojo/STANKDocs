---
layout: page
title: Fellers
permalink: /fellers/
nav_order: 4
---

Fellers are attached to your characters and NPCs.  They're responsible for handling sensory perception and triggering responses.  They do this by comparing the pungency of any smells being experienced by the Feller with the STANKResponses defined in the feller.  When a pungencyThreshold in the STANKResponse is reached, the response is triggered.

Responses is a list of STANKResponses that apply to this Feller.  Each Feller can have its own set of STANKResponses, so they may react at different thresholds or have different responses.

Acuity is a measure of how good the Feller is at smelling things.  For most purposes, this should probably always be set to 1.  It multiplies the base evaluation of a Stank's pungency.  It allows for stat modifiers to make the Feller better at smelling.

Reaction Delay is the minimum allowed time in seconds between triggered reactions.  If this is set to 0, the Feller will continually loop all responses.  This should be set to a value that's at least the duration of the Response itself, but most likely longer to avoid infinite loops.

Fellers require a companion component to define how the TakeAWhiff method in Feller should be called.  

**AutoSniffer**

AutoSniffer sniffs at regular intervals defined in the inspector.  This should be used when smelling is a passive action taken by a Feller, rather than an active action taken by the player.

**FellerSniffer**

FellerSniffer sniffs from player input.  This is the component you want to use when you want the player to be directly in control of the sniffing.
