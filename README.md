# Job Application Tracker

A simple and intuitive web application to track your job applications, interview statuses, and rejections all in one place.

## 🎯 Overview

Job Application Tracker helps you organize and monitor your job search journey. Keep track of applications, mark them as selected for interviews or rejected, and get real-time statistics on your progress.

## ✨ Key Features

### 📊 **Application Management**
- View all job applications in a clean, organized card layout
- Add, update, and remove applications easily
- Track application status (Not Applied, Selected, Rejected)

### 📈 **Real-time Statistics**
- Total applications counter
- Interview selections counter
- Rejections counter
- Live job counter that updates as you filter

### 🔀 **Smart Filtering**
- **All** - View all job applications
- **Interview** - View applications selected for interviews
- **Rejected** - View rejected applications
- Toggle between views with a single click

### 🗑️ **Application Actions**
- Mark application as **INTERVIEW** (Selected)
- Mark application as **REJECTED**
- Delete applications with trash icon button
- Automatic status updates in real-time

### 🎨 **Clean UI Design**
- Responsive grid layout (1 column on mobile, 2 columns on tablet/desktop)
- Color-coded status badges
- Smooth animations and transitions
- Modern card-based interface

## 🚀 Quick Start

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No installation or dependencies required

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Sayeed-dev/Job-Application-Tracker.git
cd Job-Application-Tracker
```

2. **Open in browser**
```bash
# Simply open the index.html file in your browser
# Or use a local server:
python -m http.server 8000
# Then visit: http://localhost:8000
```

That's it! No build steps or server setup needed.

## 📁 Project Structure

```
Job-Application-Tracker/
├── index.html              # Main HTML file with application structure
├── script/
│   └── app.js             # Core JavaScript functionality
├── src/
│   ├── input.css          # Tailwind configuration and base styles
│   ├── output.css         # Compiled Tailwind CSS
│   └── favicon-32x32.png  # Favicon
└── README.md              # This file
```

## 🛠️ Technologies Used

### Frontend
- **HTML5** - Semantic markup and structure
- **JavaScript (Vanilla)** - Core logic and interactivity
- **Tailwind CSS v4** - Utility-first styling framework
- **Font Awesome** - Icon library

### Styling & Design
- **Tailwind CSS** - Modern CSS framework
- **Inter Font** - Google Fonts typography
- **Responsive Design** - Mobile-first approach

### No Dependencies
This project is built with vanilla JavaScript and requires **no npm packages** or build tools!

## 📄 Core Components

### HTML Structure
- **Tracking Area** - 3-column stat display (Total, Interview, Rejected)
- **Toggle Buttons** - Filter between All, Interview, and Rejected views
- **Cards Container** - Grid layout for displaying job applications
- **Application Cards** - Individual job listings with actions

### JavaScript Functionality

#### State Management
```javascript
interviewCollection = []    // Stores selected applications
rejectedCollection = []     // Stores rejected applications
```

#### Key Functions

**Count()** - Updates all counters
```javascript
Count() // Updates total, interview, rejected counters and live counter
```

**stateToggle(id)** - Switches between views
```javascript
stateToggle('all')        // Show all applications
stateToggle('interview')  // Show selected for interview
stateToggle('rejected')   // Show rejected applications
```

**stateHandler(event)** - Manages application status changes
- Moves applications between collections
- Updates UI in real-time
- Re-renders all sections

**interviewRender()** - Displays selected applications
**rejectionRender()** - Displays rejected applications

#### Delete Functions
- Removes applications from DOM and collections
- Updates counters automatically
- Maintains data integrity

## 📊 Data Structure

### Application Object
```javascript
{
  companyName: "Company Name",
  status: "Selected" | "Rejected" | "Not Applied"
}
```

### Tracking Collections
```javascript
// Example data structure
interviewCollection = [
  { companyName: "Mobile First Corp", status: "Selected" },
  { companyName: "TechCorp Industries", status: "Selected" }
]

