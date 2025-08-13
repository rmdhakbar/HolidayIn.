# HolidayIn - Tourism Website

![Project Status](https://img.shields.io/badge/Status-Active-green)
![PHP Version](https://img.shields.io/badge/PHP-7.4%2B-blue)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)

> A comprehensive tourism website showcasing beautiful destinations in Yogyakarta, Indonesia. Built with modern web technologies and featuring user authentication, interactive galleries, and responsive design.

## 🌟 Overview

HolidayIn is a tourism platform designed to promote and showcase the beautiful tourist destinations in Yogyakarta. The website provides an immersive experience with video backgrounds, detailed destination information, event listings, and user account management.

## 🚀 Key Features

- ✨ **Interactive Landing Page** with video slideshow backgrounds
- 🏞️ **Destination Showcase** with detailed information and photo galleries
- 🎉 **Event Listings** for tourism events and activities
- 👤 **User Authentication** (Registration/Login system)
- 📱 **Responsive Design** - works on desktop, tablet, and mobile
- 🖼️ **Image Galleries** with carousel functionality
- 🔐 **Secure Login System** with password hashing
- 🎨 **Modern UI/UX** with smooth animations and transitions

## 🛠️ Technology Stack

### **Frontend Technologies**

- **HTML5** - Semantic markup and structure
- **CSS3** - Modern styling with Flexbox and Grid
  - Custom animations and transitions
  - Responsive design principles
  - CSS Variables for theming
- **JavaScript (Vanilla)** - Interactive functionality
  - Image carousel/slider
  - Form validation
  - Dynamic navigation
  - Video background controls

### **Backend Technologies**

- **PHP 7.4+** - Server-side logic and authentication
  - Object-oriented programming approach
  - Secure password hashing with `password_hash()`
  - Form data validation and sanitization
  - Session management

### **Database**

- **MySQL/MariaDB** - Relational database management
  - User account storage
  - Secure data handling
  - UTF8MB4 character set support

### **External Libraries & Frameworks**

- **Google Fonts** - Typography (Poppins font family)
- **Font Awesome 5.14.0** - Icon library
- **BoxIcons 2.1.4** - Additional icons
- **Bootstrap 5.3.2** - CSS framework (used in some components)

### **Development Tools**

- **VS Code** - Primary development environment
- **Git** - Version control
- **XAMPP/LAMP** - Local development server

## 📂 Project Structure

```
PABW/
├── public/                          # Public web files
│   ├── index.html                   # Main landing page (formerly landingPage.html)
│   ├── login.html                   # Login page
│   ├── profile.html                 # User profile page
│   ├── assets/                      # Static assets
│   │   ├── css/                     # Stylesheets
│   │   │   ├── landingPage.css
│   │   │   ├── login.css
│   │   │   ├── profile.css
│   │   │   └── style.css
│   │   ├── js/                      # JavaScript files
│   │   │   ├── index.js
│   │   │   ├── landingPage.js
│   │   │   ├── login.js
│   │   │   └── profile.js
│   │   ├── images/                  # Images organized by category
│   │   │   ├── general/             # General images (logo, icons, etc.)
│   │   │   ├── destinations/        # Destination photos
│   │   │   ├── events/              # Event photos
│   │   │   └── profile/             # Profile/user images
│   │   └── videos/                  # Video files
│   │       ├── vid 1.mp4
│   │       ├── vid 2.mp4
│   │       ├── vid 3.mp4
│   │       ├── vid 4.mp4
│   │       └── vid 5.mp4
│   └── pages/                       # Additional pages
│       ├── destinations/            # Destination pages
│       │   ├── des1.html
│       │   ├── des2.html
│       │   ├── detbay.html
│       │   ├── detbreksi.html
│       │   ├── dethehaocean.html
│       │   ├── dethehasky.html
│       │   ├── detindrayanti.html
│       │   ├── detloka.html
│       │   ├── detngobaran.html
│       │   ├── detolxhills.html
│       │   ├── detpinusmangun.html
│       │   ├── detpramb.html
│       │   ├── detptritis.html
│       │   └── dettmnsari.html
│       └── events/                  # Event pages
│           ├── event1.html
│           └── eventdet1.html
├── src/                            # Backend source code
│   ├── config/                     # Configuration files
│   │   └── database.php            # Database configuration
│   └── controllers/                # PHP controllers
│       ├── login.php               # Login handler
│       └── Registrasi.php          # Registration handler
├── database/                       # Database files
│   └── berwisata.sql              # Database schema
├── docs/                          # Documentation and backups
│   └── backup/                    # Backup files
└── README.md                      # Project documentation
```

## Technologies Used

### **Frontend Stack**

| Technology   | Version | Purpose                                        |
| ------------ | ------- | ---------------------------------------------- |
| HTML5        | Latest  | Semantic markup and page structure             |
| CSS3         | Latest  | Styling, animations, responsive design         |
| JavaScript   | ES6+    | Interactive functionality and DOM manipulation |
| Google Fonts | Latest  | Typography (Poppins font family)               |
| Font Awesome | 5.14.0  | Icon library for UI elements                   |
| BoxIcons     | 2.1.4   | Additional icon set                            |
| Bootstrap    | 5.3.2   | CSS framework (selective components)           |

### **Backend Stack**

| Technology   | Version              | Purpose                         |
| ------------ | -------------------- | ------------------------------- |
| PHP          | 7.4+                 | Server-side scripting and logic |
| MySQL        | 5.7+ / MariaDB 10.4+ | Database management system      |
| Apache/Nginx | Latest               | Web server                      |

### **Development Tools**

- **Code Editor**: Visual Studio Code
- **Version Control**: Git
- **Local Server**: XAMPP/LAMP/WAMP
- **Database Management**: phpMyAdmin

## 🚀 Installation & Setup

### **Prerequisites**

- PHP 7.4 or higher
- MySQL 5.7+ or MariaDB 10.4+
- Web server (Apache/Nginx)
- Modern web browser

### **Step-by-Step Installation**

1. **Clone or Download the Project**

   ```bash
   git clone <repository-url>
   cd PABW
   ```

2. **Setup Web Server**

   - Configure your web server to point to the `public/` directory
   - Ensure PHP is enabled and properly configured

3. **Database Setup**

   ```sql
   -- Create database
   CREATE DATABASE berwisata CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

   -- Import the database schema
   SOURCE database/berwisata.sql;
   ```

4. **Configure Database Connection**

   - Copy `.env.example` to `.env`
   - Update database credentials in `src/config/database.php`:

   ```php
   private $host = 'localhost';
   private $username = 'your_username';
   private $password = 'your_password';
   private $database = 'berwisata';
   ```

5. **Set Permissions**

   ```bash
   chmod 755 public/
   chmod 644 public/assets/images/*
   ```

6. **Access the Website**
   - Open your browser and navigate to your local server URL
   - Default: `http://localhost/PABW/public/`

## 📱 Browser Compatibility

| Browser           | Minimum Version | Support Status     |
| ----------------- | --------------- | ------------------ |
| Chrome            | 60+             | ✅ Fully Supported |
| Firefox           | 55+             | ✅ Fully Supported |
| Safari            | 12+             | ✅ Fully Supported |
| Edge              | 79+             | ✅ Fully Supported |
| Internet Explorer | 11              | ⚠️ Limited Support |

## Setup Instructions

## 🎯 Features

### **User Experience**

- 🎥 **Dynamic Video Backgrounds** - Engaging homepage with rotating video content
- 🖼️ **Interactive Image Galleries** - Smooth carousel navigation for destination photos
- 📱 **Fully Responsive Design** - Optimized for all device sizes
- 🎨 **Modern UI/UX** - Clean, intuitive interface with smooth animations

### **Content Management**

- 🏞️ **Destination Showcase** - Detailed information about Yogyakarta tourist spots
- 🎉 **Event Listings** - Current and upcoming tourism events
- 📸 **Photo Galleries** - High-quality images organized by location
- 📝 **Rich Content** - Comprehensive descriptions and travel information

### **User Features**

- 👤 **User Registration & Authentication** - Secure account creation and login
- 🔐 **Password Security** - BCrypt hashing for secure password storage
- 👨‍💼 **User Profiles** - Personal account management
- 📊 **User Dashboard** - Personalized experience

### **Technical Features**

- ⚡ **Fast Loading** - Optimized assets and efficient code structure
- 🔍 **SEO Friendly** - Semantic HTML and proper meta tags
- 🛡️ **Security** - Input validation, SQL injection prevention
- 📊 **Analytics Ready** - Structure prepared for tracking integration

## 🏗️ Architecture & Design Patterns

### **Frontend Architecture**

- **Modular CSS** - Separate stylesheets for different components
- **Progressive Enhancement** - Core functionality works without JavaScript
- **Mobile-First Design** - Responsive breakpoints starting from mobile
- **Component-Based Structure** - Reusable UI components

### **Backend Architecture**

- **MVC Pattern** - Separation of concerns with Models, Views, Controllers
- **Database Abstraction** - Centralized database connection management
- **Secure Authentication** - Password hashing and session management
- **Input Validation** - Server-side data sanitization

## 🛡️ Security Features

- **Password Hashing** - BCrypt algorithm for secure password storage
- **SQL Injection Prevention** - Prepared statements and input validation
- **XSS Protection** - Output escaping and input sanitization
- **CSRF Protection** - Token-based form validation
- **Secure Headers** - Content Security Policy and security headers

## 🚀 Performance Optimizations

- **Image Optimization** - Compressed images in multiple formats (JPEG, WebP, PNG)
- **CSS Minification** - Reduced file sizes for faster loading
- **Caching Headers** - Browser caching for static assets
- **Efficient Database Queries** - Optimized SQL queries
- **Lazy Loading** - Images loaded on demand

## 📊 Database Schema

### **User Table**

```sql
CREATE TABLE user (
    id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```

_Note: Complete database schema available in `database/berwisata.sql`_

## 🎨 Design System

### **Color Palette**

- Primary: Modern gradients and vibrant colors
- Secondary: Complementary accent colors
- Neutral: Grayscale for text and backgrounds

### **Typography**

- **Primary Font**: Poppins (Google Fonts)
- **Weights**: 100, 200, 300, 400, 500, 600, 700, 800, 900
- **Usage**: Clean, modern typography for excellent readability

### **Components**

- Navigation bars with responsive hamburger menu
- Card-based layouts for content presentation
- Modal dialogs for forms
- Interactive buttons with hover effects
- Image carousels with touch support

## Setup Instructions (Legacy)

## 📁 File Organization

### **Directory Structure Explanation**

- **`public/`** - Document root, all publicly accessible files
  - Contains HTML pages, assets, and client-side resources
  - Organized for optimal security (prevents direct access to source code)
- **`src/`** - Server-side PHP source code
  - Separated from public files for enhanced security
  - Contains configuration and business logic
- **`database/`** - Database-related files
  - SQL schema, migrations, and database documentation
- **`docs/`** - Project documentation and backup files
  - Development notes, backup files, and project documentation

### **Asset Organization**

- **CSS**: Modular stylesheets for different components
- **JavaScript**: Feature-specific JS files for maintainability
- **Images**: Organized by category (destinations, events, icons, etc.)
- **Videos**: Background videos and multimedia content

## 🤝 Contributing

### **Development Workflow**

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### **Code Standards**

- **PHP**: Follow PSR-12 coding standards
- **HTML**: Use semantic HTML5 elements
- **CSS**: Use BEM methodology for class naming
- **JavaScript**: Use ES6+ features with proper commenting

## 🐛 Troubleshooting

### **Common Issues**

**Database Connection Error**

```
Solution: Check database credentials in src/config/database.php
Verify MySQL service is running
```

**Images Not Loading**

```
Solution: Check file permissions (chmod 755)
Verify image paths in HTML/CSS files
```

**Login Not Working**

```
Solution: Ensure database table 'user' exists
Check password hashing implementation
```

**CSS/JS Not Loading**

```
Solution: Verify web server configuration
Check file paths in HTML files
```


**Made with ❤️ for tourism in Yogyakarta, Indonesia**
