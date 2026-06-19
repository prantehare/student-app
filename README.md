# Student Registry — Frontend

A React UI for your Spring Boot Student CRUD API.

## Setup

1. Install dependencies:
   ```
   npm install
   ```

2. Make sure your Spring Boot backend is running (default expected at `http://localhost:8080`).
   If it runs elsewhere, edit `.env`:
   ```
   REACT_APP_API_URL=http://your-backend-url
   ```

3. Start the app:
   ```
   npm start
   ```
   Opens at http://localhost:3000

## Backend requirement

Your Spring Boot `StudentController` needs CORS enabled, or the browser will block requests:

```java
@CrossOrigin(origins = "http://localhost:3000") // or "*" for testing
@RestController
@RequestMapping("/api/student")
public class StudentController { ... }
```

## Deploying

- Build for production: `npm run build` → outputs to `build/`
- Deploy the `build/` folder to Vercel, Netlify, or any static host
- Update `REACT_APP_API_URL` to your deployed backend URL before building for production
"# student-app" 
