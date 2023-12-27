# `Jekyll_google_translate` [![Gem Version](https://badge.fury.io/rb/jekyll_google_translate.svg)](https://badge.fury.io/rb/jekyll_google_translate)

Adds Google Translate to a web page.


## Installation

Add the following to your Jekyll website's `Gemfile`:

```ruby
group :jekyll_plugins do
  gem 'jekyll_google_translate'
end
```

And then execute:

```shell
$ bundle
```

Copy `demo/assets/css/jekyll_google_translate.css` to your Jekyll web site's CSS directory,
and update your layout accordingly.


## Usage

The {% google_translate_html %} tag must be called to insert HTML into the page,
then the {% google_translate_javascript %} tag must be called to insert Javascript into the page.
For example:

```html
<!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <link rel="stylesheet" href="{{ '/assets/css/style.css?v=' | append: nowMillis }}" type="text/css">
    <link rel="stylesheet" href="{{ '/assets/css/jekyll_google_translate.css?v=' | append: nowMillis }}" type="text/css">
  </head>
  <body>
    <nav id="sidebar">
      {% google_translate_html %}
    </nav>
  </body>
  {% google_translate_javascript %}
</html>
```

The above is usually incorporated into a layout, for example, `_layouts/default.html`.


## Development

After checking out this git repository, install dependencies by typing:

```shell
$ bin/setup
```

You should do the above before running Visual Studio Code.


### Run the Tests

```shell
$ bundle exec rake test
```


### Interactive Session

The following will allow you to experiment:

```shell
$ bin/console
```


### Local Installation

To install this gem onto your local machine, type:

```shell
$ bundle exec rake install
```


### To Release A New Version

To create a git tag for the new version, push git commits and tags,
and push the new version of the gem to https://rubygems.org, type:

```shell
$ bundle exec rake release
```


## Contributing

Bug reports and pull requests are welcome at https://github.com/mslinn/jekyll_google_translate.


## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
