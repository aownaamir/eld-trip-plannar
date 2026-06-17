# ELD Trip Planner & HOS Simulator

A full-stack truck driver trip planning system that generates FMCSA-compliant Hours of Service (HOS) logs, visualizes routes, and helps drivers plan long-haul trips efficiently.

> Built with Next.js, TypeScript, Django REST Framework, and Mapbox.

![App](screenshots/app.png)


## Live Demo

https://eld-frontend-pymc.vercel.app/


## Overview

Truck drivers must comply with strict Hours of Service (HOS) regulations that govern driving time, mandatory breaks, duty limits, and rest periods. Planning long-distance trips while remaining compliant can be complex and time-consuming.

The ELD Trip Planner automates this process by calculating routes, estimating trip metrics, and generating Electronic Logging Device (ELD) logs based on HOS rules. Users can enter trip locations and receive a complete trip breakdown, including driving periods, rest stops, cycle-hour tracking, and route visualization.


## Features

- Interactive route planning between locations
- Automated HOS-compliant ELD log generation
- Route visualization using Mapbox
- Trip distance and duration estimation
- Driving, on-duty, off-duty, and sleeper berth calculations
- Rest break and stop planning
- Multi-day trip simulation
- Cycle hour tracking
- Fuel stop recommendations
- Real-world logistics workflow simulation


## Tech Stack

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- Mapbox GL JS

### Backend

- Django
- Django REST Framework

### APIs & Services

- Mapbox Directions API
- Mapbox Geocoding API



## How It Works

1. User enters:
   - Current Location
   - Pickup Location
   - Dropoff Location
   - Previously Used Cycle Hours

2. Backend retrieves route data from Mapbox.

3. HOS simulation engine processes:
   - 11-Hour Driving Limit
   - 14-Hour Duty Window
   - 30-Minute Break Requirement
   - 10-Hour Reset Rule
   - 70-Hour Cycle Rule
   - Fuel Stop Planning

4. System generates:
   - Route Visualization
   - Trip Metrics
   - Stop Recommendations
   - ELD Logs



## Architecture

```text
┌─────────────────────┐
│     Next.js UI      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Django REST API     │
└──────────┬──────────┘
           │
   ┌───────┴────────┐
   │                │
   ▼                ▼
Mapbox APIs     HOS Engine
(Route Data)   (Business Logic)
   │                │
   └───────┬────────┘
           ▼
      ELD Logs
      Trip Metrics
      Stop Planning
```


## Screenshots

### Trip Details

![Form](screenshots/form.png)

### Route Planning

![Route](screenshots/route.png)

### Generated ELD Logs

![Logs](screenshots/logs.png)


## Project Structure

### Frontend

```text
eld-frontend/
├── public/
└── app/
   ├── components/
   ├── lib/
   ├── utils/
   └── types/

```

### Backend

```text
ena-backend/
   ├── ena-backend/
   └── trips/
      ├── services/
      ├── migrations/
      ├── admin.py
      ├── tests.py
      ├── views.py
      ├── urls.py
      └── models.py
```


## Source Code

### Frontend Repository

[ELD-frontend](https://github.com/aownaamir/eld-frontend)

### Backend Repository

[ELD-backend](https://github.com/aownaamir/eld-backend)


## Key Challenges

### Implementing Real HOS Regulations

One of the biggest challenges was converting real-world trucking regulations into programmatic business logic while ensuring generated logs remained realistic and compliant.

### Route & Logistics Integration

Combining route data with HOS calculations required synchronizing travel time, distance, fuel stops, and break scheduling into a single planning workflow.


## What I Learned

- Building production-style full-stack applications
- Working with mapping and routing APIs
- Handling complex business logic
- Integrating React applications with Django REST APIs


## Future Improvements

- User authentication
- Driver profiles
- Trip history
- PDF export for ELD logs
- Fleet management support
- Real-time traffic integration
- Weather-aware route planning

##

 If you found this project interesting, consider giving it a star ⭐
