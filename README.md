# AI Placement Preparation Platform

A comprehensive web-based platform that helps students prepare for campus placements using AI-powered tools — including aptitude and technical practice tests, coding challenges, mock interviews, resume analysis, and personalized learning recommendations.

> **Note:** The project skeleton (directory structure, blueprints, templates, and models) is in place. Source files are currently stubs and are being implemented incrementally.

## ✨ Features

### 🎯 Practice & Assessment
- **Aptitude Tests** — practice and timed mock tests for quantitative, logical, and verbal reasoning
- **Technical Tests** — subject-wise technical practice (Core CS / programming fundamentals)
- **Coding Challenges** — problem-solving with an in-platform code editor and result evaluation
- **Mock Tests** — full-length placement mock tests that mirror real campus recruitment pattern

### 🤖 AI-Powered Modules
- **Mock Interviews** — AI-driven mock interviews with HR and technical round simulations
- **Resume Analyzer** — upload your resume and get AI-based scoring and improvement suggestions
- **Performance Analysis** — track strengths, weaknesses, and accuracy over time
- **Recommendation Engine** — personalized study/test recommendations based on performance

### 👥 Roles & Modules
- **Student Dashboard** — progress tracking, results history, and profile management
- **Admin Panel** — manage students, questions, categories, tests, and results

## 🛠️ Tech Stack

| Layer      | Technology                                            |
|------------|-------------------------------------------------------|
| Backend    | Python 3, Flask (Blueprints)                          |
| Frontend   | HTML, CSS, JavaScript, Jinja2 Templates               |
| Database   | SQL (schema in `database/schema.sql`, seed in `database/seed.sql`) |
| AI/ML      | Python AI modules for interviews, resume, analysis, recommendation |
| Testing    | Pytest (`tests/`)                                     |

## 📁 Project Structure

```
├── app.py                      # Flask application entry point
├── config.py                   # Application configuration
├── requirements.txt            # Python dependencies
├── .env                        # Environment variables (secrets, DB config)
│
├── ai/                         # AI-powered modules
│   ├── mock_interview.py       # AI mock interview engine
│   ├── resume_analyzer.py      # Resume parsing & scoring
│   ├── performance_analysis.py # Performance & progress analytics
│   └── recommendation_engine.py# Personalized recommendations
│
├── database/
│   ├── schema.sql              # Database schema
│   └── seed.sql                # Seed/demo data
│
├── models/                     # Data models
│   ├── user.py  test.py  question.py  coding.py
│   ├── interview.py  resume.py  result.py  progress.py
│   └── recommendation.py
│
├── routes/                     # Flask blueprints (URL routes)
│   ├── auth_routes.py          # Login / registration
│   ├── student_routes.py       # Student dashboard, profile, progress
│   ├── aptitude_routes.py      # Aptitude practice & tests
│   ├── technical_routes.py     # Technical practice & tests
│   ├── coding_routes.py        # Coding challenges
│   ├── mock_test_routes.py     # Mock placement tests
│   ├── interview_routes.py     # AI mock interviews
│   ├── resume_routes.py        # Resume upload & analysis
│   ├── recommendation_routes.py# Recommendations
│   └── admin_routes.py         # Admin management
│
├── static/                     # Static assets
│   ├── css/  (style, dashboard, responsive)
│   ├── js/   (main, test, coding, interview)
│   └── images/
│
├── templates/                  # Jinja2 HTML templates
│   ├── base.html  index.html
│   ├── auth/      student/    admin/
│   ├── aptitude/  technical/  coding/
│   ├── mock_test/ interview/  resume/  recommendation/
│   └── ...
│
└── tests/                      # Pytest test suites
    ├── test_auth.py  test_aptitude.py
    ├── test_coding.py test_mock_test.py
```

## 🚀 Getting Started

### 1. Prerequisites
- Python 3.8+
- pip
- A SQL database (MySQL / PostgreSQL / SQLite)

### 2. Clone & Setup
```bash
git clone https://github.com/<your-org>/AI-PLACEMENT-PREPRATION-PLADFORM.git
cd AI-PLACEMENT-PREPRATION-PLADFORM
```

### 3. Create a Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Configure Environment
Copy the variables below into `.env` and fill in your values:

```env
SECRET_KEY=your-secret-key
DATABASE_URL=your-database-connection-string
# Add any API keys required by the AI modules (e.g., LLM/OpenAI key)
AI_API_KEY=your-ai-api-key
```

Configuration options live in `config.py`.

### 6. Initialize the Database
```bash
# Apply schema
mysql -u <user> -p <database> < database/schema.sql

# (Optional) Load seed/demo data
mysql -u <user> -p <database> < database/seed.sql
```

### 7. Run the Application
```bash
python app.py
```

Then open your browser and visit **http://localhost:5000**.

## 🧪 Running Tests
```bash
pytest tests/ -v
```

## 🔑 Default Access
- **Admin:** created/configured via the admin seed in `database/seed.sql`
- **Student:** register through the public registration page (`/register`)

## 📌 Roadmap
- [ ] Backend routes & API endpoints
- [ ] Database schema & models implementation
- [ ] AI module integrations
- [ ] UI templates & styling
- [ ] Test suites & CI

## 🤝 Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## 📄 License
This project is for educational use. Add an appropriate license before public distribution.