# Twitter Bootstrap for Rails 3 & 4
Make [Twitter Bootstrap](http://twitter.github.com/bootstrap) into Rails Engine. [Bootstrap-datepicker](https://github.com/eternicode/bootstrap-datepicker) is also included.

## Version
* Bootstrap 3.0.0rc2
* Bootstrap-datepicker 1.2.0rc1

### Older Versions

For Bootstrap 2.3.x, try [2.3 branch](https://github.com/yjchen/bootstrap-rails-engine/tree/2.3) or gem version around 2.3.x.x.

## Rails 3.1 or later
Include Gemfile,

    gem 'bootstrap-rails-engine'

Add stylesheets into application.css

    *= require bootstrap/bootstrap
    *= require bootstrap/bootstrap-responsive

Add javascripts into application.js

    //= require bootstrap/bootstrap

## CDN

This gem supports cdn the same as [jquery-rails-cdn](https://github.com/yjchen/jquery-rails-cdn). In the application layout, add

    = bootstrap_javascript_include_tag :default

and 

    = bootstrap_stylesheet_include_tag :default

then remove corresponding lines in application.js and application.css.

If you use [font-awesome-rails](https://github.com/bokmann/font-awesome-rails), you can also use fontawesome_stylesheet_inclue_tag for CDN.

### Options

Set :compressed to use minimized library locally like this:

    = bootstrap_javascript_include_tag :default, :compressed => true

Set :local_copy true to use local copy when CDN is not available.

Remember to add assets name in confign/environments/production.rb:

    config.assets.precompile += %w( bootstrap/bootstrap.min.js)

## ISSUES

If you happen to use [bootstrap-sass](https://github.com/thomas-mcdonald/bootstrap-sass), which might be included from rails_admin, it will be used first, thus, you might have problem using stylesheet from this gem. Use CDN instead.

## License

Copyright (c) 2012-2013 Yen-Ju Chen

MIT License

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
