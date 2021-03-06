# KuCoin REST Client in Ruby

This gem provides a REST client to interface with KuCoin's API. As of right now a Websocket service isn't provided by KuCoin and as such, all API calls are made over REST.

## Getting started

First of all you'll need to get an account on KuCoin, [click here to get one](https://www.kucoin.com).

After setting up your account, head to "Account", locate the "API Keys" section and click on "Create".

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'kucoin'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install kucoin

## Setup

```ruby
Kucoin.configure do |config|
  config.key = YOUR_API_KEY
  config.secret = YOUR_API_SECRET
end
```

## Usage

REST Client (see specs/source code for available methods/endpoints):

```ruby
client = Kucoin::Rest::Client.new
client.ticker("HPB-ETH")
```

## Status

Full rspec coverage suit will be added shortly. Almost all API endpoints have been implemented. Feel free to fork the repo and submit PRs for any missing endpoints!

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/kucoin. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Kucoin project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/kucoin/blob/master/CODE_OF_CONDUCT.md).
