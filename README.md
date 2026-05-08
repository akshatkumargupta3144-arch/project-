<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Bright Future School</title>

  <style>
    /* Basic page styling */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background-color: #f4f8ff;
      color: #333;
      line-height: 1.6;
    }

    /* Header section */
    header {
      background-color: #005bbb;
      color: white;
      padding: 20px;
      text-align: center;
    }

    nav {
      margin-top: 10px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
    }

    nav a:hover {
      color: #ffd700;
    }

    /* Common section styling */
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }

    h2 {
      color: #005bbb;
      margin-bottom: 15px;
      text-align: center;
    }

    /* Home section */
    .home {
      text-align: center;
    }

    .home img {
      width: 100%;
      max-width: 800px;
      border-radius: 10px;
      margin-top: 20px;
    }

    button {
      background-color: #005bbb;
      color: white;
      border: none;
      padding: 12px 20px;
      margin-top: 20px;
      cursor: pointer;
      border-radius: 5px;
      font-size: 16px;
    }

    button:hover {
      background-color: #003f88;
    }

    /* Courses section */
    .courses {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .course-card {
      background-color: white;
      padding: 20px;
      width: 250px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      text-align: center;
    }

    /* Contact form */
    form {
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }

    input,
    textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    textarea {
      resize: none;
      height: 100px;
    }

    footer {
      background-color: #005bbb;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 30px;
    }

    /* Responsive design for mobile screens */
    @media (max-width: 600px) {
      nav a {
        display: block;
        margin: 10px 0;
      }

      section {
        padding: 25px 15px;
      }

      .course-card {
        width: 100%;
      }
    }
  </style>
</head>

<body>
  <!-- Header with school name and navigation -->
  <header>
    <h1>Bright Future School</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#courses">Courses</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Home section -->
  <section id="home" class="home">
    <h2>Welcome to Bright Future School</h2>
    <p>We help students learn, grow, and prepare for a bright future.</p>

    <button onclick="showWelcomeMessage()">Click Me</button>

    <img
      src="https://images.unsplash.com/photo-1580582932707-520aed937b7b"
      alt="School classroom banner"
    />
  </section>

  <!-- About section -->
  <section id="about">
    <h2>About Our School</h2>
    <p>
      Bright Future School is a place where students receive quality education
      in a friendly and supportive environment. Our teachers focus on learning,
      creativity, discipline, and overall development.
    </p>
  </section>

  <!-- Courses section -->
  <section id="courses">
    <h2>Our Courses</h2>

    <div class="courses">
      <div class="course-card">
        <h3>Science</h3>
        <p>Learn about nature, experiments, and scientific thinking.</p>
      </div>

      <div class="course-card">
        <h3>Mathematics</h3>
        <p>Improve problem-solving and logical thinking skills.</p>
      </div>

      <div class="course-card">
        <h3>Computer Studies</h3>
        <p>Understand basic computer skills, coding, and technology.</p>
      </div>
    </div>
  </section>

  <!-- Contact section with form -->
  <section id="contact">
    <h2>Contact Us</h2>

    <form onsubmit="return validateForm()">
      <input type="text" id="name" placeholder="Enter your name" />
      <input type="email" id="email" placeholder="Enter your email" />
      <textarea id="message" placeholder="Enter your message"></textarea>

      <button type="submit">Submit</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2026 Bright Future School. All rights reserved.</p>
  </footer>

  <script>
    // This function shows a welcome alert when the button is clicked
    function showWelcomeMessage() {
      alert("Welcome to our school!");
    }

    // This function validates the contact form
    function validateForm() {
      // Get values from input fields
      let name = document.getElementById("name").value.trim();
      let email = document.getElementById("email").value.trim();
      let message = document.getElementById("message").value.trim();

      // Email pattern for basic email validation
      let emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;

      // Check if fields are empty
      if (name === "" || email === "" || message === "") {
        alert("Please fill in all fields.");
        return false;
      }

      // Check if email is valid
      if (!email.match(emailPattern)) {
        alert("Please enter a valid email address.");
        return false;
      }

      // Show success message
      alert("Form submitted successfully!");

      // Clear form fields
      document.getElementById("name").value = "";
      document.getElementById("email").value = "";
      document.getElementById("message").value = "";

      return false;
    }
  </script>
</body>
</html>
