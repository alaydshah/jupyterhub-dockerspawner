# JupyterHub DockerSpawner

This project contains a sample configuration for a JupyterHub server running in Docker. The JupyterHub allows you to start Jupyter notebooks and edit them together with other users.

## Files

- `docker-compose.yml`: Docker Compose file that starts the JupyterHub server
- `Dockerfile`: Dockerfile that defines the image for the Jupyter Notebook Server
- `jupyterhub_config.py`: Configuration file for the JupyterHub server

## Usage

1. Make sure Docker is installed
2. Download or clone the repository from Github
3. Navigate to the project directory
4. Run `docker-compose up -d` to start the JupyterHub server
5. Open `http://<host-ip>:8000` in your browser and Sign up to create new user
6. Login with the user creds created in Step 5.

## Hints

- By default, the Jupyter notebooks are stored in the `/home/jovyan/work` directory in the container.
- The user notebooks are stored in separate Docker volumes named according to the `jupyterhub-user-{username}` scheme.
- Additional configurations can be made in the `jupyterhub_config.py` file, e.g. adding users or changing the login screen.
- For more information, see the [JupyterHub documentation](https://jupyterhub.readthedocs.io/en/stable/index.html).

Have fun :-)
