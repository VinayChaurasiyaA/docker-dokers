## Docker is the container, which is isolated it does not know what are the process are running outside of the container, it just focuess on it's process.
 #### RUNTIME : Runtime is at last component of the docker architectures. Runtime allows us to start and stop the containers. There are 2 types of runtime,
1. low level runtime which is runc :- it works with the os and it helps to start and stop the container,
2. Containerd : Higher level. It has to manage the runc, it helps how to interact with the network and pulling of the images. It is used in KUBERNITES.

DOCKER ENGINE : It is used to interact with the docker, daemon is there which follows the hieracy of the,following,Docker engine is also comes after the runtime.
```
 docker Cli (command line) -> you can run the commands like: docker run ubuntu
     |
 Rest Apis -> basic apis which gets, or fetch the data
     |
 server, daemon -> this is the docker engine, server is used to get the images
      | it will make call to the runtime (runc) 
 ``` 
ORCHESTRATION:It allows us to manage the whole container, it comes after the docker engine. It also helps us to increase in the scalibility.

Docker image is what makes that application run , or you can say that instructions from which the application will run.
How everything works :
Docker file  ->> Run the docker file we'll get ->> image after running the image which contains the instruction -> we get container which has your application and then boom application starts running.

What is the OCI : The OCI currently contains three specifications: the Runtime Specification (runtime-spec), the Image Specification (image-spec) and the Distribution Specification (distribution-spec).
runtime spec : ->
image-spc : 
distri spec : 

dockerCli: After we run  ``` docker run <image_name> ```
then daemon looks whether the <image_name> is present or not, if not that goes to the registry which is at the https:dockerhub.com and downloads from there
when the images gets downloaded it also downloads the dependencies and everything which the system will require to run.
 ``` docker pull <image_name> ```
that is used to download the image. where if you want to have a particular version of it.

``` docker pull <image_name>:version ```
``` docker run it <image_name> ```

it : is used for interactive enviornment, when you execute them we directly get into that container.

``` docker container exec -it <name_of_the_other_environment> ``` bash
it'll make both the container attached with eachother

to stop the docker container: 
 ``` docker stop <image_id> ```





