<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Warwick BI & AI Integration Consulting</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f9f9f9;
      color: #333;
    }
    header {
      background: #00274D;
      color: white;
      padding: 2rem;
      text-align: center;
    }
    nav {
      background: #004080;
      padding: 0.5rem;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 1rem;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 2rem;
      max-width: 1000px;
      margin: auto;
    }
    .hero {
      background: linear-gradient(135deg, #00274D, #00509E);
      color: white;
      padding: 4rem 2rem;
      text-align: center;
    }
    .hero h1 {
      font-size: 2.5rem;
    }
    .cta-button {
      background: #FFCB05;
      color: #00274D;
      padding: 1rem 2rem;
      text-decoration: none;
      font-weight: bold;
      display: inline-block;
      margin-top: 1.5rem;
      border-radius: 5px;
    }
    footer {
      background: #00274D;
      color: white;
      text-align: center;
      padding: 1rem;
    }
    form input, form textarea {
      width: 100%;
      padding: 0.8rem;
      margin-top: 0.5rem;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    form button {
      margin-top: 1rem;
      padding: 0.8rem 2rem;
      background: #004080;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    /* Chatbot styles */
    .chatbot-icon {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #004080;
      color: white;
      border: none;
      padding: 15px;
      border-radius: 50%;
      cursor: pointer;
      font-size: 20px;
      z-index: 1000;
    }

    .chat-window {
      display: none;
      flex-direction: column;
      position: fixed;
      bottom: 80px;
      right: 20px;
      width: 300px;
      max-height: 400px;
      background-color: white;
      border: 1px solid #ccc;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      z-index: 999;
    }

    .chat-header {
      background-color: #004080;
      color: white;
      padding: 10px;
      font-weight: bold;
      text-align: center;
    }

    .chat-messages {
      padding: 10px;
      flex: 1;
      overflow-y: auto;
      font-size: 14px;
    }

    .chat-input {
      display: flex;
      padding: 10px;
      border-top: 1px solid #ccc;
    }

    .chat-input input {
      flex: 1;
      padding: 6px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    .chat-input button {
      margin-left: 5px;
      padding: 6px 10px;
      background-color: #004080;
      color: white;
      border: none;
      border-radius: 4px;
    }
  </style>
</head>
<body>

<header>
  <h1>Warwick BI & AI Integration Consulting</h1>
  <p>Turning Insight into Action with Smart AI + BI Solutions</p>
</header>

<nav>
  <a href="#about">About</a>
  <a href="#services">Services</a>
  <a href="#contact">Contact</a>
</nav>

<section class="hero">
  <h1>Powering Smarter Decisions with Data & AI</h1>
  <p>Specialists in business intelligence automation, complaint insights, and AI integration.</p>
  <a href="#contact" class="cta-button">Book a Free Consultation</a>
</section>

<section id="about">
  <h2>About Us</h2>
  <p>We specialize in bridging the gap between business intelligence and modern AI tools. From dashboard automation to predictive insights, we help businesses act smarter, faster, and with confidence.</p>
</section>

<section id="services">
  <h2>Our Services</h2>
  <ul>
    <li>📊 BI Dashboard Development & Automation</li>
    <li>🧠 AI-Powered Insights & Data Pipelines</li>
    <li>🛠️ Complaint Analytics & SLA Optimization</li>
    <li>📈 Strategic Metrics for Executive Reporting</li>
  </ul>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <form action="https://formspree.io/f/yourFormID" method="POST">
    <label>Your Name</label>
    <input type="text" name="name" required />
    <label>Your Email</label>
    <input type="email" name="email" required />
    <label>Your Message</label>
    <textarea name="message" rows="5" required></textarea>
    <button type="submit">Send Message</button>
  </form>
</section>

<footer>
  <p>© 2025 Warwick BI & AI Integration Consulting</p>
</footer>

<!-- Chatbot Widget -->
<button class="chatbot-icon" onclick="toggleChat()">💬</button>

<div class="chat-window" id="chatWindow">
  <div class="chat-header">Ask Me Anything</div>
  <div class="chat-messages" id="chatMessages">
    <div><strong>Bot:</strong> Hi! How can I help you today?</div>
  </div>
  <div class="chat-input">
    <input type="text" id="chatInput" placeholder="Type a message..." />
    <button onclick="sendMessage()">Send</button>
  </div>
</div>

<script>
  function toggleChat() {
    const chat = document.getElementById('chatWindow');
    chat.style.display = chat.style.display === 'flex' ? 'none' : 'flex';
  }

  function sendMessage() {
    const input = document.getElementById('chatInput');
    const messages = document.getElementById('chatMessages');
    if (input.value.trim() === '') return;

    const userMessage = document.createElement('div');
    userMessage.innerHTML = "<strong>You:</strong> " + input.value;
    messages.appendChild(userMessage);

    const botMessage = document.createElement('div');
    botMessage.innerHTML = "<strong>Bot:</strong> Let me look into that for you.";
    setTimeout(() => messages.appendChild(botMessage), 700);

    input.value = '';
    messages.scrollTop = messages.scrollHeight;
  }
</script>

</body>
</html>