# GPS Simulation Service – Usage Guide

## Docker Image

Pull the image from Docker Hub:
docker pull <your-dockerhub-username>/gps-simulation:latest

Replace <your-dockerhub-username> with your Docker Hub ID.

---

## Running the Service Locally

1. Clone the repository:
   git clone https://github.com/<your-github-username>/gps_simulation.git
   cd gps_simulation

2. Build and start services:
   docker-compose up --build

This launches:
- Frontend on http://localhost
- Backend API on http://localhost:3000

---

## Project Structure

gps_simulation/
├── client/            (React frontend)
│   └── src/App.jsx    (Leaflet map interface)
├── server/            (Node.js backend)
│   └── index.js       (API entry point)
├── docker-compose.yml
└── DOCUMENTATION.md   (This file)

---

## Accessing Services

Frontend:
Open http://localhost in your browser

Backend:
Example API endpoint:
GET http://localhost:3000/api/status

---

## Docker Hub Deployment

To run from the Docker image:
docker run -p 80:80 -p 3000:3000 <your-dockerhub-username>/gps-simulation

---

## Notes

- Frontend uses React + Leaflet
- Backend uses Node.js + Express
- Both are containerized with Docker and orchestrated with docker-compose
