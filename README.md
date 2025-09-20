# mkdocs

## features

- [x] documentation generator
- [x] theme Read the Docs
- [x] theme Material
- [x] pdf generation
- [x] dark mode
- [x] mermaid diagrams
- [x] include markdown

## known issues

- [ ] diagrams not working in full pdf
- [ ] introduce more environment variables

## start

- [github](https://github.com/tiogars/mkdocs)
- [https://template.mkdocs.tiogars.fr](https://template.mkdocs.tiogars.fr)

## requirements

- [docker](https://www.docker.com/products/docker-desktop/)
- [traefik](https://github.com/tiogars/traefik)
- [flame](https://github.com/tiogars/flame)
- docker-compose
- traefik_network

## usage

### run

```bash
docker compose -f "docker-compose.yml" up -d --build
```

### build image

```bash
docker login registry.tiogars.fr

docker build --pull --rm -f "dockerfile" -t registry.tiogars.fr/mkdocs:1.0.0 "." 

docker push registry.tiogars.fr/mkdocs:1.0.0

docker pull registry.tiogars.fr/mkdocs:1.0.0

docker logout registry.tiogars.fr
```

## ressources

- [mkdocs.org](https://www.mkdocs.org/user-guide/installation/)
