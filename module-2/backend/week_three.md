## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
* rails new app_name

2. What do Models generally inherit from in rails?
* ActiveRecord::Base

3. What do Controllers generally inherit from in a rails project?
* ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
* resources :horses, only: [:show]  OR  get '/horses/:id' => 'horses#show'

5. What rake task is useful when looking at routes, and what information does it give you?
* rake routes. It provides information for route helpers, verb, controller#action info and URL infromation for each route.

6. What is an example of a route helper? When would you use them?
* horses_path is an example of a route helper. They are used to move within your application. A common use is in conjunction with a redirect in the controller. 

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* _path is relative while _url is the whole URL path.

8. What are strong params and why are the necessary?
* Strong params are defined privately in a controller. They are used when inserting anytihng into the database. The reason we use them is to be very explicit with the parameters we acept form building new database objects. By using strong params we can ensure no additional params, perhaps some injected with mal intent, will be used when adding new objects to our database.

9. What role does `form_for` play in helping us create our forms?
* form_for sends a new request to the routes.rb in the form of a POST request. This includes all the info collected by the form to be posted. 

10. How does `form_for` know where to submit the user's input?
* It knows where to submit the user's input based on the object that is passed into it. From this object, it can decipher which path to post to.

11. Create a form using a `form_for` helper to create a new `Horse`. 
`
form_for @horse do |f|
  f.label :name
  f.text_field :name
  
  f.label :age
  f.text_field :age
  
  f.submit
end
`

12. Why do we want to validate our models?
* we want to validate our models to ensure that we are receiving all of the necessary information form the user in order to create an new object in our database.
