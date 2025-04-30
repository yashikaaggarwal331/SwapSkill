# SwapSkill
SkillSwap is a Gen Z-inspired platform where users can exchange skills with others nearby. Whether you’re a coding queen, dance enthusiast, or guitar newbie — this app helps you connect, learn, and grow through fun, mutual skill-sharing. With a customizable aesthetic, interactive profile system, and an AI chat buddy that helps you talk to people.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SkillSwap - Home</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      background: #f0e7ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .home-container {
      background: white;
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      width: 400px;
      text-align: center;
    }
    h1 {
      color: #ff69b4;
    }
    button {
      background: #ff69b4;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }
    .home-container p {
      color: #777;
    }
  </style>
</head>
<body>
  <div class="home-container">
    <h1>Welcome to SkillSwap</h1>
    <p>Swap skills with others nearby. It's fun and easy!</p>
    <button onclick="window.location.href='profile.html'">Go to Profile</button>
    <button onclick="window.location.href='login.html'">Login / Sign Up</button>
  </div>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SkillSwap - User Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      background: #f0e7ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .profile-container {
      background: white;
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      width: 400px;
      text-align: center;
    }
    .profile-header {
      margin-bottom: 30px;
      color: #ff69b4;
    }
    .profile-img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 20px;
    }
    .rating {
      margin-top: 20px;
      display: flex;
      justify-content: center;
    }
    .rating span {
      margin: 0 5px;
      font-size: 18px;
      color: #f39c12;
    }
    .payment, .reviews {
      margin-top: 30px;
      background-color: #fff0f5;
      padding: 20px;
      border-radius: 10px;
    }
    .payment input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 2px solid #ff8ab8;
      border-radius: 10px;
    }
    button {
      background: #ff69b4;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }
    .review-box {
      margin-top: 20px;
      background: #fffae1;
      padding: 10px;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <div class="profile-container">
    <div class="profile-header">
      <h2>User Profile</h2>
    </div>
    <img class="profile-img" src="profile-pic-placeholder.jpg" alt="Profile Picture">
    <h3>Jane Doe</h3>
    <p>Skills: Web Development, Graphic Design, Photography</p>
    <p>Location: New York City</p>

    <!-- Rating System -->
    <div class="rating">
      <span>⭐⭐⭐⭐⭐</span> <!-- Dynamic JS updates -->
    </div>

    <!-- Payment Section -->
    <div class="payment">
      <h4>Make Payment</h4>
      <input type="text" placeholder="Amount" />
      <button>Proceed to Payment</button>
    </div>

    <!-- Reviews Section -->
    <div class="reviews">
      <h4>Reviews</h4>
      <div class="review-box">
        <p><strong>John</strong>: "Great experience, super helpful!"</p>
      </div>
      <div class="review-box">
        <p><strong>Emily</strong>: "Awesome skills and easy to work with!"</p>
      </div>
      <button>Leave a Review</button>
    </div>
  </div>

  <!-- Script for Dynamic Rating -->
  <script>
    let ratings = [4, 5, 3, 4, 5];

    function calculateAverageRating(ratings) {
      let total = ratings.reduce((acc, rating) => acc + rating, 0);
      return (total / ratings.length).toFixed(1);
    }

    const ratingElement = document.querySelector('.rating span');
    ratingElement.textContent = `⭐⭐⭐⭐⭐ - Average Rating: ${calculateAverageRating(ratings)} stars`;
  </script>
</body><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SkillSwap - Login</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      background: #f0e7ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .login-container {
      background: white;
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      width: 400px;
      text-align: center;
    }
    h1 {
      color: #ff69b4;
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 2px solid #ff8ab8;
      border-radius: 10px;
    }
    button {
      background: #ff69b4;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <h1>Login to SkillSwap</h1>
    <input type="text" placeholder="Enter Username">
    <input type="password" placeholder="Enter Password">
    <button>Login</button>
    <p>Don't have an account? <a href="signup.html" style="color: #ff69b4;">Sign Up</a></p>
  </div>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SkillSwap - Sign Up</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      background: #f0e7ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .signup-container {
      background: white;
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      width: 400px;
      text-align: center;
    }
    h1 {
      color: #ff69b4;
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 2px solid #ff8ab8;
      border-radius: 10px;
    }
    button {
      background: #ff69b4;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="signup-container">
    <h1>Create an Account</h1>
    <input type="text" placeholder="Enter Username">
    <input type="password" placeholder="Enter Password">
    <input type="email" placeholder="Enter Email">
    <button>Sign Up</button>
    <p>Already have an account? <a href="login.html" style="color: #ff69b4;">Login</a></p>
  </div>
</body>
</html><!-- Chatbot Section -->
<div class="chatbot-container">
  <h3>Start Chatting with AI</h3>
  <textarea id="chatInput" rows="5" cols="50" placeholder="Ask me anything..."></textarea>
  <button onclick="startChat()">Send</button>
  <div id="chatOutput"></div>
</div>

<script>
  function startChat() {
    const input = document.getElementById('chatInput').value;
    const chatOutput = document.getElementById('chatOutput');
    
    if (input) {
      chatOutput.innerHTML += `<p><strong>You:</strong> ${input}</p>`;
      chatOutput.innerHTML += `<p><strong>AI:</strong> Let me help you with that...</p>`;
    }
  }
</script>
</html><link rel="stylesheet" href="style.css">
