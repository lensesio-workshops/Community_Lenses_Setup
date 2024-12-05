# Instructions For Setting Up Lenses Community Edition  
  
  
  
## Laptop or VM Requirements

You will need a laptop or a VM with at least 8 gigs of memory and the ability to run Docker. *Note:* Lenses Community Edition uses 4-5 gigs of RAM when up and running. For ease of use we recommend [Docker Desktop](https://www.docker.com/products/docker-desktop/). However, open source Docker and Docker Compose can be used as well. See the [Docker Docs](https://docs.docker.com/manuals/) for detailed open source installation instructions.

## Obtaining and Running the Docker Compose File

You can download the Docker compose file here: (https://lenses.io/preview). 

Once you've downloaded the file run this command to start up Lenses Community Edition:

`ACCEPT_EULA=true docker compose up`

You need to add the `ACCEPT_EULA` statment to enable the community license. The very first time you run this command it will take a few moments longer than usual because Docker has to download all the container images needed to run the various components. Once it's all up and running it should look like this in Docker Desktop
