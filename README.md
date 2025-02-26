# Sports Forecast Live

A full-stack sports forecasting application that delivers real-time statistics, predictive analytics, and live match data visualization. This project combines Django for the backend API, React with Tailwind CSS for the frontend, and AWS for deployment.

![Sports Forecast Live](https://via.placeholder.com/800x400?text=Sports+Forecast+Live)

## Features

- **Real-Time Data Streaming**: Live sports data with automatic updates
- **Predictive Analytics**: Forecasting match statistics using Exponential Smoothing
- **Interactive Dashboard**: Visualize match predictions and statistics
- **REST API**: Django-powered API endpoints for data access
- **Responsive Design**: Tailwind CSS for a mobile-friendly experience
- **AWS Deployment**: Production-ready setup with PostgreSQL on RDS

## Tech Stack

### Backend
- Python 3.x
- Django
- Django REST Framework
- PostgreSQL
- Gunicorn

### Frontend
- React
- Next.js
- Tailwind CSS
- Axios

### DevOps & Deployment
- AWS EC2
- AWS RDS
- Nginx
- Apache (optional)
- Ubuntu Server
- Screen for process management
- Cron jobs for automation

## Installation

### Prerequisites
- Python 3.x
- Node.js and npm
- Git

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/sports-forecast-live.git
   cd sports-forecast-live
   ```

2. **Set up the backend**
   ```bash
   # Create and activate virtual environment
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   
   # Install dependencies
   cd backend
   pip install -r requirements.txt
   
   # Run migrations
   python manage.py migrate
   
   # Start the development server
   python manage.py runserver
   ```

3. **Set up the frontend**
   ```bash
   cd ../frontend
   npm install
   npm run dev
   ```

4. **Start the data engine**
   ```bash
   cd ../backend
   python data_engine.py
   ```

## Project Structure

```
sports-forecast-live/
├── backend/
│   ├── api/                  # Django API views and serializers
│   ├── core/                 # Core Django settings
│   ├── data_engine/          # Real-time data processing
│   ├── forecasting/          # Prediction algorithms
│   ├── models/               # Database models
│   └── manage.py
├── frontend/
│   ├── components/           # React components
│   ├── pages/                # Next.js pages
│   ├── public/               # Static assets
│   ├── styles/               # Tailwind configuration
│   └── package.json
├── data/                     # Sample data and fixtures
├── docs/                     # Documentation
└── deployment/               # Deployment scripts and configs
    ├── aws/
    ├── nginx/
    └── apache/
```

## API Documentation

The API provides the following endpoints:

### Match Data
- `GET /api/matches/` - List all matches
- `GET /api/matches/{id}/` - Get specific match details
- `GET /api/matches/live/` - Get currently live matches

### Predictions
- `GET /api/predictions/{match_id}/` - Get predictions for a specific match
- `GET /api/predictions/upcoming/` - Get predictions for upcoming matches

### Stats
- `GET /api/stats/{match_id}/` - Get statistics for a specific match
- `GET /api/stats/trending/` - Get trending statistics

## Deployment

This application is designed to be deployed on AWS. Follow the detailed deployment guide:

1. Launch an EC2 instance with Ubuntu
2. Set up PostgreSQL on RDS
3. Configure Nginx as a reverse proxy
4. Set up Gunicorn for the Django application
5. Deploy the Next.js frontend
6. Configure process management with Screen
7. Set up cron jobs for automated tasks

Detailed deployment instructions are available in the `deployment/` directory.

## Environment Variables

Create a `.env` file in the backend directory with the following variables:

```
DEBUG=False
SECRET_KEY=your_secret_key
DATABASE_URL=postgresql://user:password@host:port/dbname
ALLOWED_HOSTS=yourdomain.com,www.yourdomain.com
CORS_ALLOWED_ORIGINS=https://yourdomain.com
```

For the frontend, create a `.env.local` file:

```
NEXT_PUBLIC_API_URL=https://api.yourdomain.com
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the GPL 3.0 License - see the LICENSE file for details.

## Acknowledgements

- Tutorial by Cagdas Yetkin
- Sports data provided by [Data Provider]
- Icons by [Icon Provider]
