
# Boinc Composed

Minimal container composition for running [BOINC client](https://hub.docker.com/r/boinc/client/). 


### Requirements

```
docker
docker-compose
```


### Setup 

```bash
git clone git@github.com:hypercodex/boinc-composed.git
cd boinc-composed

# Create a docker-compose .env file with GUI RPC password
echo "BOINC_GUI_RPC_PASSWORD=[your-password]" > .env

# Start the container
docker-compose up -d
```

After the composition starts, you can attach a BOINC Manager to the client by launching the BOINC Manager, going to File > Select computer..., and entering the IP address of the host running the docker container in the "Host name" field (127.0.0.1 if running locally) as well as the password you set with BOINC_GUI_RPC_PASSWORD env variable. 
