---
title: "Blue Writeup"
date: 2025-12-31T11:00:00+08:00
draft: false
tags: ["TryHackMe", "Blue", "EternalBlue", "Metasploit"]
---

## Introduction
This is a walkthrough of the [Blue](https://tryhackme.com/room/blue) room on TryHackMe. The target machine is vulnerable to **MS17-010 (EternalBlue)**, a famous kernel exploit used by the WannaCry ransomware.

## Reconnaissance
I started with an Nmap scan to identify open ports:

```bash
nmap -sV --script vuln <TARGET_IP>