Project overview
Features
Quick start
Technology stack
Screenshots section placeholder
Basic run instructions

LOCAL_DEVELOPMENT_GUIDE.md
Complete beginner-friendly tutorial
Required software installation
Folder structure
Backend setup
Mobile setup
Number of CMD windows required
Exact commands
Phone connection steps
Swagger testing
Database creation
Common errors and solutions

ARCHITECTURE.md
System architecture explanation
Data flow
User roles
Security architecture
AI pipeline
Development vs deployment architecture


SmartHarvest/
│
├── README.md
│
└── docs/
    │
    ├── LOCAL_DEVELOPMENT_GUIDE.md
    │
    └── ARCHITECTURE.md





1. README.md 

# SmartHarvest 🌱

## AI-Based Post-Harvest Decision Support System

SmartHarvest is an AI-powered mobile application designed to assist farmers, stakeholders, and administrators in post-harvest quality assessment and decision support.

The system uses deep learning-based image analysis to identify produce quality, estimate freshness, and provide intelligent recommendations for storage and handling.

---

# Features

## AI Produce Analysis

- Image-based fruit/vegetable recognition
- Quality classification:
  - Fresh
  - Semi-Fresh
  - Rotten
- Confidence score generation
- Shelf-life estimation
- Storage recommendation
- Geospatial Map for taking Picture Location
- Timestamps for the taken pictures

---

## Role-Based System

SmartHarvest supports three types of users:

### Farmer

Features:

- Personal dashboard
- Scan harvested produce
- View previous inspections
- Receive quality recommendations


### Stakeholder

Features:

- Inventory quality monitoring
- Incoming produce inspection
- Quality distribution overview
- Recent inventory checks


### Administrator

Features:

- User management
- Create accounts
- Edit users
- Change roles
- Reset passwords
- Delete users
- Monitor system activity

---

# System Architecture

                SmartHarvest Mobile App
                (React Native + Expo)

                          |
                          |
                     HTTPS API

                          |
                          ↓

                 FastAPI Backend
                     (Python)


      --------------------------------------

      |                 |                  |

      ↓                 ↓                  ↓
Authentication AI Engine Database
JWT Security PyTorch Model SQLite
User Roles Image Analysis Users
Permissions Prediction Inspections
      --------------------------------------


          Farmer    Stakeholder    Admin


---

# Technology Stack

## Mobile Application

- React Native
- Expo
- React Navigation
- AsyncStorage
- Lucide Icons


## Backend

- FastAPI
- Python
- SQLAlchemy
- SQLite
- JWT Authentication


## AI

- PyTorch
- Deep Learning Model
- Image Classification Pipeline


---

# Project Structure

SmartHarvest
├── backend
│ ├── app
│ │ ├── main.py
│ │ ├── models.py
│ │ ├── schemas.py
│ │ ├── predictor.py
│ │ ├── security.py
│ │ └── dependencies.py
│ │
│ └── smartharvest.db
└── mobile


├── src

│   ├── screens

│   ├── components

│   ├── auth

│   └── api.js

│

└── package.json






---

# Quick Start

## Backend

Open terminal:

```bash
cd backend

Activate environment:
Windows:
venv\Scripts\activate


Run server: 

uvicorn app.main:app --host 0.0.0.0 --port 8000


Mobile
Open another terminal:
cd mobile


Install packages: 
npm install


Start Expo: 
npx expo start



Running on Android Phone
Install Expo Go
Connect phone and PC to same WiFi
Scan Expo QR code
Application launches

API Documentation
Swagger:
http://127.0.0.1:8000/docs

Security
SmartHarvest uses JWT-based authentication.
Protected APIs require:
Authorization: Bearer TOKEN


Role permissions: 


Role
Access
Farmer
Own inspections
Stakeholder
Inventory data
Admin
Full management




Future Deployment
Current development:
Mobile App
    |
ngrok
    |
Local PC Backend



Future production: 

Mobile App

     |

Cloud FastAPI Server

     |

PostgreSQL Database

     |

AI Model Hosting



License
Academic / Research Project

---

Next I will prepare:

**`LOCAL_DEVELOPMENT_GUIDE.md`** (the detailed tutorial with CMD 1, CMD 2, CMD 3 instructions, phone setup, Swagger testing, troubleshooting).


