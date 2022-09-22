# Houstan we have lift-off

Houstan is the public repo for My Home Lab.

To keep things consistent I have decided on a couple guidelines/principles for this home lab:

1. Focused
   - I will do my best to use only one software for one purpose and to find the best software for a particular job.
   - This separation of concerns is fungible though, and I have my own biases. For example, I might use an NGINX instance as a gateway, reverse proxy and load balancer. Then a different instance as a web server for the same stack. This is because I view traffic routing and content serving as different layers in the architecture.
  
2. Cheap
   - I plan on sticking to big names in the open source world that have large enterprise clients. This is not because I don't like new projects, but that I don't am also cheap with my time and don't want to waste it on technologies that are not well documented and that don't have adoption and could disappear tomorrow. Except in certain cases where the solution is in a novel space to where it has no incumbent competitors.
  
3. Useful but Not Simple
   - The goal in this Home lab is to familiarize and become competent in various current and future technologies. I will try to keep the main branch stable, but I may/will make breaking changes to the architecture over time.
   - There are times when I might make decisions to deliberately make the stack a little confusing or use two different technologies for the same purpose in separate areas of the stack in order to acquire both skills.

# There are three sections to my Home Lab.

## Command Center

Command Center holds the programs and scripts that are used for Local Infrastructure provisioning from a single machine (X86-x64 Architectures).
The point is to have an "always on" machine such as:

- Bare Metal Provisioning & Management
- Virtual Machine Provisioning & Management
- Secrets Management
- Identity & Authentication Management
- Infrastructure Access Management

## Home Base

Home Base contains programs and scripts for my home base programs such as:

- Home Automation
- Media Server
- Private Cloud

## Laboratory

Laboratory is the portion of my home lab that is meant to mimic a commercial environmnt as possible. In terms of architecture, not proprietary software. 

A basic scaffold will look something like:

- Bare Metal Provisioning
- Nomad Cluster Management
- Openstack
- Kubernetes
- Business Applications

___

This whole project is in early development, but the underlying technologies will not be. Use this (if even working) at your very own risk. I will constantly be making changes (most likely breaking)
