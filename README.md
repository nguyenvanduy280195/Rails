# Rails
Learning ruby on rails on https://www.railstutorial.org/book
## Shell

1. Run server
	`rails server`
	or
	`rails server -b <IP> -p <PORT>`

2. Creating new project
	`rails _5.0.1_ new toy_app`
3. The Users resource
	`rails generate scaffold User name:string email:string`
4. Migrating the database
`rails db:migrate`

## *.rb

1. Changing controller#action
	*config/routes.rb*
	```
	Rails.application.routes.draw do
      resources :users
      root 'users#index'
    end
    ```
2. Validation
	*app/models/micropost.rb*
    ```
    class micropost < ApplicationRecord
      validates :content, length: {maximum: 100}
    end
    ```

## *.irb
1. 

