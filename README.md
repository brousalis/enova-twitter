### setting up basic app
```
gem install rails on system
rails new twitter
git init
rbenv local 2.0.0-p248
bundle
```
### installing some useful dev gems
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
### basic index route 
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
### live reload on code changes 
```
be guard guard init
vim Guardfile
	remove all but live-reload
vim config/env/dev.rb 
  config.middleware.use Rack::LiveReload
powsr
be guard
```
### setup file structure 
```
mv layouts/app.html.erb to app.html.haml
mv stylesheets/app.css to app.css.scss
show conversion
vim stylesheets/variables.css.scss
vim stylesheets/mixins.css.scss
mkdir stylesheets/common
mkdir stylesheets/pages
setup app.css
cp $(bundle show bootstrap-sass)/vendor/assets/stylesheets/bootstrap.scss app/assets/stylesheets/bootstrap-custom.scss
```
### break down site 
```
explain container, how to break down site on whiteboard
create container #page{class: controller_name}
explain partials
vim layouts/_navbar.html.haml
explain how to break apart navbar verbially
mock up navbar in html
show using inspect elements what it looks like
explain guess and checking

vim common/_navbar.css.scss
explain pull-right, common folder . 
vim common/_utility.css.scss
use on navbar

work on navbar .nav, introduce variables with height $navbar-height
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
  explain input ending with /
  background, rounding, positioning
  add icon to search, padding to right
  add focus interaction
  add animation

style secondary list
  add right-actions class
  proper spacing
  color of icons
  add hover style, explain difference between on a/i

add button styles
  fix spacing by adding margin
  add basic buttons to index page to show link_to
  add hover style

position fixed navbar
explain z-index
padding on body
height 9000 on body
remove container padding
```
```
let them implement profile_navbar
vim layouts/_profile_navbar.html.haml
add to app.haml
vim stylesheets/_navbar.css.scss
extend .navbar
top: $navbar-height
style .nav
  add $profile-navbar-height
  style value
  fix more button
  fix issue with icon 
  global link decoration
```
```
discuss how grids work
break into xs-3 and xs-9
add avatar html/class, image into avatar
add body background color
position relative on profile_navbar
add more margin top profile_navbar
style avatar
  display inline block vs block
  explain box-shadow and border combo
  explain border radius adjustment
wrap with profile-avatar for positioning
```
```
add user-actions, button and btn-secondary
make profile .nav width 100%
add user-actions to position right
style btn-secondary
  use linear-gradient
style btn-icon
align buttons
remove hover on more and user-actions
```
```
vim layouts/_profile_hero.html.haml
vim pages/profile.css.scss
move profile-navbar into profile
background-image, height 500px 
