# Kuristar Website

## Requiremets
* Ruby 3.4.5

## Setup
* `bundle install`
* `jekyll serve`

## Deployment
* push to Github and let Github Actions do the rest

## Notes
* To ignore files from the build, include it in the `_config.yml` file under the `exclude` section.
* To run jekyll on a different port, run `bundle exec jekyll serve --port <port_number>`

# Agents
* This project uses `AGENTS.md`, create a symlink to it for your agent of choice:
```
ln -s AGENTS.md CLAUDE.md
```
