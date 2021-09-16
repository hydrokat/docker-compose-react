# docker-compose-react
A pretty simplified Docker Compose workflow that sets up a react app.


## Usage

To get started, make sure you have [Docker installed](https://www.docker.com/get-started) on your system, and then clone this repository.

Next:
1. Navigate in your terminal to the directory you cloned this.
2. Run `docker-compose run --rm init` and respond with `y` when asked about creating a react app.
3. Spin up the container for the dev server by running `docker-compose up -d --build react-app`.

After that completes, you now have a react dev server running. The react app source code is inside the app-src directory.

Bringing up the Docker Compose network with `react-app` instead of just using `up`, ensures that only our site's containers are brought up at the start, instead of all of the command containers as well.

Additional containers are included that handle npm commands *without* having to have it installed on your local computer. Use the following command examples from your project root, modifying them to fit your particular use case.

- `docker-compose run --rm npm "command goes here without the quotes"`
- `docker-compose run --rm npx "command goes here without the quotes"`