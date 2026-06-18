# soc-analyst-journey
A structured documentation repository tracking my professional development toward a career in Security Operations. This repo catalogs my progress through security concepts, hands-on lab exercises, network defense strategies, and cryptographic implementations. Follow my journey as I build the skills necessary to excel as a SOC Analyst.
---

## 📈 30-Day Progress Dashboard

| Phase | Focus Area | Status |
| :--- | :--- | :--- |
| **Phase 1** | Core Networking & OS Telemetry | 🔄 In Progress |
| **Phase 2** | SIEM Processing & SPL Query Mastery | ⏳ Pending |
| **Phase 3** | Attack Lifecycles & Threat Intelligence | ⏳ Pending |
| **Phase 4** | Live SOC Incident Triage Simulations | ⏳ Pending |
| **Phase 5** | Consolidation & Certification Challenge | ⏳ Pending |

---

## 📓 Daily Activity & Lab Logs

### Day 01 — 2026-06-12
**Topic:** Repository initialization & environment setup

**Tasks completed:**
- Created public GitHub repository with professional folder structure
- Created accounts on TryHackMe, LetsDefend, picoCTF, BTLO, CyberDefenders
- Enrolled in Cisco NetAcad Intro to Networking (free badge)
- Registered for Splunk free training
- Set up VirtualBox with Ubuntu VM and Kali Linux VM
- Subscribed to NetworkChuck, Professor Messer, John Hammond on YouTube

**Key takeaway:** A well-structured repo from Day 1 is much easier than reorganizing later. Documentation discipline is itself a SOC skill.

---

### Day 02 — 2026-06-13
**Topic:** Networking fundamentals — switches, MACs, LAN communication

**What I learned:**
- What a network is — devices communicating to share resources
- How a **switch** works — connects devices within the same LAN using **MAC addresses**
- Switch operates at **Layer 2 (Data Link)** of the OSI model
- Difference between a switch (Layer 2, same network) and a hub
- learned about the cisco commands like **Switch# show mac-address-table**
- How a frame travels from source to destination inside a local network

**Resource:** [NetworkChuck FREE CCNA Course](https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)

### Day 03 — 2026-06-14
**Topic:** Routers, TCP/IP stack & OSI model

**What I learned:**
- How a **router** works — connects different networks, operates at **Layer 3 (Network)** using **IP addresses**
- Router vs Switch — switch moves frames within a LAN (MAC), router moves packets between networks (IP)
- using router CLI commands to see the routing
- The **OSI model** — 7 layers and what each does:
  | Layer | Name |
  |-------|------|
  | 7 | Application |
  | 6 | Presentation |
  | 5 | Session |
  | 4 | Transport |
  | 3 | Network |
  | 2 | Data Link |
  | 1 | Physical |
- **TCP/IP model** — the real-world 4-layer version of OSI:
  | TCP/IP Layer |
  |-------------|
  | Application |
  | Transport |
  | Internet |
  | Network Access |

**Resource:** [NetworkChuck FREE CCNA Course](https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)

### Day 04 — 2026-06-15
**Topic:** Python fundamentals & Linux basics

**What I learned:**

**Python:**
- Core functions — `print()`, `input()`, `type()`, type casting
- Built a coffee shop program — greets customer, takes order, calculates total cost
- Understanding how Python reads and processes user input

**Linux:**
- History and philosophy of Linux — why everything is a file
- The CLI (Command Line Interface) — why it matters for security work
- Essential commands learned:
  | Command | What it does |
  |---------|-------------|
  | `pwd` | print current directory |
  | `ls` | list files and folders |
  | `cd` | change directory |
  | `cat` | read file contents |
  | `cp` | copy files |
  | `rm` | remove files |
  | `whoami` | show current user |
  | `which` | find location of a program |
  | `adduser` | create a new user |
- Linux directory structure — `/`, `/home`, `/etc`, `/var`, `/root`, `/bin`, `/sbin`
- The **root user** — superuser with full system access, why it matters in security

**Tools used:** VS Code (Python), HackTheBox — Linux Fundamentals module

**Key takeaway:** In Linux, everything is a file — even hardware devices and running processes. This is why Linux log analysis is so powerful for SOC work: attacker activity always leaves traces in the filesystem.

**Resource:** [NetworkChuck – Python RIGHT NOW!!] · [NetworkChuck – Linux for Hackers]

### Day 05 — 2026-06-16
**Topic:** Linux system & network commands + Python conditionals

