# Installing Houstan

## Gitpod

I personally use [Gitpod](https://gitpod.io/) which is a Cloud Development Environment (CDE).

It is the quickest way to try out Houstan without touching your personal system, but there is no requirement to use Gitpod for Houstan to function.

If you go to [HoustanGP Repo](https://www.github.com/JesseRigon/HoustanGP) you can see the repo that houses all the files necessary to run Houstan on Gitpod are located. Further Instruction will be on the readme in the mentioned. You will need to create an account but there is a free tier for testing their service and for testng out Houstan preliminarily. 

## Doppler

  *Houstan was developed using [Doppler.com](https://docs.doppler.com/docs/getting-started) for Secret and Configuration management.*

Doppler injects your environment variables into your environment when called. This eliminates the need to have any secrets locally stored and increases security on your system. 

If you would like to learn more about how this works, and how you can use it too, continue reading this section. Otherwise you may skip to the [install](#install) section and use the .env files included in the repo. You will want to run the following command in your terminal (bash, from houstan/) as it will remove all doppler.yaml files which are used for configuring projects with doppler.

```
find -name doppler.yaml -execdir rm {} \+
```

and also *delete* the file doppler.sh as you will not need it.

### If you are reading this far then you decided to use Doppler.  

This section will teach you how to set it up and use it to get your homelab up and running. Please read all the steps first before attempting to implement.

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

   5. From Houstan dir run  `bash doppler.sh`
      - Please see doppler.sh comments for what exactly is happening.

You are now setup with doppler. To use doppler when initializing anything that will require doppler secrets injection you will need to use the 'doppler run -- ' syntax. Please refer to this [docs](https://docs.doppler.com/docs/accessing-secrets) page.
