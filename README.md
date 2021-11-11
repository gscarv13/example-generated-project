# README

### Walkthrough video
[Click on this link](https://www.loom.com/share/b76f8fd281314b78ac3fe16808ae6ce5)
### Steps taken to generate this app:
Generate the app:
```
rails new --skip-sprockets --skip-turbolinks react_on_rails_webpacker-v6

cd react_on_rails_webpacker-v6
```

Add to the Gemfile:
```ruby
# Update webpacker version to:
gem 'webpacker', '6.0.0.rc.6'

# Add react on rails
gem 'react_on_rails', git: 'https://github.com/gscarv13/react_on_rails.git', branch: 'update-webpacker-config'
```

Install webpacker:
```terminal
./bin/bundle install

./bin/rails webpacker:install

# enter `a` to replace all
```

Make sure the version of `@rails/webpacker` on `package.json` match the same version of `webpacker`. 

Commit all changes and install react_on_rails:
```terminal
# commit all changes
git add .
git commit -m "Initial commit"

bundle exec rails generate react_on_rails:install
```

delete `.browserslistrc`

Add rails dependencies
```terminal
yarn add @rails/ujs @rails/activestorage
```

Run the project
```terminal
foreman start -f Procfile.dev
```
