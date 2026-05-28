# Epic Integration Web

A simple Angular proof-of-concept application for Epic SMART on FHIR patient registration and search.

## Overview

This repository contains an Angular 20 standalone application that provides a basic UI for:
- Adding a new patient record via an Epic-compatible FHIR backend
- Searching patients and viewing patient data
- Displaying patient vitals and core app navigation

The app uses Angular standalone components and communicates with a backend API located at `http://3.131.105.103:8110/api` by default.

## Key Features

- `Add Patient` form with demographic, contact, and address fields
- `Patients` search and patient lookup functionality
- `Vitals` display component
- `Home` landing page and reusable header/footer components
- HTTP integration via `CommonService`

## Prerequisites

- Node.js 20+ and npm
- Angular CLI compatible with Angular 20
- A running backend API for patient creation and search

## Setup

1. Install dependencies:

```bash
npm install
```

2. Start the development server:

```bash
npm start
```

3. Open the app in your browser:

```text
http://localhost:4200
```

## Backend Configuration

The frontend expects a backend API at:

```text
https://<YOUR_BACKEND_DOMAIN>/api
```

Update the URL in `src/services/common.ts` if your API is hosted elsewhere.

## Project Structure

- `src/main.ts` — Angular bootstrap and root app component
- `src/components/` — standalone UI components (`header`, `home`, `patients`, `add-patient`, `vitals`, `footer`)
- `src/services/common.ts` — HTTP service for patient create/search operations
- `src/app/models/patient-registration.dto.ts` — patient registration DTO shape
- `src/models/patient.interface.ts` — patient interface model

## Scripts

- `npm start` — run development server
- `npm run build` — build production output

## Notes

- This repository is a frontend proof-of-concept and requires a compatible C# API backend to fully function.
- The app is currently configured to use the Epic FHIR sandbox style integration as a demonstration.
