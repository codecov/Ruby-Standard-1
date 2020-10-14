# Ruby-Standard-1 (Codecov Gem Edition)

[![Build Status](https://travis-ci.org/codecov/Ruby-Standard-1.svg?branch=master)](https://travis-ci.org/codecov/Ruby-Standard-1) [![codecov](https://codecov.io/gh/codecov/Ruby-Standard-1/branch/master/graph/badge.svg)](https://codecov.io/gh/codecov/Ruby-Standard-1)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fcodecov%2Fruby-standard-1.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fcodecov%2Fruby-standard-1?ref=badge_shield)

### Last Updated: 10/14/20 20:05:42

## What is this?

This is a **Ruby on Rails** application, with basic unit tests, for which coverage is uploaded to Codecov on a daily basis via the [Codecov Gem](https://rubygems.org/gems/codecov/versions/0.1.4). It can also serve as an example for how to integrate Codecov into your Ruby project. If the build is passing for this project, then Codecov's Ruby report processing is functional and correct on codecov.io.

## What's the difference between `Ruby-Standard-1` and `Ruby-Standard-2`?

This repo, Ruby-Standard-1, uses the Codecov gem to process coverage reports, while [Ruby-Standard-2](https://github.com/codecov/Ruby-Standard-2) uses Codecov's bash uploader to process reports. Otherwise, everything is the same between these two repos.

## Configuration

This project is written in `Ruby 2.6.3` using `Rails 5.2.3`. Unit tests are written in the [RSpec Rails](https://github.com/rspec/rspec-rails) framework. Coverage reports are generated through the [SimpleCov](https://github.com/colszowka/simplecov) gem.

Unit tests: `spec/index_spec.rb` which tests `lib/index.rb`

Gemfile configuration:
```ruby
gem 'codecov', require: false
gem 'simplecov', require: false
```
RSpec configuration (top of `spec/spec_helper.rb`):
```ruby
require 'simplecov'
SimpleCov.start

require 'codecov'
SimpleCov.formatter = SimpleCov::Formatter::Codecov
```
> `spec_helper.rb` is a file that contains settings specific to RSpec. If you're using another testing framework, you'll need to put this information in some other helper Ruby file. For example, if you're using Minitest, which is prepackaged with all Rails applications, you'll need to put the above lines of code inside `test/test_helper.rb`

## Reporting Issues

If you've discovered an issue with this repository or with Ruby processing in general, it is recommended to email support@codecov.io rather than post an issue here. This repository will not be checked regularly for open issues.

## Contributing

Contributions are welcome! If you'd like to contribute to this repository, feel free to open a pull request or flag an issue. If you would like to contribute a new lanaguage standard, [you can get more information here](https://github.com/codecov/standards-scripts/blob/master/README.md#contributing). 


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fcodecov%2Fruby-standard-1.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fcodecov%2Fruby-standard-1?ref=badge_large)