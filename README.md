# Docker Assignment

A C-DAC Docker assignment demonstrating a web form backed by a Flask service, with a Node.js/Express frontend and Docker Compose configuration.

## Current status

The repository contains frontend and backend source, service Dockerfiles, a Compose file, and a Jenkins pipeline. The Jenkinsfile uses Windows `bat` steps, so its pipeline expects a Windows Jenkins agent. The Docker Hub commands in the existing documentation are examples with placeholders; publishing images is not configured as an automated workflow here.

From the repository root, start the services with:

```bash
docker compose up --build
```

Then open [http://localhost:3000](http://localhost:3000). Review the Compose and service configuration for your environment. This README does not claim the workflow has been run or tested.

Technologies: Node.js, Express, Python, Flask, Docker, Docker Compose, and Jenkins.

Portfolio category: C-DAC project.
