---
title: "Handle Tags in Obsidian and on the Quartz Website"

---
# Handle Tags in Obsidian and on the Quartz Website

**Problem**: I want to use obsidians nice autosuggestions when adding tags, but this is not possible when adding tags that is understandable for Quartz (Hugo under the hood).

A few things to know about tags for Quartz and Obsidian.
- The tags described for Quartz are working and searchable in Obsidian
- If a Quartz tag starts with # it is not showing on the web
- When writing Quartz tags no autosuggestion is showing
- When writing Obsidian tags (starting with #)autosuggestion is showing

## Discord Discussion
https://discord.com/channels/927628110009098281/927628110009098284/1021167575964586026

	This is something that you could bring up in Obsidian forums/discord. I'm pretty sure if you add a `#` before typing while in the yaml it still autocompletes, so i'm sure there's a plugin that could just remove the `#` after

-CyanDuck

## Resources for Solving the Problem
[Serhii Hamotsky blog post](https://serhii.net/blog/it/2021-11-29-211129-0126-obsidian-to-hugo-tags-script-and-template/) has a hacky solution with issues.

