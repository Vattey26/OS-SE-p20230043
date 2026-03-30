# OS Lab 2 Submission

- **Student Name:** HEN Chhorda Vattey
- **Student ID:** p20230043

---

## Overview

This lab covers essential Linux command-line skills practiced inside a simulated company directory structure called `techcorp/`. Tasks include navigating the filesystem using absolute and relative paths, organizing files with `mv`, `cp`, and `rm`, and auditing directory contents using advanced `ls` flags.

---

## Final Directory Structure

```
lab2/
├── README.md
├── images/
│   ├── Task_1.png
│   ├── Task_2.png
│   ├── Task_3.png
│   ├── Task_4.png
│   ├── Task_4_-_Challenge.png
│   ├── Task_5.png
│   ├── Task_5_-_Challenge.png
│   ├── Task_6.png
│   └── Task_6_-_Challenge.png
├── task1_basic_navigation.txt
├── task2_filesystem_exploration.txt
├── task3_directory_structure.txt
├── task4_navigation_paths.txt
├── task5_file_organization.txt
├── task6_advanced_listing.txt
└── techcorp/
    ├── hr/
    │   ├── policies/
    │   │   ├── leave_policy.txt
    │   │   └── remote_work.txt
    │   └── onboarding/
    │       ├── checklist.txt
    │       ├── handbook.txt
    │       ├── leave_policy.txt
    │       └── welcome_guide.txt
    ├── engineering/
    │   ├── frontend/
    │   │   ├── frontend_config.txt
    │   │   ├── index.html
    │   │   └── styles.css
    │   ├── backend/
    │   │   ├── server_config.txt
    │   │   ├── pipeline_backup.txt
    │   │   ├── app.js
    │   │   └── database.sql
    │   └── devops/
    │       ├── pipeline.txt
    │       ├── server_notice.txt
    │       ├── security_audit.txt
    │       ├── Dockerfile
    │       └── docker-compose.yml
    └── marketing/
        ├── campaigns/
        │   ├── q1_2026_launch.txt
        │   └── social_media.txt
        └── assets/
            ├── logo.png
            ├── banner.jpg
            ├── brochure.pdf
            └── logo_brief.txt
```

---

## Task Output Files

Each task redirected its terminal output into a `.txt` file as the primary proof of work.

| File | Task |
|------|------|
| `task1_basic_navigation.txt` | Task 1 — Basic Navigation Warm-Up |
| `task2_filesystem_exploration.txt` | Task 2 — Exploring the File System |
| `task3_directory_structure.txt` | Task 3 — Building the Company Directory Structure |
| `task4_navigation_paths.txt` | Task 4 — Navigating with Absolute and Relative Paths |
| `task5_file_organization.txt` | Task 5 — Organizing Files Across Directories |
| `task6_advanced_listing.txt` | Task 6 — Advanced Listing & Directory Audit |

---

## Tasks

### Task 1 — Basic Navigation Warm-Up
**Output:** `task1_basic_navigation.txt`

Got comfortable with the three fundamental navigation commands by exploring the home directory, root `/`, and returning to the lab working directory.

**Commands used:** `pwd`, `ls`, `ls -la`, `cd ~`, `cd /`

**Screenshot:**

![Task 1](images/Task_1.png)

---

### Task 2 — Exploring the File System
**Output:** `task2_filesystem_exploration.txt`

Navigated to key Linux system directories and documented their contents to understand the Linux directory hierarchy.

| Directory | Purpose |
|-----------|---------|
| `/` | Root of the entire filesystem |
| `/etc` | System configuration files |
| `/var` | Variable data — logs, caches |
| `/home` | User home directories |
| `/tmp` | Temporary files |

**Commands used:** `cd`, `pwd`, `ls -la`

**Screenshot:**

![Task 2](images/Task_2.png)

---

### Task 3 — Building the Company Directory Structure
**Output:** `task3_directory_structure.txt`

Created the entire `techcorp/` directory tree in a single command, then populated each department's folder with placeholder files.

```bash
mkdir -p techcorp/{hr/{policies,onboarding},engineering/{frontend,backend,devops},marketing/{campaigns,assets}}
```

**Commands used:** `mkdir -p`, `touch`, `echo >`, `tree`

**Screenshot:**

![Task 3](images/Task_3.png)

---

### Task 4 — Navigating with Absolute and Relative Paths
**Output:** `task4_navigation_paths.txt`

