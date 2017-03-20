## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET - gets the infromation displayed to the user
  * POST - posts information from the user to the database
  * PUT - edits a record in the database using information supplied by the user
  * PATCH - edits a record in the database using informatin supplid by the user
  * DELETE - Allows user to delete a record from the database
  
2. What is Sinatra?
  * Sinatra is a web framework for Ruby.
  
4. What is MVC?
  * MVC stands for Model, View, Controller. Combined with a browser and a database, A complete CRUD application can be mapped out.
  
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  *  ? Something to do with CRUD and how Sinatra traverses our folder structure
  
6. What types of variables are accessible in our view templates without explicitly passing them?
  * Instance variables.
  
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = Horse.count
    :locals => {:name => 'Mr. Ed'}
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

9. What's the purpose of ERB?
  * ERB allows ruby code to be run and evaluate within HTML.
  
10. Why do I need a development AND test database?
 * need different configs for each
  * Having a test database allows for a sandbox for testing. If you neeed to wipe this database and start over, that isnt a problem. By separating test and development, development is able to remain a closer version to production.
  
11. What's responsive design?
  * Respnosive design is a technique to design a very intuitive website for optimal use. 

12. What is CRUD and why is it important?
  * CRUD is a convention for web applications. A CRUD web application allows for Creating, Reading, Updating, and Deleting records in its associated database.
  
13. What does HTTP stand for? 
  * HyperTextTranserProtocol
  
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  
  * <% ruby_code %> ruby code will evaluate but the result will not be displayed
  * <%= ruby_code %> ruby code will evalute and then the result will be displayed
  
15. What's an ORM?
  * An Object Relational Mapper is a tool used to allow for communication between database and ruby code (model)
  
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * Active Record
  
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  * GET '/' --> Homepage
  * GET '/restaurants' --> View all restaurants
  * GET '/restaurants/:id' --> View individual restaurant
  * GET 'restaurants/new' --> Create new restaurant
  * POST '/restaurants' --> Add new restaurant to database
  * PUT '/restaurants/:id --> Edit individual restaurant
  * DELETE '/restaurants' --> Delete restaurant
  
18. What's a migration? 
  * A migration adds a table to your database
  
19. When you create a migration, does it automatically modify your database?
  * Yes, it adds a new table to it.
  
20. How does a model relate to a database?
  * A model is how the connection between different database tables is maintained. Additionally, a class in the model represents  the class of each of rows in a table in the database.
  
21. What's the difference between agile workflow and waterfall method?
  * Agile workflow develops a product in small incremental stages. Waterfall method plans the entire project out start to finish. It is then built to those specs.
  
22. What is the difference between `#new` and `#create`?
  * `#new` creates a new instance in the database but it isnt saved. `#create` creates a new instance and saves it to the database.
