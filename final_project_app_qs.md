# SI 364 - Final Project questions

## Overall

* **What's a one-two sentence description of what your app will do?**

I would want to migrate my current skill mapping project from spreadsheet to database with views.

The Timeline would be:

Version 1: 
(Features: Account, Adding Skills with Levels and Classes, Delete Wrong Rows)

Version 2(Next Semester):
Figuring out the relationship between rows(skills) and columns(classes),sending e-mail, fancy CSS) 



## The Data

* **What data will your app use? From where will you get it? (e.g. scraping a site? what site? -- careful not to run it too much. An API? Which API?)**

I want to use Course API from https://api.umich.edu/node/171 just for basic schedule information rather than in-depth data points


* **What data will a user need to enter into a form?**


User will have to enter: Course Number, Skills for pre-reqs, Skills for outcomes

* **How many fields will your form have? What's an example of some data user might enter into it?**

Three fields with expanable items. 

Sample Data enter: 364, SQL, Python Immediate, 

* **After a user enters data into the form, what happens? Does that data help a user search for more data? Does that data get saved in a database? Does that determine what already-saved data the user should see?**

The data would be searched in existing databse and then saved in a database. 




* **What models will you have in your application?**

1. Class
(ID, Number, Pre-reqs(a list), and Outcomes(a list) 

2. Skills
(id, description)


3. Levels
(id, Foreign Key to Skills and Class, description

* **What fields will each model have?**

See Above

* **What uniqueness constraints will there be on each table? (e.g. can't add a song with the same title as an existing song)**


1.Cant add same course number with same skills.
2.Cant add skills without a course number 




* **What relationships will exist between the tables? What's a 1:many relationship between? What about a many:many relationship?**

there will be a 1:many relationship between Class and Skills
There will also be a 1:many relationship between skills and classes.

-> There will be a many:many relationship between classes and skills

There will be a 1:many relationship between skill to levels.


* **How many get_or_create functions will you need? In what order will you invoke them? Which one will need to invoke at least one of the others?**


Three get_or_create function. 

The order will be Class -> Skills- > Leves. 

Skill and Levek would invoke class. 



## The Pages

* **How many pages (routes) will your application have?**


One Page for Form

One Page for View Class

One Page For Class Details

One Page Reserved For Others


* **How many different views will a user be able to see, NOT counting errors?**

3 Views:
1. Form 
2. Class,
3. Skills


* **Basically, what will a user see on each page / at each route? Will it change depending on something else -- e.g. they see a form if they haven't submitted anything, but they see a list of things if they have?**

## Extras

* **Why might your application send email?**

In order to remind people that their course has been changed, but I might not implement it. 


* **If you plan to have user accounts, what information will be specific to a user account? What can you only see if you're logged in? What will you see if you're not logged in -- anything?**

When a user is logged in, he/she can see the information he added. 
Otherwise, can only see a secured page


* **What are your biggest concerns about the process of building this application?**

I have some more questions regarding the relationships between the skills and levels on more complicated stuff. I will visit Jackie/Mauli's office hour for more details. 