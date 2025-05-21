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
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>PLP Learning Acad & Grid Layout</title>
  <style>
    /* Reset and base styles */
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: #333;
      background: #f9f9f9;
    }

    /* Navigation bar using Flexbox */
    nav {
      background-color: #004466;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      flex-wrap: wrap;
    }

    nav .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
      padding-left: 0;
      margin: 0;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s ease;
    }

    nav ul li a:hover {
      color: #ffa500;
    }

    /* Main content layout using CSS Grid */
    main {
      display: grid;
      grid-template-columns: 1fr 3fr;
      gap: 2rem;
      padding: 2rem;
      max-width: 1200px;
      margin: 0 auto;
      background: white;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    /* Sidebar styles */
    aside {
      background: #e6f0ff;
      padding: 1.5rem;
      border-radius: 8px;
    }

    aside h2 {
      margin-top: 0;
    }

    /* Article styles */
    article {
      background: #fff;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: inset 0 0 5px #ddd;
    }

    article h1 {
      margin-top: 0;
      margin-bottom: 1rem;
      font-size: 2rem;
    }

    article p {
      margin-bottom: 1rem;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
      background-color: #004466;
      color: white;
      font-size: 0.9rem;
    }

    /* MEDIA QUERIES */

    /* Mobile: stack nav items vertically and main content into one column */
    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        align-items: flex-start;
      }
      nav ul {
        flex-direction: column;
        width: 100%;
        gap: 0.8rem;
        margin-top: 0.5rem;
      }
      main {
        grid-template-columns: 1fr;
        padding: 1rem;
      }
      aside {
        margin-bottom: 1.5rem;
      }
    }

    /* Tablet: adjust grid columns to 1fr 2fr */
    @media (min-width: 601px) and (max-width: 900px) {
      main {
        grid-template-columns: 1fr 2fr;
        padding: 1.5rem;
      }
      nav ul {
        gap: 1rem;
      }
    }
  </style>
</head>
<body>

  <nav>
    <div class="logo">AkSam</div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Features</a></li>
      <li><a href="#">Pricing</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main>
    <aside>
      <h2>The Menu</h2>
      <ul>
        <li><a href="#">Overview</a></li>
        <li><a href="#">Reports</a></li>
        <li><a href="#">Analytics</a></li>
        <li><a href="#">Export</a></li>
      </ul>
    </aside>

    <article>
      <h1>Welcome to AkSam Page</h1>
      <p>
        This webpage demonstrates a responsive layout using modern CSS techniques including Flexbox, CSS Grid, and media queries.
      </p>
      <p>
        The navigation bar adapts to different screen sizes, while the main content switches between a two-column grid layout and a stacked layout on smaller screens.
      </p>
      <p>
        Resize your browser or open this page on different devices to see the responsiveness in action.
      </p>
    </article>
  </main>

  <footer>
    &copy; 2025 AkSam. All rights reserved.
  </footer>

</body>
</html>

