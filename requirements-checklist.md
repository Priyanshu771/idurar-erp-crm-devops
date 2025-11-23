# ✅ Requirements Checklist – IDURAR ERP CRM

This checklist ensures the project can run smoothly on any machine before development or deployment.

---

## 🖥️ System Requirements

### **1. Operating System**
- Windows 10/11  
- Ubuntu 20.04+ / Debian / macOS  
- Recommended: Ubuntu (for Docker + CI/CD)

---

## 🔧 Required Software

### **2. Node.js**
- Minimum version: **Node.js 20+**
node -v

markdown
Copy code

### **3. NPM**
npm -v

yaml
Copy code

---

## 🐳 Docker Requirements

### **4. Docker**
- Docker version 24+
docker -v

markdown
Copy code

### **5. Docker Compose**
- Version 2.20+
docker compose version

yaml
Copy code

---

## 🌐 Backend Requirements

### **6. Environment Variables**
File: `backend/.env`
DATABASE="mongodb://admin:password123@mongo:27017/idurar_db?authSource=admin"
JWT_SECRET="your_private_secret"
NODE_ENV="production"
PUBLIC_SERVER_FILE="http://localhost:5000/"

yaml
Copy code

---

## 🎨 Frontend Requirements

### **7. Environment Variables**
File: `frontend/.env`
VITE_BACKEND_SERVER="http://localhost:5000/"
VITE_FILE_BASE_URL="http://localhost:5000/"

yaml
Copy code

---

## 🗄️ Database Requirements

### **8. MongoDB**
Options:
- Local Docker MongoDB
- OR MongoDB Atlas

Default Docker Mongo:
mongo:6
username: admin
password: password123
database: idurar_db

yaml
Copy code

---

## 🚀 Project Startup Checklist

### **9. Backend**
cd backend
npm install
npm run setup
npm start

markdown
Copy code

### **10. Frontend**
cd frontend
npm install
npm run build
npm run preview

markdown
Copy code

### **11. Docker Setup**
docker-compose up --build -d

yaml
Copy code

---

## ✔ Confirm Everything Works
- [ ] MongoDB running  
- [ ] Backend reachable at `http://localhost:5000/api`  
- [ ] Frontend reachable at `http://localhost:5173`  
- [ ] Login working  
- [ ] Docker builds successful  

---

## 🎯 CI/CD Requirements

- GitHub Actions enabled  
- Docker Hub credentials configured  
- Workflow file: `.github/workflows/ci-cd.yml`  

---

# ✅ All requirements fulfilled. Ready for development & deployment.