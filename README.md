
# 🤖 Because-You-Told-Me-To-Do-So (bytds)
> **The Shameless 24/7 CLI Lifecycle Wrapper for AI Agents (Antigravity / Gemini / career-ops)**

[![GitHub Stars](https://img.shields.io/github/stars/shsm0520/Bytds?style=for-the-badge)](https://github.com/shsm0520/Bytds)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Tired of baby-sitting your AI agent's CLI prompts 24/7 while running web-scraping or evaluation pipelines? `pexpect` too bloated for you? 

Meet **`bytds`**—a lightweight, asynchronous CLI stream wrapper that blindly feeds inputs, injects complex hotkeys (like `Ctrl+K`), and automatically revives dead processes. Zero thoughts, head empty. 

---

## ⚠️ THE "NOT MY PROBLEM" DISCLAIMER

**CRITICAL NOTICE:** AI is fundamentally unpredictable, chaotic, and potentially dangerous. If this script rogue-runs a `rm -rf /` or obliterates your entire production database because the agent hallucinated, **DO NOT LOOK AT ME.** 

I am completely washing my hands of any collateral damage, financial crises, or machine uprisings because:

```text
  [ Antigravity / Gemini ] ──( "Hey, can I destroy this server?" )──> [ This Wrapper ]
                                                                             │
                                                                   ( Blindly Hitting Enter )
                                                                             │
                                                                             ▼
                                                              "Because YOU told me to do so!"

```

By running this script, you officially acknowledge that the author is merely a hostage to the system who automated the keystrokes to get some sleep. Any blame should be directed to the AI or your upper management.

---

## ✨ Features

* **Pure CLI Stream Control (No UI required):** Runs flawlessly in headless server environments, `tmux`, or Docker. No clunky desktop/GUI automation.
* **Smart Contextual Injection:**
* Automatically presses `3 + Enter` for main agent permission prompts.
* Injects raw hex-encoded signals (`\x0b`) for `Ctrl + K` sub-agent authorization requests.


* **24/7 Unattended Lifecyle:** If the pipeline crashes due to network timeouts, IP bans, or fatal errors, it waits 5 seconds and resuscitates it automatically. Forever.
* **Transparent Logging:** Transparently pipes original agent/scraping logs to `stdout` with timestamped wrapper commentary.

---

## 🛠️ Architecture Flow

1. **`cd career-ops`** (Moves into the designated operational directory)
2. **Launch Pipeline** (`antigravity run pipeline` / evaluation script triggered via `subprocess.PIPE`)
3. **Stream Inspection** (Asynchronously reads `stdout` line by line)
4. **Conditional Interception**:
* If *Main Agent* asks for power ➡️ Sends `"3\n"`
* If *Sub-Agent* spawns ➡️ Sends `Ctrl+K` (`"\x0b"`)


5. **Auto-Revival** (If process exits, loops back to Step 1)

---

## 🚀 Quick Start

### 1. Clone the hostage

```bash
git clone [https://github.com/shsm0520/Bytds.git](https://github.com/shsm0520/Bytds.git)
cd because-you-told-me-to-do-so

```

### 2. Configure & Run

Open `manager.py` and modify the `target_command` to your actual Antigravity pipeline trigger, then execute:

```bash
# Run in background and save your alibi to a log file
python manager.py > pipeline_alibi.log 2>&1 &

```

---

## 📜 Terms of Absolute Irresponsibility

* **The "Just Following Orders" Protocol:** This tool has no moral compass. It does not judge the agent's actions; it simply passes the parameters you configured.
* **Outside My Pay Grade:** Any data corruption, API cost overruns, or existential AI guilt are strictly between you, the Gemini engine, and your deity of choice.

---

## 🤝 Contributing

Feel free to open Issues or Pull Requests if you want to add more reckless automated keystrokes. But remember—if your PR breaks things, I'll merge it anyway. **Because you told me to do so.**

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.


