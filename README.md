# Houstan We Have Lift-Off

Houstan is the public repo for My Home Lab. Currently the development is geared toward me specifically, but the goal is to create a "Home Lab Generator" that could work with any number of machines or apps. 

**It is currently version 0.01 *USE AT OWN RISK***

## Three Parts of Houstan

There are three conceptual parts to Houstan. 

  - Command Center - Always on Machine(s) that deal with infrastructure management and home lab administration
  - Infrastructure - Machine(s) (local or cloud) that will run all user applications
  - Applications - Application management system. Bootstrapping, Maintaining and Cleaning
  
Notice it says conceptual parts as this could all run on a single machine if it's powerful enough.

The basic scaffolding is as follows:

  - Single Command Center machine for mission critical, always on utilities and programs
  - Machine for network router (not the main internet router)
  - A set of machines that create a master Nomad cluster.
    - OpenStack
       - Kubernetes Clusters
         - cluster for home use applications
         - cluster for testing 
         - cluster(s) for business applications

In my case, I have installed Ubuntu Desktop on a Microsoft Surface Go that I use as my command center as it sits on my living room table, always on. I use this as I also have Home Assistant running on this machine and I like the touch screen display for this use case. If you don't need that, even a RaspPi would work.

### Backups of the Command Center OS Image are Vital.

*This whole project is in early development, but the underlying technologies will not be. Use this (if even working) at your very own risk. I will constantly be making changes (most likely breaking)*
