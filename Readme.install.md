# Installing Houstan

## Gitpod

I personally use [Gitpod](https://gitpod.io/) as my Integrated Online Development Environment or IODE. Like Github Codespaces but older, mature, and more available. Exactly how I like 'em.

It is the quickest way to try out Houstan without touching your personal system, but there is no requirement to use Gitpod for Houstan to function. There are two files that are in the root directory that are excess if you don't use it that you may delete. 

- .gitpod.yml
- main.code-workspace

## Doppler

  *Houstan was developed using [Doppler.com](https://docs.doppler.com/docs/getting-started) for Secret and Configuration management.*

Doppler injects your environment variables into your environment when called. This eliminates the need to have any secrets locally stored and increases security on your system. 

If you would like to learn more about how this works, and how you can use it too, continue reading this section. Otherwise you may skip to the [install](#install) section and use the .env files included in the repo. You will want to run the following command in your terminal (bash, from houstan/) as it will remove all doppler.yaml files which are used for configuring projects with doppler.

```
find -name doppler.yaml -execdir rm {} \+
```

and also *delete* the file doppler.sh as you will not need it.

### If you are reading this far then you decided to use Doppler.  

This section will teach you how to use it to get your homelab up and running. Please read all the steps first before attempting to implement.

   1. [Create an account on doppler.com](https://dashboard.doppler.com/register)
   2. Create a doppler workspace for your homelab
   3. Create a personal token for your homelab workspace
      - Under Tokens/Personal on the main UI dashboard
      - copy the token and save it somewhere secure such as a github secret.
1. In the terminal of the machine you are going to use as your commandcenter run: 

```
export HISTIGNORE='export DOPPLER_TOKEN*'
export DOPPLER_PERSONAL_TOKEN="<your-token>"
```

   5. From Houstan/ run bash doppler.sh
      - Please see doppler.sh comments for what exactly is happening.

You are now setup with doppler. To use doppler when initializing anything that will require doppler secrets injection you will need to use the 'doppler run -- ' syntax. Please refer to this [docs](https://docs.doppler.com/docs/accessing-secrets) page.

<a name="install"></a>
## Install

*Currently this home lab will assume you have sudo access but not that you are logged in as root.*

Prerequisites for Houstan are:
   - linux
   - docker and docker-compose
   - git

On the computer you wish to use as the command center and in the dir you want Houstan installed:

```
git clone https://github.com/JesseRigon/Houstan.git
cd Houstan/
```

Again If you opted not to use Gitpod or Doppler as discussed above then you may proceed to remove the excess files at this time.

```
make
```

relative to the Houstan/ directory:

- Houstan mounts volumes for all containers into ../HoustanData/ by default.
- Houstan and will place all generated logs into ../HoustanLogs/ by default.
