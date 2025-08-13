# HolidayIn Tourism Website - Development Guide

## 📋 Table of Contents

- [Getting Started](#getting-started)
- [Development Environment](#development-environment)
- [Code Standards](#code-standards)
- [Database Management](#database-management)
- [Testing](#testing)
- [Deployment](#deployment)

## 🚀 Getting Started

### Quick Start for Developers

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd PABW
   ```

2. **Setup local environment**

   ```bash
   cp .env.example .env
   # Edit .env with your local database credentials
   ```

3. **Start local server**

   ```bash
   # Using PHP built-in server
   cd public
   php -S localhost:8000

   # Or use XAMPP/LAMP and point to public/ directory
   ```

## 🔧 Development Environment

### Recommended Setup

- **Operating System**: Windows 10/11, macOS, or Linux
- **PHP**: Version 7.4 or higher
- **Database**: MySQL 5.7+ or MariaDB 10.4+
- **Web Server**: Apache 2.4+ or Nginx 1.18+
- **Code Editor**: Visual Studio Code with extensions:
  - PHP Intelephense
  - HTML CSS Support
  - JavaScript (ES6) code snippets
  - Prettier - Code formatter

### Local Development Tools

```bash
# Install XAMPP (Windows/macOS/Linux)
https://www.apachefriends.org/

# Or install individual components:
# PHP: https://www.php.net/downloads
# MySQL: https://dev.mysql.com/downloads/
# Apache: https://httpd.apache.org/download.cgi
```

## 📝 Code Standards

### PHP Standards (PSR-12)

```php
<?php
// Class names in PascalCase
class UserController
{
    // Method names in camelCase
    public function getUserData(): array
    {
        // Constants in UPPER_CASE
        const MAX_USERS = 100;

        // Variables in camelCase
        $userData = [];

        return $userData;
    }
}
```

### HTML Standards

```html
<!-- Use semantic HTML5 elements -->
<header>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
    </ul>
  </nav>
</header>

<main>
  <section>
    <article>
      <!-- Content here -->
    </article>
  </section>
</main>
```

### CSS Standards (BEM Methodology)

```css
/* Block */
.navbar {
  display: flex;
}

/* Element */
.navbar__item {
  padding: 1rem;
}

/* Modifier */
.navbar__item--active {
  background-color: #007bff;
}
```

### JavaScript Standards (ES6+)

```javascript
// Use const/let instead of var
const apiUrl = "https://api.example.com";
let userData = null;

// Use arrow functions
const fetchUserData = async (userId) => {
  try {
    const response = await fetch(`${apiUrl}/users/${userId}`);
    return await response.json();
  } catch (error) {
    console.error("Error fetching user data:", error);
  }
};

// Use template literals
const welcomeMessage = `Welcome, ${user.name}!`;
```

## 🗄️ Database Management

### Database Schema Updates

1. **Create migration file**

   ```sql
   -- migrations/001_create_users_table.sql
   CREATE TABLE users (
       id INT PRIMARY KEY AUTO_INCREMENT,
       email VARCHAR(255) UNIQUE NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

2. **Update main schema**
   ```bash
   # Add new migration to database/berwisata.sql
   ```

### Database Best Practices

- Always use prepared statements
- Implement proper indexing
- Use appropriate data types
- Follow naming conventions (snake_case for tables/columns)

## 🧪 Testing

### Manual Testing Checklist

- [ ] All pages load without errors
- [ ] Forms submit correctly
- [ ] User authentication works
- [ ] Responsive design on mobile/tablet
- [ ] Cross-browser compatibility
- [ ] Image galleries function properly
- [ ] Video backgrounds play correctly

### Browser Testing Matrix

| Feature          | Chrome | Firefox | Safari | Edge |
| ---------------- | ------ | ------- | ------ | ---- |
| Login/Register   | ✅     | ✅      | ✅     | ✅   |
| Image Gallery    | ✅     | ✅      | ✅     | ✅   |
| Video Background | ✅     | ✅      | ⚠️     | ✅   |
| Mobile Menu      | ✅     | ✅      | ✅     | ✅   |

## 🚀 Deployment

### Production Checklist

- [ ] Update database credentials in production config
- [ ] Set environment to production in `.env`
- [ ] Optimize images and compress assets
- [ ] Enable HTTPS and security headers
- [ ] Test all functionality in production environment
- [ ] Setup database backups
- [ ] Configure error logging
- [ ] Test performance and loading times

### Security Considerations

- Change default database passwords
- Implement proper input validation
- Use HTTPS for all pages
- Set up proper file permissions
- Enable security headers
- Regular security updates

## 📊 Performance Optimization

### Frontend Optimization

- Compress images (use WebP where supported)
- Minify CSS and JavaScript
- Enable browser caching
- Implement lazy loading for images
- Optimize video file sizes

### Backend Optimization

- Implement database query optimization
- Use appropriate PHP opcache settings
- Enable compression (gzip)
- Optimize database indexes
- Implement caching strategies

## 🔍 Debugging

### Common Debug Scenarios

```php
// Enable error reporting in development
error_reporting(E_ALL);
ini_set('display_errors', 1);

// Database connection debugging
try {
    $connection = new mysqli($host, $user, $pass, $db);
    if ($connection->connect_error) {
        die("Connection failed: " . $connection->connect_error);
    }
    echo "Connected successfully";
} catch (Exception $e) {
    echo "Error: " . $e->getMessage();
}
```

### Browser Developer Tools

- Use Console for JavaScript debugging
- Use Network tab for performance analysis
- Use Elements tab for CSS debugging
- Use Application tab for storage inspection

---

_This development guide is maintained by the PABW development team. Last updated: August 2025_
