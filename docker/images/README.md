# JupyterHub DockerSpawner

Modified Docker files from docker-stacks repo: https://github.com/jupyter/docker-stacks project to support cuda.

## Hierarchy

- `scipy-notebook:`: Final image used by docker spawner
  - `minimal-notebook`
    - `base-notebook`
      - `docker-stacks-foundation`

> Note: In order to build or modify an intermediate image, all subsequent children images would have to be rebuilt.
> 
Have fun :-)
