# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="grid-container">
    <section class="box box1">Box 1</section>
    <section class="box box2">Box 2</section>
    <section class="box box3">Box 3</section>
    <section class="box box4">Box 4</section>
  </main>

  <footer>
    <p>&copy; 2025 MySite. All rights reserved.</p>
  </footer>
</body>
</html>



/* Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  line-height: 1.6;
}

/* Navbar with Flexbox */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #2e3a59;
  padding: 1rem 2rem;
  color: white;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

/* Grid Layout */
.grid-container {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(4, 1fr);
  padding: 2rem;
}

.box {
  padding: 2rem;
  background-color: #f4f4f4;
  border: 1px solid #ccc;
  text-align: center;
  font-weight: bold;
}

/* Footer */
footer {
  text-align: center;
  padding: 1rem;
  background: #2e3a59;
  color: white;
}

/* MEDIA QUERIES */

/* Tablet */
@media (max-width: 992px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Mobile */
@media (max-width: 600px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    flex-direction: column;
    width: 100%;
    gap: 0.5rem;
    margin-top: 1rem;
  }

  .grid-container {
    grid-template-columns: 1fr;
  }
}
