# CBC_B-012: Comprehensive Mental Health & Wellness Platform

A multi-component digital health platform that integrates various mental health and wellness tools, featuring AI-powered mental health support, speech emotion recognition, medicine price tracking, therapist mapping, health data analytics, and user authentication systems.

## 🏗️ Project Overview

This repository contains a comprehensive suite of mental health and wellness applications, each designed to address different aspects of digital health and well-being. The platform consists of multiple independent but interconnected modules that can be deployed individually or as a complete ecosystem.

## 📁 Project Structure

```
CBC_B-012/
├── frontend/                 # MindWell Frontend (React + TypeScript)
├── backend/                  # MindWell Backend (Django + AI)
├── sentio/                   # Sentio Dashboard (React + Vite + Shadcn)
├── medicine/                 # Medicine Price Tracker (Django + React)
├── map/                      # Therapist Map Application (React + Google Maps)
├── speech/                   # Speech Emotion Recognition (Flask + ML)
├── health dashboard/         # Health Data Analytics (Django + React)
└── login/                    # User Authentication System (Node.js + MongoDB)
```

## 🚀 Individual Components

### 1. **MindWell - AI Mental Health Support** (`frontend/` & `backend/`)
**Technology Stack:** React + TypeScript + Django + Google Generative AI

A conversational AI platform that provides mental health support and generates personalized wellness roadmaps.

**Features:**
- AI-powered mental health conversations
- Personalized wellness roadmaps
- Interactive chat interface
- Material-UI based responsive design

**Setup:**
```bash
# Backend Setup
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend Setup
cd frontend
npm install
npm start
```

### 2. **Sentio - Modern Health Dashboard** (`sentio/`)
**Technology Stack:** React + TypeScript + Vite + Shadcn/UI + Tailwind CSS

A modern, feature-rich health dashboard with authentication and comprehensive UI components.

**Features:**
- Modern authentication system
- Interactive dashboard
- Feature showcase
- Responsive design with Shadcn/UI components
- MongoDB integration

**Setup:**
```bash
cd sentio
npm install
npm run dev
```

### 3. **Medicine Price Tracker** (`medicine/`)
**Technology Stack:** Django + React + Tailwind CSS

A web application that tracks and compares medicine prices across different online platforms.

**Features:**
- Real-time price comparison
- Historical price tracking
- Search functionality
- Responsive web interface

**Setup:**
```bash
# Backend Setup
cd medicine
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend Setup
cd frontend
npm install
npm start
```

### 4. **Therapist Map Application** (`map/`)
**Technology Stack:** React + TypeScript + Google Maps API

An interactive map application for locating therapists and healthcare providers.

**Features:**
- Google Maps integration
- Therapist location markers
- Directions and navigation
- Address autocomplete
- Current location detection

**Setup:**
```bash
cd map
npm install
# Add your Google Maps API key to src/App.tsx
npm start
```

### 5. **Speech Emotion Recognition** (`speech/`)
**Technology Stack:** Flask + Python + Machine Learning + Librosa

An AI-powered application that analyzes speech patterns to detect emotional states.

**Features:**
- Real-time emotion detection from audio
- Support for multiple audio formats
- Machine learning model integration
- Web-based interface

**Setup:**
```bash
cd speech
pip install -r requirements.txt
python app.py
```

### 6. **Health Data Analytics Dashboard** (`health dashboard/`)
**Technology Stack:** Django + React + Pandas + Data Visualization

A comprehensive health data analytics platform for tracking and visualizing health metrics.

**Features:**
- Health data import and processing
- Interactive charts and visualizations
- File upload capabilities
- Data analytics and insights

**Setup:**
```bash
# Backend Setup
cd "health dashboard/backend"
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend Setup
cd frontend
npm install
npm start
```

### 7. **User Authentication System** (`login/`)
**Technology Stack:** Node.js + Express + MongoDB + bcrypt

A secure user authentication system with signup and signin functionality.

**Features:**
- User registration and login
- Password hashing with bcrypt
- MongoDB user storage
- RESTful API endpoints

**Setup:**
```bash
cd login
npm install
# Ensure MongoDB is running
npm start
```

## 🛠️ Prerequisites

Before running any component, ensure you have the following installed:

- **Node.js** (v16 or higher)
- **Python** (v3.8 or higher)
- **MongoDB** (for authentication system)
- **Google Maps API Key** (for map application)
- **Git**

## 🔧 Environment Setup

### Python Dependencies
Most components use Python virtual environments. Create and activate them:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Node.js Dependencies
Install dependencies for each frontend component:

```bash
npm install
```

### Database Setup
- **MongoDB**: Required for the authentication system
- **SQLite**: Used by Django applications (auto-created)

### API Keys
- **Google Maps API**: Required for the therapist map application
- **Google Generative AI**: Required for MindWell AI features

## 🚀 Quick Start

1. **Clone the repository:**
```bash
git clone <repository-url>
cd CBC_B-012
```

2. **Choose a component to run:**
```bash
# For MindWell
cd frontend && npm install && npm start
cd backend && pip install -r requirements.txt && python manage.py runserver

# For Sentio
cd sentio && npm install && npm run dev

# For Medicine Tracker
cd medicine && pip install -r requirements.txt && python manage.py runserver
cd medicine/frontend && npm install && npm start
```

3. **Access the applications:**
- MindWell: http://localhost:3000
- Sentio: http://localhost:5173
- Medicine Tracker: http://localhost:8000
- Speech Recognition: http://localhost:5000
- Health Dashboard: http://localhost:8000
- Authentication: http://localhost:5000

## 📊 Features Summary

| Component | AI/ML | Authentication | Database | API Integration |
|-----------|-------|----------------|----------|-----------------|
| MindWell | ✅ Google AI | ❌ | SQLite | ✅ |
| Sentio | ❌ | ✅ | MongoDB | ❌ |
| Medicine Tracker | ❌ | ❌ | SQLite | ✅ |
| Therapist Map | ❌ | ❌ | - | ✅ Google Maps |
| Speech Recognition | ✅ ML Model | ❌ | - | ❌ |
| Health Dashboard | ❌ | ❌ | SQLite | ❌ |
| Authentication | ❌ | ✅ | MongoDB | ❌ |

## 🔒 Security Features

- Password hashing with bcrypt
- CORS configuration
- Input validation
- Secure file upload handling
- Environment variable management

## 🧪 Testing

Each component includes its own testing setup:

```bash
# Django tests
python manage.py test

# React tests
npm test

# Frontend build
npm run build
```

## 📝 API Documentation

### MindWell API
- `POST /api/mental-health-support/` - AI mental health support

### Medicine Tracker API
- `GET /api/search/?medicine=<name>` - Search medicine prices

### Authentication API
- `POST /api/signup` - User registration
- `POST /api/signin` - User login

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the individual component README files
- Review the setup instructions for each component

## 🔮 Future Enhancements

- [ ] Unified authentication across all components
- [ ] Real-time notifications
- [ ] Mobile applications
- [ ] Advanced analytics dashboard
- [ ] Integration with wearable devices
- [ ] Telemedicine features
- [ ] Multi-language support

---

**Note:** This is a comprehensive mental health and wellness platform. Each component can be developed and deployed independently, making it suitable for both learning and production use cases.
