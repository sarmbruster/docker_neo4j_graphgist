# docker_neo4j_graphgist

This repository contains a [docker cookbook](http://www.docker.io) for running a [Neo4j](http://www.neo4j.org) [console](https://github.com/neo4j-contrib/rabbithole) together with [graphgists](https://github.com/neo4j-contrib/graphgist) in a docker image.
 
## how to use

* install [docker](http://www.docker.io) locally, see http://www.docker.io/gettingstarted/#h_installation for installation guide.
* pull image using `docker pull sarmbruster/docker_neo4j_graphgist`
* use the image: 

```
docker run -d -v <absolute_path_for_local_gists>:/var/lib/tomcat7/webapps/ROOT/gists:ro -p 8080:8080 sarmbruster/neo4j_graphgist
```
  The above command maps a local path `<absolute_path_for_local_gists>` to a in-container location and connects local port 8080 to the in-container equivalent.

* point your browser to [http://localhost:8080](http://localhost:8080), you should see the graphgist webpage
* to use graphgists locally create a file ending with `.adoc` in the folder `<absolute_path_for_lcal_gists>` from above 
* to render your graphgist files, there are two options:
    1. type the filename exlcuding the `.adoc` extension in the upper right corner of [http://localhost:8080](http://localhost:8080)
    2. call [http://localhost:8080?myfile_without_adoc](http://localhost:8080?myfile_without_adoc) 
* for some examples see the contents of the `gists` folder in this repo
