# employee backend api

Simple Express + TypeScript backend for employee management with MySQL.

## tech stack
- Node.js
- Express
- TypeScript
- MySQL (`mysql2`)
- Vitest

## project structure
```
src/
   index.ts
   Server.ts
   config/
      dbConfig.ts
   controllers/
      EmplController.ts
   model/
      Employee.ts
   repository/
      EmplRepository.ts
      InMemoryRepository.ts
   routes/
      EmplRoutes.ts

createTable.sql
requests.http
test/
```

## setup
1. Install dependencies:
    ```bash
    npm install
    ```
2. Set your DB config in `src/config/dbConfig.ts`.
3. Run SQL table creation from `createTable.sql`.

## run
```bash
npm start
```

Server starts on: `http://localhost:3000`

## scripts
- `npm start` - run app with `tsx`
- `npm test` - run tests in watch mode
- `npm run test:run` - run tests once

## api endpoints
Base path: `/empl`

- `GET /empl/hello`
- `GET /empl/`
- `GET /empl/get/:id`
- `POST /empl/add`
- `PUT /empl/position/:id`
- `DELETE /empl/delete/:id`

Sample requests are in `requests.http`.

## notes
- CORS is enabled for all origins.
- Repository is currently wired to `EmplRepository` (MySQL).
