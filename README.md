# Travel, Health, Education & Social Hub

A comprehensive platform connecting people through travel experiences, health tips, educational resources, and social networking.

## 🚀 Features

### 🌍 Travel
- Destination discovery and recommendations
- Trip planning tools
- User reviews and ratings
- Travel itineraries
- Hotel and flight information

### 💪 Health Tips
- Wellness articles and tips
- Nutrition guides
- Fitness routines
- Mental health resources
- Health tracking

### 📚 Education
- Online courses and tutorials
- Learning resources
- Expert articles
- Certification paths
- Community learning

### 👥 Social Hub
- User profiles and connections
- Direct messaging
- Community discussions
- Activity feed
- Friend recommendations

## 🛠 Tech Stack

### Frontend
- **Framework**: Next.js 14+
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **State Management**: Redux Toolkit
- **HTTP Client**: Axios
- **Icons**: Lucide React

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: MongoDB
- **Authentication**: JWT
- **Real-time**: Socket.io
- **Security**: Helmet, CORS

### DevOps
- **Version Control**: Git/GitHub
- **Containerization**: Docker & Docker Compose
- **CI/CD**: GitHub Actions

## 📁 Project Structure

```
Beyond_the_Grid/
├── frontend/                  # Next.js application
│   ├── app/                   # App router
│   ├── components/            # React components
│   ├── public/                # Static assets
│   ├── package.json
│   ├── tsconfig.json
│   ├── tailwind.config.js
│   ├── next.config.js
│   └── Dockerfile.dev
│
├── backend/                   # Express.js API
│   ├── src/
│   │   ├── models/            # MongoDB schemas
│   │   ├── routes/            # API routes
│   │   ├── controllers/       # Business logic
│   │   ├── middleware/        # Auth, validation
│   │   ├── utils/             # Helpers
│   │   └── server.ts          # Entry point
│   ├── package.json
│   ├── tsconfig.json
│   ├── .env.example
│   └── Dockerfile
│
├── docker-compose.yml         # Docker services
├── package.json              # Root package.json
├── .gitignore
├── .github/
│   └── workflows/
│       └── ci.yml            # GitHub Actions CI/CD
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- MongoDB 5.0+ (or use Docker)
- Git
- Docker & Docker Compose (optional but recommended)

### Quick Start with Docker (Recommended)

```bash
# 1. Clone the repository
git clone https://github.com/lukexingsn-web/Beyond_the_Grid.git
cd Beyond_the_Grid

# 2. Start all services
docker-compose up -d

# 3. Access the application:
# - Frontend: http://localhost:3000
# - Backend API: http://localhost:5000
# - MongoDB Express (Database UI): http://localhost:8081
# - API Health Check: http://localhost:5000/api/health
```

### Manual Setup

**Backend Setup:**
```bash
cd backend

# Copy environment file
cp .env.example .env

# Install dependencies
npm install

# Start development server
npm run dev
```

**Frontend Setup (in another terminal):**
```bash
cd frontend

# Copy environment file
cp .env.example .env

# Install dependencies
npm install

# Start development server
npm run dev
```

## 🔧 Environment Variables

### Backend (.env)
```
# Database
MONGODB_URI=mongodb://admin:password@localhost:27017/travel_hub?authSource=admin

# JWT
JWT_SECRET=your_jwt_secret_key_change_in_production
JWT_EXPIRE=7d

# Server
PORT=5000
NODE_ENV=development
API_URL=http://localhost:5000

# Frontend
FRONTEND_URL=http://localhost:3000

# Email Service (Optional)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password

# AWS S3 (Optional)
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_S3_BUCKET=your_bucket_name
AWS_REGION=us-east-1
```

### Frontend (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:5000/api
NEXT_PUBLIC_SOCKET_URL=http://localhost:5000
```

## 📊 Database Schema

### Users Collection
- Username, email, password (hashed)
- Avatar, bio, interests
- Followers/following relationships
- Subscription level

### Travel Collection
- Destinations, reviews, ratings
- Itineraries, plans
- User bookmarks/wishlist

### Health Collection
- Articles, tips, guides
- User health tracking data
- Preferences and goals

### Education Collection
- Courses, modules, lessons
- Certifications
- Progress tracking

### Social Collection
- Messages and conversations
- User connections
- Activity feed
- Notifications

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/profile` - Get current user profile

### Travel
- `GET /api/travel/destinations` - Get all destinations
- `GET /api/travel/destinations/:id` - Get destination details
- `POST /api/travel/itineraries` - Create itinerary

### Health
- `GET /api/health/tips` - Get health tips
- `GET /api/health/articles` - Get health articles
- `POST /api/health/track` - Track health data

### Education
- `GET /api/education/courses` - Get courses
- `GET /api/education/courses/:id` - Get course details
- `POST /api/education/enroll` - Enroll in course

### Social
- `GET /api/social/users` - Search users
- `POST /api/social/connect` - Send friend request
- `GET /api/social/messages` - Get messages
- `POST /api/social/messages` - Send message

## 🧪 Testing

```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test

# Lint code
npm run lint

# Type checking
npm run type-check
```

## 📦 Build & Deployment

### Build for Production
```bash
npm run build
```

### Deploy Frontend (Vercel)
```bash
npm install -g vercel
vercel
```

### Deploy Backend (Docker)
```bash
# Build Docker image
docker build -t travel-hub-backend:latest ./backend

# Push to registry and deploy
docker push your-registry/travel-hub-backend:latest
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 💬 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Contact the development team

## 🗺️ Roadmap

- [x] Project setup and structure
- [x] Docker configuration
- [ ] User authentication & profiles
- [ ] Travel module MVP
- [ ] Health tips section
- [ ] Education platform
- [ ] Social messaging
- [ ] Real-time notifications
- [ ] Payment integration
- [ ] Mobile app
- [ ] AI recommendations
- [ ] Analytics dashboard

---

**Built with ❤️ by the Beyond the Grid Team**
