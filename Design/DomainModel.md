![Domain_Model](/Design/Domain_Model.png)

* ***User:***
The User class is the base for each of the accounts offered by EVE. The member and sponsor classes will come from this directly and is what will be used when someone new wants to join.
* **Member:**
This class will be used mainly by entrepreneurs wanting to grow their business and plan to look at sponsor content
* **Sponsor:**
This class makes up the base of users that will be providing content for members to interact with.
* **Admin:**
This class is important because it will handle all the posts by the sponsors. The admin class will make sure the users do not violate company policy in any way.
* ***Post:***
The post class serves as a place to put the content that the posts will have. This class is necessary because this will be what the User is primarily going to be looking at.
* **Blog Post:**
This class will contain all the blogs uploaded by sponsors. This class will distinguish video posts from blog posts.
* **Video Post:**
This class will contain all the videos uploaded by the sponsors. This is important because it will let the users easily find videos they want to see in video posts. 
* ***Comments:***
This class will let the users communicate with each other by commenting. This is important because this will be one of the only ways that a member and a sponsor can interact using our platform.
* **Sponsor Package:**
The sponsor package class will contain details about the sponsor’s specific package they chose. This is important because to make any post, you must have a sponsor package first.