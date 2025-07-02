Team Roles:

Discovery/PoC :
Product owner (usually on the client’s side), project manager, business analyst, UI/UX designer, and at least one software developer, depending on the complexity of a PoC.

MVP development :
Product owner (usually on the client’s side), project manager, business analyst, UI/UX designer, software engineers, test engineers

Product development :
Product owner (usually on the client’s side), project manager, business analyst, UI/UX designer, software architect, software engineers, test engineers.

Optionally: test automation engineers, performance engineers, DevOps engineers, security engineers



Technology Stack:

Django: A high-level Python web framework used to build secure and scalable RESTful APIs.

PostgreSQL: A powerful open-source relational database for storing and managing project data.

GraphQL: A query language for APIs that allows clients to request exactly the data they need.

Docker: Used to containerize the application for consistent development and deployment environments.

Nginx: A web server used for serving static files and as a reverse proxy for the application.

Git & GitHub: Version control and collaboration tools to manage project code and track changes.



Database Design:


Entities & Key Fields
User

id: Unique identifier

name: Full name of the user

email: User’s email address

password: Hashed password

role: Defines if user is a guest or host

Property

id: Unique identifier

title: Property name or title

description: Details about the property

location: Address or area

owner_id: References the User who owns it

Booking

id: Unique identifier

user_id: References the guest who booked

property_id: References the booked property

start_date: Booking start

end_date: Booking end

Review

id: Unique identifier

user_id: Reviewer’s ID

property_id: Reviewed property ID

rating: Score (e.g., 1-5)

comment: Optional review text

Payment

id: Unique identifier

booking_id: Linked booking

amount: Payment total

status: e.g., Paid, Pending, Failed

method: e.g., Credit Card, PayPal
