# ActiveService

ActiveService is a service object framework.

It is lightweight and fast, almost no performance loss. It's test friendly, work well with all test framework like minitest/respec.

It add a servcie layer in Rails, you can Rails generator to generate service just like controller and model.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'activeservice', github: 'chloerei/activeservice'
```

And then execute:

    $ bundle

## Usage

Declare a service like so:

```ruby
class HelloService < ActiveService::Base
  def initialize(name)
    @name = name
  end

  def say_hello
    "Hello #{@name}!"
  end
end
```

Initialize service object:

```ruby
hello_service = HelloService.new('David')
```

Execute service:

```ruby
hello_service.say_hello
```

Of course you can use other method name.

## Rails generator

If you are using Rails:

```bash
rails g service hello
```

It will create a template service file in app/services and a test file in test/services.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/activeservice/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
