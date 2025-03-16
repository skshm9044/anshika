<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday Anshika</title>
  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    /* Body Styling */
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #fff;
      overflow-x: hidden;
    }
    
    /* Container for each section */
    .section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 2rem;
      text-align: center;
      position: relative;
      transition: opacity 0.5s ease;
    }
    
    /* Banner Section */
    #welcomeSection {
      background: linear-gradient(135deg, #ffd1ff, #fad0c4);
    }
    
    /* Wishes Section */
    #wishesSection {
      background: linear-gradient(135deg, #ffafbd, #ffc3a0);
    }
    
    /* Balloon Game Section */
    #balloonGameSection {
      background: linear-gradient(135deg, #a1c4fd, #c2e9fb);
      overflow: hidden;
    }
    
    /* Cake Section */
    #cakeSection {
      background: linear-gradient(135deg, #d4fc79, #96e6a1);
    }
    
    /* Final Message Section */
    #finalMessageSection {
      background: linear-gradient(135deg, #f6d365, #fda085);
    }
    
    /* Section Heading */
    h1 {
      font-size: 3rem;
      font-weight: bold;
      margin-bottom: 20px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    }
    
    h2 {
      font-size: 2.5rem;
      font-weight: bold;
      margin-bottom: 15px;
      text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
    }
    
    /* Subtitle Section */
    p.subtitle {
      font-size: 1.5rem;
      margin-bottom: 40px;
      color: #f7f7f7;
    }
    
    /* Content Paragraph */
    .content {
      font-size: 1.2rem;
      margin: 20px 0;
      line-height: 1.6;
      max-width: 800px;
    }
    
    /* Welcome Cake Animation */
    .welcome-cake {
      position: relative;
      width: 120px;
      height: 100px;
      background-color: #f8c7cc;
      border-radius: 10px;
      margin: 30px auto;
      animation: cakeBounce 2s infinite;
    }
    
    .welcome-cake-top {
      position: absolute;
      width: 120px;
      height: 20px;
      background-color: #ffb6c1;
      border-radius: 10px 10px 0 0;
      top: 0;
    }
    
    .welcome-candle {
      position: absolute;
      width: 6px;
      height: 20px;
      background-color: #fff;
      top: -20px;
      left: 57px;
    }
    
    .welcome-flame {
      position: absolute;
      width: 10px;
      height: 20px;
      background: #ffcc33;
      border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      top: -40px;
      left: 55px;
      transform-origin: center bottom;
      animation: flicker 1s infinite alternate;
    }
    
    @keyframes cakeBounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-10px);
      }
    }
    
    /* Heart Animation */
    .heart {
      position: relative;
      width: 100px;
      height: 100px;
      background-color: red;
      transform: rotate(-45deg);
      animation: heartbeat 1.5s infinite;
      margin: 20px auto;
    }
    
    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 100px;
      height: 100px;
      background-color: red;
      border-radius: 50%;
    }
    
    .heart::before {
      top: -50px;
      left: 0;
    }
    
    .heart::after {
      left: 50px;
      top: 0;
    }
    
    @keyframes heartbeat {
      0%, 100% {
        transform: scale(1) rotate(-45deg);
      }
      50% {
        transform: scale(1.1) rotate(-45deg);
      }
    }
    
    /* Button Styling */
    .btn {
      margin: 15px 0;
      padding: 12px 25px;
      font-size: 1.1rem;
      color: #fff;
      background-color: #ff6f61;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    
    .btn:hover {
      background-color: #e9b8dd;
      transform: scale(1.05);
    }
    
    /* Navigation buttons */
    .nav-buttons {
      display: flex;
      gap: 15px;
      margin-top: 30px;
    }
    
    /* Balloon Styling */
    .balloon {
      position: absolute;
      width: 60px;
      height: 75px;
      border-radius: 50%;
      cursor: pointer;
      animation: float 15s linear infinite;
    }
    
    @keyframes float {
      0% {
        transform: translateY(100vh) translateX(0);
      }
      100% {
        transform: translateY(-100px) translateX(50px);
      }
    }
    
    /* Cake Container */
    .cake-container {
      position: relative;
      width: 300px;
      height: 300px;
      margin: 30px auto;
    }
    
    .cake {
      position: relative;
      width: 250px;
      height: 200px;
      background-color: #f8c7cc;
      border-radius: 10px;
      margin: 0 auto;
    }
    
    .cake-top {
      position: absolute;
      width: 250px;
      height: 40px;
      background-color: #ffb6c1;
      border-radius: 10px 10px 0 0;
      top: 0;
    }
    
    .candle {
      position: absolute;
      width: 10px;
      height: 30px;
      background-color: #fff;
      top: -30px;
      left: 120px;
    }
    
    .flame {
      position: absolute;
      width: 15px;
      height: 30px;
      background: #ffcc33;
      border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      top: -60px;
      left: 117px;
      transform-origin: center bottom;
      animation: flicker 1s infinite alternate;
    }
    
    @keyframes flicker {
      0%, 100% {
        transform: scaleY(1);
        background: #ffcc33;
      }
      50% {
        transform: scaleY(1.1);
        background: #ff9933;
      }
    }
    
    /* Hidden sections */
    .hidden {
      display: none;
    }
    
    /* Footer */
    footer {
      padding: 20px;
      text-align: center;
      font-size: 0.9rem;
      color: #e210b8;
      font-weight: bold;
      background-color: rgba(255, 255, 255, 0.1);
    }
    
    /* Wish Cards */
    .wish-card {
      background-color: rgba(255, 255, 255, 0.2);
      padding: 20px;
      border-radius: 10px;
      margin: 15px 0;
      max-width: 600px;
      width: 100%;
      backdrop-filter: blur(5px);
      transition: transform 0.3s ease;
    }
    
    .wish-card:hover {
      transform: translateY(-5px);
    }
    
    /* Pop animation */
    @keyframes pop {
      0% { transform: scale(1); opacity: 1; }
      50% { transform: scale(1.4); opacity: 0.7; }
      100% { transform: scale(0); opacity: 0; }
    }
    
    /* Message animation */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .pop-message {
      position: absolute;
      font-size: 1.2rem;
      font-weight: bold;
      color: white;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
      animation: fadeIn 0.5s forwards;
    }
    
    /* Score Display */
    .score-display {
      position: absolute;
      top: 20px;
      right: 20px;
      background-color: rgba(255, 255, 255, 0.3);
      padding: 10px 20px;
      border-radius: 50px;
      font-size: 1.2rem;
      backdrop-filter: blur(5px);
    }
    
    /* Balloon Counter */
    .balloon-counter {
      position: absolute;
      top: 20px;
      left: 20px;
      background-color: rgba(255, 255, 255, 0.3);
      padding: 10px 20px;
      border-radius: 50px;
      font-size: 1.2rem;
      backdrop-filter: blur(5px);
    }
    
    /* Confetti */
    .confetti {
      position: fixed;
      width: 10px;
      height: 10px;
      background-color: #f00;
      opacity: 0;
      pointer-events: none;
    }
    
    /* Cake Knife */
    .knife {
      position: absolute;
      width: 100px;
      height: 20px;
      background: linear-gradient(to right, #d1d1d1, #f5f5f5);
      border-radius: 2px;
      top: 50px;
      right: -120px;
      transform-origin: left center;
      transform: rotate(0deg);
      z-index: 10;
      opacity: 0;
      transition: opacity 0.5s;
    }
    
    .knife::before {
      content: '';
      position: absolute;
      width: 30px;
      height: 30px;
      background-color: #a0a0a0;
      border-radius: 5px;
      top: -5px;
      left: -25px;
    }
    
    /* Cake Slice Animation */
    .cake-slice {
      position: absolute;
      width: 0;
      height: 0;
      border-left: 0px solid transparent;
      border-right: 125px solid transparent;
      border-bottom: 200px solid #f8c7cc;
      top: 0;
      left: 0;
      opacity: 0;
      transform-origin: top left;
      transition: transform 1s ease, opacity 1s ease;
    }
    
    .cake-slice-top {
      position: absolute;
      width: 0;
      height: 0;
      border-left: 0px solid transparent;
      border-right: 125px solid transparent;
      border-bottom: 40px solid #ffb6c1;
      top: 0;
      left: 0;
      opacity: 0;
      transform-origin: top left;
      transition: transform 1s ease, opacity 1s ease;
    }
    
    /* Knife Animation */
    @keyframes cutCake {
      0% { transform: rotate(0deg); right: -120px; }
      30% { transform: rotate(0deg); right: 120px; }
      40% { transform: rotate(45deg); right: 120px; }
      70% { transform: rotate(45deg); right: 10px; }
      100% { transform: rotate(0deg); right: -120px; }
    }
    
    /* Plate for cake slice */
    .cake-plate {
      position: absolute;
      width: 150px;
      height: 20px;
      background-color: rgba(255, 255, 255, 0.7);
      border-radius: 50%;
      bottom: 20px;
      right: 20px;
      opacity: 0;
      transition: opacity 1s ease;
    }
  </style>
</head>
<body>
  <!-- Welcome Section -->
  <section id="welcomeSection" class="section">
    <h1>Happy Birthday Anshika! ❤️</h1>
    <p class="subtitle">A special celebration for the most amazing person in my life!</p>
    <div class="welcome-cake">
      <div class="welcome-flame"></div>
      <div class="welcome-candle"></div>
      <div class="welcome-cake-top"></div>
    </div>
    <p class="content">Today is all about you! Let's make it memorable...</p>
    <button class="btn" id="startButton">Start The Celebration</button>
  </section>

  <!-- Wishes Section -->
  <section id="wishesSection" class="section hidden">
    <h2>Birthday Wishes For You</h2>
    <div class="wish-card">
      <p>May your smile never fade, and your heart always be filled with joy. Wishing you a day as wonderful as you are!</p>
    </div>
    <div class="wish-card">
      <p>May this special day bring you endless happiness and begin the best year of your life so far!</p>
    </div>
    <div class="wish-card">
      <p>Your presence in my life is a gift I cherish every day. Happy Birthday, my special one!</p>
    </div>
    <div class="nav-buttons">
      <button class="btn" id="toBalloonsButton">Pop Some Balloons!</button>
    </div>
  </section>

  <!-- Balloon Game Section -->
  <section id="balloonGameSection" class="section hidden">
    <h2>Pop The Balloons!</h2>
    <p class="subtitle">Click on balloons to pop them and reveal hidden messages!</p>
    <div class="score-display">Score: <span id="score">0</span></div>
    <div class="balloon-counter">Balloons: <span id="balloonCount">0</span>/10</div>
    <div id="balloonContainer"></div>
    <div class="nav-buttons">
      <button class="btn hidden" id="toCakeButton">Let's Cut The Cake!</button>
    </div>
  </section>

  <!-- Cake Cutting Section -->
  <section id="cakeSection" class="section hidden">
    <h2>Cake Cutting Ceremony</h2>
    <p class="subtitle">It's time to make a wish and cut the cake!</p>
    <div class="cake-container">
      <div class="flame" id="flame"></div>
      <div class="candle"></div>
      <div class="cake-top"></div>
      <div class="cake"></div>
      <div class="knife" id="knife"></div>
      <div class="cake-slice" id="cakeSlice"></div>
      <div class="cake-slice-top" id="cakeSliceTop"></div>
      <div class="cake-plate" id="cakePlate"></div>
    </div>
    <button class="btn" id="blowCandle">Blow Out The Candle</button>
    <button class="btn hidden" id="cutCake">Cut The Cake</button>
    <p class="content hidden" id="cakeMessage">Happy Birthday! May all your wishes come true!</p>
    <div class="nav-buttons">
      <button class="btn hidden" id="toFinalMessageButton">See My Special Message</button>
    </div>
  </section>

  <!-- Final Message Section -->
  <section id="finalMessageSection" class="section hidden">
    <h2>A Special Message For You</h2>
    <div class="heart"></div>
    <p class="content">
      On your special day, I want you to know how much you mean to me. Your smile brightens my day, your laughter fills my heart with joy, and your presence in my life is the greatest gift I could ever ask for. Thank you for being the amazing person that you are.
    </p>
    <p class="content">
      Happy Birthday, my dear! May all your dreams come true, and may this year bring you all the happiness and success you deserve!
    </p>
    <p class="subtitle">With all my love ❤️</p>
    <footer>Made with love for your special day ❤️</footer>
  </section>

  <script>
    document.addEventListener('DOMContentLoaded', function() {
      // Variables
      let score = 0;
      let balloonCount = 0;
      const totalBalloons = 10;
      const balloonMessages = [
        "You are amazing!",
        "Happy Birthday!",
        "Have an awesome day!",
        "You're the best!",
        "Keep shining!",
        "Make a wish!",
        "Stay beautiful!",
        "Enjoy your day!",
        "You deserve the best!",
        "Sending you love!"
      ];
      const colors = [
        '#FF6B6B', '#4ECDC4', '#45B7D1', '#FFBE0B', 
        '#FB5607', '#8338EC', '#3A86FF', '#FF006E',
        '#A5E6BA', '#FFAFCC'
      ];

      // Section Navigation
      document.getElementById('startButton').addEventListener('click', function() {
        document.getElementById('welcomeSection').classList.add('hidden');
        document.getElementById('wishesSection').classList.remove('hidden');
      });

      document.getElementById('toBalloonsButton').addEventListener('click', function() {
        document.getElementById('wishesSection').classList.add('hidden');
        document.getElementById('balloonGameSection').classList.remove('hidden');
        createBalloons();
      });

      document.getElementById('toCakeButton').addEventListener('click', function() {
        document.getElementById('balloonGameSection').classList.add('hidden');
        document.getElementById('cakeSection').classList.remove('hidden');
      });

      document.getElementById('blowCandle').addEventListener('click', function() {
        document.getElementById('flame').style.display = 'none';
        document.getElementById('cakeMessage').classList.remove('hidden');
        document.getElementById('cutCake').classList.remove('hidden');
        createConfetti();
      });
      
      document.getElementById('cutCake').addEventListener('click', function() {
        // Show knife
        const knife = document.getElementById('knife');
        knife.style.opacity = 1;
        
        // Animate knife
        knife.style.animation = 'cutCake 3s forwards';
        
        // After knife finishes cutting, show the cake slice and plate
        setTimeout(function() {
          const cakeSlice = document.getElementById('cakeSlice');
          const cakeSliceTop = document.getElementById('cakeSliceTop');
          const cakePlate = document.getElementById('cakePlate');
          
          // Show slice and plate
          cakeSlice.style.opacity = 1;
          cakeSliceTop.style.opacity = 1;
          cakePlate.style.opacity = 1;
          
          // Animate slice moving to plate
          setTimeout(function() {
            cakeSlice.style.transform = 'translate(100px, 150px) rotate(90deg)';
            cakeSliceTop.style.transform = 'translate(100px, 150px) rotate(90deg)';
            
            // Show final message button
            setTimeout(function() {
              document.getElementById('toFinalMessageButton').classList.remove('hidden');
            }, 1000);
          }, 500);
        }, 3000);
      });

      document.getElementById('toFinalMessageButton').addEventListener('click', function() {
        document.getElementById('cakeSection').classList.add('hidden');
        document.getElementById('finalMessageSection').classList.remove('hidden');
      });

      // Create Balloons Function
      function createBalloons() {
        const balloonContainer = document.getElementById('balloonContainer');
        for (let i = 0; i < totalBalloons; i++) {
          createBalloon(i);
        }
        
        function createBalloon(index) {
          const balloon = document.createElement('div');
          balloon.className = 'balloon';
          balloon.style.backgroundColor = colors[index % colors.length];
          balloon.style.left = Math.random() * 80 + 10 + '%';
          balloon.style.animationDuration = (10 + Math.random() * 10) + 's';
          balloon.style.animationDelay = (Math.random() * 5) + 's';
          
          balloon.addEventListener('click', function() {
            popBalloon(balloon, balloonMessages[index % balloonMessages.length]);
          });
          
          balloonContainer.appendChild(balloon);
        }
      }

      // Pop Balloon Function
      function popBalloon(balloon, message) {
        // Animate the pop
        balloon.style.animation = 'pop 0.5s forwards';
        
        // Create and display message
        const popMessage = document.createElement('div');
        popMessage.className = 'pop-message';
        popMessage.textContent = message;
        popMessage.style.left = balloon.style.left;
        popMessage.style.top = balloon.offsetTop + 'px';
        document.getElementById('balloonContainer').appendChild(popMessage);
        
        // Remove message after animation
        setTimeout(function() {
          popMessage.remove();
        }, 2000);
        
        // Update score and count
        score += 10;
        balloonCount++;
        document.getElementById('score').textContent = score;
        document.getElementById('balloonCount').textContent = balloonCount;
        
        // Remove balloon after animation
        setTimeout(function() {
          balloon.remove();
        }, 500);
        
        // Check if all balloons are popped
        if (balloonCount >= totalBalloons) {
          document.getElementById('toCakeButton').classList.remove('hidden');
        }
      }

      // Create confetti
      function createConfetti() {
        const colors = ['#FF6B6B', '#4ECDC4', '#45B7D1', '#FFBE0B', '#FB5607', '#8338EC', '#3A86FF'];
        
        for (let i = 0; i < 100; i++) {
          const confetti = document.createElement('div');
          confetti.className = 'confetti';
          confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
          confetti.style.left = Math.random() * 100 + '%';
          confetti.style.top = Math.random() * 100 + '%';
          confetti.style.width = Math.random() * 10 + 5 + 'px';
          confetti.style.height = Math.random() * 10 + 5 + 'px';
          confetti.style.opacity = 1;
          confetti.style.transform = 'rotate(' + Math.random() * 360 + 'deg)';
          
          document.body.appendChild(confetti);
          
          // Animate confetti falling
          let animationDuration = Math.random() * 3 + 2;
          confetti.style.animation = `fall ${animationDuration}s forwards`;
          
          // Define the animation dynamically
          const style = document.createElement('style');
          style.innerHTML = `
            @keyframes fall {
              0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
              }
              100% {
                transform: translateY(${Math.random() * 500 + 200}px) rotate(${Math.random() * 360}deg);
                opacity: 0;
              }
            }
          `;
          document.head.appendChild(style);
          
          // Remove confetti after animation
          setTimeout(function() {
            confetti.remove();
            style.remove();
          }, animationDuration * 1000);
        }
      }
    });
  </script>
</body>
</html>
