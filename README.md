# A sample project for xDebug usage

Full description is available in [the blog post](https://viktorprogger.name/posts/xdebug-docker-config-example.html?utm_source=github&utm_campaign=xdebug-example-repo).

To get the project up and working, do these things:

1. [Set up PhpStorm](https://viktorprogger.name/posts/xdebug-docker-config-example.html?utm_source=github&utm_campaign=xdebug-example-repo#phpstorm)
1. Create a `.env` file with the following content:
   ```dotenv
   XDEBUG_MODE=debug
   ```
1. Set a breakpoint in the `index.php` file
1. Enable xDebug connection listening in PhpStorm
1. If you are using Windows or macOS, remove `extra_hosts` from `docker-compose.yml`
1. Run the `docker-compose up -d` command.  We don't need to start services, but we need to create a network. The next command will not work without it.
1. Run the `docker-compose run --rm php php index.php` command. Before the first launch, the container image will be built, this will take a few minutes.
1. Voila, script execution is stopped at your breakpoint!
