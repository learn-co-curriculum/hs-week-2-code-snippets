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

###Creating a new tweet - code snippet 2

This goes in `application_controller.rb`
```ruby
  post '/tweets' do
    Tweet.new(params[:username], params[:status])
    redirect '/tweets'
  end
```

###Setting up input fields - code snippet 3

This is your completed form with input fields
```
  <form action="/tweets" method="POST">
    <p>Username: <input type="text" name="username"></p>
    <p>Status: <input type="text" name="status"></p>
    <input class="btn btn-primary" type="submit">
  </form>
```
