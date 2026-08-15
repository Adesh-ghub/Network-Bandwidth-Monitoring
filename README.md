# Network Bandwidth Monitoring Using iftop and vnStat

## Project Overview

This project demonstrates Linux-based network bandwidth and traffic monitoring using **iftop** and **vnStat** on AlmaLinux.

The project monitors the active network interface `enp0s3` and provides both real-time traffic information and bandwidth usage statistics.

## Objectives

- Identify the active network interface.
- Monitor real-time network traffic.
- Measure received (RX) and transmitted (TX) data.
- Collect daily and monthly bandwidth statistics.
- Understand network connections and traffic rates in a Linux environment.

## Tools and Technologies

- AlmaLinux
- iftop
- vnStat
- Linux Terminal
- Oracle VirtualBox

## Working

1. The active network interface is identified using `ip -br link`.
2. The required network monitoring tools are installed.
3. The vnStat service is enabled and started.
4. vnStat records bandwidth usage over time.
5. iftop displays active network connections and real-time traffic.
6. The collected information is analyzed using RX, TX, total data and traffic rates.

## Important Commands

```bash
ip -br link
sudo dnf install epel-release -y
sudo dnf install iftop vnstat -y
sudo systemctl enable --now vnstat
systemctl status vnstat
vnstat -i enp0s3
sudo iftop -i enp0s3
