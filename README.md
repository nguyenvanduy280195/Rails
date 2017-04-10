# Rails
Learning ruby on rails on https://www.railstutorial.org/book
## Shell



1. Creating new project
	```
    $ rails _5.0.1_ new toy_app
    ```
2. Clone the repo and install the needed gem
	```
    $ bundle install --without production
    ```
3. Run server
	```
    $ rails server
    ```
	or
	```
    $ rails server -b <IP> -p <PORT>
    ```

4. The Users resource
	```
    $ rails generate scaffold User name:string email:string
    ```
5. Migrating the database
	```
    $ rails db:migrate
    ```
6. Undo a single migration step using
	```
    $ rails db:rollback
    ```
7. To go all the way back to the beginning
	```
    $ rails db:migrate VERSION=0
    ```
8. Run the test
	```
    $ rails test
    ```
9. Generating a Static Pages controller
	```
    $ rails generate controller StaticPages home help
    ```
10. Destroying the Static Pages controller
	```
	$ rails destroy  controller StaticPages home help
    ```
11. 

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
3. The routes for the home and help actions in the Static Pages controller.
	```
	Rails.application.routes.draw do
  	  get  'static_pages/home'
  	  get  'static_pages/help'
  	  root 'application#hello'
	end
    ```
4. 

## *.irb
1. 

