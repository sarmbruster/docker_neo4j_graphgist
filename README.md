# docker_neo4j_graphgist

This repository contains a [docker cookbook](http://www.docker.io) for running a [Neo4j](http://www.neo4j.org) [console](https://github.com/neo4j-contrib/rabbithole) together with [graphgists](https://github.com/neo4j-contrib/graphgist) in a docker image.
 
## how to use

* install [docker](http://www.docker.io) locally, see http://www.docker.io/gettingstarted/#h_installation for installation guide.
* pull image using `docker pull sarmbruster/docker_neo4j_graphgist`
* use the image: `docker run -d -v <absolute_path_for_local_gists>:/var/lib/tomcat7/webapps/ROOT/gists:ro -p 8080:8080 sarmbruster/neo4j_graphgist`
* point your browser to http://localhost:8080, you should see a graphgist
* to use graphgists locally edit a file ending with `.adoc` in the folder `<absolute_path_for_local_gists>` from above and type the filename with the `.adoc` extension in the upper right corner.
