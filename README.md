<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Our Wedding RSVP</title>
  <style>
    body {
      margin: 0;
      font-family: Helvetica, sans-serif;
      background-color: #fdfdfd;
      color: #333;
    }

    /* Hero Banner */
    .hero {
      background: url(https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&q=80&w=2370) no-repeat center center;
      background-size: cover;
      height: 300px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      text-shadow: 1px 1px 5px rgba(0,0,0,0.6);
    }

    .hero h1 {
      font-size: 3em;
      margin: 0;
    }

    /* RSVP Form */
    .form-container {
      max-width: 400px;
      margin: 40px auto;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #fff;
    }

    .form-container h2 {
      text-align: center;
    }

    label {
      display: block;
      margin-top: 15px;
    }

    input[type="text"],
    input[type="email"] {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      margin-top: 20px;
      width: 100%;
      padding: 10px;
      background-color: #4CAF50;
      color: white;
      font-size: 16px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    button:hover {
      background-color: #45a049;
    }

    .success-message {
      text-align: center;
      color: green;
      margin-top: 15px;
    }
  </style>
</head>
<body>

  <!-- Hero Banner -->
  <div class="hero">
    <h1>You're Invited!</h1>
  </div>

  <!-- RSVP Form -->
  <div class="form-container">
    <h2>RSVP to Our Wedding</h2>
    <form id="rsvpForm">
      <label for="name">Your Name:</label>
      <input type="text" id="name" name="name" required />

      <label for="email">Your Email:</label>
      <input type="email" id="email" name="email" required />

      <button type="submit">Confirm Attendance</button>
      <div class="success-message" id="successMsg"></div>
    </form>
  </div>

  <script>
    const form = document.getElementById('rsvpForm');
    const successMsg = document.getElementById('successMsg');

    form.addEventListener('submit', function(event) {
      event.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();

      if (name && email) {
        console.log(`RSVP Received: ${name} - ${email}`);
        successMsg.textContent = "Thank you for your RSVP!";
        form.reset();
      } else {
        successMsg.textContent = "";
      }
    });
  </script>

</body>
</html>
