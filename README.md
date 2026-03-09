<div align="center">

# Hush Hub Backend
</div>

### Application Features
- [x] Dockerize Application 
- [x] Docker Hot reloading for local development 
- [x] Multistage build 
- [x] Separate credentials for local dev and production (.env)
- [x] Local docker image 
- [x] Pull/push from the docker hub 
- [x] Log formatting (Configure logging in application) 
- [x] Seeding data for the application 
- [x] Docker tool to wrap complex docker commands in a simpler format

### CI/CD Features
- [x] Setup Production and Dev Environment servers **using Ansible**

- **On PR**:
    - [x] Linter
    - [x] Unit Test
    - [x] CodeQL
    - [x] SonarQube, With results in PR annotations (integrated with SonarCloud)

- **On Push to feature branch**:
    - [x] Unit Test
    - [x] Build Image

- [x] Deploy to dev env from feature branch 
    - [x] run dev deployment workflow by **commit-msg**. commit with `deploy-dev` message
    - [x] run workflow by **pr-comment**. comment on pr - `/deploy-dev`
- [x] on CD deploy image to dockerHub
- [x] Implement CD from `main` branch to both the envs (dev, prod)
- [x] Implement a simple rollback job that we use the last successful image to do the deployment 
- [x] Implement a rollback table with PRs and SHAs
- [ ] Calculate disaster recovery time of the CI/CD
- [ ] Notify on failed deployments with details in the email
