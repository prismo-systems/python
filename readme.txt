This repository contains the python agent and supporting files.

Add an entry in the requirements.txt file to include the agent with the application
requirements.txt
===============
https://raw.github.com/prismo-systems/python/master/pyAgent-0.0.880.tar.tz

Change startup toi add prismo agent
app.yaml 
========
entrypoint: prismopy gunicorn -b :$PORT main:app

Add the following 2 ennvironment variables to app.yaml with IP address/ hostname of controller and 
set the flag "prismo_iclude_host_id" to false if system agent is not deployed with the app agent

app.yaml
==========

env_variables:
  prismo_controller_host: "34.73.167.120" 
  prismo_include_host_id:”false”

