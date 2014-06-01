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


