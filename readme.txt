This repository contains the python agent and supporting files.

Add an entry in the requirements.txt file to include the agent with the application
requirements.txt
===============
https://raw.github.com/prismo-systems/python/master/pyAgent-0.0.900.tar.gz

Change app startup - add prismo agent
app.yaml 
========
entrypoint: prismopy gunicorn -b :$PORT main:app

Add the following 2 ennvironment variables to app.yaml. They are for the  IP address/ hostname of controller and the flag "prismo_iclude_host_id" to false if system agent is not deployed with the app agent

app.yaml
==========

env_variables:
  prismo_controller_host: "34.73.167.120" 
  prismo_include_host_id:”false”

