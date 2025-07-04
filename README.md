# 🖼️ Stable Diffusion VPN Access – Remote AI Image Generation via Hamachi

This repository documents the configuration of a distributed AI image generation environment using Stable Diffusion (Automatic1111) hosted on a high-performance desktop system ("Project Horizons") and remotely accessed via Hamachi VPN from a lower-powered client laptop ("Rose Red"). The project highlights VPN tunneling, remote workflow orchestration, folder sharing protocols, and fallback access strategies.

---

## 🌐 Overview

Stable Diffusion is notoriously resource-intensive. This setup enables remote image generation tasks to be initiated from a low-end laptop by leveraging a more capable GPU-equipped desktop system over a private mesh VPN, securely routed via Hamachi.

---

## 🧰 Hardware & Software Configuration

### 🖥️ Host Machine – "Rose Red" (Gaming PC)

| Component | Details |
|-----------|--------|
| OS | Windows 11 Pro |
| GPU | NVIDIA RTX 3060 (12GB) |
| Frontend | Stable Diffusion Web UI – Automatic1111 |
| VPN Tool | Hamachi (Mesh Network Mode) |
| Remote Access | TeamViewer + Chrome Remote Desktop |
| File Access | Shared output folder via local account |

### 💻 Client Machine – "Project Horizons" (Laptop)

| Component | Details |
|-----------|--------|
| OS | Windows 11 Pro |
| CPU | AMD Ryzen 3 3200U |
| VPN Tool | Hamachi client (joined mesh network) |
| Access Method | Web browser (Stable Diffusion UI) |
| File Access | Network share via Hamachi + local credential login |

---

## ⚙️ Workflow & Connection Setup

1. Installed **Stable Diffusion Web UI (Automatic1111)** on desktop host.
2. Configured it to listen on local IP, accessible via Hamachi virtual address.
3. Created a **Hamachi mesh network** and joined both laptop and desktop.
4. Allowed Hamachi and Stable Diffusion traffic through **Windows Defender Firewall**.
5. Shared Stable Diffusion output folder with **a dedicated local account**.
6. From the laptop:
   - Accessed the host’s Stable Diffusion UI via browser at `Hamachi_IP:PORT`
   - Initiated image generation tasks remotely
   - Used **Hamachi “Browse” feature** to access shared folder after signing in with local credentials

---

## 🧠 Hybrid Compute Architecture

This project evolved from early LAN gaming setups using Hamachi (e.g., Apprentice/MTG) into a modern hybrid compute model for AI workloads. When the laptop’s hardware proved insufficient for local image generation, I engineered a distributed system that:

- Offloads Stable Diffusion processing to a remote gaming PC
- Uses Hamachi VPN to simulate a secure LAN environment
- Implements credentialed SMB file sharing for output retrieval
- Enables full job orchestration from a thin client interface

> This isn’t just a workaround—it’s a continuation of a 15+ year systems mindset. The same tool that once enabled multiplayer Magic: The Gathering now powers distributed AI workflows. It reflects a consistent ability to bridge technical constraints with creative, secure solutions.

---

## 🔄 Redundant Access Methods

To ensure remote management even if Hamachi service is interrupted:

- **TeamViewer**: Primary contingency remote desktop access
- **Chrome Remote Desktop**: Secondary remote access tool
- Both allow full graphical login and service management remotely

---

## 🎨 Use Cases & Output Themes

- Fantasy character portraits
- Avatar concepts for storytelling or RPGs
- Style exploration using models and prompts from Automatic1111

---

## ✅ Outcomes & Technical Skills Demonstrated

- **VPN Architecture**: Hands-on configuration of Hamachi mesh mode and firewall adjustments
- **AI Workflow Deployment**: Remote orchestration of image generation with web-based frontends
- **Resource Optimization**: Offloading heavy tasks to a high-performance node from a low-spec client
- **File Sharing Strategy**: Secure folder access through credentials and Hamachi's native tools
- **Redundancy Planning**: Multi-tool fallback for continuous system uptime and control
- **Interdisciplinary Application**: Blends network engineering, AI tooling, and digital asset creation

---

> Maintainer: Allen Bartley  
> Repository Created: July 2025  
> Status: Active Workflow
