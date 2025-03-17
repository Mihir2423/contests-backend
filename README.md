# Coding Contests API

## Overview
This API provides information about upcoming coding contests from Codeforces, LeetCode, and CodeChef. It fetches contest data from their respective platforms and returns active contests.

## Features
- Retrieve all active contests from Codeforces, LeetCode, and CodeChef.
- Fetch contests from individual platforms.
- Returns contest details including name, start time, duration, and URL.

## Endpoints
### Root Endpoint
```http
GET /
```
Response:
```json
{
  "message": "Coding Contests API",
  "endpoints": {
    "/contests": "Get all active contests from Codeforces, LeetCode, and CodeChef",
    "/contests/codeforces": "Get active Codeforces contests",
    "/contests/leetcode": "Get active LeetCode contests",
    "/contests/codechef": "Get active CodeChef contests"
  }
}
```

### Get All Contests
```http
GET /contests
```
Response:
```json
{
  "status": "success",
  "count": 3,
  "data": [
    {
      "platform": "Codeforces",
      "name": "Contest Name",
      "startTime": "2024-09-15T12:00:00Z",
      "duration": "2 hours 30 minutes",
      "url": "https://codeforces.com/contest/1234"
    }
  ]
}
```

### Get Codeforces Contests
```http
GET /contests/codeforces
```

### Get LeetCode Contests
```http
GET /contests/leetcode
```

### Get CodeChef Contests
```http
GET /contests/codechef
```

## Installation and Setup
### Prerequisites
- Node.js installed
- npm or yarn installed

### Steps to Run
1. Clone the repository:
   ```sh
   git clone https://github.com/Mihir2423/contests-backend.git
   cd coding-contests-api
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node index.js
   ```
4. The API will run on `http://localhost:4000` by default.

## Dependencies
- `express` - Web framework
- `axios` - HTTP requests
- `cors` - Cross-origin requests

## Notes
- Ensure your internet connection is active since the API fetches data from external sources.
- The API does not store data; it fetches live data from contest platforms.

