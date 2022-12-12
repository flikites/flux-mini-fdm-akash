# flux-mini-fdm-akash

Credit: https://github.com/RunOnFlux/flux-mini-fdm

SDL to deploy a Flux Mini Domain Management Instance For Any Flux App (Load Balancer) onto the Akash Network

Flux makes it easy to spawn a large number of instances for your docker applications. 

This docker image and SDL combo allows you to self host a load balancer on Akash and automatically update it with all of the instances of your deployed Flux app.

# Instructions

```/etc/letsencrypt``` is persisted to store generated certs

Enviornment Variables must be added to the SDL only after the Akash deployment has succeeded and you have obtained the leased IP for the instance. 

#IMPORTANT - MUST DO# You must set the DNS 'A' record for you domain and point it to the leased IP before proceeding to update the deployment with the enviornment variables.

       APP_NAME=my-flux-app-name 
       APP_PORT=my-flux-app-port 
       DOMAIN=my.domain 
       EMAIL=my.email@my.domain 
       STAGING=false

# Set up your own Flux App

You can register a flux app here: https://home.runonflux.io/apps/registerapp

You will need to whitelist your public docker image here: https://github.com/RunOnFlux/flux/blob/master/helpers/repositories.json

You can use the Zelcore wallet to pay for your deployments: https://zelcore.io/
