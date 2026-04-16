# E-Commerce Backend: Switch MongoDB Atlas Cluster & Seed Data

## Plan Status: Approved & In Progress

### Step 1: Setup New Atlas (User Manual)
- Create new Atlas cluster at cloud.mongodb.com.
- Get connection string: Database > Connect > Drivers > Copy `mongodb+srv://<username>:<password>@cluster0.xxx.mongodb.net/ecommerce?retryWrites=true&amp;w=majority`
- Network Access > Add IP: 'Add Current IP Address'.

### Step 2: Update .env (User: Security)
```
cd backend
```
Create/edit `.env`:
```
MONGO_URI=your_new_connection_string_here
JWT_SECRET=your_super_secret_jwt_key_here (generate new if needed)
PORT=5000
```

### Step 3: Secure .env (Done below)
- Added to .gitignore.

### Step 4: Test Connection
```
cd backend
npm run dev
```
Expect: `MongoDB Connected: cluster0.xxx.mongodb.net`

### Step 5: Seed Products (After connection success)
```
node seeder.js
```
Expect: `✅ 100 products seeded successfully!`

### Step 6: Test Frontend
- Start frontend: `cd frontend && npm run dev`
- Visit localhost:5173, check products load.

**Progress: Steps 3 completed. Complete 1-2 manually, run 4-6, mark done.**

**New Atlas string ready? Reply with confirmation to verify setup.**

