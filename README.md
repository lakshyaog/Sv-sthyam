# Svāsthyam

A comprehensive health technology web application with ML-powered disease prediction and symptom analysis.

## Features

- Disease prediction based on symptoms
- Skin disease detection
- X-ray analysis
- Mental health assessment
- Healthcare chatbot
- Patient and doctor management system

## Tech Stack

- **Frontend**: React + Vite
- **Backend**: Node.js + Express
- **ML Models**: Python (Django)
- **Database**: MongoDB

## Project Structure

- `/MEDTECHWEBAPP_ML_Final-main/health` - React frontend application
- `/MEDTECHWEBAPP_ML_Final-main/health/server` - Node.js backend server
- `/MEDTECHWEBAPP_ML_Final-main/djangoMLDeployment` - Django ML models deployment

## Getting Started

### Prerequisites

- Node.js
- Python 3.x
- MongoDB

### Installation

1. Clone the repository
```bash
git clone https://github.com/lakshyaog/Sv-sthyam.git
cd Sv-sthyam
```

2. **⚠️ IMPORTANT: Set up environment variables**
```bash
cd MEDTECHWEBAPP_ML_Final-main/health/server
cp .env.example .env
# Edit .env and add your MongoDB credentials
```

3. Install frontend dependencies
```bash
cd MEDTECHWEBAPP_ML_Final-main/health
npm install
```

4. Install backend dependencies
```bash
cd server
npm install
```

5. Start the development servers
```bash
# Start backend server
cd MEDTECHWEBAPP_ML_Final-main/health/server
npm start

# In another terminal, start frontend
cd MEDTECHWEBAPP_ML_Final-main/health
npm run dev
```

## Security

⚠️ **Please read [SECURITY.md](SECURITY.md) for important security information.**

Never commit `.env` files or hardcode credentials in source code.

## License

This project is licensed under the ISC License.
