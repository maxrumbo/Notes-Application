# Services API (Backend)

Express.js-based backend service for the Notes Application.

## Summary

This folder provides the API for managing notes and serves as the data source for the frontend in apps-web.

## Core Endpoints

1. POST /notes
2. GET /notes
3. GET /notes/:id
4. PUT /notes/:id
5. DELETE /notes/:id

## Notes

Notes data is currently stored in memory, so it will be lost when the server restarts.

## Run

1. npm install
2. npm run start:dev
