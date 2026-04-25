# Notes Application

Notes Application is a monorepo project that separates the web app (client) and API service (server) for note management. This project is designed as a full-stack JavaScript learning foundation with a clear structure, easy development workflow, and straightforward deployment separation.

## Overview

The application allows users to create, read, update, and delete notes (CRUD). The frontend is built with Next.js for a responsive user interface, while the backend is built with Express.js to provide lightweight API endpoints.

## Monorepo Structure

1. `apps-web`
Next.js-based frontend that handles views, user interactions, and API consumption.

2. `services-api`
Express.js-based backend that provides `notes` endpoints and in-memory note data management logic.

## Communication Architecture

The frontend communicates with the backend through an HTTP API. By default, the frontend points to `http://localhost:5000/` as the API base URL, and it can be changed from the app interface through the `Change URL` feature.

This separation provides several benefits:

1. Frontend and backend can be developed independently.
2. API integration can be tested without relying on a unified codebase.
3. The structure is ready to scale for production scenarios (for example: auth service, database persistence, and separate deployment).

## Current Feature Status

Currently available and well integrated:

1. Basic note management (CRUD) through `notes` endpoints.
2. Frontend-backend integration for the main note workflow.

Still under further development:

1. Full authorization/authentication in the backend.
2. Support for upload, collaboration, and note export on the API side.
3. Permanent data persistence (currently still in-memory).

## Development Goals

This repository is suitable for:

1. A starter template for a full-stack notes application.
2. A learning medium for Next.js + Express.js integration.
3. A foundation for refactoring into a more modular architecture (service-per-domain).