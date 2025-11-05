---
layout: post
title: "Starting My Security Journey"
date: 2025-11-05
categories: learning
---

## Why I'm Here

I'm autistic. In-person communication is hard. So I'm building in public, hoping the internet town square connects me to people who care about the things I do. Vulnerability and authenticity work better than performance.

I'm coming from work that makes me feel existentially dead inside. I'm tired of solving problems that don't matter in organizations where depth is punished and superficiality rewarded, where every day feels like asking permission to turn on my brain. I have what feels like a useless MBA and have spent most of my time post-graduation in data roles automating reports and building tools/dashboards for business stakeholders who don't know how to download and manipulate a CSV file.

But I grew up on the internet. I was writing scripts and building websites as a 6th grader. I'm a digital native who spends more time online than talking or working in real life. I can play corporate politics when I force myself to, but I'd rather move my work life into the same place my personal life lives instead of commuting my mind and splitting my attention.

So here I am: taking time off work to learn cybersecurity because protecting the value individuals and organizations create is more interesting than anything I've done so far.

## What I'm Building Toward

Financial and intellectual sovereignty. I want to work on things I care about and make money doing it without stressing everyday about whether I can afford the meals I want to eat. My end-preference is not a corporate security job, although that may be the step between where I am now and where I want to be. I'm not training to get hired. I'm learning a skill with a ceiling high enough to support working for myself.

Over the next 12 months I'll learn to hunt for bugs, do research, build tools, and hopefully gain some reputation even if it's as a junior in the field. I'm treating this journey as a job. 10-12 hours a day focused on doing everything I can to learn and grow into the future me I want to be.

Job offers might come. If the right one appears - remote, autonomous, meaningful work - I'll consider it. But employment is a temporary option, not the final destination.

## The Boring Infrastructure Part

Being autistic makes it hard to work without first building foundational guardrails, so I spent the first week setting up:

**Technical Environment**
- Set up TryHackMe as a cybersecurity starting place because it has easy entry points and structured paths
- Set up SSH keys and public repositories on GitHub to document my learning journey
- Configured VS Code for Python security work
- Registered for AWS and Azure accounts so I can jump right into later cloud security work
- Set up Bitwarden to keep secrets private

**Public Presence**
- Built this blog using Jekyll and GitHub Pages
- Fought with dark mode configuration to make it so the blog doesn't hurt reader's eyes
- Set up X account and followed professional security researchers
- Wrote this post

**What actually took time:**
- Learning an open source credential manager
- Understanding Jekyll's theme system and why dark mode wasn't working
- Debugging OAuth issues with Azure portal (ended up being an Azure outage, not me)
- Learning the difference between `theme:` and `remote_theme:` in Jekyll
- Making navigation sticky (required custom CSS injection)

None of this is sexy. But it's real. And now I have a working environment.

## What I Actually Built

Week 1 wasn't just infrastructure. I built my first security tool.

**CS50 Problem Set 3:**
Finished three algorithm problems - identifying sorting algorithms by runtime analysis, implementing plurality voting, and building a runoff election system. The sorting problem made conceptual sense (I understand why merge sort is O(n log n)), but I wouldn't be able to implement these from scratch yet. Programming is hard. I'm good at understanding what needs to happen and why, but syntax memorization isn't my strength. My mind uses code as a tool, not a subject to master. I lean on Claude (the LLM) heavily for implementation help, but I type everything myself to internalize patterns. It's working.

Runoff was complex - ranked preferences, multiple elimination rounds, tie detection. I needed help structuring it. But I understand the concepts. Systems thinking and security stuff click immediately. Programming syntax is what requires help. That's fine. It'll improve with repetition.

**Security Log Parser:**
Built a Python tool that parses syslog files into structured data. Not groundbreaking, but functional and documented. It reads log files, uses regex to parse syslog format (timestamp, hostname, process, PID, message), handles errors gracefully, and outputs structured results. Added proper error handling for missing files and bad permissions. Created test files for edge cases. Wrote comprehensive documentation.

The tool works. It's on GitHub. First public security tool. Version 1.0.

## What I Learned (Technical)

**SSH Keys**: Not just "magic GitHub authentication" - it's practical asymmetric cryptography. Private key stays on my machine, public key goes to GitHub. GitHub challenges me to prove I own the private key without ever seeing it. Foundational security knowledge, not just a setup step.

**Jekyll + GitHub Pages**: Static site generators are elegant. Write Markdown, push to Git, site rebuilds automatically. No server, no database, no CMS complexity. The `remote_theme` workaround taught me how Ruby gem dependencies work in GitHub's build environment.

**Credential management**: Setting up Bitwarden forced me to understand credential hierarchies - root vs. IAM users, SSO vs. direct auth. Started thinking like an attacker would about credential theft.

**Regular expressions for parsing**: Built a regex pattern to parse syslog format. Understanding that `(\w+\s+\d+\s+\d+:\d+:\d+)` captures timestamps and `\[(\d+)\]` extracts PIDs isn't just syntax - it's pattern recognition, which is what security work is.

**File I/O and error handling**: Reading files, catching FileNotFoundError and PermissionError, providing helpful error messages instead of crashes. Professional tools handle edge cases. Amateur tools break and blame the user.

## What Surprised Me

**Friction matters more than I expected**: The 1-hour TryHackMe AttackBox limit would derail me on bad executive function days. Paying $10/month for unlimited access removes a daily decision point. When you're neurodivergent, reducing friction isn't laziness - it's architectural necessity.

**Building in public creates accountability**: I almost didn't make my repos public on Day 1. "They're empty, what's the point?" But empty repos say "watch this space." Public commits create pressure to keep going. Future me will be glad I started visibly.

**Programming is harder than systems thinking**: Security concepts click immediately. Systems thinking - how logs work, why parsing matters, how attacks leave traces - all clicks. Programming syntax is what requires help. I'm not intuitively understanding half the implementation problems. It would be nice to just get it. But concepts > syntax at this stage. Syntax will come with repetition.

**Troubleshooting teaches security thinking**: Debugging the Azure OAuth timeout wasn't just IT help desk work. I tested authentication flows, session state, cookie management. Every technical problem is a security lesson if you're paying attention.

## Week 2 Preview

Week 1 of Month 1 done - 3 more weeks of foundations ahead. Next week I'm building more:

- Finish CS50 Weeks 4-7 (continuing algorithm foundations)
- Master Linux command line (actual practice, not just reading)
- Enhance log parser (add Apache/nginx support)
- Complete TryHackMe Pre Security path
- Build second tool (port scanner)
- Ship both tools publicly
- Write Week 2 reflection

The goal isn't perfection. It's consistent shipping. Professional quality, publicly visible work. Building evidence that I can do hard things.

## Why Document This Publicly

Most career transition stories are retrospective. "Here's how I became an XYZ" written after success. Selection bias makes everything seem easier than it was.

I'm documenting from Day 1. This might succeed. It might take 18 months instead of 12. I might discover I'm not as capable as I hope. But the process will be honest and public.

If you're considering a similar transition: watch me make mistakes in real-time. Watch where I get stuck. Watch what actually takes time versus what I thought would be quick. Watch me lean on AI assistance while still doing the work myself.

And if I succeed, you'll have seen every step. Not the highlight reel. The whole thing.

## Building in Public

This blog, my security-tools repo, and my research-notes are all public from Day 1 because accountability matters more than fear.

Week 1 done. Infrastructure exists. First tool shipped.

Time to build more.

---

*This is post 1 of 50+ documenting my 12-month journey. Follow along: [X @kaybrickz](https://x.com/kaybrickz) • [GitHub](https://github.com/kbrickz)*