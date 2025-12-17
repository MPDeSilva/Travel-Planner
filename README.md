# Travel Planner App

A full-stack travel planning application built with modern web technologies, demonstrating production-ready architecture, API integrations, and interactive user experiences.

## 🎯 Project Overview

This application allows users to create and manage travel itineraries with interactive maps, drag-and-drop functionality, and real-time location geocoding. Built to showcase expertise in full-stack development, database design, and third-party API integration.

## ✨ Key Features

- **Authentication & Authorization**: Secure OAuth 2.0 authentication using NextAuth.js with GitHub provider
- **Interactive Trip Planning**: Create trips with dates, descriptions, and cover images
- **Location Management**: Add destinations with automatic geocoding via Google Maps API
- **Drag & Drop Itineraries**: Reorder locations with smooth animations using dnd-kit
- **Interactive Maps**: Visualize trip locations with Google Maps JavaScript API integration
- **3D Globe Visualization**: Interactive globe view for exploring trip destinations
- **File Uploads**: Seamless image uploads with UploadThing integration
- **Responsive Design**: Mobile-first UI built with Tailwind CSS and shadcn/ui components

## 🛠️ Technology Stack

### Frontend
- **Framework**: Next.js 15 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS 4
- **UI Components**: Radix UI, shadcn/ui
- **Maps**: Google Maps JavaScript API, react-globe.gl
- **Drag & Drop**: @dnd-kit/core, @dnd-kit/sortable
- **Icons**: Lucide React

### Backend
- **Runtime**: Node.js
- **API**: Next.js API Routes (Server Actions)
- **Authentication**: NextAuth.js v5
- **Database**: PostgreSQL
- **ORM**: Prisma
- **File Storage**: UploadThing

### APIs & Services
- Google Maps Geocoding API
- Google Maps JavaScript API
- GitHub OAuth
- UploadThing for file management

## 🏗️ Technical Highlights

### Database Design
Implemented a relational database schema with proper relationships:
- User authentication with accounts and sessions
- Trip management with user associations
- Location ordering with drag-and-drop persistence

### Server Actions
Utilized Next.js Server Actions for type-safe, server-side data mutations:
- `createTrip`: Trip creation with form validation
- `addLocation`: Geocoding addresses and storing coordinates
- `reorderItinerary`: Persisting drag-and-drop changes

### API Integration
- Integrated Google Maps Geocoding API for address-to-coordinate conversion
- Implemented Google Maps JavaScript API for interactive map displays
- Configured OAuth 2.0 flow with GitHub for authentication

### State Management
- Client-side state with React hooks
- Server state with Prisma and PostgreSQL
- Optimistic updates for better UX

### Type Safety
- End-to-end TypeScript implementation
- Prisma-generated types for database models
- Type-safe API routes and server actions

## 🚀 Getting Started

### Prerequisites
- Node.js 20+
- PostgreSQL database
- Google Cloud Platform account (for Maps API)
- GitHub OAuth App
- UploadThing account

### Environment Variables
Create a `.env.local` file with:

```env
DATABASE_URL="postgresql://..."
AUTH_SECRET="your-auth-secret"
AUTH_GITHUB_ID="your-github-oauth-id"
AUTH_GITHUB_SECRET="your-github-oauth-secret"
GOOGLE_MAPS_API_KEY="your-server-side-api-key"
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY="your-client-side-api-key"
UPLOADTHING_TOKEN="your-uploadthing-token"
```

### Installation

```bash
# Install dependencies
npm install

# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma migrate dev

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## 📝 Project Structure

```
├── app/                    # Next.js app router
│   ├── api/               # API routes (auth, trips, uploadthing)
│   ├── trips/             # Trip pages and routes
│   └── globe/             # Globe visualization
├── components/            # React components
│   ├── ui/               # Reusable UI components
│   ├── map.tsx           # Google Maps integration
│   └── sortable-itinerary.tsx  # Drag & drop functionality
├── lib/                   # Utility functions and actions
│   ├── actions/          # Server actions
│   └── prisma.ts         # Database client
└── prisma/               # Database schema and migrations
```

## 🎓 Skills Demonstrated

- **Full-Stack Development**: Building complete features from database to UI
- **Modern React Patterns**: Server Components, Client Components, and Server Actions
- **API Integration**: Working with third-party services and handling authentication
- **Database Design**: Relational modeling with Prisma ORM
- **User Experience**: Implementing drag-and-drop, loading states, and optimistic updates
- **Security**: OAuth implementation and environment variable management
- **TypeScript**: Type-safe development across the entire stack
- **Responsive Design**: Mobile-first approach with Tailwind CSS

## 🔧 Available Scripts

```bash
npm run dev          # Start development server with Turbopack
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
```

## 📦 Deployment

This application can be deployed on:
- **Vercel** (recommended for Next.js)
- **Railway** or **Render** (for PostgreSQL hosting)
- Any platform supporting Node.js and PostgreSQL

## 🤝 Contributing

This is a portfolio project, but suggestions and feedback are welcome!

## 📄 License

This project is open source and available under the MIT License.
