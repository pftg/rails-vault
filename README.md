# RailsVault

[RailsVault](https://railsvault.netlify.com), is a leaderboard of the top Ruby on Rails starter repos

## Contributing

Missing a Ruby on Rails starter repo here? Just fork the repo and add your starter project
as a `<name>.md` in the `source/projects` folder.

Make sure to follow the following rules:

* **Ruby on Rails Starter:** The ideal starter is either a for Production starter or a hack-it-really-fast perfect for an MVP starter.
* **Open Source:** The project must be released under an open source license.
* **Accessible on GitHub:** The project must have a public repository on GitHub that we can link to and pull in stats from.
* **Stick to the format:** Fill out all the same fields as the other Ruby on Rails projects in `source/projects`.

## Running locally

RailsValut is built with Middleman. To install and run locally:

    git clone git@github.com:heyspacetime/rails-vault.git
    cd rails-vault
    bundle install (requires ruby 2.1.2 to work w/o errors)
    bundle exec middleman

You'll run into GitHub's API limits very quickly if you just do this. To avoid this we recommend you create a Github API token with permissions to access public repositories and Gist.

Then create a Gist with a single file `data.json` with an empty javascript object literal as content: {}

Then set these environment variables before running middleman:

    export GITHUB_TOKEN=YOUR_TOKEN
    export GIST_ID=ID_OF_YOUR_GIST

Then middleman will use the Gist you specified to archive stats (stars, forks and issues) for the repositories.

## Netlify

RailsVault is cloned from StaticGen. A project built and maintained by [Netlify](https://www.netlify.com), a hosting and automation service for static websites and apps.

## License

RailsVault and StaticGen is released under the [MIT License](LICENSE).
Please make sure you understand its [implications and guarantees](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html).
