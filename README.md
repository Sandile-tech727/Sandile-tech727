
# Hi there, I'm Prince Sandile 👋

💻 IT Support Specialist | Certified in CompTIA A+ & Network+ | Aspiring DevOps Engineer  
🌍 Based in South Africa | Passionate about tech, football, and digital innovation

---

## 🔧 Tech Stack
- **Languages**: JavaScript, Python, Bash, SQL
- **Frontend**: React, HTML, CSS, Tailwind
- **Backend**: Node.js, Express
- **DevOps/Tools**: Git, Docker, GCP, VS Code, Linux
- **Certifications**: CompTIA A+, Network+ , BCS Computer Science

---

## 📂 Projects

### 🚀 [System Monitor Script](https://github.com/your-username/system-monitor)
A Python/Bash script that logs system metrics and alerts if usage crosses thresholds.

### 🛡️ [Secure Web Login Page](https://github.com/your-username/secure-login)
Built with HTML/CSS and JavaScript. Includes form validation and password encryption.

### 🧠 [ChatGPT-Powered Resume Builder](https://github.com/your-username/resume-builder)
Generate ATS-optimized resumes using an AI backend (Python Flask + OpenAI API).

---

## 📈 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=your-username&show_icons=true&theme=radical)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=your-username&layout=compact&theme=radical)

---

## 📫 Let's Connect

- 💼 [LinkedIn](https://linkedin.com/in/princesandilencube)
- 🌐 [Portfolio Website](https://yourwebsite.com)
- 📧 Email: princencube083@gmail.com
<!--
**1. System Resource Monitor (Python + Bash)

Description: A cross-platform system monitor script that logs CPU, memory, and disk usage. Sends alerts when thresholds are crossed.

Tech: Python, Bash, Cron (Linux), Task Scheduler (Windows)

Features:

Logs usage to a file

Email or terminal alert if CPU > 80% or RAM > 75%** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- import psutil
import datetime

cpu = psutil.cpu_percent()
memory = psutil.virtual_memory().percent
disk = psutil.disk_usage('/').percent
now = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")

log = f"{now} | CPU: {cpu}% | Memory: {memory}% | Disk: {disk}%\n"

with open("system_log.txt", "a") as f:
    f.write(log)

if cpu > 80 or memory > 75:
    print("⚠️ Resource usage high!")
    2. Simple Helpdesk Ticketing Web App (HTML + JS + Firebase)

Description: A lightweight helpdesk system where users can submit issues and support can update ticket statuses.

Tech: HTML, JavaScript, Firebase (Firestore for database)

Features:

Add/View/Delete tickets

Realtime database sync

Status updates (Pending, In Progress, Resolved)
Basic Website Uptime Monitor (Node.js + Express)

Description: Monitor any website's availability by pinging it every minute and logging downtime.

Tech: Node.js, Express, Axios, Node-cron

Features:

Add/remove websites to monitor

Logs uptime/downtime to a file

Simple JSON API
const axios = require("axios");
const fs = require("fs");
const cron = require("node-cron");

const sites = ["https://google.com", "https://yourdomain.com"];

cron.schedule("* * * * *", () => {
  sites.forEach(async (site) => {
    try {
      await axios.get(site);
      log(site, "UP");
    } catch {
      log(site, "DOWN");
    }
  });
});

function log(site, status) {
  const entry = `${new Date().toISOString()} | ${site} is ${status}\n`;
  fs.appendFileSync("uptime_log.txt", entry);
}
