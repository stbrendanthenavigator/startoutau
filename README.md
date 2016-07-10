# startoutau
StartOut Australia

Models
 - User
 - Message
 - Conversation
 - Article
 - Topic
 - Story

Contoller
 - Pages
   - Interfaces
     - home page
     - about us page
     - T&C page
     - privacy policy
     - code of conduct

Security considerations
- force SSL
- full audit log of every User interaction including IP address and values if creating or editing
- fully spec'd authorisation and authentication


Model details:

####User
### logic

* Users can have one of three roles (mentor, admin, moderator)
* these roles can only be assigned by an admin

### attributes

* name (full name of person)
* email (string)
* nickname (string)
* age (integer validation)
* passion (string)
* occupation
* about (string)
* avatar (image)

### associations

* has many Topics
* has many Stories
* has many Conversations
* has many Messages through Conversations
* has many Articles

### interfaces

* there will be multiple indexes
    * admins can see an index of all Users
    * everyone can see an index of all mentors (you can filter mentors by Topic)

