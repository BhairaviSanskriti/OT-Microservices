<div align="center">
  <img src="./static/logo.svg" height="249" width="255">
  <h1>OT-Microservices</h1>
</div>

It is a sample Employee System designed to understand the microservices' nature and behavior. This system is loaded with microservice applications. 

## Purpose

The purpose of the application is to provide an individual with a holistic idea of microservice architecture, working, and setup.

## Applications

Below are some of the microservices used in the entire project:

| **Application Name**           | **Default Port** | **Dependency**                | **Language**                                                                                                                                          | **Description**                                                                                       |
|--------------------------------|------------------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [attendance](./attendance)     | 8081             | MySQL                         | <img src="https://cdn.worldvectorlogo.com/logos/python-5.svg" height="32" width="32">                                                                 | Attendance is a microservice designed in Golang to manage attendance information of the employees. |
| [employee](./employee)         | 8083             | Elasticsearch                 | <img src="https://cdn.worldvectorlogo.com/logos/gopher.svg" height="32" width="32">                                                                   | Employee microservice is also designed in Golang to manage employee information.                    |
| [salary](./salary)             | 8080             | Elasticsearch                 | <img src="https://cdn.worldvectorlogo.com/logos/java.svg" height="32" width="32">                                                                     | Salary is a Golang-based application that creates and manages employees' salary information.    |
| [notification](./notification) | -                | SMTP Server                   | <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png" height="32" width="32"> | Notification is a scheduled service used to send mail notifications to employees.          |
| [frontend](./frontend)         | 3000             | attendance, employeee, salary | <img src="https://www.vectorlogo.zone/logos/reactjs/reactjs-icon.svg" height="32" width="32">                                                         | The front end is written in ReactJS and gets served using a proxy.|
| [traefik]()                    | 80               | frontend                      | <img src="https://cdn.worldvectorlogo.com/logos/gopher.svg" height="32" width="32">                                                                   | The web server is a traefik-based proxy that proxies the frontend application.                            |

For further information about the component, you can click on the application name.

## Databases

These applications use two types of databases- structured and non-structured.

| **Application Name** | **Default Port** | **Dependency** | **Description**                                                                                               |
|----------------------|------------------|----------------|---------------------------------------------------------------------------------------------------------------|
| [elastic](./elastic) | 9200             | -              | Elasticsearch, a non-structured database, manages the employee's information and salary.   |
| [mysql](./mysql)     | 3306             | -              | MySQL, a structured database, manages the attendance information of the employees.            |

For further information, click on the DB applicaton name.

## Architecture

The architecture of the complete microservice interaction looks like this:-

<div align="center">
  <img src="./static/architecture.png">
</div>

## Screenshot

<div align="center">
  <img src="./static/frontend.png">
</div>

## Quickstart

Quick start the application using `docker` and `docker-compose`. To build the images and start the setup, use the `docker-compose` command.

```shell
# To build all the images of ot-microservices
make build-images

# To start the setup locally
make setup
```

For further details checkout [GETTING_STARTED](./GETTING_STARTED.md)

## Release History

Please see our [CHANGELOG.md](./CHANGELOG.md) for details.

## Contact

If you have any suggestions or queries, contact us at opensource@opstree.com
