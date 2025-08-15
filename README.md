# This is devansh pandey
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Devansh Pandey - Resume</title>
  <style>
    /* General Styling */
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      color: white;
      background: linear-gradient(270deg, #001f3f, #002952, #003366);
      background-size: 600% 600%;
      animation: gradientShift 12s ease infinite;
      scroll-behavior: smooth;
    }
    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1920&q=80') no-repeat center center fixed;
      background-size: cover;
      opacity: 0.25;
      z-index: -1;
    }

    /* Navigation */
    nav {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      background: rgba(0, 0, 50, 0.85);
      padding: 10px 0;
      display: flex;
      justify-content: center;
      z-index: 1000;
    }
    nav a {
      color: #ffda79;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #ffd369;
    }

    /* Sections */
    .overlay {
      padding: 80px 20px 20px; /* space for navbar */
    }
    .section {
      margin: 30px auto;
      max-width: 800px;
      background: rgba(0, 0, 80, 0.65);
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .section:hover {
      transform: scale(1.02);
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.5);
    }
    h1 {
      font-size: 2.5em;
      margin-bottom: 5px;
    }
    h2 {
      color: #ffda79;
      margin-bottom: 10px;
    }
    p {
      line-height: 1.6;
    }
    strong {
      color: #ffd369;
    }

    /* Button */
    .btn {
      display: inline-block;
      padding: 10px 20px;
      background: #ffda79;
      color: #001f3f;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 10px;
      transition: background 0.3s;
    }
    .btn:hover {
      background: #ffd369;
    }

    /* Modal (Popup) */
    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background-color: rgba(0,0,0,0.7);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background: rgba(0, 0, 50, 0.9);
      padding: 20px;
      border-radius: 10px;
      text-align: center;
      width: 300px;
      color: white;
    }
    .close {
      color: #ffda79;
      float: right;
      font-size: 24px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <a href="#about">About Me</a>
    <a href="#education">Education</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#" id="contactBtn">Contact</a>
  </nav>

  <!-- Content -->
  <div class="overlay">
    <h1>Devansh Pandey</h1>
    <p><em>B.Tech Second-Year Student | Aspiring Software Developer</em></p>

    <div class="section" id="about">
      <h2>🙋 About Me</h2>
      <p>I am a <strong>B.Tech second-year student</strong> at <strong>Shri Ramswaroop College of Engineering and Management</strong>, passionate about exploring technology and building innovative solutions. With a growing interest in software development and problem-solving, I aim to enhance my skills in programming, databases, and application design.</p>
    </div>

    <div class="section" id="education">
      <h2>🎓 Education</h2>
      <p><strong>Higher Secondary (12th Standard)</strong><br>
         Rani Laxmi Bai, Vikas Nagar, Lucknow — <em>2023</em></p>
      <p><strong>Secondary School (10th Standard)</strong><br>
         STCPMA, Pachwas Basti — <em>2021</em></p>
    </div>

    <div class="section" id="skills">
      <h2>💻 Skills</h2>
      <p>Basic knowledge of Python, MySQL, DBMS</p>
    </div>

    <div class="section" id="projects">
      <h2>📂 Projects</h2>
      <p><strong>Portfolio Website</strong> — Personal website showcasing skills and projects.</p>
      <p><strong>Calculator App</strong> — Command-line calculator developed in C language to perform basic arithmetic operations efficiently.</p>
    </div>
  </div>

  <!-- Contact Modal -->
  <div class="modal" id="contactModal">
    <div class="modal-content">
      <span class="close" id="closeModal">&times;</span>
      <h3>📞 Contact Me</h3>
      <p>📍 Dayal Farm, Deva Rd, Chinhat, Lucknow, UP 226019</p>
      <p>📧 devanshpandey2604@gmail.com</p>
      <p>📱 8081115046</p>
    </div>
  </div>

  <script>
    // Modal Handling
    const contactBtn = document.getElementById("contactBtn");
    const contactModal = document.getElementById("contactModal");
    const closeModal = document.getElementById("closeModal");

    contactBtn.addEventListener("click", (e) => {
      e.preventDefault();
      contactModal.style.display = "flex";
    });

    closeModal.addEventListener("click", () => {
      contactModal.style.display = "none";
    });

    window.addEventListener("click", (e) => {
      if (e.target === contactModal) {
        contactModal.style.display = "none";
      }
    });
  </script>

</body>
</html>

