# Setting up semantic-ui

## 1. Install the fomantic-ui-sass package via gem

```js
gem 'jquery-rails'
gem 'fomantic-ui-sass' #add to your Gemfile

bundle install
```

## 2. Setup CSS pipeline

import semantic-ui as up as possible in app/assets/stylesheets/application.scss

```css
@import "semantic-ui";
```

## 3.  Setup JS

If its a new rails project, then create the app/assets/javascripts/application.js file. 
Add the js dependencies for semantic-ui

```js
// ...
//= require jquery
//= require semantic-ui
```

Update app/assets/config/manifest.js to link the newly created app/assets/javascripts folder. Add this line at top of the manifest file.

```js
//= link_directory ../javascripts .js
```

### 4. Update layouts

By default rails 6 doesn’t load the Javascript files under the app/assets folder to layout. 
Add this tag to the header in app/views/layout/application.html.erb.

```erb
<%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>
```

### 5. Making semantic-ui responsive on mobile devices

Add the viewport meta tag to the header in app/views/layout/application.html.erb

```erb
<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1">
```
