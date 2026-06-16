# ELD Trip Planner & HOS Simulator

A full-stack truck driver trip planning system that generates FMCSA-compliant Hours of Service (HOS) logs, visualizes routes, and helps drivers plan long-haul trips efficiently.


![Dashboard](screenshots/app.png)

![Form](screenshots/form.png)

![Map](screenshots/map.png)

![Logs](screenshots/logs.png)

## Problem

Truck drivers must comply with strict Hours of Service (HOS) regulations regarding driving time, rest periods, and cycle limits. Planning long-distance trips while remaining compliant can be complex and time-consuming.

## Solution

The ELD Trip Planner automates trip planning by calculating routes, estimating travel metrics, and generating Electronic Logging Device (ELD) logs based on HOS rules. Drivers can enter trip locations and receive a complete trip breakdown, including driving periods, mandatory breaks, rest periods, and route visualization.

## Features

- Route planning between pickup and destination locations
- Interactive map visualization using Mapbox
- Automated HOS-compliant ELD log generation
- Driving, on-duty, off-duty, and sleeper berth calculations
- Trip distance and duration estimation
- Stop and rest-break planning
- Fuel stop recommendations
- Multi-day trip simulation

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- Mapbox GL

### Backend
- Django
- Django REST Framework

### APIs & Services
- Mapbox Directions API
- Mapbox Geocoding API

## Architecture

```text
User Input
    │
    ▼
Next.js Frontend
    │
    ▼
Django REST API
    │
    ├── Route Calculation
    ├── HOS Simulation Engine
    └── ELD Log Generation
    │
    ▼
Mapbox APIs
    │
    ▼
Next.js
