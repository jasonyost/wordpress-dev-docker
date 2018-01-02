# WordPress Development Docker Environment

This project serves as a simple local WordPress development environment. It depends on [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/install)

## Setup

1. `git clone git@github.com:jasonyost/wordpress-dev-docker.git [project-name]`
2. `cd [project-name]`

## Usage

The development environment can be started with the command:

`docker-compose up -d`

Which will start the development environment in the background. The first the the environment starts, it will download all the necessary images and files and may take a few minutes to complete. Subsequent starts will be faster.

Once the environment is running the development WordPress instance can be accessed in your browser at `http://localhost:8282/`.

The first time you access the development URL you will be presented with the WordPress installation screen, which should be filled out as any other standard WordPress installation.

Data is persisted between restarts of the environment.

The environment also includes the latest [phpMyAdmin](https://www.phpmyadmin.net/) which can be accessed at `http://localhost:8383/`

The environment can be stopped using the following command:

`docker-compose down`

## Committing your work

The `wordpress` directory will contain all of the files for the full WordPress installation and by default is ignored via the `.gitignore` file.

You will need to edit the last few lines of the file to ensure that your theme and/or plugin is committed to your git repository.

Examples:  
`!/wordpress/wp-content/themes/your-theme-name/`
`!/wordpress/wp-content/plugins/your-plugin-name/`

### Remotes

Be sure to remove the WordPress Development Docker Environment remote with:

`git remote rm origin`

and add your own.
