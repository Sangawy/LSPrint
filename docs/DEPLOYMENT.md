#  Deployment Guide | ڕێنمایی دیپلۆیمێنت

## پلاتفۆرمەکانی هۆستینگ | Hosting Platforms

### 1. Railway (پێشنیارکراو | Recommended)
```bash
# Install Railway CLI
npm install -g @railway/cli

# Login to Railway
railway login

# Deploy
railway up
```

### 2. Heroku
```bash
# Install Heroku CLI
# Create new app
heroku create your-app-name

# Set environment variables
heroku config:set DB_SERVER=your_server
heroku config:set DB_DATABASE=your_database
heroku config:set DB_USER=your_username
heroku config:set DB_PASSWORD=your_password

# Deploy
git push heroku main
```

### 3. Vercel
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Set environment variables in Vercel dashboard
```

### 4. Render
1. Connect your GitHub repository
2. Set build command: `npm install`
3. Set start command: `npm start`
4. Add environment variables

## گرنگ | Important Notes

1. **Database Access**: Make sure your SQL Server allows external connections
2. **Environment Variables**: Set all required variables in your hosting platform
3. **Port Configuration**: Most platforms set PORT automatically
4. **SSL/TLS**: Enable for production databases

## تاقیکردنەوە | Testing

After deployment, test these endpoints:
- `/` - Landing page
- `/dashboard` - Dashboard
- `/waredat2023` - Main application
- `/api/test` - Database connection test
