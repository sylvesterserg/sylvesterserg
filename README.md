# Hi, I'm Sylvester Sergeant

**Linux & Infrastructure Builder · Homelab Builder · Founder, Sylvect IT Services · Creator, SlyBuilds**

Homelab builds that teach production infrastructure — one build, one test, and what broke included.

I build in Proxmox, Linux, and Ansible, document it with real commands and real screenshots, and publish the full build logs on SlyBuilds. Through Sylvect IT Services, I bring that same infrastructure work to small businesses across NJ and NYC.

**Links:** [SlyBuilds on Substack](https://slybuilds.substack.com) · [sylvect.biz](https://sylvect.biz) · [LinkedIn](https://www.linkedin.com/in/sylvester-sergeant/) · [Threads @sergeant_sly](https://www.threads.com/@sergeant_sly) · [Instagram @sylvect_it_solutions](https://www.instagram.com/sylvect_it_solutions)

---

## Start here

- **Building your own homelab?** Get the free guide: [Build Your First Production-Style Homelab](https://sylvesterserg.github.io/sly-command-center/guide/) — then follow the build logs on [SlyBuilds](https://slybuilds.substack.com/subscribe).
- **Hiring for Linux / infrastructure?** Skip to [For recruiters](#for-recruiters) — every skill below links to a repo that proves it.
- **Run a small business that needs IT handled?** Skip to [Work with Sylvect](#work-with-sylvect) — or [book a call](https://sylvect.biz/book/).

---

## At a glance

|  |  |
| --- | --- |
| **My brand** | Founder, **SYLVECT TECH LLC** (dba Sylvect IT Services) — managed IT, infrastructure, and cybersecurity for small businesses in NJ / NYC metro. Creator of **SlyBuilds**, my personal build-in-public brand. |
| **Focus** | Linux infrastructure, Ansible automation, Proxmox virtualization, identity, networking, and the infrastructure AI workflows run on. |
| **Homelab** | Proxmox VE 9.2.24 node, Ansible controller LXC, Rocky Linux VMs, Docker host, QNAP NAS, Tailscale remote access, n8n automation. Network upgrade to UniFi with VLAN segmentation is in progress. |
| **Content** | SlyBuilds — follow-along build logs with real screenshots, real commands, and the failures included. |
| **Cares about** | Documentation that proves the work, idempotent automation, honest scope — no claims I haven't tested. |

---

## Featured project: Ansible Linux Infrastructure Lab

**[ansible-linux-infrastructure-lab](https://github.com/sylvesterserg/ansible-linux-infrastructure-lab)** — a working, repeatable Linux web-server deployment on Proxmox, validated end to end.

- Ubuntu 26.04 LXC Ansible controller managing a Rocky Linux 9.5 VM over SSH key auth
- Playbook installs/enables Nginx, deploys a custom landing page, configures firewalld, authorizes HTTP, and asserts the page is served
- GitHub Actions CI on the repo: ansible-lint + syntax check, with a documented green → red → green failure-recovery test

Verified results from the live build:

| Test | Outcome |
| --- | --- |
| SSH + Ansible ping | `pong` from Rocky node |
| Initial Nginx deployment | `ok=6 changed=3 failed=0` |
| Firewall rollout | `ok=8 changed=1 failed=0` |
| HTTP test | `200 OK`, expected page served |
| Idempotency rerun | `ok=8 changed=0 failed=0` |

Read the build log: [I Automated a Linux Web Server with Ansible](https://slybuilds.substack.com/p/i-automated-a-linux-web-server-with)

Scope, honestly: one managed node, private lab network, HTTP only. No fleet, AWS, Kubernetes, or HA claims — that's the point of documenting it this way.

---

## My homelab stack

Where I test infrastructure, automation, and identity before it touches anyone else's environment.

- **Virtualization:** Proxmox VE 9.2.24 (node `sly`) — QEMU VMs and LXC containers
- **Automation:** Ubuntu 26.04 Ansible controller LXC, Ansible Core, GitHub Actions CI for playbook validation
- **Linux:** Rocky Linux 9.5 managed nodes, Ubuntu / Debian guests, Docker host VM for self-hosted services and n8n workflows
- **Storage:** QNAP TS-231P3 NAS
- **Remote access:** Tailscale — no public port forwards for lab access
- **Networking:** Currently Netgear RAX80 at the edge. *In progress:* UniFi Cloud Gateway Ultra with VLAN segmentation (Trusted / IoT / Guest) and U6 Lite access points — planned and staged, not claimed as finished until it's installed and verified
- **Dashboard:** [Homelab Command Center](https://github.com/sylvesterserg/homelab-command-center) — Python snapshot script pulling node health, guests, and storage from the Proxmox API into one dashboard, refreshed hourly

---

## Projects

### Infrastructure & automation

| Project | What it does |
| --- | --- |
| **[Ansible Linux Infrastructure Lab](https://github.com/sylvesterserg/ansible-linux-infrastructure-lab)** | Ansible + Proxmox + Rocky Linux deployment with SOPs, architecture docs, troubleshooting notes, and screenshot evidence. CI-validated. |
| **[Linux Automation Toolkit](https://github.com/sylvesterserg/linux-automation-toolkit)** | Ansible + OpenSCAP automation for audit-ready compliance reporting on Red Hat systems — CIS/STIG scans with HTML and XML report generation. |
| **[Homelab Command Center](https://github.com/sylvesterserg/homelab-command-center)** | One dark dashboard for an entire Proxmox homelab: node health, every guest, service launchers, storage. Python snapshot script + full build log. |

### Portfolio & brand

| Project | What it does |
| --- | --- |
| **[SLY Command Center](https://github.com/sylvesterserg/sly-command-center)** | My public portfolio hub: free homelab build guide, lab project walkthroughs, toolkit, and services funnel. |
| **[Sylvect Brand Kit](https://github.com/sylvesterserg/sylvect-brand-kit)** | The official brand system for Sylvect IT Services: 15 SVG logo masters, color palette, typography, templates, usage guidelines. |

### In progress

| Project | Status |
| --- | --- |
| **Keycloak IAM lab** | Identity / joiner-mover-leaver workflows in the homelab. In build — mover/leaver flows not yet tested, not claimed as complete. |
| **UniFi network upgrade** | Gateway, managed switching, and VLAN design staged for install. Documented when verified live. |

Study forks on my profile (Fleet, osquery, OpenSCAP, NetworkChuck guides) are research references for the work above — labeled as forks in their descriptions, not presented as my own projects.

---

## For recruiters

I build and document production-style Linux infrastructure. No buzzword list — each skill links to the work:

| Skill | Proof |
| --- | --- |
| Ansible automation & idempotency | [Ansible Linux Infrastructure Lab](https://github.com/sylvesterserg/ansible-linux-infrastructure-lab) — verified deployment, firewall, HTTP, and zero-change rerun evidence |
| CI for infrastructure code | Same repo — GitHub Actions with ansible-lint + syntax check, documented green → red → green recovery test |
| Linux administration (Rocky / RHEL, Ubuntu, Debian) | Ansible Lab + [Linux Automation Toolkit](https://github.com/sylvesterserg/linux-automation-toolkit) |
| Compliance automation (CIS / STIG) | [Linux Automation Toolkit](https://github.com/sylvesterserg/linux-automation-toolkit) — Ansible + OpenSCAP, HTML/XML audit reporting |
| Virtualization (Proxmox) | Ansible Lab (Proxmox VE host) + [Homelab Command Center](https://github.com/sylvesterserg/homelab-command-center) (Proxmox API tooling in Python) |
| Technical documentation | Deployment SOPs, architecture docs, and troubleshooting notes in every project repo; build logs on [SlyBuilds](https://slybuilds.substack.com) |

**Open to:** remote Linux / infrastructure / systems roles where documented, automated work matters. Based in the NJ / NYC metro.
**Reach me:** [LinkedIn](https://www.linkedin.com/in/sylvester-sergeant/) — or through [sylvect.biz](https://sylvect.biz).

This profile covers my own builds and my own company only — SlyBuilds and Sylvect. That's deliberate: what you see here is work I designed, built, and can walk you through line by line.

---

## Work with Sylvect

Sylvect IT Services is my company — managed IT, infrastructure, and cybersecurity for small businesses in NJ / NYC metro that have outgrown break-fix but don't need a full-time IT hire.

- Infrastructure and network projects, built and documented the same way as the labs above
- IT oversight and vendor accountability for teams of 10–75
- Microsoft 365 and endpoint management

**Next step:** [Book a call at sylvect.biz/book](https://sylvect.biz/book/) — or start with the free [homelab guide](https://sylvesterserg.github.io/sly-command-center/guide/) and the [SlyBuilds build logs](https://slybuilds.substack.com) to see how I work before you ever talk to me.

---

## Writing & building in public

- **SlyBuilds (Substack)** — [slybuilds.substack.com](https://slybuilds.substack.com) — homelab and infrastructure build logs: one build, one test, what broke
  - [I Automated a Linux Web Server with Ansible](https://slybuilds.substack.com/p/i-automated-a-linux-web-server-with)
  - [I Built a Command Center for My Entire Homelab](https://slybuilds.substack.com/p/i-built-a-command-center-for-my-entire)
- **Threads** — [@sergeant_sly](https://www.threads.com/@sergeant_sly)
- **Business** — [sylvect.biz](https://sylvect.biz) · Sylvect IT Services for NJ/NYC small businesses

---

I document everything I build. Code, write-ups, and mistakes included.