Demonstrated mastery of all navigation methods across the `techcorp/` tree.

| Method | Example |
|--------|---------|
| Absolute path | `cd ~/os-se-p20230043/.../techcorp/hr/policies` |
| Relative path | `cd onboarding` |
| Parent shortcut | `cd ..` or `cd ../..` |
| Sideways navigation | `cd ../../engineering/frontend` |
| Previous directory | `cd -` |

**Screenshot — Guided Steps:**

![Task 4](images/Task_4.png)

#### 🧩 Challenge (8a–8e)

Given only the goal, chose the right `cd` method for each step independently.

| Step | From | To | Method used |
|------|------|----|-------------|
| 8a | `lab2/` | `techcorp/engineering/backend` | Relative path |
| 8b | `backend/` | `techcorp/marketing/assets` | `../..` shortcuts only |
| 8c | `assets/` | `/usr/bin` | Absolute path |
| 8d | `/usr/bin` | `assets/` (previous dir) | `cd -` |
| 8e | `assets/` | `techcorp/hr/onboarding` | Relative `../../hr/onboarding` |

**Screenshot — Challenge Commands:**

![Task 4 Challenge](images/Task_4_Challenge.png)

---

### Task 5 — Organizing Files Across Directories
**Output:** `task5_file_organization.txt`

Fixed a series of misplaced files left by an intern by moving, copying, renaming, and deleting files across the `techcorp/` tree.

| Fix | Action | Command |
|-----|--------|---------|
| `server_notice.txt` in wrong dept | Move to `devops/` | `mv` |
| `logo_brief.txt` in backend | Move to `marketing/assets/` | `mv` |
| `temp_debug.log` in HR policies | Delete | `rm` |
| `handbook.txt` in devops | Move to `hr/onboarding/` | `mv` |
| `leave_policy.txt` | Copy to onboarding for new hires | `cp` |
| `q1_launch.txt` | Rename to include year | `mv` (rename) |

**Screenshot — Guided Steps:**

![Task 5](images/Task_5.png)

#### 🧩 Challenge (9a–9d)

Given only a description of the problem, figured out the correct commands independently.

| Step | Task | Key command |
|------|------|-------------|
| 9a | Create `security_audit.txt` in wrong place, move to `devops/` | `echo > file` then `mv` |
| 9b | Copy `pipeline.txt` to `backend/` as `pipeline_backup.txt` | `cp src dst/newname` |
| 9c | Create and delete three `.tmp` files in one command | `rm *.tmp` (wildcard) |
| 9d | Rename `app_config.txt` → `frontend_config.txt` in same dir | `mv oldname newname` |

**Screenshot — Challenge Commands:**

![Task 5 Challenge](images/Task_5_Challenge.png)

---

### Task 6 — Advanced Listing & Directory Audit
**Output:** `task6_advanced_listing.txt`

Performed a full audit of the `techcorp/` file server using advanced `ls` flag combinations.

| Flags | Effect |
|-------|--------|
| `-l` | Long format (permissions, owner, size, date) |
| `-h` | Human-readable sizes (KB, MB) |
| `-S` | Sort by size, largest first |
| `-t` | Sort by modification time, newest first |
| `-r` | Reverse the sort order |
| `-R` | Recursive — include all subdirectories |
| `-a` | Show hidden files (dotfiles) |

**Screenshot — Guided Steps:**

![Task 6](images/Task_6.png)

#### 🧩 Challenge (6a–6d)

Given only the investigative question, chose the right flag combination independently.

| Step | Question | Flags used |
|------|----------|------------|
| 6a | Most recently modified file in `hr/onboarding/`? | `ls -lt` |
| 6b | All files in `marketing/` with human-readable sizes? | `ls -lhR` |
| 6c | Files in `devops/` with smallest at top? | `ls -lrS` |
| 6d | Hidden files in home dir, largest first? | `ls -lhSa ~` |

**Screenshot — Challenge Commands:**

![Task 6 Challenge](images/Task_6_Challenge.png)

---

## Key Concepts Practiced

- Absolute vs. relative path navigation
- Using `cd -`, `..`, and `~` as navigation shortcuts
- File operations: `mv` (move/rename), `cp` (copy), `rm` (delete) with wildcards
- `ls` flag combinations for sorting, filtering, and recursive directory listings
- Redirecting and appending command output to log files with `>` and `>>`
- Building nested directory trees with `mkdir -p`
