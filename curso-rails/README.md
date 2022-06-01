# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

Primera App de Ruby&rails

# Instrucciones
- rails new curso-rails -d mysql
- gem install bundler
- gem install mysql2 --platform=ruby -- --with-mysql-dir="C:\Program Files\MySQL\Connector C++ 8.0"
gem install mysql2 --platform=ruby -- --with-mysql-dir=C:\Users\MIMP\Documents\mysql-connector-c++-8.0.29-winx64
- bundle install
- rails db:create
- rails db:migrate 
- rails db:seed
- rails webpacker:install //ya no lo instale
- rails s

# Part 2
- rails g scaffold Product name:string description:string stock:integer 'price:decimal{10,2}'
- para generarlo de otra forma tenemos:
- rails generate
    - generamos el controlador:
        -- rails generate controller [NAME in plural][actions names]
        - rails generate controller CreditCards principal payment
    - Generamos el modelo
        --rails generate model NAME [field[:type][:index] field[:type][:index]] [options]
        - rails generate model CreditCard no_card:string owner:string provider:string
    - Ver las migraciones pendientes
        - rails db:migrate:status //down significa que deben correrse antes de ejecutar la app
            - rails db:migrate
            - rails db:migrate:status //deberian estar en up
  -- Gemfile
- gem 'annotate'
    - bundle install
    - rails g annotate:install
- rails webpacker:install
- gem install foreman
-   touch Procfile.dev
    - dentro del archivo en la raiz del proyecto:
        - web: bundle exec rails s
        - webpacker: ./bin/webpack-dev-server
-  foreman start -f Procfile.dev -p 3000


