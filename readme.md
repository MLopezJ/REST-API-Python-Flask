# Basic Blog Application with Python and Flask 

This is a simple app created with Python and Flask. The app let the users:
* Register into it
* Log in
* Create post
* Edit their posts 
* Delete their posts

It use an virtual enviroment, in that way the app manage the dependencies without affect or be affected for others projects' dependencies. 


For the develoment of this project, I'm following the suggested tutorial in the Flask documentation (https://flask.palletsprojects.com/en/1.1.x/tutorial/).


## Notes

### Factory method pattern
Is a pattern using for create objects. And its about to use a fuction to create instances of a class hiding the details for the client of that function, so, it is a interface for the creation of objects.  


### Blueprints
Is a template for generating a "section" of an app, like a "mold". 

### Decorator
A decorator is a function how takes another function and extends the behavior of the latter function without modifying it explicitly. It allow the calling of higher-order functions (similar to higher-order components, in React). They can be used for create middlewares. 

### Templates 
Are files who can contains static or dynamic data. For example, a html doc. 


In python, functions are first-class objects. It means there are no restrictions on the object's use, it can be dynamically created, destroyed, passed to a function and returned as a value and still have all the rights. But actually,  