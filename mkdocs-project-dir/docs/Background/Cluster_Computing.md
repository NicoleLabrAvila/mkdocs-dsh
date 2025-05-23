---
title: Cluster Computing
categories:
 - User Guide
 - Background
layout: docs
---

# Cluster Computing

## What is a cluster?

In this context, a cluster is a collection of computers (often referred to as "nodes"). 
They're networked together with some shared storage and a scheduling system that lets people 
run programs on them without having to enter commands "live".

The UCL Moodle course "ARC - Introduction to High Performance Computing at UCL" has a video explanation of this here: [(Moodle)](https://moodle.ucl.ac.uk/mod/page/view.php?id=4623810) (UCL users)

This video is also available here: [(mediacentral)](https://mediacentral.ucl.ac.uk/Play/96444) (non-UCL users)

## Why would I want to use one?

Some researchers have programs that require a lot of compute power, like simulating weather patterns or the quantum behaviour of molecules.

Others have a lot of data to process, or need to simulate a lot of things at once, like simulating the spread of disease or assembling parts of DNA into a genome.

Often these kinds of work are either impossible or would take far too long to do on a desktop or laptop computer, as well as making the computer unavailable to do everyday tasks like writing documents or reading papers.

By running the programs on the computers in a cluster, researchers can use many powerful computers at once, without locking up their own one.

## What is DAata Save Haven (DSH)? 


## How do I use a cluster in DSH?

Most people use something like the following workflow:

 - connect to the cluster's "login nodes"
 - create a script of commands to run programs
 - submit the script to the scheduler
 - wait for the scheduler to find available "compute nodes" and run the script
 - look at the results in the files the script created

Most people connect using a program called a Secure Shell Client ("ssh client" for short).

The ssh client gives you a command prompt when you can enter text commands, but you can also tell it to 
pass graphical windows through the network connection, using a system called X-Forwarding.
This can be useful for visualising your data without transferring all the files back, but the network
 connection makes it a bit slower to use than running it on your own computer.
You'll need an X server on your own computer to use this: check [our page on X-Forwarding](../Supplementary/X-Forwarding.md) for details.

Please be aware that login nodes are shared resources, so users should not be running memory intensive jobs nor jobs with long runtimes in the login node. Doing so may negatively impact the performance of the login node for other users. Hence, identified culprit user processes are systematically killed.
