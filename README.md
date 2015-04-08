---
tags: forms, kids, ruby, advanced, code snippets
language: ruby
level: 2
type: code snippets
---

##FORMS!

###Setting up a form - code snippet 1

This goes in `tweets.erb`
```
  <form action="/tweets" method="POST">

  </form>
```

###Setting up a get route in our application controller - code snippet 2

This goes in `application_controller.rb`
```ruby
  get '/tweets' do

  end
```

###Setting up a post route in our application controller - code snippet 3

This goes in `application_controller.rb`
```ruby
  post '/tweets' do

  end
```

###Setting up input fields - code snippet 4

This is your completed form with input fields
```
  <form action="/tweets" method="POST">
    <p>Username: <input type="text" name="username"></p>
    <p>Status: <input type="text" name="status"></p>
    <input class="btn btn-primary" type="submit">
  </form>
```

###Checking out the params hash - code snippet 5

This goes in `application_controller.rb`
```ruby
  post '/tweets' do
    puts params
    binding.pry
  end
```

###Creating a new tweet in our controller - code snippet 6

```ruby
  post '/tweets' do
    Tweet.new(params[:username], params[:status])
    redirect '/'
  end
```
