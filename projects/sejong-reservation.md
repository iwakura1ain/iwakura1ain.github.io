---
layout: project
title: Sejong Reservation
desc: 회의실 예약 시스템 
categories: REST microservice flask mariadb vue github-actions docker docker-compose docker-swarm 
repo: https://github.com/iwakura1ain/sejong-reservation
---

# Sejong-Reservation
## Services
- gatewayservice
- dbservice
- userservice
- adminservice
- reservationservice
- alertservice
- adminer (db manager)

## Integrated Features
- Email send API
- User login, logout, register, jwt API
- User CRUD API with query params
- Room CRUD API
- Room preview image upload, download API
- Single+Regular Reservation RETRIEVE with query params
- Single+Regular Reservation CREATE
- Single Reservation Update, Delete

## How to run
### Build containers
```bash
  docker compose down --volumes
  docker compose build --no-cache
```

### Run newly built containers
- Run with console output
```bash
  docker compose up 
```

- Run in background
```bash
  docker compose up 
```
