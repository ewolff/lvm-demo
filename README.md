#Docker Container for ROCA LVM Demo

This project provides Docker containers for the LVM ROCA demo, see
https://lvm-it.github.io/index_de.html . ROCA is a specific style of
web applications.

It consists of four Self-Contained Systems (SCS): general portal,
letter, notify claims and postbox.

To start run ´docker-compose up -d´

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

Find more information about SCS see http://scs-architecture.org . ROXA
is 

