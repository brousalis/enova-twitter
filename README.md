```
TODO: slides on basic html/css
```
```
gem install rails
rails new twitter
git init
rbenv local 2.0.0-p248
bundle
```
```
gem install powify
pow create
	pow server restart
	pow browse
	pow logs
vim Gemfile
	haml
normalize-rails 	
bootstrap-sass
	development:
		thin
		quiet assets
		guard-livereload, require: false
		rack-livereload
bundle
powsr
```
```
vim app/controllers/site_controller.rb 
class sitecontroller < applicationcontroller
vim config/routes.rb 
root to: ‘site#index’
mkdir app/views/site
vim app/views/site/index.html.haml
testing
pow browse
```
```
be guard guard init
vim Guardfile
	remove all but live-reload
vim config/env/dev.rb 
config.middleware.use Rack::LiveReload
powsr
be guard
```
```
mv layouts/app.html.erb to app.html.haml
mv stylesheets/app.css to app.css.scss
bundle 
powsr
```
```
vim stylesheets/variables.css.scss
vim stylesheets/mixins.css.scss
mkdir stylesheets/common
mkdir stylesheets/pages
setup app.css
cp $(bundle show bootstrap-sass)/vendor/assets/stylesheets/bootstrap.scss 
app/assets/stylesheets/bootstrap-custom.scss
```
```
explain container
#page{class: controller_name}
explain partials
explain how to break apart topbar
mock up navbar in html
show using inspect elements what it looks like
create common/navbar.css.scss
explain pull-right, common. use on navbar
style logo basic
create common/icon.css.scss
work on navbar .nav, introduce variables
introduce shorthand with padding
work on icons, show span.icon
explain image asset pipeline
add font-awesome
explain icon font
align icon and font-size 
brand primary, link color variables
tighten nav, color, padding
add navbar border-bottom, explain rgba
center logo, resize
style searchbar
style secondary list, one icon, then button
create basic button styles, primary/secondary
position fixed navbar
explain z-index
padding on body
```
move to content





