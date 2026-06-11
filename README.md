# 🏋️ Hypertrophy Tracker

**S&C Coaching Tool for Athlete Training Volume Management**

A mobile-first web app for strength & conditioning coaches to track athlete training volume, monitor weekly set counts per muscle, and manage periodized training mesocycles.

## ✨ Features

✅ **Weekly Set Tracking** - Log sets per muscle group per week  
✅ **Visual Charts** - Real-time volume trends with threshold alerts  
✅ **Threshold Alerts** - Optimal range: 10-20 working sets per muscle/week  
✅ **Auto-Calculation** - Volume = Sets × Reps × Weight  
✅ **Mesocycle Planning** - Periodized training blocks with progressive overload  
✅ **Mobile Optimized** - Responsive design for on-gym logging  
✅ **Multi-Athlete Management** - Coach dashboard for team oversight  

## 🛠 Tech Stack

- **Frontend**: React + TypeScript + TailwindCSS (mobile-first)
- **Backend**: Node.js + Express + PostgreSQL
- **Charts**: Recharts for data visualization
- **Auth**: JWT + bcrypt
- **Deployment**: Docker + Railway/Vercel

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- Docker (optional)

### Installation

```bash
# Clone the repo
git clone https://github.com/connorsmythfitness-debug/hypertrophy-tracker.git
cd hypertrophy-tracker

# Install all dependencies
npm run install-all

# Set up environment
cp .env.example .env

# Run with Docker
npm run dev

# Or run separately:
npm run backend    # Terminal 1: http://localhost:5000
npm run frontend   # Terminal 2: http://localhost:3000
```

## 📊 Key Features

### Analytics Dashboard
- **Volume-by-Muscle Charts**: Visualize weekly set totals with Recharts
- **Threshold Alerts**: Automatic warnings for below/above 10-20 set range
- **Progression Tracking**: Monitor improvements across mesocycles
- **Auto-Volume Calculation**: Sets × Reps × Weight

### For Athletes
- Quick workout logging (exercise, sets, reps, weight, RIR)
- Weekly volume summary per muscle
- Training compliance monitoring

### For Coaches
- Multi-athlete dashboard
- Team volume analysis
- Mesocycle planning & tracking
- Alert-based compliance monitoring

## 📁 Project Structure

```
hypertrophy-tracker/
├── backend/
│   ├── src/
│   │   ├── controllers/analytics.js    # Threshold logic
│   │   ├── routes/                     # API endpoints
│   │   └── server.js
│   ├── migrations/001_init.sql         # Database schema
│   ├── Dockerfile
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── VolumeChart.tsx
│   │   │   ├── ThresholdAlert.tsx
│   │   │   └── Navigation.tsx
│   │   ├── pages/Dashboard.tsx
│   │   └── App.tsx
│   ├── public/index.html
│   ├── Dockerfile
│   └── package.json
├── docker-compose.yml
├── .env.example
└── README.md
```

## 📊 API Endpoints

### Athletes
- `POST /api/athletes` - Create athlete
- `GET /api/athletes/:id` - Get athlete profile
- `GET /api/athletes/:id/volume` - Get weekly volume data

### Workouts
- `POST /api/workouts` - Log workout session
- `GET /api/workouts/:athleteId/week` - Get weekly workouts
- `PUT /api/workouts/:id` - Update workout

### Mesocycles
- `POST /api/mesocycles` - Create training block
- `GET /api/mesocycles/:athleteId` - Get athlete mesocycles
- `PUT /api/mesocycles/:id` - Update mesocycle

### Analytics (Key Feature!)
- `GET /api/analytics/:athleteId/volume-by-muscle` - Weekly volume per muscle
- `GET /api/analytics/:athleteId/threshold-status` - Alert status vs 10-20 range ⭐
- `GET /api/analytics/:athleteId/progression` - Progressive overload tracking

## 🎯 Threshold Logic

**Optimal Range: 10-20 working sets per muscle per week**

Based on: Schoenfeld et al. (2017) - CS Performance Hypertrophy Guide (2025)

- 🟡 **Below 10 sets**: Insufficient volume (warning)
- 🟢 **10-20 sets**: Optimal range (success)
- 🔴 **Above 20 sets**: Excessive volume (alert)

System auto-calculates: **Volume = Sets × Reps × Weight**

## 📚 Based On

- **CS Performance Hypertrophy Guide (2025)**: Evidence-based training systems
- **Schoenfeld et al. (2017)**: 10-20 sets per muscle per week for hypertrophy
- **Krieger (2010)**: Dose-response meta-analysis
- **Morton et al. (2018)**: Protein and muscle growth

## 🐳 Docker Deployment

```bash
# Start all services
docker-compose up

# Services:
# - Backend API: http://localhost:5000
# - Frontend: http://localhost:3000
# - PostgreSQL: localhost:5432
```

## 📱 Mobile Usage

App is fully responsive for on-gym use:
- Quick workout logging on phones
- Real-time threshold alerts
- Weekly summary view
- Easy navigation

## 🚀 Production Deployment

### Railway
```bash
railway link
railway up
```

### Vercel (Frontend)
```bash
cd frontend
vercel deploy
```

### Heroku (Backend)
```bash
heroku create
git push heroku main
```

## 📄 License

MIT - Use freely for S&C coaching

## 👤 Author

**Connor Smyth** - CS Performance  
📧 connor.smyth.fitness@gmail.com  
🌐 csperformance.co.uk

---

**Built with ❤️ for strength coaches and athletes**
