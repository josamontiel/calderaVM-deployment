# Caldera deployment to Azure VMs

This guide will be built as I figure out what I am doing, this is my first time trying to do this. It will be divided into as few parts as possible(so far).

## Table of Contents
1. Deploying the VM
2. Connecting VM to Sentinel (SIEM)
3. Installing Caldera
4. Using as a training tool for new SOC analysts


### Deploying the VM
VM deployment via Azure. It will likely start with One manual deployment, and work its way up to automated ad hoc deployments. According to [Calderas documentation](https://caldera.readthedocs.io/en/latest/Installing-Caldera.html) a VM with the following requirements are required:

 - Linux or MacOS operating system
 - Python 3.8 or later (with pip3)
 - NodeJS v16 or later (for Caldera v5)
 - A modern browser (Google Chrome is recommended)
 - GoLang 1.17+ (for optimal agent functionality)
 - Hardware: 8GB+ RAM and 2+ CPUs

> There are some packages required for compiling agents with caldera, linsted [here](https://github.com/mitre/caldera/blob/master/requirements-dev.txt)

The first manual deployment, will probably be done straight from the portal with RDP and SSH access to the machine. As the project grows, we may need these VMs to have their own NSGs and VNets.

### Connecting VM to Sentinel (SIEM)
This will be to ingest logs for analysis and triage. This assumes we have a [Log Analystics Workspace](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-workspace-overview) and Sentinel environment deployed already.

### Installing Caldera
[Caldera](https://github.com/mitre/caldera) is an Automated Adversary Emulation Platform, this will be used to simulate real attacks.

### Using as a training tool for new SOC analysts
The end game is to be able to use this to train your SOC analysts using a "compromised machine" from detection through remediation.
