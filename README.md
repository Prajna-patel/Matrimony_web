# Django Matrimonial Platform - README

## Project Overview

### **Purpose**
This application serves as a **matrimonial platform** where users can:
- Sign up and create personal profiles
- Specify preferences for potential partners
- Interact with other users through **messaging and events**
- Utilize a matchmaking system based on **user-defined criteria**

## **Key Features**

### **1. User Registration and Authentication**
- Users can register by providing a **username, email, and password**.
- The application uses Django's **built-in authentication system** to manage user accounts securely.
- Email verification can be implemented to ensure authenticity.

### **2. Profile Management**
- Users create and manage a profile containing:
  - Bio, Location, Birth Date, Gender, Religion, Caste, Height, Education, Occupation, Income, Profile Picture
- Users can edit their profiles after registration.

### **3. Partner Preferences**
- Users can specify their preferences for potential matches, including:
  - Age range, Height range, Religion, Caste, Education Level, Occupation, and Location.

### **4. Messaging System**
- Users can send and receive messages.
- Messaging is restricted based on **profile preferences and gender compatibility**.

### **5. Event Management**
- Users can **create and participate** in events.
- Events contain **title, description, location, and date/time**.
- Other users can accept or reject event invitations.

### **6. Matchmaking Algorithm**
- A scoring system evaluates potential matches based on **user preferences and compatibility**.
- Considered factors include **age, height, religion, caste, education level, occupation, and location**.

### **7. WebSocket Integration for Real-Time Chat**
- Django Channels enable **real-time chat functionality**.
- Users can join **chat rooms based on events** or matchmaking criteria.

## **Technical Stack**
- **Django Framework** - Core backend framework
- **PostgreSQL Database** - Storing user data and application state
- **Django Channels** - Enables WebSocket support for real-time features
- **Django Forms** - Handles user input for forms such as signup and profile creation
- **Custom User Model** - Extends Django's default user model for additional features

## **Application Structure**

### **1. Models**
- **User** - Extends `AbstractUser`, includes email verification
- **Profile** - Stores user personal details
- **PartnerPreference** - Captures user-defined matching criteria
- **Message** - Represents messages exchanged between users
- **Event** - Represents user-created events
- **EventResponse** - Tracks user responses to events

### **2. Forms**
- **SignupForm** - Handles user registration
- **ProfileForm** - Handles profile creation/editing
- **PartnerPreferenceForm** - Manages user partner criteria
- **MessageForm** - Handles user messages
- **EventForm** - Manages event creation and participation

### **3. Views**
- Logic for rendering templates and processing form submissions.
- Includes views for:
  - **Signup** (`signup`)
  - **Login** (`login_view`)
  - **Profile Management** (`create_profile`)
  - **Messaging**
  - **Event Handling**

### **4. Templates**
- HTML templates for frontend rendering.
- Each **view** corresponds to a template displaying user-specific data.

### **5. URLs**
- URL routing managed through Django's **URL dispatcher**.

## **Security Considerations**
- **Password Hashing** - Securely stores user passwords using Django's built-in mechanisms.
- **CSRF Protection** - Implemented via Django middleware.

## **Deployment Instructions**
To deploy the application on another system:
1. **Set up PostgreSQL database**
2. **Install dependencies** using `requirements.txt`
3. **Configure environment variables** (database credentials, secret key, etc.)
4. **Run migrations** to set up the database schema
5. **Start the server** using Django's development server or a production-ready configuration

## **Conclusion**
This project encapsulates essential functionalities of **matrimonial services**, leveraging modern web development practices with Django. 🚀

