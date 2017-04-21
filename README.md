# Rails
Learning ruby on rails on https://www.railstutorial.org/book
## Shell


### bundle
    
    $ bundle install
    
### bin/rails

1. Create a new project
	```
    $ rails _5.0.1_ new toy_app
    ```
    
2. Run server
	```
    $ rails server
    $ rails server -b <IP> -p <PORT>
    ```

3. Genarate

	3.1. controller + view + model
    ```
    $ rails generate scaffold User name:string email:string
    ```
    3.2. controller
    ```
    $ rails generate controller StaticPages home help
    # controller:	StaticPages
    # action:		home
    # action:		help
    ```
    3.3.
    
4. Migrate

	4.1. Migrating the database
    ```
    $ rails db:migrate
    ```
    4.2. Undo a single migration step using
    ```
    $ rails db:rollback
    ```
    4.3. To go all the way back to the beginning
	```
    $ rails db:migrate VERSION=0
    ```
    
5. Test

	5.1. Run the test
    ```
    $ rails test
    ```

6. Destroy

	6.1.
	```
	$ rails destroy controller StaticPages home help
    ```
    
    6.2.
    ```
    $ rails destroy model User
    ```
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
      validates :content, length: {maximum: 100}, presence: true
      #length: {maximum: 100}	-> length maximum 100
      #presence: true			-> Name cant be blank
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
4. Associations between different data models

	*app/models/user.rb*
    ```
    class User < ApplicationRecord
      has_many :microposts
    end
    ```
    
    *app/models/micropost.rb*
    ```
    class Micropost < ApplicationRecord
      belongs_to :user
	  validates :content, length: { maximum: 140 }
	end
    ```

## *.erb
1. 

