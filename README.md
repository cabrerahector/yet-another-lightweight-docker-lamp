# Yet Another Lightweight Docker LAMP stack
A lightweight Docker LAMP stack ([Apache](http://www.apache.org/), [MySQL](https://www.mysql.com/) and [PHP](http://php.net/)) based (mostly) on [Alpine](https://www.alpinelinux.org/about/) images.

### Why Alpine?

Because Alpine images are lightweight, and that means faster (down)loading times so you can start working on your web application as quick as possible.

## Prerequisites

Before you proceed, make sure that you have the following components installed and properly set up on your machine:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/get-started)

## Installation

1. [Clone](https://help.github.com/en/articles/cloning-a-repository) or download this repository on your local computer.
2. Open a command prompt/[CLI](https://en.wikipedia.org/wiki/Command-line_interface) and run `docker-compose build` to download the images. This might take a while if your Internet connection isn't fast so you may want to go grab a cup of coffee.

## Configuration and Usage

Out of the box, you'll get:

- Apache 2.4
- PHP 8.1
- MySQL 8.0
- phpMyAdmin 5.2

You'll also find an `.env.example` file at the root directory that you can use to create a new `.env` file (eg. `cp .env.example .env`) to change the configuration of your LAMP stack. You may need to do a full rebuild (`docker-compose build --no-cache`) afterwards to update your LAMP stack accordingly.

Once you're satisfied with the configuration, place your web application files inside the `src` folder, open a command prompt/[CLI](https://en.wikipedia.org/wiki/Command-line_interface) and run `docker-compose up -d` to start your LAMP stack.

To view your web application on a browser, load `http://localhost` (or run `docker-machine ip` to get the IP address of your LAMP stack and use that instead.)

### Connecting to MySQL

MySQL `root` user's default password is `supersecret`. There's also another user that gets created called `user` with a default password `123abc`.

The hostname you'll need to use is `db` (or the IP address of your docker machine) and the port is `3306`.

### Connecting to phpMyAdmin

To access phpMyAdmin visit `http://localhost:8080` (or the IP address followed by `:8080`). Use either of the users mentioned above to log in.
