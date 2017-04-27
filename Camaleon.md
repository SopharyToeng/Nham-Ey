*Requirements
  - Rails 4.1+
  - MySQL 5+ or SQlite or PostgreSQL
  - Ruby 1.9.3+
  - Imagemagick
**Installation
  - Install Ruby on Rails 4.1+

  *Create your rails project
    rails new my_project

  *Add the gem in your Gemfile
    gem "camaleon_cms",  '>= 2.4.3.5' # Stable versions 2.4.3.2, 2.3.6, 2.2.1, 2.1.1, 2.1.0
    # gem "camaleon_cms", github: 'owen2345/camaleon-cms' # current development version

  *Only Rails 5 support
    Add in your Gemfile draper for Rails 5
      -gem 'draper', github: 'drapergem/draper'
      In your Gemfile, change sass-rails into (Camaleon doesn't support for sprockets >= 4 which is included in sass-rails >= 6)
      -gem 'sass-rails', '~> 5.0'
  *Add this configuration to your config/application.rb
    -config.active_record.belongs_to_required_by_default = false
  *Install required Gem and dependencies
    -bundle install

  ***Install the CMS (before this, you can change defaut configuration in config/system.json)
    - rails generate camaleon_cms:install
  **Create database structure
    -rake db:migrate
  **Start your server
    -rails server or rails s # and then go to your browser http://localhost:3000/
