# Instructions For Setting Up Lenses Community Edition  
  
  
  
## Laptop or VM Requirements

You will need a laptop or a VM with at least 8 gigs of memory and the ability to run Docker. *Note:* Lenses Community Edition uses 4-5 gigs of RAM when up and running. For ease of use we recommend [Docker Desktop](https://www.docker.com/products/docker-desktop/). However, open source Docker and Docker Compose can be used as well. See the [Docker Docs](https://docs.docker.com/manuals/) for detailed open source installation instructions.

## Obtaining and Running the Docker Compose File

You can download the Docker compose file here: https://lenses.io/preview 

Once you've downloaded the file run this command to start up Lenses Community Edition:

`ACCEPT_EULA=true docker compose up`

You need to add the `ACCEPT_EULA` statment to enable the community license. The very first time you run this command it will take a few moments longer than usual because Docker has to download all the container images needed to run the various components. Once it's all up and running it should look like this in Docker Desktop:

![screenshot of Docker Desktop with Lenses Community Edition running](/images/docker_desktop.png)

Or from the command line: 

![screenshot of Docker PS command output](/images/docker_ps.png)

When you are finished you can bring it all down with the following command:

`docker compose down` Don't worry about the warning about the EULA it's harmless. 

## What's In the Community Dcoker Compose Package?

A fully functional single node Apache Kafka cluster, Schema Registry, and  Kafka Connect instance. All of these are running in a single container.

An instance of Lenses HQ - the control plane of Lenses 6. 

An instance of Lenses Agent - the agent that runs adjacet to your Kafka instances in Lenses 6. [See Lenses docs for details.](https://docs.lenses.io/latest)

A datagenerator that makes sure there is snythetic data in your Kafka cluster for demonstration purposes. 

## Connecting to Lenses Community Edition

Lenses Community edition user interface runs on port 9991. To login just point your browser to `http://localhost:9991` if you're on your laptop. Or `http://{your VM's IP address}:9991` if you're running this on a VM. 

Once the login page comes up:

![screenshot of Community Edition login page](/images/login_page.png)

User name: admin
Password: admin
