# Docker Build

An Action for building a Docker image of an app.

The action can be configured to only build an image (for tests), or publish two tagged images (defined tag and latest).

Steps:
- Code checkout
- Builds docker image
- Login to Registry
- Image Tagging
- Publish image to Registry

## Inputs

| Input | Description | Required | Default |
|-|-|-|-|
| `IMAGE_NAME` | Name of the image to be built | `false` | latest |
| `IMAGE_TAG` | Tag of the image to be built | `false` | ghcr.io/${{ github.repository }} |
| `IMAGE_REGISTRY` | Registry to push the image | `false` | ghcr.io |
| `DOCKER_USERNAME` | Username to login to the registry| `false` | ${{ github.repository_owner }} |
| `DOCKER_PASSWORD` | Password to login to the registry| `true` | |
| `DOCKERFILE_PATH` | Path to the Dockerfile | `false` | Dockerfile |
| `PUBLISH` | Publish the image to the registry | `false` | true |
