# Drupal development notes

## Managing code

Use Git and [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) to manage code.

If we're working across multiple major Drupal versions, prefix the branch with `d7-`, `d8-` etc.

Two options:

1. Keep the `sites` directory under version control.
2. Keep the entire `drupal` directory under version control; this gives us an extra bit of protection in the unlikely event that an update to Drupal core breaks our site.

## Modules and Features

Organise the `sites/(all|whatever)/modules` directory into:

- `contrib` modules downloaded from `drupal.org`
- `custom` modules just for this site, not intended for release on `drupal.org`
- `features` for site configuration managed using the [Features](https://www.drupal.org/project/features) module

If we're modifying a `contrib` module and might want to contribute our changes back to the community, consider adding it as a git submodule. (See the `drupal.org` handbook on [Git](https://www.drupal.org/node/1013552).)
