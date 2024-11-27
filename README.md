Features
User Authentication:

Users can log in using a username and password.
On successful login, a JWT token is generated for the user.
Authorization:

JWT tokens are used to authenticate users and protect routes.
Each token includes user information (e.g., username, role) to verify access.
Role-Based Access Control (RBAC):

Roles like Admin, Moderator, and User control access to specific routes.
Decorators check user roles before granting access to endpoints.
API Endpoints:

/: Root endpoint, public.
/token: Generates a JWT token for authenticated users.
/admin/: Protected endpoint, accessible only by Admins.
/moderator/: Protected endpoint, accessible by Admins and Moderators.
/public/: Public endpoint, accessible by anyone.
Setup and Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/your-username/repository-name.git
cd repository-name
Create a Virtual Environment:

bash
Copy code
python -m venv venv
source venv/bin/activate       # On macOS/Linux
venv\Scripts\activate          # On Windows
Install Dependencies:

bash
Copy code
pip install -r requirements.txt
Run the Application:

bash
Copy code
uvicorn app.main:app --reload
Access the API:

Swagger UI: http://127.0.0.1:8000/docs
Redoc: http://127.0.0.1:8000/redoc
