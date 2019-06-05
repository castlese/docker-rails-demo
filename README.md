# Welcome to Docker Rails Demo
Rails, Docker and Webpacker is an awesome combination, for instance to develop React/Rails apps with.
This demo app uses [Rails 5](https://rubyonrails.org/), [Webpacker](https://github.com/rails/webpacker) and [Docker](https://www.docker.com/). In development mode, it uses [webpack-dev-server](https://github.com/webpack/webpack-dev-server) for live Javascript reloading. As database it uses [PostgreSQL](https://www.postgresql.org/).

## First, build the app for development
`docker-compose build`

## Create the database
`docker-compose run web scripts/wait-for-it.sh db:5432 --  "rake db:create db:migrate"`

## Run the app in development mode
`docker-compose up`

## Build the app for production
`docker build -t docker-rails-demo .`

Now open http://localhost:3000 and look at your Javascript console to see messages

Released under the  [MIT License](https://opensource.org/licenses/MIT)
