# Drupal development notes

## Managing code

Use Git and [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) to manage code.

If we're working across multiple major Drupal versions, prefix the branch with `d7-`, `d8-` etc.

Keep the entire Drupal directory under version control; this gives us an extra bit of protection in the unlikely event that an update to Drupal core breaks our site.

For new sites, use the [Composer](https://github.com/drupal-composer/drupal-project) template. Drupal is installed in the `web` directory.

    composer create-project drupal-composer/drupal-project:8.x-dev <project> --stability dev --no-interaction

## Modules and Features

Organise the `sites/(all|whatever)/modules` directory into:

- `contrib` modules downloaded from `drupal.org`
- `custom` modules just for this site, not intended for release on `drupal.org`
- `features` for site configuration managed using the [Features](https://www.drupal.org/project/features) module

[FIXME for Drupal Packagist.]  
If we're modifying a `contrib` module and might want to contribute our changes back to the community, consider adding it as a git submodule. (See the `drupal.org` handbook on [Git](https://www.drupal.org/node/1013552).)

## Suggested base themes

- [Bootstrap](https://www.drupal.org/project/bootstrap) -- uses the Bootstrap framework
- [Omega](https://www.drupal.org/project/omega) -- uses Compass/SASS
- [Zen](https://www.drupal.org/project/zen) -- uses Compass/SASS
