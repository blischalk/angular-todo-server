angular-todo-server
===================

This is an api app utilizing rails to serve as a backend for angular-todo-client app.

Notes:

- To get this to work I have had to add the https://github.com/cyu/rack-cors gem
- Rails has been configured to utilize CORS:

```ruby
config.middleware.use Rack::Cors do
  allow do
    origins '*' 
    resource '*', :headers => :any, :methods => [:get, :post, :put, :patch, :delete :options]
  end 
end
```

- To test locally, rails needs to be started on port 80 using: rvmsudo rails s -p 80
- Hosts file needs to be setup to map domain used by client app routes to this app
