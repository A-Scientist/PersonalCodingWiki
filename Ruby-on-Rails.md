[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Ruby)

## Commands

**console** or **c**<br>
Opens the rails console where commands can be given, such as the creation of databases or tables in a database or items in a table.<br>
For example... 
```
Users.create(username:"user",password:"user")
DatabaseName.create(columnName:data,)
```
<br>

**server** or **s**<br>
Creates the rails server that can be accessed from http://localhost:3000/<br>

**rails.db:migrate:redo**<br>
Updates any changes made to a database from the backend.<br>

To add<br>
**test \_\_**<br>
**generate**<br>
**db:create**<br>
**routes**<br>
**dbconsole**<br>
**new app_name**<br>

## Patterns

### Relationships between Routes and Controllers and Views
The file routes.rb takes a URL request and finds(needs explanation) the correct page to serve. When it does, it sends a request, in the form of "pages#pagename", to the appropriate controller, where "pages" is both the name of the controller and the folder that holds the pages, a hash, and then "pagename" which is the name of both the method in the controller and name of the .html.erb page.

```
myApp
	app
		controllers
			mypages_controller.rb
		views
			mypages
				myWebPage.html.erb
	config
		routes.rb
```

```
mypages_controller.rb
	class PagesController < ApplicationController
		def mainpage
		end
  	end
```
```
myWebPage.html.erb
	<h1> Hello World<h1>
```
```
routes.rb
	Rails.application.routes.draw do
  		root to: 'pages#mainpage'
	end
```
<br>
creating a user object<br>
```
railsdb:migrate
rails console --sandbox
user.all
aUser = User.new(username: 'tom', password: 'yellow', role: 'human')
aUser.save
ctrl d
User.create(username: "frank", password: "blue", role: "sheep")
```

### Creating a default main page<br>
Involves setting up a directory in app/views to hold an html page, adding a new controllers.rb file in app/controllers, and changing routes.rb in config to match.<br>
Primary: https://davidpots.com/rails/tutorial/development/2013/03/19/rails-basics-setting-up-a-homepage.html<br>
Secondary: https://guides.rubyonrails.org/routing.html#the-purpose-of-the-rails-router<br>

### Flash messages
You can use this code inside your controller actions, like index, create, new, etc. It will create a message that will be caught and displayed on the next page that is sent provided that it is caught and used.<br>
`flash.alert = "User not found."`<br>
`flash[:alert] = "User not found."`<br>
This version redirects and sends a message in the same line.<br>
`redirect_to :books_path, notice: "Book not found"`<br>
This code can be used to catch and display a message within a page.<br>
```
<% flash.each do |type, msg| %>
  <%= msg %>
<% end %>
```
Resources used https://www.rubyguides.com/2019/11/rails-flash-messages/<br>