# go-micro-base
Go Base Microservice

# Structure
|-- micro-scaffolding
  |-- builld: Strategy of construction of the device separated by environment.
    |-- docker
      |-- dev
        |-- Dockerfile: For local environment.
      |-- drone
        |-- Dockerfile: For deployed environments.
  |-- cmd: Starting point of the different layers of the device.
    |-- worker: Agregation's abstraction.
      |-- job.go: Main file for init dependencies & call job service.
  |-- pkg: Go source on package organization.
    |-- job: Aggregate containing use cases.
      |-- service.go: Aggregation's use cases.
      |-- repository.go
      |-- model.go
    |-- persistence: Data storage layer.
      |-- mongodb
      |-- mysql
  |-- .dockerignore
  |-- .drone.yml
  |-- .gitignore
  |-- go.mod
  |-- go.sum
  |-- Makefile
  |-- README.md
