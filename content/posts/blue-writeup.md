---
title: "TryHackMe: Blue Writeup"
date: 2025-12-31T11:45:00+08:00
draft: false
tags: ["TryHackMe", "Windows", "EternalBlue", "MS17-010"]
---

**Room:** [Blue](https://tryhackme.com/room/blue)  
**Difficulty:** Easy  
**Target:** Windows 7 Professional (x64)

In this room, we exploit a Windows machine vulnerable to the famous **EternalBlue** (MS17-010) exploit, which was used to spread the WannaCry ransomware. This is a classic example of why patching SMB is critical.

## Task 1: Reconnaissance

The first step is to identify the target machine's services and potential vulnerabilities. I started with a comprehensive Nmap scan to enumerate open ports and service versions.

### 1. Initial Nmap Scan
I used the following command to scan the target:

```bash
nmap -sV -sC -T4 <TARGET_IP>