**What I learned:**

**Linux — System & Network Reconnaissance Commands:**
| Command | What it does |
|---------|-------------|
| `whoami` | shows current logged-in user |
| `id` | shows user ID, group ID, and group memberships |
| `hostname` | displays the system's hostname |
| `uname` | shows system/kernel information |
| `ifconfig` / `ip` | displays network interface configuration |
| `netstat` / `ss` | shows active network connections and listening ports |
| `ps` | lists running processes |
| `who` | shows who is currently logged into the system |
| `env` | displays environment variables |
| `lsblk` | lists block devices (drives, partitions) |
| `lsusb` | lists connected USB devices |
| `lsof` | lists open files and which processes opened them |
| `lspci` | lists PCI hardware devices |

**Linux — User & Group Management:**
- Used `man` and `--help` to read command documentation directly in the terminal
- Created a new user and assigned specific permissions
- Modified user permissions after creation
- Deleted a user account
- Created a new group and understood group-based access control

**Python — Conditionals:**
- Learned `if / elif / else` logic
- Extended the Barista program: added a menu with different prices per item
- Used **logical operators** (`and`, `not`) to block specific customers from ordering
- Combined input validation with conditional logic for access control

**Key takeaway:** Commands like `netstat`, `ss`, `ps`, and `lsof` are exactly what a SOC analyst runs first when investigating a compromised Linux host — they answer "what's running, what's connected, and what's open" in seconds. User/group management is also core to understanding privilege escalation attacks later.

**Resource:** NetworkChuck – Linux for Hackers (continued) · NetworkChuck – Python Course (continued)

### Day 06 — 2026-06-17
**Topic:** Linux package management + Git/Python package installation

**What I learned:**

**Linux Package Managers:**
| Tool | What it does |
|------|-------------|
| `apt` | high-level package manager for Debian/Ubuntu — install, update, remove software |
| `dpkg` | low-level package manager — handles `.deb` files directly, what `apt` runs underneath |
| `aptitude` | alternative front-end to `apt` — more detailed dependency resolution view |
| `snap` | universal package manager — sandboxed apps, works across Linux distros |

- Understood the difference between **high-level** (`apt`, `aptitude`) and **low-level** (`dpkg`) package managers
- Learned how `apt` resolves dependencies automatically, while `dpkg` requires manual dependency handling
- Practiced installing, updating, and removing packages using `apt install`, `apt update`, `apt remove`
- Explored `snap` as a containerized alternative — useful when a package isn't in the standard repos

**Git & Python Package Management:**
- Used **Git** to clone repositories and pull external tools/code
- Used **pip** (Python's package manager) to install Python libraries
- Understood the parallel: `apt` manages system software, `pip` manages Python libraries, `git` manages source code/version control

**Key takeaway:** Package management is a core Linux security skill — understanding what's installed on a system (and via which manager) is essential during incident response. Attackers sometimes install malicious packages disguised as legitimate ones, so knowing how `dpkg -l` or `apt list --installed` works helps spot anomalies on a compromised host.

**Resource:** NetworkChuck — Linux for Hackers (continued)

### Day 07 — 2026-06-18
**Topic:** Linux file search tools — which, find, locate (HackTheBox module)

**What I learned:**

| Tool | Purpose |
|------|---------|
| `which` | finds the path to an executable — checks if a tool like Python, cURL, netcat, wget exists on the system |
| `find` | powerful filtering search — by type, name, owner, size, modification date; supports running commands on results |
| `locate` | fast search using a pre-built database (`updatedb`) — much quicker than `find` but fewer filter options |

- `which python` → confirms a program exists and shows its exact path
- `find` syntax: `find <location> <options>` — can combine filters like `-type f`, `-name *.conf`, `-user root`, `-size +20k`, `-newermt <date>`
- `-exec` lets `find` run a command (like `ls -al`) on every result it finds
- `2>/dev/null` redirects errors to the null device so they don't clutter output
- `locate` requires running `sudo updatedb` first to refresh its file index, then searches that database instead of the live filesystem

**Key takeaway:** `find` with filters like `-user root -newermt <date>` is exactly how you'd hunt for recently modified config files during an incident — a classic technique for spotting unauthorized changes or backdoors planted on a compromised host. `which` is the fastest way to confirm what tools an attacker (or defender) has available on a system.

**Resource:** HackTheBox Academy — Linux Fundamentals module

---