# Docker + Wordpress + Underscores Theme 

![Docker](https://www.docker.com/sites/default/files/legal/small_h.png)

This small setup is a playoff and a quick way to setup Wordpress locally using Docker. This method works on any OS and takes around 5-10 minutes to get your local Wordpress working. No need to setup apache, mysql, wordpress and so on. Everything is handled via a single `docker-compose.yml`.

You can use the already setup starting theme from Underscores or use you're own.
Once you get Docker running and installed, you can setup your new tempale or a plugin
in the proper `/wp-content/***` folder
 
## Installation & Requirements
##### Install Docker
[Download from here](https://www.docker.com/)
##### Copy this repo
You can do this true Terminal or true [GitHub Desktop](https://desktop.github.com/).
```sh
$ git clone https://github.com/petsto/wordpress-docker-underscores.git
```

##### Next-Run commands
After you have Docker installed and the repo locally downloaded. Via your Terminal/Console go to the main project folder `/wordpress-docker-underscores/*` and in here run:
```
$ docker-compose up
-- Downloading MariaDB and Wordpress packages from Docker Hub
-- Once the setup is complete you might be ready to open localhost:8080. Once you see wordpress running, just kill the command running in the Terminal and run...
$ docker-compose start
-- This will run both things again, but as a background proccesses.
```

That should run the local server properly and now you can visit [http://localhost:8080/](http://localhost:8080/) and start working on your new local setup. Everything you put in `wp-content/` will be synced to the virtual machine instantly.

#### Other helpfull commands

```
$ docker-compose stop
```
-- Stop the machine images, so you can be sure your proccess will stay untouched if you switch off your pc.
```
$ docker-compose down
```
-- Stopping and removing Docker images. If you do that, this will destroy your current proccess and you'll have to re-run and setup everything from scratch. BUT, this will keep your stuff in wp-content/, but be thoughtful when doing this.