rejectedCollection = [
  { companyName: "StartupXYZ", status: "Rejected" }
]
```

## 🎨 Design System

### Color Palette
- **Primary Blue**: `#3498db` - Total counter background
- **Success Green**: `#2ecc71` - Interview button & counter
- **Danger Red**: `#e74c3c` - Rejected button & counter
- **Dark Blue**: `#2c3e50` - Headings
- **Light Blue**: `#34495e` - Body text
- **Light Background**: `#F3F4F6` - Page background

### Typography
- **Font Family**: Inter (Google Fonts)
- **Headings**: Bold, 24-32px
- **Body Text**: Regular, 14-16px
- **Buttons**: Semibold, 14px

### Layout
- **Max Width**: 1200px centered container
- **Grid Columns**: 1 (mobile) → 2 (tablet/desktop)
- **Card Gap**: 32px spacing
- **Padding**: Responsive (3px to 6px padding)

## 📱 Responsive Design

- **Mobile** (< 768px): Single column layout
- **Tablet/Desktop** (≥ 768px): Two-column grid layout
- **Large Screens**: Centered max-width container
- **Flexible Cards**: Adapt to screen size

## 🎯 User Workflows

### Adding an Application
1. Application cards are pre-loaded in the "All" view
2. Each card shows job details (title, location, salary, description)

### Marking as Selected for Interview
1. Click the green **INTERVIEW** button on any card
2. Application moves to "Interview" section
3. Status badge updates to "Selected"
4. Interview counter increments

### Marking as Rejected
1. Click the red **REJECTED** button on any card
2. Application moves to "Rejected" section
3. Status badge updates to "Rejected"
4. Rejected counter increments

### Deleting an Application
1. Click the trash icon (right side of card)
2. Application removed from all sections
3. Counters update automatically

### Filtering Views
1. Click **All** tab - See all applications
2. Click **Interview** tab - See selected applications
3. Click **Rejected** tab - See rejected applications
4. Live counter updates based on active view

## 🚀 Build & Deployment

### Development
Simply open `index.html` in your browser or use a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server
```

### Deployment
Upload the entire project folder to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting
- AWS S3

No build process required!

## 🐛 Known Limitations

- Data is stored in browser memory (clears on page refresh)
- No backend database integration
- Limited to pre-loaded sample job data
- No user authentication
- No data export feature

## 📈 Future Enhancements

- [ ] **Local Storage** - Persist data between sessions
- [ ] **Add New Applications** - Form to add custom job listings
- [ ] **Database Integration** - Save data to backend
- [ ] **Search & Filter** - Find applications by company or role
- [ ] **Notes Section** - Add interview notes or follow-ups
- [ ] **Timestamps** - Track when applications were added/updated
- [ ] **Export Data** - Download application list as CSV/PDF
- [ ] **User Authentication** - Multi-user support
- [ ] **Dark Mode** - Theme toggle
- [ ] **Statistics Dashboard** - Visual charts and insights

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Sayeed-dev**
- GitHub: [@Sayeed-dev](https://github.com/Sayeed-dev)
- Project: [Job-Application-Tracker](https://github.com/Sayeed-dev/Job-Application-Tracker)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

### How to contribute:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit (`git commit -m 'Add amazing feature'`)
5. Push to branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## 📞 Support

For support, questions, or suggestions:
- Open an issue on GitHub
- Contact the author

---

## 🌟 Quick Tips

- **Color Meanings**:
  - 🔵 Blue = Total applications
  - 🟢 Green = Interview selected
  - 🔴 Red = Rejected

- **Status Indicators**:
  - 📝 Not Applied - Initial state
  - ✅ Selected - Marked for interview
  - ❌ Rejected - Application rejected

- **Keyboard Shortcuts** (Future enhancement):
  - Consider using keyboard shortcuts for faster navigation

---

**Built with ❤️ by Sayeed-dev | Track your job search progress with ease!**
