
hoodie-vagrant setup v0.0.1
=============================

Goal of this project is to enable hoodie based development in a vagrant vm.

Prerequirements
===============

* [vagrant](http://www.vagrantup.com/)

Setup the VM
============

* checkout this repository [hoodie-vagrant](https://github.com/cainvommars/hoodie-vagrant)
* ``cd hoodie-vagrant``
* ``vagrant up``

Now your VM with a fresh couchdb, nodejs and hoodie-cli will be setup.

You can either:
* ``vagrant ssh``
* ``hoodie new myappname``
* ``cd myappname``
* set variables (view next part: Exports) 
* ``hoodie start no-open-browser``

Or start from your own machine:
* [setup hoodie](http://hood.ie/#installation) (skip couchdb setup, thats included in the VM ;-))
* ``hoodie new myappname``
* ``cd myappname``
* set variables (view next part: Exports)
* ``./node_modules/hoodie-app/bin/start --no-open-browser``

Exports
=======

To make sure hoodie talks to the right databse export your config:

``export COUCH_URL=http://localhost:5985``
``export HOODIE_ADMIN_USER=admin``
``export HOODIE_ADMIN_PASS=mysecretpassword``

enable access from other ips
``export HOODIE_BIND_ADDRESS=0.0.0.0``