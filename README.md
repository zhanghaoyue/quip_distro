# Building and running the QUIP containers and application

# Requirements

1. docker should be installed. You should be able to run docker commands (e.g., pull, run).
2. git should be installed.
3. QUIP requires access to a folder (data folder) on the host machine to store whole slide tissue images 
   and the database. You should have read/write permissions to the folder.
4. The installation scripts and the QUIP softwar has been tested on Linux systems and with Google Chrome 
   browser. 
5. QUIP requires three ports to be open: 80, 6002, 3000. 
   
# Clone the distribution repository

Clone this repository.

         git https://github.com/SBU-BMI/quip_distro
         
# Run the containers

Before pulling and running the containers, create a data folder if one doesn't exist. The data folder will be used to 
store images and the database as well as a set of configuration files required by the containers.

Execute run_containers.sh script. At the command prompt, 

$ ./run_containers.sh \<full path of data folder\> 

The startup process will create an "img" sub-folder in the data folder where tissue images will be stored and 
a "data" sub-folder where the database files will be stored. Please make sure the storage folder has enough 
space for images and the database. 

The startup process will pull the QUIP containers from their respective docker image repositories, create a user-defined 
docker network (quip_nw), start up the containers and attach them to the user-defined docker network. 

After the containers are started, you may access the QUIP web applications using a browser at http://<hostname> . Here, hostname is the name or IP address of the host machine where the containers are installed and running. 

# Additional information

This video shows the use of the QUIP system: https://www.youtube.com/watch?v=gbUzUmzvwEk




