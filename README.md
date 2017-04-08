# Rails

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

## *.irb
1. 

