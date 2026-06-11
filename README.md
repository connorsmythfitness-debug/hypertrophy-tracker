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

# Run migrations
npm run migrate

# Start with Docker
npm run dev
```

## 📊 Key Features

### Analytics Dashboard
- **Volume-by-Muscle Charts**: Visualize weekly set totals with Recharts
- **Threshold Alerts**: Automatic warnings for below/above 10-20 set range
- **Progression Tracking**: Monitor improvements across mesocycles
- **Auto-Volume Calculation**: Sets × Reps × Weight

### For Athletes
- Quick workout logging
- RIR (Reps in Reserve) tracking
- Weekly summary

### For Coaches
- Multi-athlete dashboard
- Team volume analysis
- Mesocycle planning & tracking
- Compliance monitoring

## 📁 Project Structure

```
hypertrophy-tracker/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── routes/
│   │   └── server.js
│   ├── migrations/
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.tsx
│   └── package.json
├── docker-compose.yml
├── .env.example
└── package.json
```

## 📚 Based On

- **CS Performance Hypertrophy Guide (2025)**
- **Schoenfeld et al. (2017)**: 10-20 sets/muscle/week optimal
- Evidence-based S&C principles

## 📄 License

MIT - Connor Smyth @ CS Performance
