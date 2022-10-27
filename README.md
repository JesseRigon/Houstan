# Houstan we have lift-off

Houstan is the public repo for My Home Lab. It is currently version 0.01 *USE AT OWN RISK*

# Three heads of the Hydra

These next sections explain the overall structure of the repo. 
*Keep in mind these are separated by functionality not by which machine they will run on.*

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

Laboratory is the portion of my home lab that is meant to mimic a commercial environment as much as possible.

A basic scaffold will look something like:

- Bare Metal Provisioning
- Nomad Cluster Management
- Openstack
- Kubernetes
- Business Applications

*This whole project is in early development, but the underlying technologies will not be. Use this (if even working) at your very own risk. I will constantly be making changes (most likely breaking)*
