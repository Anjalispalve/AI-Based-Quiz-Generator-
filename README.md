# AI-Based-Quiz-Generator-
**Use Case:** Generate quiz questions and answers based on a given topic. **Steps:** 1. Input a topic or subject. 2. Send to ChatGPT API with a quiz generation prompt. 3. Save topic, questions, and answers in a database. 4. Display the quiz. **Prompt Example:** Generate 5 quiz questions with answers about: [Topic].
MyQuizProject
MyQuizProject is a Django-based web application that generates quiz questions and answers based on a given topic using OpenAI's API.

Features
Users can input a topic to generate quiz questions.
AI-powered question and answer generation.
Saves quizzes to a database for future reference.
Pagination support for better quiz navigation.
Simple UI for answering quizzes and submitting responses.
Admin panel for managing quizzes.
Installation & Setup
1. Clone the Repository

git clone https://github.com/your-repo/myquizproject.git
cd myquizproject
2. Create a Virtual Environment

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
3. Install Dependencies

pip install -r requirements.txt
4. Configure the Database

python manage.py migrate
5. Create a Superuser (Optional)

python manage.py createsuperuser
6. Run the Server

python manage.py runserver
Visit http://127.0.0.1:8000/ in your browser.

Project Structure

myquizproject/
│── quizapp/                 # Main quiz application
│   │── migrations/          # Database migrations
│   │── templates/           # HTML templates
│   │── admin.py             # Django admin settings
│   │── models.py            # Database models
│   │── views.py             # Business logic
│   │── urls.py              # URL routing
│── myquizproject/           # Django project settings
│   │── settings.py          # Configuration settings
│   │── urls.py              # Main URL routes
│   │── wsgi.py              # WSGI settings
│   │── asgi.py              # ASGI settings
│── manage.py                # Django management script
│── requirements.txt         # Dependencies list
Usage
Navigate to the homepage and enter a topic.
Click "Generate Quiz" to fetch AI-generated questions.
Answer the quiz and submit responses.
View scores and retry quizzes.
Admin Panel
Access the Django admin panel at http://127.0.0.1:8000/admin/ using the superuser credentials.

API Integration
This project uses OpenAI's API to generate quiz questions and answers dynamically.

Modify views.py to add your OpenAI API Key:


openai.api_key = "your-openai-api-key"
Deployment
To deploy, configure the following:

Database: Use PostgreSQL/MySQL instead of SQLite for production.
Environment Variables: Store the OpenAI API key securely.
Static Files: Configure settings for serving static files.
Hosting: Deploy on platforms like Heroku, AWS, or DigitalOcean.
License
This project is open-source and available under the MIT License.
