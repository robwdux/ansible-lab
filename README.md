# ansible-lab
Ansible local development environment - lab and testing setup example(s) using common tooling.

-   [OVERVIEW](#overview)
-   [COMMON](#common)
-   [CLUSTER](#cluster)
-   [TODO](#todo)

## Overview

### Why - quickly and easily get working

The objective is to establish a local working lab environment enabling quick and safe iterations with short feedback loops (providing direct access to the target platform).

Much thanks to PCs and virtualization, we can achieve working code faster and more comfortably.

Contemplate the era not so long ago - [punch card programming](https://en.wikipedia.org/wiki/Computer_programming_in_the_punched_card_era) and mainframes.

> Overnight and even 24x6-hour turnaround times were not uncommon. During peak times, it was common to stand in line waiting to submit a deck. However, on a lightly used system, it was possible to make alterations and rerun a program in less than an hour. Dedicated programmers might stay up well past midnight to get a few quick turnarounds. Use of this expensive equipment was often charged to a user's account. A mainframe computer could cost millions of dollars and usage was measured in seconds per job.

-   long feedback loops
-   forces more design (assumptions) up front (more waterfall less agile/iterative)
-   generally working in a vacummn until able to submit for execution and get feedback
-   compute highly scrutinized due to high cost of mainframes

### How - automation and tooling

Automation under your project folder to setup and manage the lab environment.

Make(file) or Shell Scripting
-   commonly available task runner for setup and test automation
-   os identification
-   install tools and dependencies
-   simplify managing the lab and executing code in it

Vagrant (commonly used, works in all cases)
-   mature and common, has been around for some time
-   simulate locally working against a multi-node cluster


Docker (can be used in most cases)
-   minimal resource usage and fast
-   typical role testing and playbook testing in a local context rather than that of typical remote ssh access (excludes testing modification of the kernel, boot loader or graphical boot)

## Common

Test a playbook or role.

Vagrant (driving VirtualBox) or Docker

## Cluster

Create and orchestrate a (multi-node) cluster. Implement capabilities to support and maintain the cluster throughout its lifecycle with a focus on optimizing the MTTR (Mean Time To Recovery).

Multi-node Vagrantfile, parallel execution of tasks by Ansible

## TODO

-   Makefile
    -   OS detection
    -   Document requirements
        -    python2
        -    pip
        -    Vagrant
        -    VirtualBox
        -
    -   Setup - requirements etc
        -   fedora
        -   ubuntu
        -   mac?
    -   Ansible Configuration
-   Playbook and or role development and testing
    -   Vagrant single node example
        -   ansible vs ansible_local
    -   Vagrant multi-node example
        -   parallel Ansible execution example
    -   Docker example
-   Role development and testing for continuous integration
    -   Molecule
