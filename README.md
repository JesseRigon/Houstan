# Houstan we have lift-off

Houstan is the public repo for My Home Lab.

To keep things consistent I have decided on a couple guidelines/principles for this home lab:

1. Cheap
   - I plan on sticking to big names in the open source world that have large enterprise clients. This is not because I don't like new projects, but that I am also cheap with my time and don't want to waste it on technologies that are not well documented, that don't have adoption and could disappear tomorrow. Except in certain cases where the solution is in a novel space to where it has no incumbent competitors.
  
2. Useful but Not Simple
   - The goal in this Home lab is to familiarize and become competent in various current and future technologies. I will try to keep the main branch stable, but I may/will make breaking changes to the architecture over time.
   - There are times when I might make decisions to deliberately make the stack a little confusing by using two different technologies for the same purpose in separate areas of the stack in order to acquire both skills.
   - I will do my best to use only one software for one purpose and to find the best software for a particular job, but the previous statements hold priority.

# Three heads of the Hydra

These next sections explain the overall structure of the repo. Keep in mind these are separated by functionality not by which machine they will run on.

## Command Center

Command Center holds the programs and scripts that are used for Local Infrastructure provisioning.
The main point is to have an "always on" Home Lab interface for low power/high availability administrative tasks such as:

- Bare Metal Provisioning & Management
- Virtual Machine Provisioning & Management
- Secrets Management
- Identity & Authentication Management
- Infrastructure Access Management

In my case, I have installed Ubuntu Desktop on a Microsoft Surface Go that I use as my command center as it sits on my living room table, always on.

Backups of this OS Image are going to be vital to the Home Lab resiliency.

## Home Base

Home Base contains programs and scripts for my home use programs such as:

- Home Automation
- Media Servers
- Private Clouds
- etc

These may or may not run on the same machine, or might even run on 3rd party hardware. For Example, I run Home Automation software on my windows tablet that I use as my command center but the scripts required for that service will be located here.

## Laboratory

Laboratory is the portion of my home lab that is meant to mimic a commercial environmnt as possible. In terms of architecture, not proprietary software. 

A basic scaffold will look something like:

- Bare Metal Provisioning
- Nomad Cluster Management
- Openstack
- Kubernetes
- Business Applications

# Install

Currently this home lab assumes you have sudo access but does not assume you are loggin in as root.

Clone the Houstan repo to your users home directory on the computer you wish to use as the command center.

It will place all configs and output all logs outside the git folder into ~/HoustonConfigs as the default.






___

This whole project is in early development, but the underlying technologies will not be. Use this (if even working) at your very own risk. I will constantly be making changes (most likely breaking)
