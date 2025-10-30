---
layout: post
title: "Week 1: Starting My Security Research Journey"
date: 2025-11-01
categories: learning
---

## Why I'm Here

I'm coming from work that makes me feel dead inside. Not "bad job" dead—*existentially* dead. The kind where you're solving problems that don't matter, where depth is punished and superficiality rewarded, where every day feels like asking permission to use your brain.

I have an MBA. I've built BI systems and ETL pipelines. I can navigate corporate politics when I force myself to. But I'm autistic, and masking for 40+ hours a week while pretending complexity is a liability rather than an asset is unsustainable.

I need to prove to myself that I can do genuinely hard things. I need work where divergent thinking is an advantage, not something to hide. And I need evidence—public, undeniable evidence—that I'm capable of mastering something complex and valuable.

So here we are: a 12-month sprint to become a security researcher.

## What I'm Building Toward

Not a corporate security job. I'm not training to get hired—I'm becoming a researcher. My goal is to operate independently by Month 12:

- **Bug bounty income**: $2-5k/month sustainable
- **Original research**: Published findings on AI/cloud security
- **Tools people use**: 6-8 production-quality security tools
- **Reputation**: Known in the AI security community

Job offers might come. If the right one appears—remote, autonomous, meaningful work—I'll consider it. But employment is an option, not the destination.

## Week 1: The Boring Infrastructure Part

I have a hard time working without foundational guardrails, so Week 1 was pure setup:

**Day 1: Technical Environment**
- Chose TryHackMe over Hack The Box (easier entry, structured paths) as a starting place
- Set up SSH keys for GitHub (learned basics about public/private key cryptography)
- Configured VS Code for Python security work
- Registered AWS and Azure accounts for later cloud security work
- Set up Bitwarden for credential management (first lesson in security: manage secrets properly)

**Day 2: Public Presence**
- Built this blog using Jekyll and GitHub Pages
- Fought with dark mode configuration (GitHub Pages uses old minima version, required `remote_theme` workaround)
- Created security-tools and research-notes repositories
- Set up X account and followed professional security researchers
- Wrote this post

**What actually took time:**
- Learning an open source credential manager
- Understanding Jekyll's theme system and why dark mode wasn't working properly
- Debugging OAuth issues with Azure portal (ended up being an outage)
- Learning the difference between `theme:` and `remote_theme:` in Jekyll
- Making navigation sticky (required custom CSS injection)

None of this is sexy. But it's real. And now I have a working environment.

## What I Learned (Technical)

**SSH Keys**: Understanding practical asymmetric cryptography and not just "magic GitHub authentication". Private key stays on my machine, public key goes to GitHub. GitHub challenges me to prove I own the private key without ever seeing it. This is fairly foundational security knowledge, not just a setup step.

**Jekyll + GitHub Pages**: Static site generators are basic but also quite elegant. Pretty cool. Write Markdown, push to Git, site rebuilds automatically. No server, no database, no CMS complexity. Perfect for student technical blogging. The `remote_theme` trick to get newer minima features taught me how Ruby gem dependencies work in GitHub's build environment.

**Credential management**: Setting up Bitwarden wasn't just "password manager because I should." I learned about the hierarchy of credentials (root vs. IAM users, SSO vs. direct auth) and some basics of thinking like an attacker would about credential theft.

## What Surprised Me

**How much friction matters**: The 1-hour TryHackMe AttackBox limit could have derailed me on a bad executive function day. Paying for unlimited access removes a daily decision point. Reducing friction is a necessity when you're neurodivergent.

**The value of building in public**: I almost didn't make my repos public on Day 1. "They're empty, what's the point?" But public repos create accountability. Empty repos say "watch this space." Future me will probably be glad I started visibly.

**Troubleshooting teaches security thinking**: Debugging the Azure OAuth timeout wasn't just "IT help desk" work. I tested authentication flows, session state, cookie management. Every technical problem was a mini lesson.

## Next Week: First Real Work

Week 2 is when I stop setting up and start building:

- Finish remaining CS50 weeks (currently on Week 3)
- Master Linux command line basics
- Build my first security tool: a log parser in Python
- Start TryHackMe Pre Security and Introduction to Cyber Security paths
- Publish tool to security-tools repo
- Write Week 2 reflection

The goal is shipping a functional tool, documented, and public. Version 1.0, doesn't have to be perfect.

## Why I'm Documenting This

Most career transition stories you read are retrospective. "Here's how I became a security researcher" written after success is achieved. Selection bias makes it seem easier than it is.

I'm documenting from Day 1. This might succeed. It might take 18 months instead of 12. I hope I don't discover I'm terrible at this. But the process will be honest and public.

If you're considering a similar transition: watch me make mistakes in real-time. Watch me get stuck and work through it. Watch what actually takes time versus what I thought should be quick.

And if I succeed, you'll have seen every step from zero to independent researcher.

## Building in Public

This blog, my security-tools repo, and my research-notes are all public from Day 1. Because authenticity and accountability matter.

Week 1 is done. Infrastructure exists. Time to start building.

---

*This is post 1 of 50+ documenting my 12-month security research journey. Follow along: [X @kaybrickz](https://x.com/kaybrickz) • [GitHub](https://github.com/kbrickz)*
