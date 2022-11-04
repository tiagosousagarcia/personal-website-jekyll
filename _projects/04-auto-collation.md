---
title: Auto Collation
blurb: An ATNU pilot project that allows editors to upload transcriptions of witness for automated collation.
layout: page
---

This is an [ATNU project]({{ site.baseurl }}{% link _projects/02-atnu.md %}) led by me in collaboration with [James Cummings](https://www.ncl.ac.uk/elll/people/profile/jamescummings.html), developed by Kate Court and Fiona Galston from [Newcastle University's Research Software Engineering Team](https://rse.ncldata.dev/). The idea for this project grew from a problem I encountered during the conception of the [*Coopers Hill* edition]({{ site.baseurl }}{% link _projects/03-coopers-hill.md %}): how can we make preliminary results from textual editing work available, without having to re-encode and re-publish the edition everytime we add a new witness?

The solution we found is a combination of [stand-off markup](https://wiki.tei-c.org/index.php/Stand-off_markup), a user-friendly uploading system, and some rudimentary automatic collation achieved by comparing the existing witnesses with the newly uploaded encoded transcriptions.

In the specific case of *Coopers Hill* this works by having a set of stand-off markup archetypes (i.e., one for each edition of the poem) which will collect both annotation and textual variants. These archetypes will be automatically updated when a new witness is uploaded: each time a new variant is discovered, the system will compare it with existing witnesses that conform to the same archetype (for example, each existing witness for 1642), identify any line variation, and record its place of variation in the archetype, linking to the original encoded transcription.

This system ensures that, unless major variants are discovered for each archetype, the framework of the edition remains stable whether it includes one or one hundred witnesses, greatly diminishing the work of manually adding each small variant, reducing the need for constant re-encoding and re-publishing of the edition, while ensuring that the latest version possible is always available to readers.

This systems is currently under development, but its release is imminent! Stay tuned for more.