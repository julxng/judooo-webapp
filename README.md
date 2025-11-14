# Judooo Webapp

**Art Event Discovery Platform with Advanced Admin Management**

> Discover, explore, and manage Vietnamese art events at your fingertips.
> Reference: [judooo.com](https://judooo.com)

## 📋 Project Overview

This is a full-stack web application for discovering and managing art events in Vietnam. The platform provides:

### 🎨 User Features
- **Event Discovery**: Browse upcoming art events with advanced filtering
- **Smart Filters**: Filter by date, location, event type, art medium, and more
- **Event Details**: View comprehensive event information including location maps
- **Save Events**: Bookmark favorite events for later reference
- **Language Support**: Vietnamese (VI) and English (EN)

### 🛠️ Admin Features
- **Event Management**: Create, edit, and delete art events
- **Dynamic Filters**: Configure which filters are available to users
- **Event Gallery**: Upload and manage multiple images per event
- **Featured Events**: Manually select hero section featured events

## 📁 Project Structure

```
judooo-webapp/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   └── styles/
│   └── package.json
├── backend/
│   ├── config/
│   ├── routes/
│   ├── models/
│   ├── controllers/
│   └── package.json
├── docs/
│   └── API_REFERENCE.md
├── README.md
├── REQUIREMENTS.md
└── .gitignore
```

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- npm or yarn
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/julxng/judooo-webapp.git
   cd judooo-webapp
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   npm start
   ```
   Backend runs on `http://localhost:5000`

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   npm start
   ```
   Frontend runs on `http://localhost:3000`

## 📊 Data Schema

### Event Fields
- `name_vie`: Event name in Vietnamese
- `name_en`: Event name in English
- `description_vie`: Vietnamese description
- `description_en`: English description
- `image_url`: Featured image
- `art_medium`: Type of art (painting, sculpture, etc.)
- `event_type`: Exhibition, festival, workshop, etc.
- `place_type`: Gallery, museum, outdoor, online, etc.
- `start_date`, `end_date`: Event dates
- `city`, `district`: Location info
- `is_virtual`: Boolean for virtual events
- `is_free`: Boolean for free events
- `price`: Price if applicable
- `address`: Physical address
- `google_map_link`: Map embed
- `latitude`, `longitude`: Coordinates
- `registration_link`: External registration URL
- `tags`: Event tags
- `saved_count`: Popularity metric

## 🔍 Available Filters

- Name / Search
- Description
- Art Medium
- Event Type
- Place Type
- Start Date / End Date
- City
- District
- Is Virtual
- Is Free
- Price Range
- Registration Required
- Tags

## 📄 Key Pages

### Home Page
- **Hero Section**: Featured events (admin-selected)
- **Sắp hết**: Ending soon events
- **Mới**: Newly added events
- **Free**: Free events
- **Hot**: Popular events

### Admin Dashboard
- Event CRUD operations
- Filter configuration
- Image management
- Event analytics

## 🎨 Design Reference

- **Figma**: [Design file](https://www.figma.com/design/RINHgEbIgrd9nGiunic6JM/Untitled)
- **Font**: Nunito Sans
- **Language**: Vietnamese (primary) + English

## 📚 Documentation

- [Requirements](./REQUIREMENTS.md) - Detailed project requirements
- [API Reference](./docs/API_REFERENCE.md) - API endpoints and schemas

## 🔧 Stack

**Frontend**: React, CSS3, JavaScript
**Backend**: Node.js, Express
**Database**: To be determined
**Deployment**: TBD

## 🤝 Contributing

This is a reference implementation. Future developers should:

1. Refer to REQUIREMENTS.md for complete specs
2. Check the Figma file for design reference
3. Follow the existing code structure
4. Maintain language support (VI/EN)

## 📝 License

Private project - for Judooo.com only

## 👥 Author

Initial setup for art event management platform

---

**Last Updated**: January 2025
