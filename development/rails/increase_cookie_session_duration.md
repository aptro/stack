# Increase cookie session duration

1. Add expiration to `config/initializer/session_store.rb`. Create the file if not present.

```rb
Rails.application.config.session_store :cookie_store, expire_after: 100.days, key: '_project_name_session'
```
