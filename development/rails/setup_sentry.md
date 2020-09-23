# Setting up Sentry

1. Installation
Install the SDK via Rubygems by adding it to your Gemfile:

```rb
gem "sentry-raven"
```

2. In your config/application.rb:

```rb
config.filter_parameters << :password
```

3. Configuration

Create config/sentry.rb and configure the DSN, and any other settings you need:

```rb
Raven.configure do |config|
  config.dsn = 'https://xyz@abc.ingest.sentry.io/jkl'
  config.sanitize_fields = Rails.application.config.filter_parameters.map(&:to_s)
end
```

4. Setup params and sessions. Add before action and request metadata in `/app/controllers/application_controller.rb`

```rb
class ApplicationController < ActionController::Base
  before_action :set_raven_context

  private

  def set_raven_context
    Raven.user_context(id: session[:current_user_id]) # or anything else in session
    Raven.extra_context(params: params.to_unsafe_h, url: request.url)
  end
end
```

5. Test an exception, commit and deploy the code.