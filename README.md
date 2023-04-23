# flux-mini-fdm-akash

Credit: https://github.com/RunOnFlux/flux-mini-fdm

SDL to deploy a Flux Mini Domain Management Instance For Any Flux App (Load Balancer) onto the Akash Network

Flux makes it easy to spawn a large number of instances for your docker applications. 

# Instructions for Handshake x Varo Version: 

Example Enviornment Variables: (Change APP_NAME and APP_PORT, and specify your Varo API key.)

For a full list of options and configurations please see the original repo: 

https://github.com/FliKites/flux-mini-fdm/tree/nginx

```
     - CERT=self
     - APP_NAME=ipify
     - APP_PORT=39443
     - DOMAIN=ipify.fluxos
     - DNS_SERVER_ADDRESS=https://varo.domains/api
     - DNS_SERVER_API_KEY=<your-api-key>
     - FRONTEND_HEALTH_INTERVAL=10
     - BACKEND_HEALTH_INTERVAL=60
```
This docker image and SDL combo allows you to self host a load balancer on Akash and automatically update it with all of the instances of your deployed Flux app.

# Instructions for `orginal-deploy.yaml`

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
