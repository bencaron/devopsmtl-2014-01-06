# Getting more from Dokku

## Environments supported

Dokku will detect from simple heuristics the langage/platform of the code pushed to it. It follow Heroku conventions around application buildpack, e.g. by using a [Procfile](https://devcenter.heroku.com/articles/procfile) file.

### Buildsteps

Build applications for Heroku (and/or Dokku!) with [Jeff Lindsay's Buildstep](https://github.com/progrium/buildstep)

Supports a bunch of langages/environments:

* [Ruby](https://github.com/heroku/heroku-buildpack-ruby)
 * [Node.js](https://github.com/heroku/heroku-buildpack-nodejs)
 * [Java](https://github.com/heroku/heroku-buildpack-java)
 * [Play!](https://github.com/heroku/heroku-buildpack-play)
 * [Python](https://github.com/heroku/heroku-buildpack-python)
 * [PHP](https://github.com/heroku/heroku-buildpack-php.git)
 * [Clojure](https://github.com/heroku/heroku-buildpack-clojure.git)
 * [Go](https://github.com/kr/heroku-buildpack-go.git)
 * [Dart](https://github.com/igrigorik/heroku-buildpack-dart.git)

You can also build your own: follow the instrutions!

## Plugins

Dokku makes a somewhat heavy uses of [plugins](https://github.com/progrium/dokku/wiki/Plugins); the default nginx frontend itself is made with a plugin!

There is a bunch of plugins to extend Dokku. Installation is a bit manual but straightforward:

```bash
cd /var/lib/dokku/plugins
git clone <git url>
dokku plugins-install
```
Plugins work as hooks that act on specific events (install, post-deploy, post-delete, etc.).