# SkillSync 🚀  
*A Microservice-based Platform for Tracking Learning Progress and Collaborating with Like-minded Learners*

---

## ✅ Minimum Viable Product (MVP)

SkillSync empowers users to manage their skill development journey by offering goal tracking, collaboration suggestions, and progress monitoring.

### 🎯 Core Features
- User authentication and profile management
- Add, edit, and view skill profiles
- Set and update learning goals
- Track progress against goals
- Recommend collaborators with similar or complementary skills

---

## 🧩 Microservices Architecture

| Service | Responsibility |
|--------|----------------|
| **User Service** | Authentication & user profile management |
| **Skill Service** | CRUD operations for skills and suggestions |
| **Learning Tracker Service** | Goal creation & progress tracking |
| **Collab Recommendation Service** | Suggest users for collaboration based on skills |

---

## 📋 Requirements

### ✅ Functional Requirements
- **User Features**
  - Sign up / Login
  - Add skills with experience level
  - Set and track learning goals
  - View recommended collaborators
- **Admin Features**
  - View overall skill stats
  - Approve flagged content (optional moderation)

### 🔐 Non-Functional Requirements
- Role-based access control (RBAC)
- RESTful API design for frontend/backend separation
- Support for both **PostgreSQL** (you) and **MySQL** (friend)
- Profile switching via **Spring Profiles**
- Secure endpoints via **Spring Security + JWT**
- Efficient use of **Java 8+ Stream API**
- **Docker Compose** setup for local development *(bonus)*

---

## 🔌 API Endpoints

### 🧑 User Service

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/auth/signup` | Register a new user |
| `POST` | `/auth/login` | Authenticate and return JWT |
| `GET`  | `/users/{id}` | Get user profile |
| `PUT`  | `/users/{id}` | Update profile info |

---

### 📚 Skill Service

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET`  | `/skills` | List all skills |
| `POST` | `/skills` | Add a new skill |
| `GET`  | `/skills/{userId}` | List user's skills |
| `PUT`  | `/skills/{userId}/{skillId}` | Update skill level |
| `DELETE` | `/skills/{userId}/{skillId}` | Remove a skill |

---

### 📈 Learning Tracker Service

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/learning` | Add a learning goal |
| `GET`  | `/learning/{userId}` | View all goals for a user |
| `PUT`  | `/learning/{goalId}` | Update goal progress |
| `DELETE` | `/learning/{goalId}` | Delete a learning goal |

---

### 🤝 Collab Recommendation Service

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET`  | `/recommendations/{userId}` | Get recommended collaborators |
| `GET`  | `/collab/match?skill=Java&level=Intermediate` | Find users by skill and level |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Backend** | Spring Boot, Spring Core |
| **API Security** | Spring Security + JWT |
| **ORM & DB** | Spring Data JPA, PostgreSQL / MySQL |
| **Profile Management** | Spring Profiles |
| **Inter-Service Communication** | REST Template / FeignClient |

---

## 📦 Deployment (Bonus)

- Dockerized services
- Docker Compose for running all services locally
- Environment-specific configuration via Spring Profiles

---

## 👥 Contributing

We welcome contributions! Feel free to fork, raise issues, or submit pull requests.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
