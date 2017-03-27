## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
* ActiveRecord is an object relational mapper and it allows your models in your application to interact with your database.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

* You can call, create, save, and new  in order to create new instances of Team in the database.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team? 
* Owner.find4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
* team = Team.find_by(id: 4)
* team.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* The relationship will be many to many, linked together through and additional table named student_teachers
6. Define foreign key, primary key, and schema.
* Student Primary Key: id
* Student Foriegn Key: student_teachers_id
* Teacher Primary Key: id
* Teacher Primary Key: student_teachers_id
* student_teachers Primary Key: id
* student_teachers will have two columns one dedicated to teacher_id another dedicated to student_id

7. Describe the relationship between a foreign key on one table and a primary key on another table.
* A foriegn key on one table is the primary key of another, if the relationship is set up correctly.

8. What are the parts of an HTTP response?
* A HTTP request is sent to the routes.rb, then this is sent to the appropriate controller. Controller interfaces with the model which in turn queries the database. Model returns this infor to a view which is rendered for the client. The last step being the response.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
