# Clients

Given the constraints, running dokku commands remotely via SSH is fine. For certain configurations, the extra complication of manually invoking ssh can be a burden.

While dokku does not yet have an official client, there are various ways in which you can interact with your dokku installation.

## (bash) `dokku_client.sh`

Of all methods, this is the *most* official method of interacting with your dokku installation. It is a bash script that interacts with a remote dokku installation via ssh. It is available in `contrib/dokku_client.sh` in the root of the dokku repository.

To install, simply clone the dokku repository down and add the `dokku` alias pointing at the script:

```shell
git clone git@github.com:progrium/dokku.git ~/.dokku

# add the following to either your
# .bashrc, .bash_profile, or .profile file
alias dokku='$HOME/.dokku/contrib/dokku_client.sh'
```

Configure the `DOKKU_HOST` environment variable or run `dokku` from a repository with a git remote named dokku pointed at your dokku host in order to use the script as normal.

## (python) dokku-client

dokku-client is an extensible python-based cli wrapper for remote dokku hosts.  You can install it via the following shell command (assuming you have python and pip installed):

```shell
pip install dokku-client
```

See [documentation here](https://github.com/adamcharnock/dokku-client) for more information.

## (ruby) Dokku CLI

Dokku CLI is a rubygem that acts as a client for your dokku installation. You can install it via the following shell command (assuming you have ruby and rubygems installed):

```shell
gem install dokku-cli
```

See [documentation here](https://github.com/SebastianSzturo/dokku-cli) for more information.

## (ruby) DokkuClient

DokkuClient is another rubygem that acts as a client for your dokku installation with built-in support for certain external plugins. You can install it via the following shell command (assuming you have ruby and rubygems installed):

```shell
gem install dokku_client
```

See [documentation here](https://github.com/netguru/dokku_client) for more information.
