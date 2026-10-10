---
name: Jekyll preview watching
description: A Replit-specific watch-loop risk when previewing a root-level Jekyll site.
---

Explicitly exclude Replit-generated log and cache directories from the Jekyll source watcher, even when they are hidden directories and would not be copied to the public website.

**Why:** A root-level Jekyll preview can watch its own host-generated workflow logs; each rebuild then writes a new log entry and triggers another rebuild.

**How to apply:** Keep host-maintained log/cache trees excluded whenever configuring a root-level Jekyll preview.
