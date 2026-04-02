# Interactive Tool Images

This directory is intended to be pushed to a separate Git repository dedicated to interactive tool images.

## Layout

- jupyter
- ml-jupyter
- qiskit-jupyter
- .github/workflows

Each image directory is independent and can be built on its own.

## Build policy

- A change under one image directory should only rebuild that image.
- Documentation-only changes must not trigger image rebuilds.
- The repository is designed for GitHub Actions with GHCR publishing.

## Suggested repository split

Push the contents of this directory into a dedicated repository, for example:

- galaxy-interactive-images

Then publish images such as:

- ghcr.io/<owner>/galaxy-interactive-jupyter
- ghcr.io/<owner>/galaxy-interactive-ml-jupyter
- ghcr.io/<owner>/galaxy-interactive-qiskit-jupyter
