---
layout: page
title: Smeller
permalink: /smeller/
nav_order: 5

---

![Smeller](https://github.com/user-attachments/assets/aeda0dc5-56ba-47d2-a17d-dd4e2f6a4837)

Smellers are the things in your game that stink.  Anything that Fellers should smell need a Smeller component to give them that special aroma.  Smellers define a Stank, a radius, and a pungency curve.

Stank is obviously the smell you want your Fellers to smell.

Radius is the radius around the smeller within which fellers may be able to detect the Stank.  The radius is visualized as a colored sphere in the editor.  You can adjust the color of the sphere by editing the Gizmo color of the Stank.

PungencyCurve is an AnimationCurve that defines the pungency falloff from the Smeller.  It should define a 0-1 multiplier applied over the radius of the Smeller where the center of the radius is defined by the beginning of the curve and the outermost edge of the radius is defined by the end of the curve.

Expansion Rate defines the rate at which the radius will expand in meters per second.  If the smeller's radius should stay static, set this to 0;

hudImage defines an image to be used by STANKEye to create and display an icon when the Smeller is detected.

ShowStankLines and StankLinesEmitters allows you to display a visual indication of the scent at the location of the scent.  You can have traditional "stink lines" or you could use something like flies.
