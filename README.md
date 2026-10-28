# nginx-buildpack-slim

Minimal nginx buildpack for Floship. It installs the pinned Heroku nginx
binary and the `start-nginx` process supervisor. It does not install Ruby or
`nginx-debug`.

The application supplies `bin/render_nginx_config.py`; `start-nginx` renders
the plain nginx configuration with the Python runtime that is already part of
the slug.

The nginx binary and `mime.types` come from
[`heroku/heroku-buildpack-nginx`](https://github.com/heroku/heroku-buildpack-nginx)
and remain under their upstream license.
