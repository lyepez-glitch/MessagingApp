Real-Time Chat Application
A real-time web chat app built with Django, Django Channels, WebSockets, HTML, and CSS. This app enables multiple users to communicate instantly in dedicated chat rooms.

Table of Contents
Features
Tech Stack
Installation
Usage
Project Structure
Contributing
License
Features
Instant Messaging: Real-time updates via WebSockets.
User Authentication: Sign-up, login, and logout functionalities.
Multiple Chat Rooms: Users can create or join chat rooms.
Persistent Chat History: Stores messages to allow users to view past conversations.
Responsive Design: Optimized for both desktop and mobile devices.
Tech Stack
Backend: Django, Django Channels
Frontend: HTML, CSS, JavaScript
Database: SQLite (default), PostgreSQL (production)
WebSockets: Django Channels with Redis channel layer (production)
Asynchronous Server: ASGI
Installation
Prerequisites
Python 3.7+
Redis (for the channel layer in production)
Steps
Clone the repository:

bash
Copy code
git clone https://github.com/lyepez-glitch/MessagingApp.git
cd MessagingApp
Set up a virtual environment:

bash
Copy code
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install required packages:

bash
Copy code
pip install -r requirements.txt
Configure environment variables:

Create a .env file in the project root and add necessary configurations (e.g., SECRET_KEY, DEBUG).
Ensure Redis is running locally, or update the channel layer configuration to point to your Redis server URL.
Run migrations:

bash
Copy code
python manage.py migrate
Create a superuser:

bash
Copy code
python manage.py createsuperuser
Start the development server:

bash
Copy code
python manage.py runserver
Access the app: Visit http://127.0.0.1:8000/ in your browser.
Access the Live App:

To see the chat app in action, visit https://lyep.pythonanywhere.com/rooms/ in your browser.


Usage
Sign Up or Login: Create an account or log in to an existing one.
Join or Create Chat Rooms: Find existing rooms or create a new one.
Chat in Real-Time: Send messages and interact with other users in the chat room.
Project Structure
plaintext
Copy code
MessagingApp/
├── messaging/                 # Django app for chat functionality
│   ├── templates/             # HTML templates
│   ├── static/                # Static files (CSS, JS)
│   ├── consumers.py           # WebSocket consumers for handling events
│   ├── routing.py             # Channels routing configuration
│   └── views.py               # Views for rendering chat pages
├── config/
│   ├── settings.py            # Project settings
│   ├── asgi.py                # ASGI configuration for Channels
│   └── urls.py                # URL configuration
├── manage.py
└── README.md
Contributing
Fork the project.
Create a feature branch:
bash
Copy code
git checkout -b feature-name
Commit changes:
bash
Copy code
git commit -m 'Add feature name'
Push to branch:
bash
Copy code
git push origin feature-name
Open a pull request.
For more information, visit the GitHub repository.






