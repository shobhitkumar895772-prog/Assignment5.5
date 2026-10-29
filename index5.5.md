File 1: index.html (Home Page)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Campus Tech Club - Home</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Navigation Bar -->
  <header>
    <nav class="navbar">
      <div class="logo">Campus Tech Club</div>
      <ul class="nav-links">
        <li><a href="index.html" class="active">Home</a></li>
        <li><a href="contact.html">Join Us</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <main class="container">
    <section class="hero-card">
      <h1 class="heading-large">Welcome to Campus Tech Club</h1>
      <p class="body-text">
        Empowering students through collaborative coding, workshops, hackathons, and tech talks. Whether you are a beginner or an advanced developer, there is a place for you here!
      </p>
      <a href="contact.html" class="btn btn-primary">Become a Member</a>
    </section>

    <!-- Events Table Section -->
    <section class="section">
      <h2 class="heading-medium">Upcoming Club Events</h2>
      <div class="table-container">
        <table class="styled-table">
          <thead>
            <tr>
              <th>Date</th>
              <th>Event Name</th>
              <th>Location</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Nov 10, 2026</td>
              <td>Intro to HTML & CSS Workshop</td>
              <td>Science Hall 101</td>
            </tr>
            <tr>
              <td>Nov 18, 2026</td>
              <td>Git & GitHub Masterclass</td>
              <td>Library Lab B</td>
            </tr>
            <tr>
              <td>Dec 02, 2026</td>
              <td>Fall Semester Hackathon</td>
              <td>Student Union Ballroom</td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Campus Tech Club. All rights reserved.</p>
  </footer>

</body>
</html>
File 2: contact.html (Join/Contact Page)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Campus Tech Club - Join Us</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Navigation Bar -->
  <header>
    <nav class="navbar">
      <div class="logo">Campus Tech Club</div>
      <ul class="nav-links">
        <li><a href="index.html">Home</a></li>
        <li><a href="contact.html" class="active">Join Us</a></li>
      </ul>
    </nav>
  </header>

  <!-- Membership Form Section -->
  <main class="container">
    <section class="form-card">
      <h1 class="heading-medium">Join the Club</h1>
      <p class="body-text">Fill out the form below to register as an official member of the Campus Tech Club.</p>
      
      <form action="#" method="POST" class="styled-form">
        <div class="form-group">
          <label for="fullname">Full Name</label>
          <input type="text" id="fullname" name="fullname" placeholder="Jane Doe" required>
        </div>

        <div class="form-group">
          <label for="email">Campus Email</label>
          <input type="email" id="email" name="email" placeholder="student@university.edu" required>
        </div>

        <div class="form-group">
          <label for="major">Major / Field of Study</label>
          <input type="text" id="major" name="major" placeholder="Computer Science">
        </div>

        <div class="form-group">
          <label for="experience">Experience Level</label>
          <select id="experience" name="experience">
            <option value="beginner">Beginner (Little to no experience)</option>
            <option value="intermediate">Intermediate (Knows basic programming)</option>
            <option value="advanced">Advanced (Built projects before)</option>
          </select>
        </div>

        <button type="submit" class="btn btn-primary">Submit Application</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Campus Tech Club. All rights reserved.</p>
  </footer>

</body>
</html>
File 3: styles.css (External Stylesheet with Variables)
CSS
/* ==========================================================================
   1. DESIGN TOKENS (:root)
   ========================================================================== */
:root {
  --color-primary: #1d4ed8;       /* Deep Blue */
  --color-secondary: #0ea5e9;     /* Sky Blue Accent */
  --color-bg: #f8fafc;            /* Light gray background */
  --color-surface: #ffffff;       /* Card / Container white */
  --color-text: #1e293b;          /* Dark slate text */
  --color-muted: #64748b;         /* Muted gray text */
  --color-border: #cbd5e1;        /* Border color */
  
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 24px;
  --spacing-xl: 40px;
  
  --border-radius: 8px;
}

/* ==========================================================================
   2. GLOBAL & RESET STYLES
   ========================================================================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background-color: var(--color-bg);
  color: var(--color-text);
  line-height: 1.6;
}

.container {
  max-width: 800px;
  margin: var(--spacing-xl) auto;
  padding: 0 var(--spacing-md);
}

/* ==========================================================================
   3. NAVIGATION BAR
   ========================================================================== */
.navbar {
  background-color: var(--color-surface);
  border-bottom: 1px solid var(--color-border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--spacing-md) var(--spacing-xl);
}

.logo {
  font-weight: 700;
  font-size: 1.25rem;
  color: var(--color-primary);
}

.nav-links {
  list-style: none;
  display: flex;
  gap: var(--spacing-lg);
}

.nav-links a {
  text-decoration: none;
  color: var(--color-muted);
  font-weight: 600;
  transition: color 0.2s;
}

.nav-links a:hover,
.nav-links a.active {
  color: var(--color-primary);
}

/* ==========================================================================
   4. TYPOGRAPHY & CARDS
   ========================================================================== */
.heading-large {
  font-size: 2.2rem;
  color: var(--color-primary);
  margin-bottom: var(--spacing-md);
}

.heading-medium {
  font-size: 1.5rem;
  color: var(--color-text);
  margin-bottom: var(--spacing-md);
}

.body-text {
  color: var(--color-muted);
  margin-bottom: var(--spacing-lg);
}

.hero-card, .form-card, .section {
  background-color: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--border-radius);
  padding: var(--spacing-xl);
  margin-bottom: var(--spacing-lg);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
}

/* ==========================================================================
   5. BUTTONS
   ========================================================================== */
.btn {
  display: inline-block;
  padding: 10px 20px;
  font-size: 1rem;
  font-weight: 600;
  border-radius: var(--border-radius);
  border: none;
  cursor: pointer;
  text-decoration: none;
  transition: background-color 0.2s;
}

.btn-primary {
  background-color: var(--color-primary);
  color: #ffffff;
}

.btn-primary:hover {
  background-color: #1e40af;
}

/* ==========================================================================
   6. TABLES
   ========================================================================== */
.table-container {
  overflow-x: auto;
}

.styled-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: var(--spacing-sm);
  text-align: left;
}

.styled-table th,
.styled-table td {
  padding: 12px var(--spacing-md);
  border-bottom: 1px solid var(--color-border);
}

.styled-table th {
  background-color: var(--color-bg);
  color: var(--color-text);
  font-weight: 600;
}

.styled-table tr:hover {
  background-color: #f1f5f9;
}

/* ==========================================================================
   7. FORMS
   ========================================================================== */
.styled-form {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-md);
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.form-group label {
  font-weight: 600;
  font-size: 0.9rem;
}

.form-group input,
.form-group select {
  padding: 10px;
  border: 1px solid var(--color-border);
  border-radius: var(--border-radius);
  font-size: 1rem;
  outline: none;
  transition: border-color 0.2s;
}

.form-group input:focus,
.form-group select:focus {
  border-color: var(--color-primary);
}

/* Footer */
footer {
  text-align: center;
  padding: var(--spacing-lg);
  color: var(--color-muted);
  font-size: 0.9rem;
  border-top: 1px solid var(--color-border);
  background-color: var(--color-surface);
}
Design Choices Explanation
The website uses a clean, modern design aesthetic centered around a professional academic tech palette (deep blues and neutral slates). CSS custom properties (:root) are leveraged to maintain consistent spacing, borders, and color schemes across both pages. Typography and element padding were optimized to ensure high readability for both structured tables and interactive form elements. Reusable utility classes and modular card layouts keep the CSS codebase clean, lightweight, and easy to maintain.