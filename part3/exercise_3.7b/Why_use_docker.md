#Why use docker and what are the benefits?

If an application is developed and tested on a single machine, it is often difficult for the developer to find out why the application wil run into bugs when used on other computers. If the libraries the application depends on are updated on the computer the application is used, the application may stop working or behave incorrectly. Moreover, there may be applications on the same machine, that require different versions of some of their shared dependencies, forcing the user to choose which of the applications to keep usable. 

Docker answers these issues by creating an image that combines the application and its dependencies. From this image containers can be created, that work on any machine that can run docker. This way the container is not affected by changes in e.g. the versions of its dependencies on the host machine running docker. The contained application will run the same whether on development computer or in the production server. In addition docker-composer makes it possible to combine several contained micro-services (and their contained databases) together into a set of connected containers that are easily launched simultaneously.  

As an example, let us take a look on a system with two web servers (microservices A and B), nginx  and a PostGreSQL server for the databases needed by the microservices. In the figure 1, a setup without docker for this system is shown. The servers must have compatible dependencies, as they share all the libraries and binaries of the underlying system.

Figure 1

![System without docker]
(system_without_docker.png)

In the figure 2, a setup for a similar system using docker is shown. Each server and even both databases run in their own containers and having incompatible dependencies would not cause problems.


Figure 2

![System with docker]
(system_with_docker.png)




