# MobSOS

A framework for community information systems (CIS) success awareness

MobSOS Toolkit:
* [MobSOS Data Processing](https://github.com/rwth-acis/mobsos-data-processing)
* [MobSOS Success Modeling](https://github.com/rwth-acis/mobsos-success-modeling)
* [MobSOS Surveys](https://github.com/rwth-acis/mobsos-surveys)
* [MobSOS Query Visualization](https://github.com/rwth-acis/mobsos-query-visualization)
* [MobSOS Evaluation Center](https://github.com/rwth-acis/mobsos-evaluation-center)


[![Join the chat at https://gitter.im/rwth-acis/mobsos](https://badges.gitter.im/rwth-acis/mobsos.svg)](https://gitter.im/rwth-acis/mobsos?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Installation

To get started using the MobSOS framework, you can use the `docker-compose.yml` file. Simply run 
```sh
docker-compose up
```
and visit `localhost:4200` (Note that you need to have docker installed to run the command)
Docker will create a MobSOS las2peer network under the name `mobsos_backend`. 

## Adding services
You can connect your own las2peer services by builing them in a docker container and then connecting it to the network. The command should look similar to this:
```
docker run --network mobsos_backend -e LAS2PEER_PORT=<PORT> --name <NAME> <IMAGE:TAG> 
```
Note that your service might need aditional environment variables.
You can also directly add your service to the docker compose file.
