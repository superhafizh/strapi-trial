# Starting project

### 1. After cloning project clone submodules.
    
```bash
git submodule update --init
```

### 2. Setup and running backend

2.1. Setup local PostgreSQL database.
```bash
# Create a new postgresql database
createdb {database_name}
psql {database_name} < ./database-dump/dump-strapi_trial-full.sql
```

2.2. Create environment variable
```bash
cd backend
cp .env.example .env
```

2.3. Edit database connection in environment variable
```
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME={local_database_name}
DATABASE_USERNAME={local_database_user}
DATABASE_PASSWORD={local_database_password}
```

2.4. Install dependencies and run Strapi in development mode
```bash
npm install
npm run develop
```

### 3. Setup and running frontend

3.1. Install dependencies and run Next.js in development mode
```bash
cd frontend
npm install
npm run develop
```
