ORMs and APIs

Python, as with other languages, uses Object-Oriented Programming (OOP).
An 'object' is a discrete item.

This type of programming allows us to create classes, which are generic forms of 
these objects.

Class example: 

      class Flight:

      def __init__(self, origin, destination, duration):
          self.origin = origin
          self.destination = destination
          self.duration = duration
          
__init__ is a method, which is a function performed on single objects. In this case, it describes what
should occur when a flight object is created. 

Methods usually take 'self' as their first argument, as it refers to THAT object being worked with.
The origin, destination, and duration here are just the info that should be stored about a certain
flight. This info is stored as properties inside the obhect (using dot notation).

OBJECT RELATIONAL MAPPING (ORM) - allows us to combine the OOP of Python and the relational
DB world of SQL. With ORM, classes, methods, and objects in Python are our tools for interacting 
with SQL DBs. The Flask-SQLAlchemy package can be used for this. 

- Relationships: A powerful aspect of ORM. Allows us to relate tables, and in a manner that allows them
to refer to each other. A relationship is set up with one line. In these examples, it would be added to the definition of the Fight class. 

      passengers = db.relationship("Passenger", backref="flight", lazy=True)
  
    --> passengers is a relationship, given the flight object, is can extract the passenger info for htat flight
    --> backref creates a relationship in the other direction, from Flight to Passenger.
    --> lazy tells us that the info should only be fetched when it's requested.

APIs (Application Programming Interfaces) is a protocol for comms between different web apps or between different components of the same web app. These components might want to perform actions or share info. Necessary, therefore, is a standard language for how this communcation will occur. 

  - JSON is one such language, meaning Javascript Object Notation, which is a simple method of representing info in a human and computer readable way, so that it can be passed between different parts of web apps. 
 
HTTP METHODS: 

      GET : retrieve a resource
      POST : create a new resource
      PUT : replace a resource
      PATCH : update a resource
      DELETE : delete a resource

CREATE AN API
- To implement an API, we just need to define a route that returns a JSON object. 

API KEYS
- With larger APIs, rate limiting is common. It is undesirable to have users making a large number of requests that might overload the API or make it harder for other users to access it. To restrict access, users must first obtain an API key (a long string) which must be provided with any API request. 
- Keys allow for the tracking of individual users only allowing, for example, 100 requests per hour per user.




