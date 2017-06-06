# account-demo
Account demo operation guide.

## Deployment Guide

There are two ways to deploy demo application:

1. From Docker Hub:
  1.1. Download docker compose: docker-compose-dockerhub.yml
  1.2. Run command: docker-compose -f docker-compose-dockerhub.yml up -d

2) Locally:
 - Clone git repositories:
  a) Account Service API: git clone git@github.com:hugo-costa-tek/account-service-api.git
  b) Account UI: git clone git@github.com:hugo-costa-tek/account-ui.git
 - Build each project:
  a) cd account-service-api; mvn clean package -DskipTests; mvn docker:build
  b) cd account-ui; mvn clean package -DskipTests; mvn docker:build
 - Run command: docker-compose -f docker-compose-local.yml up -d
