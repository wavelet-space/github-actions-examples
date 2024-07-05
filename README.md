# GitHub Actions Examples

- scheduled action
- container registry

## Scheduled action

- The shortest interval you can run scheduled workflows is once every 5 minutes, see <https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule>

```shell
on:
  schedule:
    - cron: '*/5 * * * *'
```

- <https://github.com/actions/github-script>

## GitGub Container Registry

This repository contains simple examples how to build and push Docker images to GitHub Container Registry ([GitHub Packages](https://docs.github.com/en/packages)).

### Usecases

- [x] Jak vývojář chci mít GHA workflow, které sestaví a přidá Docker image do GitHub Container Registry.
  - Potřebujeme `GITHUB_TOKEN`.
  - <https://docs.github.com/en/actions/publishing-packages/publishing-docker-images>

- [ ] Nastav a popiš vhodnou strategii pro souběžné tagování několika balíků v monorepozitáři.

### Examples

- **Python**:  

  - Build the image.
  
  ```powershell
  docker build -t project-python:latest project-python
  ```

  - Run the container.

  ```powershell
  docker run -it --rm --name project-python project-python:latest
  ```

  ```powershell
  Hello, world!
  ```

- **Rust**

  - Build the image.
  
  ```powershell
  docker build -t project-rust:latest project-rust
  ```

  - Run the container.

  ```powershell
  docker run -it --rm --name project-rust project-rust:latest
  ```

  ```powershell
  Hello, world!
  ```
