# Task Implementation Steps: Docker Build & Push Workflow

This package contains the requested GitHub Actions workflow (`ci-cd.yml`) extended with the steps shown in your task:

1. **Add steps to log in to Docker Hub using secrets** (`docker/login-action@v2` with `DOCKER_HUB_USERNAME` and `DOCKER_HUB_ACCESS_TOKEN`).
2. **Build the Docker image with `docker build`** (handled via `docker/build-push-action@v4`).
3. **Push the image tag to Docker Hub** (`push: true` with appropriate repository tagging).
4. **Ensure the workflow fails if tests fail** (`pytest` failure stops the workflow before reaching Docker login/push).

## How to use:
1. Place `.github/workflows/ci-cd.yml` in your repository.
2. Add your `DOCKER_HUB_USERNAME` and `DOCKER_HUB_ACCESS_TOKEN` as Repository Secrets in GitHub.
