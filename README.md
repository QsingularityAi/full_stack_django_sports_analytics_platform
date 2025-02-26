# Django Sports Analytics Platform

A full-stack sports forecasting application built with Django, Python, and React that provides real-time sports statistics, predictive analytics, and interactive visualizations.

## 🏆 Features

- **Live Data Streaming**: Real-time sports statistics and match data
- **Predictive Analytics**: Forecasting match outcomes using exponential smoothing
- **Interactive Dashboard**: Dynamic UI built with React and Tailwind CSS
- **RESTful API**: Django-powered backend API for data access
- **AWS Deployment**: Complete setup for production environment
- **Database Integration**: PostgreSQL on AWS RDS for persistent storage

## 🛠️ Tech Stack

### Backend
- Django
- Django REST Framework
- Python for data processing and analytics
- PostgreSQL database
- Gunicorn for production server

### Frontend
- React
- Next.js
- Tailwind CSS
- Axios for API requests

### Deployment & Infrastructure
- AWS EC2
- AWS RDS
- Nginx as reverse proxy
- Apache web server
- Ubuntu Server

## 📊 Project Architecture

```
django-sports-analytics-platform/
├── backend/                      # Django API and data processing
│   ├── api/                      # REST API endpoints
│   ├── core/                     # Core Django app
│   ├── data_engine/              # Data processing and forecasting
│   └── sports_analytics/         # Main Django project settings
├── frontend/                     # React/Next.js frontend
│   ├── components/               # Reusable UI components
│   ├── pages/                    # Next.js pages
│   ├── public/                   # Static assets
│   └── styles/                   # Tailwind CSS styles
├── scripts/                      # Deployment and automation scripts
└── docs/                         # Documentation
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+
- PostgreSQL
- Git

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/django-sports-analytics-platform.git
   cd django-sports-analytics-platform
   ```

2. **Backend Setup**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   python manage.py migrate
   python manage.py runserver
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

4. **Running Data Engine**
   ```bash
   cd backend
   python data_engine/run.py
   ```

## 📝 Project Structure

### Data Flow

1. Raw sports data is fetched from external sources
2. Data is processed and analyzed using Python
3. Forecasting models generate predictions
4. Django API serves processed data and predictions
5. React frontend consumes API data and renders UI
6. Real-time updates refresh the UI automatically

### API Endpoints

- `/api/matches/` - Get all matches data
- `/api/matches/<id>/` - Get specific match data
- `/api/predictions/` - Get all predictions
- `/api/stats/live/` - Get real-time match statistics

## 🌐 Deployment

Follow the detailed deployment guide in the documentation to set up:

1. AWS EC2 instance with Ubuntu
2. PostgreSQL on AWS RDS
3. Nginx and Apache configuration
4. Environment variables and security settings
5. Process management with Screen
6. Automated tasks with Cron jobs

## 🔄 Continuous Integration

This project uses GitHub Actions for CI/CD. The workflow includes:

- Automated testing
- Linting and code quality checks
- Build and deployment to AWS

## 📚 Documentation

For in-depth documentation, refer to the `/docs` folder or visit the project wiki.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

Developed by [Your Name]

## 🙏 Acknowledgements

- [Cagdas Yetkin](https://github.com/cagdasyetkin) for the original tutorial
- Sports data providers
- Open source community
```
