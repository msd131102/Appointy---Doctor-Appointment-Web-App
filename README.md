# 🎯 Modex Assessment - Appointy Doctor Booking System

> **📊 Assessment Scale**: 2,500 candidates | **⏱️ Duration**: Self-paced | **🎯 Goal**: Stand out from the crowd

---

## 🌟 Introduction

Welcome to the Modex Assessment for the Appointy Doctor Appointment Booking System. This is a production-ready, full-stack MERN application that serves as the foundation for your technical evaluation.

**💡 Important Note**: We understand that many candidates will rely on AI tools during this assessment. However, this is your opportunity to demonstrate genuine expertise, creativity, and problem-solving skills that go beyond automated solutions.

---

## 🎯 Assessment Objectives

### 🚀 What We're Looking For

1. **Technical Excellence**: Deep understanding of MERN stack architecture
2. **Problem-Solving**: Ability to identify and resolve complex issues
3. **Code Quality**: Clean, maintainable, and well-documented code
4. **Innovation**: Creative solutions and feature enhancements
5. **Best Practices**: Security, performance, and scalability considerations

### 🏆 How to Stand Out

- **Don't just fix bugs** - improve the overall architecture
- **Don't just add features** - explain the business value
- **Don't just use AI** - demonstrate genuine understanding
- **Don't just complete tasks** - document your thought process

# 🏥 Appointy - Complete Doctor Appointment Booking System

A full-stack MERN application for booking doctor appointments with separate interfaces for patients, doctors, and administrators.

## 👨‍💻 Created by [Shiva](https://github.com/msd131102)

