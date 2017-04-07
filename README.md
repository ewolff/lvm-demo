# Docker Container for ROCA LVM Demo

This project provides Docker containers for the LVM ROCA demo, see
https://lvm-it.github.io/index_de.html . ROCA is a specific style of
web applications.

It consists of four Self-Contained Systems (SCS): general portal,
letter, notify claims and postbox.

* To build the base image use `docker build --tag npm-base-image
npm-base-image`. 

* To start run `docker-compose up -d`. This will also build the rest of
the Docker images.

* Note that there is currently a problem so the application only
really works if you switch JavaScript off.

https://lvm-las-roca.herokuapp.com/ is a running instance of the
application that is deployed on Heroku.

The Docker containers should run on `localhost`. Otherwise set the
environment variable `ROCA_SERVER` to the host the containers run on.

Points to note:

* There are some customers - try Mei or Mül etc
* The postbox is transcluded from the server running on port 3001
* The link to write a letter or notify a claim will go to different
  applications (on port 3002 and 3003)
* Behind the scenes a project with the shared assets ensure common UI
elements.
* The Postbox is written in Java / Spring Boot, the other projects in NodeJS.

This project is based on a very similar project by @mjansing and
@moonglum .

Find more information about SCS see http://scs-architecture.org . ROCA
is at http://roca-style.org/ .

The source code for the services can be found at:

* https://github.com/LVM-IT/roca-las-damage
* https://github.com/LVM-IT/roca-las-letter
* https://github.com/LVM-IT/roca-las-postbox
* https://github.com/LVM-IT/roca-las

The asset project is https://github.com/LVM-IT/roca-las-assets .


