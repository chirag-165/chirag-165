<div align="center">

<pre>
  ╭──────────────────────────────────────────────╮
  │  $ whoami                                     │
  │  chirag_shetty — backend & devops engineer     │
  │  status: building reliable systems             │
  ╰──────────────────────────────────────────────╯
</pre>

</div>

<h1 align="center">Hey, I'm Chirag 👋</h1>

<p align="center">
  CS Engineering student who'd rather build the thing that <i>detects and fixes failures</i><br/>
  than the thing that just shows you a red dashboard after it's too late.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/chirag-shetty-a1827a261"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:shettychirag16@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://github.com/chirag-165"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"/></a>
</p>

<br/>

## System Status

A small honesty check before the badges: this is roughly how I'd describe my own stack right now, written the way I'd write a service-health row in a monitoring dashboard.

| Service | Status | Notes |
|---|---|---|
| `backend-development` | 🟢 `STABLE` | Node.js, Express, REST APIs — daily driver |
| `devops-pipeline` | 🟢 `STABLE` | Docker, CI/CD, Ansible, Linux |
| `distributed-systems` | 🟡 `LEARNING` | Building a self-healing microservices platform — see below |
| `cloud-infra` | 🟡 `LEARNING` | AWS EC2 + S3, OCI Foundations certified |
| `frontend` | ⚪ `MINIMAL` | I can ship a dashboard, I won't pretend to love it |

<br/>

## What I'm building

**Distributed Log Analysis, Predictive Failure Detection & Self-Healing System**
*Node.js · Python · Docker · Redis · MongoDB*

The short version: most monitoring tells you a service died *after* it died. This doesn't.

```
logs → Redis stream → 60s window aggregation → Z-score anomaly detection
                                                        ↓
                                          Random Forest failure prediction
                                                        ↓
                                    Policy Engine (decides — never executes)
                                                        ↓
                                         MongoDB (recovery_actions, intent only)
                                                        ↓
                                   Controller (reconciles, calls the right host)
                                                        ↓
                                  Agent (1 per host — restarts / scales locally)
```

The part I'm actually proud of: **the thing that decides a service is unhealthy is never the thing that touches Docker.** Decision and execution are separate services talking through MongoDB, the same way Kubernetes splits its control plane from kubelet. It means a hung Docker call can't block log analysis, and the controller can crash and pick up exactly where it left off.

Currently mid-build on running this across real EC2 instances instead of one machine — turns out "make it work across hosts" is 90% making sure your network names and container labels actually match what you think they are. (They did not, several times. Learned a lot from that.)

<br/>

## Other things I've shipped

<table>
<tr>
<td width="50%" valign="top">

**Job Application Tracker**
*Microservices · Express.js · AWS*

Decomposed a monolith into independently deployable services for zero-downtime deploys. Deployed on EC2 behind Nginx, S3 for document storage with pre-signed URLs, health-check endpoints for horizontal scaling under load.

</td>
<td width="50%" valign="top">

**Backend Scaffolding CLI**
*Node.js · Shell*

Generates a fully wired backend skeleton in under 30 seconds. Plugin architecture — Docker, JWT auth, DB adapters, CI/CD config — all composable at init. Cut new-project setup time by ~80% for the stacks I use most.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Cloud Resource Monitor**
*Bash · AWS CLI*

Replaced manual console-checking with scheduled, alert-capable scripts watching EC2/S3 utilization. Surfaces idle resources so right-sizing decisions happen before the bill does.

</td>
<td width="50%" valign="top">

**Autonomous Rescue Drone** *(contributor)*
*Sensor pipelines · disaster response*

Built real-time obstacle-avoidance data pipelines for a drone project aimed at disaster-response operations.

</td>
</tr>
</table>

<br/>

## Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=js,nodejs,express,mongodb,mysql,redis,docker,aws,nginx,linux,bash,git,c,cpp,py&theme=dark" />

</div>

<br/>

<table align="center">
<tr>
<td valign="top" width="33%">

**Languages**
C · C++ · JavaScript · Python · Bash

</td>
<td valign="top" width="33%">

**Backend & Data**
Node.js · Express.js · REST APIs
Redis · MongoDB · MySQL

</td>
<td valign="top" width="33%">

**DevOps & Cloud**
Docker · AWS (EC2, S3) · Nginx
Ansible · Linux · CI/CD

</td>
</tr>
</table>

<br/>

## GitHub Activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=chirag-165&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=chirag-165&layout=compact&theme=tokyonight&hide_border=true" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=chirag-165&theme=tokyonight&hide_border=true" />

</div>

<br/>

## Currently

🎓 3rd year CSE @ MITE Moodabidri — CGPA 8.81
🛠️ Building the self-healing system above, properly, not just to demo it once
☁️ OCI Foundations Associate · Walmart Global Tech Advanced SWE Job Simulation
🧑‍💻 Ran *Trail of Bytes* — a college-wide tech event, 100+ participants, my logistics-and-judging era

<br/>

<div align="center">
<sub>If a restart fixes it, it wasn't really fixed — but it bought time to find out why. That's basically my engineering philosophy.</sub>
</div>
