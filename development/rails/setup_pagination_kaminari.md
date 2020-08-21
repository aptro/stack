# Setup pagination with Kaminari

Kaminari lets you paginate list views in rails with few lines of configuration.

The good part, it integrates with the existing list views with minimal changes.

The documentation from kaminari is exhaustive and error-free.

## Setting up kaminari with the Semantic-UI theme

### 1.  Add to Gemfile

```ruby
gem 'kaminari'
```

### 2. Configure kaminari as an initializer

create `/config/initializers/kaminari_config.rb`

```ruby
# frozen_string_literal: true

Kaminari.configure do |config|
    config.default_per_page = 10
    # config.max_per_page = nil
    # config.window = 4
    # config.outer_window = 0
    # config.left = 0
    # config.right = 0
    # config.page_method_name = :page
    # config.param_name = :page
    # config.max_pages = nil
    # config.params_on_first_page = false
  end
```

### 3. Activate Semantic-UI theme

```sh
rails g kaminari:views semantic_ui
```
