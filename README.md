# README

A sample app to show an issue with rails_event_store-rspec.

# Steps to reproduce

    bundle
    RAILS_ENV=test rake db:create

```
NameError: uninitialized constant RSpec::Matchers
/Users/michal/.rvm/gems/ruby-2.3.3/gems/rails_event_store-rspec-0.17.0/lib/rails_event_store/rspec/be_event.rb:115:in
`<class:BeEvent>'
/Users/michal/.rvm/gems/ruby-2.3.3/gems/rails_event_store-rspec-0.17.0/lib/rails_event_store/rspec/be_event.rb:3:in
`<module:RSpec>'
/Users/michal/.rvm/gems/ruby-2.3.3/gems/rails_event_store-rspec-0.17.0/lib/rails_event_store/rspec/be_event.rb:2:in
`<module:RailsEventStore>'
/Users/michal/.rvm/gems/ruby-2.3.3/gems/rails_event_store-rspec-0.17.0/lib/rails_event_store/rspec/be_event.rb:1:in
`<top (required)>'
/Users/michal/.rvm/gems/ruby-2.3.3/gems/rails_event_store-rspec-0.17.0/lib/rails_event_store/rspec.rb:8:in `<top
(required)>'
```

# Workaround

Add 'rspec' to the Gemfile

```ruby
group :test do
  gem 'rspec'
  gem 'rails_event_store-rspec'
end
```
