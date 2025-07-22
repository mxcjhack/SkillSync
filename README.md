# SkillSync
Microservice based platform for tracking their learning progress.


✅ MVP (Minimum Viable Product)
Core Features:
1.	User authentication and profile management
2.	Add/edit/view skill profiles
3.	Create and update learning goals
4.	Track progress against learning goals
5.	Recommend collaborators with overlapping or complementary skillsets
Microservices:
1.	User Service – Authentication, profile
2.	Skill Service – CRUD for skills, suggestions
3.	Learning Tracker Service – Learning goals, progress tracking
4.	Collab Recommendation Service – Suggest collaborators
________________________________________
📋 Requirements
Functional
•	Signup/Login (Spring Security + JWT)
•	User can:
o	Add their current skills and experience level
o	Add learning goals
o	Track learning progress
o	See recommended collaborators
•	Admin users can:
o	View overall skill stats
o	Approve flagged content (optional moderation feature)
Non-Functional
•	Role-based access control
•	RESTful APIs for frontend/backend separation
•	PostgreSQL (you) and MySQL (friend) support
•	Profile switching via Spring Profiles
•	Secure APIs via Spring Security
•	Proper use of Java 8+ Stream API for filtering/mapping skills and progress
•	Docker Compose for multi-container environment (bonus)
________________________________________
🔌 APIs Needed
🧑 User Service
Method	Endpoint	Description
POST	/auth/signup	Register user
POST	/auth/login	Authenticate user, return JWT
GET	/users/{id}	Get user profile
PUT	/users/{id}	Update profile info
________________________________________
📚 Skill Service
Method	Endpoint	Description
GET	/skills	List all skills
POST	/skills	Add new skill
GET	/skills/{userId}	List user's skills
PUT	/skills/{userId}/{skillId}	Update skill level
DELETE	/skills/{userId}/{skillId}	Remove a skill
________________________________________
📈 Learning Tracker Service
Method	Endpoint	Description
POST	/learning	Add a learning goal
GET	/learning/{userId}	View all goals for a user
PUT	/learning/{goalId}	Update goal progress
DELETE	/learning/{goalId}	Delete a goal
________________________________________
🤝 Collab Recommendation Service
Method	Endpoint	Description
GET	/recommendations/{userId}	Get recommended collaborators
GET	/collab/match?skill=Java&level=Intermediate	Find users with this skill level
________________________________________
🛠️ Technologies
Layer	Tech Stack
Backend	Spring Boot, Spring Core
API Security	Spring Security + JWT
ORM & DB	Spring Data JPA, PostgreSQL (you), MySQL (friend)
Profile Mgmt	Spring Profiles
Inter-Service	REST Template / FeignClient (for microservices)

