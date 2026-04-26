# Taiga ARM

ARM-compatible Docker images for the [Taiga](https://taiga.io/) open-source project management platform.

## Overview

This repository contains GitHub Actions workflows that build **ARM-only** Docker images for all Taiga components. Each pipeline automatically builds, tags, and publishes a specific Taiga service image to DockerHub.

> For **AMD64 versions** of Taiga images, see the official repository at [taigaio on DockerHub](https://hub.docker.com/u/taigaio).

## Available Images

All images are available on DockerHub under the organization `ahmgam`:

- **[taiga-front](https://hub.docker.com/r/ahmgam/taiga-front)** - Frontend application (Angular-based UI)
- **[taiga-back](https://hub.docker.com/r/ahmgam/taiga-back)** - Backend API server (Django)
- **[taiga-events](https://hub.docker.com/r/ahmgam/taiga-events)** - Events service (real-time notifications)
- **[taiga-protected](https://hub.docker.com/r/ahmgam/taiga-protected)** - Protected media service (file uploads)

### Pull Images

```bash
docker pull ahmgam/taiga-front
docker pull ahmgam/taiga-back
docker pull ahmgam/taiga-events
docker pull ahmgam/taiga-protected
```

## CI/CD Pipelines

This repository uses GitHub Actions workflows to automatically build and publish ARM-compatible images:

- **backend.yaml** - Builds the taiga-back image
- **frontend.yaml** - Builds the taiga-front image
- **events.yaml** - Builds the taiga-events image
- **protected.yaml** - Builds the taiga-protected image

Each workflow triggers on relevant changes and pushes the built image to DockerHub.

## License

These Docker images are built from Taiga's source code. Please refer to the [Taiga license](https://github.com/taigaio/taiga) for licensing information.

## Contributing

To contribute improvements to these ARM builds, please feel free to submit issues or pull requests.