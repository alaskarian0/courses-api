# Courses API

Backend REST API for the Courses Management System.

## Overview

This is the API backend that powers the [courses-web](https://github.com/alaskarian0/courses-web) frontend application. It provides authentication, data management, and reporting endpoints.

## API Endpoints

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/login` | User login |
| POST | `/auth/register` | Register new user |
| PUT | `/auth/change-password` | Change password |
| POST | `/auth/reset-password` | Reset password |
| GET | `/auth/users` | List all users |

### Response Format

```json
{
  "status": "success",
  "message": "Optional message",
  "data": {},
  "errors": []
}
```

### Paginated Response

```json
{
  "status": "success",
  "data": {
    "items": [],
    "pagination": {
      "current_page": 1,
      "per_page": 10,
      "total_items": 100,
      "total_pages": 10
    }
  }
}
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
git clone https://github.com/alaskarian0/courses-api.git
cd courses-api
npm install
```

### Environment Variables

Create a `.env` file:

```env
NODE_ENV=development
PORT=3003
```

### Development

```bash
npm run dev
```

The API runs at **http://localhost:3003**.

## Deployment

### PM2 (Production)

```bash
npm run build
pm2 start ecosystem.config.js
```

### Manual

```bash
npm run build
PORT=3003 npm start
```

## Related

- [courses-web](https://github.com/alaskarian0/courses-web) - Frontend application

## License

MIT
