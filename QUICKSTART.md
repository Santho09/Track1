# Quick Start Guide

## 🚀 Get Started in 3 Steps

### Step 1: Install Backend Dependencies
```bash
cd backend
npm install
```

### Step 2: Start the Backend Server
```bash
npm start
```
You should see: `🚀 Server is running on http://localhost:3000`

### Step 3: Open the Frontend
**Option A: Direct File Open**
- Simply open `frontend/index.html` in your browser

**Option B: Local Server (Recommended)**
```bash
# From the project root
cd frontend
python -m http.server 8000
# Then visit http://localhost:8000
```

## ✅ Test the Application

1. **Browse Products**: You should see 12 products displayed
2. **Test Search**: Type "headphones" in the search bar
3. **Test Filters**: Select a category from the dropdown
4. **Add Favorites**: Click the heart icon on any product
5. **View Favorites**: Click the floating action button (bottom right)
6. **Test Dark Mode**: Click the moon icon in the navigation
7. **Create Account**: Click "Login" → "Sign Up" tab
8. **Login**: Use your credentials to login
9. **View Dashboard**: Click "Dashboard" in the navigation
10. **Add to Cart**: Click "Add to Cart" on any product (requires login)

## 🎯 Default Test Account

After creating an account, you can use it to test:
- Email: `test@example.com`
- Password: `password123` (or any password you set)

## 📝 Notes

- The backend must be running for authentication to work
- Products are loaded from `frontend/data.json`
- Favorites are stored in browser localStorage
- Purchase history is stored in browser localStorage
- User data is stored in `backend/users.json` (auto-created)

## 🐛 Troubleshooting

**Backend won't start?**
- Make sure Node.js is installed: `node --version`
- Check if port 3000 is available
- Run `npm install` in the backend directory

**Frontend can't connect?**
- Ensure backend is running on port 3000
- Check browser console for errors
- Verify CORS is enabled (it should be by default)

**Products not showing?**
- Check that `data.json` exists in the `frontend/` folder
- Open browser console (F12) to see any errors
- Try refreshing the page

Happy coding! 🎉

