# Docker-based Drupal stack for Contenta Headless CMS

## Introduction

Docker4Drupal is a set of docker images optimized for Drupal. Use `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4drupal/releases) to spin up local environment on Linux, Mac OS X and Windows.

* Read the docs on [**how to use**](https://wodby.com/docs/stacks/drupal/local#usage)
* Ask questions on [Slack](http://slack.wodby.com/)
* Follow [@wodbycloud](https://twitter.com/wodbycloud) for future announcements

## Documentation

Full documentation is available at https://wodby.com/docs/stacks/drupal/local.

## Contenta CMS

Download the distribution using composer:

```
docker run --rm --interactive --tty \
--volume $PWD:/app \
composer create-project contentacms/contenta-jsonapi-project www --stability dev --no-interaction --remove-vcs --no-progress --prefer-dist
```

Configure `.env` file, see `.env.example` for an example.

Run `docker-compose up`. Site should be available at `contenta.drupal.docker.localhost`.