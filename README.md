This is a simple CRUD (Create, Read, Update, Delete) application (Task Manager) powered by open-source Ruby on Rails web application framework. This Application works based on the principle of MVC(Model-View-Controller) pattern, in-fact Rails framework itself follows the MVC architecture. 

To run the application on local server following commands are needed before running:

1.	$ bundle install
2.	$ rails db:migrate
3.	$ rails db:seed
4.	$ rails server

Now hit http://localhost:3000 on your favorite browser, you are supposed to see the home page of the application. Make sure you have everything (ruby, ruby on rails and other required gems) installed on your local computer. The home page URL is set to root URL of the application which triggers the index Action of the TasksController through the routing mechanism resulting 'index.html.erb' page on the browser (MVC pattern) as html format. Now you are supposed to see the listing of all available task. If you click on the click button of the Details column (right side of the table) you will see the full details of that specific task. When you click the click button(a link basically) the show method of the Controller (TasksController) is triggered which is responsible for presenting ‘show.html.erb’ view on the browser as html format. During the execution of show method an id parameter of that specific task is passed which pulls out the required information from the database using the Active Record (ORM framework for rails). You can also create a new task using “Create a new task” button(bottom of the home page) or New task on navbar. When you attempt to create a new task a method named “new” is triggered on TasksController which renders a form for the object of Task model and eventually hitting on submit (create) button with required information results to save the model objects on the database by triggering create action of the controller. Here you cannot submit a blank form as the form validation is performed by using ‘validates’ method on the model ‘Task’. ‘Edit’ and ‘Update’ (corresponding ‘edit’ and ‘update’ actions in the controller) operations are almost same as ‘new’ and ‘create’ except we pass an id parameter of the task we want to edit. To delete an object we just call the ‘destroy’ action of the controller and it performs the deletion of the specific object. In the TaskController two private methods ‘set_task’ and ‘task_params’ are used which are responsible for finding the specific task and supply the required parameters of a model object to be saved or edited (on database) respectively, these methods are called with before_action call back applicable to appropriate methods.

The detail documentation can be found on the following link:
https://drive.google.com/file/d/0B2cQFVa6QaCCcTlrN1o0SVVTNU0/view?usp=sharing

Live link: https://rocky-castle-24996.herokuapp.com/

That’s all the basic working principle of this CRUD application (task_manager).

Contact: Email: ahrony90@gmail.com, skype- eee.ahsan

Copyright © 2017 Md. Ahsanul Hoque,
