# Judooo Webapp - Detailed Requirements

**Project**: Art Event Discovery Platform
**Status**: Development Ready
**Reference**: [judooo.com](https://judooo.com)
**Design**: [Figma](https://www.figma.com/design/RINHgEbIgrd9nGiunic6JM/Untitled)
**Font**: Nunito Sans

---

## Core Features

### 1. Event Browsing & Discovery

**Home Page Sections**:
- **Hero Section**: Featured events with full-width images (admin-selected)
  - Show 1 event per section with overlaid title, start date, end date
  - Manually controlled by admin

- **Sắp hết (Last Chance)**: Events ending soon
  - Ordered: earliest to latest end_date
  - Horizontal scroll cards (10 max)
  - Show: name, image, start date, city
  - "Xem thêm" button to filtered view

- **Mới (Newly Added)**: Recent events
  - Ordered by start date
  - Horizontal scroll (10 max)
  - "Xem thêm" button

- **Free (Free Events)**: Events with is_free = true
  - Horizontal scroll cards
  - "Xem thêm" button

- **Hot (Popular)**: Events sorted by saved_count
  - Horizontal scroll cards
  - "Xem thêm" button

### 2. Advanced Filtering

**Configurable Filters** (Admin can enable/disable):
- Name / Full-text Search
- Description
- Art Medium
- Event Type
- Place Type
- Start Date
- End Date
- City
- District
- Is Virtual (yes/no)
- Is Free (yes/no)
- Price Range
- Registration Required
- Tags

**Search Behavior**:
- Real-time as users type
- Multiple filter combinations
- Default: Show all if no filters applied

### 3. Event Details Page

**Displays**:
- Event name (Vietnamese & English)
- Full description (Vietnamese & English)
- All images/gallery
- Location: address, city, district, map embed
- Event dates: start_date, end_date
- Art medium, event type, place type
- Price (if applicable)
- Registration link (if available)
- Tags
- Saved count / popularity
- Social media video (if available)

**Actions**:
- Save event (bookmark)
- Share event
- View location on map

### 4. Admin Dashboard

**Event Management**:
- **Create**: Add new event with all required fields
- **Read**: View all events in table/list
- **Update**: Edit event details
- **Delete**: Remove events
- **Bulk Actions**: Select multiple events (future)

**Filter Management**:
- Toggle which filters appear to users
- Customize filter order
- Enable/disable based on feedback

**Featured Events**:
- Select events for hero section
- Drag-to-reorder
- Preview hero appearance

**Image Gallery**:
- Upload multiple images per event
- Set featured image
- Reorder images
- Delete images

---

## Data Schema

### Event Model

```javascript
{
  id: unique_identifier,
  
  // Bilingual content
  name_vie: string,
  name_en: string,
  description_vie: text,
  description_en: text,
  
  // Imagery
  image_url: string (featured image),
  socialvideo_url: string (optional),
  
  // Categorization
  art_medium: string, // painting, sculpture, photography, etc.
  event_type: string, // exhibition, festival, workshop, etc.
  place_type: string, // gallery, museum, outdoor, online, etc.
  
  // Dates
  start_date: datetime,
  end_date: datetime,
  
  // Location
  city: string,
  district: string,
  address: string,
  google_map_link: string (embed URL),
  latitude: number,
  longitude: number,
  
  // Event Info
  is_virtual: boolean,
  is_free: boolean,
  price: number (optional),
  registration_link: string (optional),
  
  // Tagging & Metadata
  tags: array<string>,
  saved_count: number (default: 0),
  
  // System
  created_at: datetime,
  updated_at: datetime,
  created_by: user_id,
  is_featured: boolean (for hero section)
}
```

---

## API Endpoints (TBD)

### Events
- `GET /api/events` - List all events with filters
- `GET /api/events/:id` - Get event details
- `POST /api/events` - Create event (admin)
- `PUT /api/events/:id` - Update event (admin)
- `DELETE /api/events/:id` - Delete event (admin)

### Admin
- `GET /api/admin/filters` - Get filter config
- `POST /api/admin/filters` - Update filter config
- `GET /api/admin/featured` - Get featured events
- `POST /api/admin/featured` - Set featured events

### User Interactions
- `POST /api/events/:id/save` - Save/bookmark event
- `DELETE /api/events/:id/save` - Unsave event
- `GET /api/user/saved` - Get user's saved events

---

## UI/UX Specifications

### Language Support
- Primary: Vietnamese (VI)
- Secondary: English (EN)
- Language switcher in header

### Design Font
- **Font Family**: Nunito Sans
- Apply to all text elements

### Responsive Design
- Mobile-first approach
- Breakpoints: 320px, 768px, 1024px, 1440px
- Touch-friendly on mobile
- Desktop optimizations

### Components
- Event cards (horizontal scroll, vertical grid)
- Filter panel (collapsible on mobile)
- Navigation header with language switcher
- Admin sidebar (dashboard)
- Modal forms (create/edit events)
- Image gallery slider
- Map embed component

---

## Technology Stack (Recommended)

**Frontend**:
- React 18+
- React Router for navigation
- Axios for API calls
- CSS-in-JS or CSS Modules for styling
- Responsive design utilities

**Backend**:
- Node.js + Express
- RESTful API architecture
- Database: (TBD - MongoDB, PostgreSQL, etc.)
- Authentication: (TBD)

**Deployment**:
- Frontend: Vercel/Netlify
- Backend: Heroku/AWS/DigitalOcean
- Database: Cloud-hosted

---

## Development Phases

### Phase 1: MVP
- Event listing page
- Basic filters
- Event details page
- Simple admin dashboard

### Phase 2: Polish
- Advanced filtering
- Hero section management
- Image gallery
- User saved events

### Phase 3: Enhancement
- Analytics dashboard
- Bulk operations
- Calendar view
- Map view
- Social sharing

---

## Notes for Developers

1. **Language**: Always support both Vietnamese (primary) and English
2. **Dates**: Use ISO 8601 format internally, display in local format
3. **Images**: Optimize for web; support multiple formats
4. **Performance**: Implement pagination/virtualization for large lists
5. **Accessibility**: Follow WCAG 2.1 AA standards
6. **Testing**: Unit tests for components, integration tests for API
7. **Git Workflow**: Feature branches, pull request reviews
8. **Documentation**: Keep docs updated with code changes

---

**Last Updated**: January 2025
**Reference Doc**: [Google Doc - judooo v2. 09.01.2025](https://docs.google.com/document/d/170APgACcxFo_mIm0713bOEncKaEkRPHPduXL58iI6L4/edit)