**🔗 GitHub Repository**: [https://github.com/msd131102/Appointy---Doctor-Appointment-Web-App](https://github.com/msd131102)

**📧 Contact**: NA

---

## 🌟 Features

### 👤 Patient Features
- Browse doctors by specialty
- Book appointments online
- Pay via Stripe or Razorpay
- View appointment history
- Manage profile
- Cancel/reschedule appointments

### 👨‍⚕️ Doctor Features
- Manage availability
- View appointment schedule
- Update profile information
- Manage patient appointments
- Track earnings

### 👨‍💼 Admin Features
- Dashboard with analytics
- Manage doctors and patients
- View all appointments
- Add/remove doctors
- System configuration

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │      Admin     │    │     Backend     │
│   (React)       │    │     (React)     │    │    (Node.js)    │
│                 │    │                 │    │                 │
│ • Patient UI    │    │ • Admin UI      │    │ • REST API      │
│ • Doctor Browse │    │ • Dashboard     │    │ • Auth (JWT)    │
│ • Booking       │    │ • Management    │    │ • Payment       │
│ • Payments      │    │ • Analytics     │    │ • File Upload   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────┐
                    │   MongoDB       │
                    │   Atlas         │
                    │                 │
                    │ • Users         │
                    │ • Doctors       │
                    │ • Appointments  │
                    └─────────────────┘
```

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- MongoDB Atlas account
- Stripe/Razorpay account
- Cloudinary account

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/msd131102/Appointy---Doctor-Appointment-Web-App
cd appointy
```

2. **Install dependencies**
```bash
# Backend
cd backend
npm install

# Frontend
cd ../frontend
npm install

# Admin
cd ../admin
npm install
```

3. **Environment Setup**

Create `.env` files in each directory:

**Backend (.env)**
```env
MONGO_URI=mongodb+srv://YOUR_USERNAME:YOUR_PASSWORD@cluster0.m0h23x0.mongodb.net/?appName=Cluster0
JWT_SECRET=your_jwt_secret_minimum_32_characters
STRIPE_API_KEY=sk_test_YOUR_STRIPE_SECRET_KEY
RAZORPAY_KEY_ID=rzp_test_YOUR_RAZORPAY_KEY_ID
RAZORPAY_KEY_SECRET=YOUR_RAZORPAY_KEY_SECRET
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key
CURRENCY=INR
ADMIN_EMAIL=admin@appointy.com
ADMIN_PASSWORD=admin123
```

**Frontend (.env)**
```env
VITE_API_URL=http://localhost:4000
VITE_CLOUDINARY_NAME=your_cloudinary_name
```

**Admin (.env)**
```env
VITE_API_URL=http://localhost:4000
VITE_CLOUDINARY_NAME=your_cloudinary_name
```

4. **Start Development Servers**
```bash
# Backend (Terminal 1)
cd backend
npm run dev

# Frontend (Terminal 2)
cd frontend
npm run dev

# Admin (Terminal 3)
cd admin
npm run dev
```

5. **Access Applications**
- Frontend: http://localhost:5173
- Admin: http://localhost:5174
- API: http://localhost:4000

## 📱 Live Demo

### 🌐 **Live Application Links**

**🏥 Patient Application**
- **URL**: https://appointy-doctor-appointment-web-app.onrender.com
- **Features**: Book appointments, browse doctors, manage profile
- **Test Credentials**: Use any email to register or try existing users
- Email: user1@example.com
- Password: user1234

**👨‍💼 Admin Dashboard**
- **URL**: https://appointy-doctor-appointment-web-app-admin.onrender.com
- **Features**: Manage doctors, view analytics, system configuration
- **Test Credentials**: 
  - Email: admin@appointy.com
  - Password: admin123

**🔧 API Documentation**
- **Base URL**: https://appointy-backend.onrender.com
- **Interactive Docs**: Import Postman collection below for testing

### 🚀 **Quick Demo Experience**

1. **Patient Flow**: Register → Browse Doctors → Book Appointment → Make Payment
2. **Admin Flow**: Login → View Dashboard → Manage Doctors → Monitor Appointments
3. **Doctor Experience**: View Schedule → Manage Availability → Update Profile

### 📱 **Mobile Responsive**

The application is fully responsive and works seamlessly on:
- Desktop browsers
- Tablets
- Mobile devices

## 🔧 API Documentation

### Base URL
- Development: `http://localhost:4000`
- Production: `https://appointy-backend.onrender.com`

### Authentication
All protected endpoints require JWT token in headers:
```
Authorization: Bearer <token>
```

### Main Endpoints

#### User Authentication
```http
POST /api/user/register
POST /api/user/login
```

#### Doctor Management
```http
GET /api/doctor/list
POST /api/doctor/change-availability
GET /api/doctor/profile
POST /api/doctor/update-profile
```

#### Appointments
```http
POST /api/user/book-appointment
GET /api/user/appointments
POST /api/user/cancel-appointment
GET /api/admin/appointments
```

#### Admin
```http
POST /api/admin/add-doctor
GET /api/admin/all-doctors
POST /api/admin/login
```

## 🧪 Testing with Postman

1. **Import Collection**
   - Open Postman
   - Click Import
   - Select `Appointy_API_Collection.postman_collection.json`
   - Select `Appointy_Environment.postman_environment.json`

2. **Set Environment Variables**
   - Update variables with your actual values
   - Test endpoints starting with health checks

3. **Authentication Flow**
   - Register/login to get tokens
   - Use tokens for protected endpoints
   - Refresh tokens as needed

## 🚀 Deployment

### Render Deployment

1. **Update render.yaml**
   ```yaml
   services:
     - type: web
       name: appointy-backend
       env: node
       repo: 
       rootDir: backend
       buildCommand: npm install
       startCommand: npm start
       envVars:
         - key: NODE_ENV
           value: production
   ```

2. **Set Environment Variables in Render**
   - Go to Render dashboard
   - Add all backend environment variables
   - Configure frontend and admin URLs

3. **Deploy**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

### Environment Variables for Production

Set these in your deployment platform (NOT in code):

**Backend**
- `MONGO_URI`
- `JWT_SECRET`
- `STRIPE_API_KEY`
- `RAZORPAY_KEY_ID`
- `RAZORPAY_KEY_SECRET`
- `CLOUDINARY_NAME`
- `CLOUDINARY_API_KEY`
- `CLOUDINARY_SECRET_KEY`

**Frontend & Admin**
- `VITE_API_URL` (your production backend URL)
- `VITE_CLOUDINARY_NAME`

## 🏗️ Project Structure

```
appointy/
├── backend/                    # Node.js API Server
│   ├── config/                # Database and service configs
│   ├── controllers/           # Route controllers
│   ├── middlewares/            # Authentication and validation
│   ├── models/                # MongoDB schemas
│   ├── routes/                # API routes
│   ├── server.js              # Express server setup
│   └── package.json
├── frontend/                   # React Patient App
│   ├── src/
│   │   ├── components/        # Reusable components
│   │   ├── pages/            # Page components
│   │   ├── context/          # React context
│   │   └── assets/           # Images and icons
│   ├── public/
│   └── package.json
├── admin/                     # React Admin Dashboard
│   ├── src/
│   │   ├── components/        # Admin components
│   │   ├── pages/            # Admin pages
│   │   ├── context/          # Admin context
│   │   └── assets/           # Admin assets
│   ├── public/
│   └── package.json
├── docs/                      # Documentation
├── render.yaml                # Render deployment config
└── README.md
```

## 🔐 Security & Compliance

### 🛡️ Authentication & Authorization
- **JWT-based Authentication**: Secure token-based authentication with expiration
- **Role-Based Access Control (RBAC)**: User/Doctor/Admin role segregation
- **Secure Password Hashing**: bcrypt with salt rounds (12+)
- **Session Management**: Automatic token refresh and invalidation
- **Multi-Factor Authentication**: Ready for 2FA implementation

### 💳 Payment Security
- **PCI DSS Compliance**: Secure payment handling through Stripe/Razorpay
- **Webhook Verification**: Cryptographic signature verification
- **SSL/TLS Encryption**: End-to-end encryption for all transactions
- **Fraud Detection**: Integrated payment gateway security measures
- **Audit Logging**: Complete payment transaction logs

### 🔒 Data Protection & Privacy
- **Input Validation & Sanitization**: XSS and SQL injection prevention
- **CORS Configuration**: Restricted cross-origin requests
- **Rate Limiting**: DDoS and brute force protection
- **Environment Variable Protection**: Secure credential management
- **Data Encryption**: Sensitive data encryption at rest and in transit
- **GDPR Compliance**: User data handling and privacy controls

### 🌐 Network Security
- **HTTPS Enforcement**: SSL/TLS for all endpoints
- **Security Headers**: HSTS, CSP, X-Frame-Options, etc.
- **API Rate Limiting**: Request throttling per user/IP
- **IP Whitelisting**: Admin access restrictions
- **Firewall Configuration**: Network-level protection

### 🔍 Security Monitoring
- **Audit Trails**: Complete user action logging
- **Error Handling**: Secure error responses without information leakage
- **Security Headers**: OWASP recommended headers implementation
- **Vulnerability Scanning**: Regular dependency updates and scanning
- **Intrusion Detection**: Suspicious activity monitoring

### 📋 Security Best Practices Implemented

#### Authentication Security
```javascript
// JWT Configuration
- Token expiration: 15 minutes (access), 7 days (refresh)
- Secure token storage: HttpOnly cookies
- Password requirements: 8+ chars, uppercase, lowercase, numbers, symbols
- Account lockout: 5 failed attempts = 15 minute lockout
```

#### API Security
```javascript
// Security Middleware
- Helmet.js for security headers
- Express rate limit: 100 requests per 15 minutes
- Request validation with Joi/Yup
- SQL injection prevention with Mongoose
- File upload security with Multer
```

#### Database Security
```javascript
// MongoDB Security
- Connection string with TLS/SSL
- Database user with limited privileges
- Field-level encryption for sensitive data
- Query injection prevention
- Regular backup with encryption
```

### 🚨 Security Checklist

#### ✅ Implemented
- [x] Password hashing with bcrypt
- [x] JWT token authentication
- [x] CORS configuration
- [x] Input validation
- [x] Rate limiting
- [x] HTTPS enforcement
- [x] Security headers
- [x] Environment variables
- [x] File upload security
- [x] Payment gateway security

#### 🔄 Regular Maintenance
- [ ] Weekly dependency updates
- [ ] Monthly security scans
- [ ] Quarterly penetration testing
- [ ] Annual security audit
- [ ] Security training updates

### 🛠️ Security Tools Used

#### Backend Security
- **Helmet.js**: Security headers middleware
- **bcryptjs**: Password hashing
- **jsonwebtoken**: JWT authentication
- **express-rate-limit**: Rate limiting
- **joi**: Input validation
- **multer**: Secure file uploads

#### Frontend Security
- **DOMPurify**: XSS prevention
- **Axios interceptors**: Request/response security
- **Local storage security**: Token management
- **CSP headers**: Content Security Policy

#### Infrastructure Security
- **MongoDB Atlas**: Enterprise-grade security
- **Cloudinary**: Secure media storage
- **Render**: Secure deployment platform
- **GitHub**: Secure code management

### 🔐 Environment Security

#### Production Environment Variables
```env
# Security Configuration
NODE_ENV=production
JWT_SECRET=your_super_secure_jwt_secret_key_minimum_32_characters
JWT_REFRESH_SECRET=your_refresh_token_secret_key
BCRYPT_ROUNDS=12

# Database Security
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/dbname?ssl=true&authSource=admin

# Payment Security
STRIPE_WEBHOOK_SECRET=whsec_your_webhook_secret
RAZORPAY_WEBHOOK_SECRET=your_webhook_secret

# File Upload Security
CLOUDINARY_SECRET_KEY=your_cloudinary_secret
MAX_FILE_SIZE=5242880  # 5MB
ALLOWED_FILE_TYPES=jpg,jpeg,png,pdf

# Rate Limiting
RATE_LIMIT_WINDOW_MS=900000  # 15 minutes
RATE_LIMIT_MAX_REQUESTS=100
```

### 🚨 Incident Response Plan

#### Security Incident Types
1. **Data Breach**: Immediate containment and notification
2. **DDoS Attack**: Rate limiting and IP blocking
3. **Unauthorized Access**: Account suspension and password reset
4. **Payment Fraud**: Transaction blocking and investigation

#### Response Procedures
1. **Detection**: Automated monitoring and alerts
2. **Containment**: Immediate isolation of affected systems
3. **Investigation**: Forensic analysis and log review
4. **Recovery**: System restoration and security patches
5. **Reporting**: User notification and regulatory compliance

### 📞 Security Contact

For security-related issues:
- **Security Team**: security@appointy.com
- **Bug Bounty**: Report vulnerabilities responsibly
- **Emergency Response**: +1-XXX-XXX-XXXX (24/7)

---

**⚠️ Security Notice**: This application implements industry-standard security practices. However, no system is completely secure. Regular security audits and updates are essential for maintaining security posture.

## 🛠️ Technologies Used

### Frontend
- React 18
- Vite
- Tailwind CSS
- Axios
- React Router

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- Multer
- Cloudinary

### Payment
- Stripe
- Razorpay

### Deployment
- Render
- MongoDB Atlas
- Cloudinary

## 🐛 Troubleshooting

### Common Issues

1. **MongoDB Connection Error**
   - Check MONGO_URI in backend/.env
   - Verify IP whitelist in MongoDB Atlas
   - Ensure database user has correct permissions

2. **CORS Errors**
   - Verify frontend URL in backend CORS config
   - Check environment variables
   - Ensure API_URL is correct in frontend

3. **Payment Gateway Issues**
   - Verify API keys are correct
   - Check webhook URLs
   - Ensure test mode is enabled

4. **Image Upload Issues**
   - Check Cloudinary credentials
   - Verify file size limits
   - Check multer configuration

### Debug Mode

Enable debug logging:
```bash
# Backend
DEBUG=appointy:* npm run dev

# Frontend
VITE_DEBUG=true npm run dev
```

## 📊 Monitoring & Analytics

### Health Checks
```http
GET /api/health
```

### Monitoring Tools
- Render built-in monitoring
- MongoDB Atlas metrics
- Custom error logging

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

### Development Guidelines
- Follow ESLint rules
- Write meaningful commit messages
- Update documentation
- Test before deploying

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support

For support and questions:

- Create an issue in GitHub
- Email: support@appointy.com
- Documentation: Check `/docs` folder

## 🔄 Updates & Changelog

### Version 2.0.0
- Added React Admin Dashboard
- Implemented payment gateways
- Enhanced security features
- Mobile-responsive design

### Version 1.0.0
- Basic appointment booking
- User authentication
- Doctor management
- MongoDB integration

## 🎯 Roadmap

### Upcoming Features
- [ ] Video consultation integration
- [ ] Prescription management
- [ ] SMS/Email notifications
- [ ] Advanced analytics dashboard
- [ ] Mobile apps (iOS/Android)
- [ ] Multi-language support

### Improvements
- [ ] Performance optimization
- [ ] Enhanced security
- [ ] Better error handling
- [ ] Automated testing

---

## 🚀 Quick Deployment Command

For immediate deployment to Render:

```bash
# After setting up environment variables
git add .
git commit -m "Deploy to Render"
git push origin main
```

Your application will be live at:
- Frontend:https://appointy-doctor-appointment-web-app.onrender.com
- Admin:https://appointy-doctor-appointment-web-app-admin.onrender.com
- API: https://appointy-backend.onrender.com

---

**⚠️ Security Note**: Never commit real API keys or sensitive data to version control. Always use environment variables for production deployments.


