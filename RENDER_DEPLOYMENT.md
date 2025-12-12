# Render Deployment Guide

## Environment Variables

Copy and paste these environment variables in your Render web service:

### Environment Variables (Copy and Paste)
```
DATABASE_URL=jdbc:postgresql://dpg-d4tvrnu3jp1c73f6g9n0-a.oregon-postgres.render.com:5432/userprofile_db
DB_USERNAME=userprofile_db_user
DB_PASSWORD=Bh2RxPQBSxeA8RhLlS9GLTTPxBuZjQI0
PORT=10000
SPRING_PROFILES_ACTIVE=prod
DDL_AUTO=update
```

### Alternative: Using Individual Database Components
```
SPRING_DATASOURCE_URL=jdbc:postgresql://dpg-d4tvrnu3jp1c73f6g9n0-a.oregon-postgres.render.com:5432/userprofile_db
SPRING_DATASOURCE_USERNAME=userprofile_db_user
SPRING_DATASOURCE_PASSWORD=Bh2RxPQBSxeA8RhLlS9GLTTPxBuZjQI0
PORT=10000
SPRING_PROFILES_ACTIVE=prod
DDL_AUTO=update
```

**Note**: Replace `dpg-xxxxxxxxx-a.oregon-postgres.render.com` with your actual Render PostgreSQL host URL.

## How to Add Environment Variables in Render:

1. Go to your Render dashboard
2. Click on your web service
3. Go to "Environment" tab
4. Click "Add Environment Variable"
5. Copy each line above (format: KEY=VALUE)
6. Paste the key in "Key" field and value in "Value" field

## Service Configuration:

- **Name**: userprofile-service
- **Environment**: Docker
- **Build Command**: (leave empty)
- **Start Command**: (leave empty)
- **Health Check Path**: `/actuator/health`
- **Port**: 10000

## Database Details:
- **Host**: Your Render PostgreSQL host
- **Port**: 5432
- **Database**: userprofile_db
- **Username**: userprofile_db_user
- **Password**: Bh2RxPQBSxeA8RhLlS9GLTTPxBuZjQI0

## Deployment Steps:
1. Push your code to GitHub
2. Connect GitHub repo to Render
3. Add environment variables above
4. Deploy!

Your app will be available at: `https://your-service-name.onrender.com`