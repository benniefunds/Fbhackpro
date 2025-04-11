<marquee behavior="scroll" direction="left">
Bennie is a pro web developer... chat him up on telegram @jlord!
</marquee>
<html lang="en">
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>FB H4CK Pro by bennie</title> 
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"> 
  <style>
        :root {
            --primary: #1877f2;
            --secondary: #42b72a;
            --dark: #18191a;
            --darker: #121212;
            --light: #e4e6eb;
            --lighter: #f0f2f5;
            --danger: #e41e3f;
            --terminal: #0a0a12;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
            padding: 1rem 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            z-index: 100;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .logo-icon {
            color: var(--primary);
            font-size: 2rem;
        }
        
        .logo-text {
            font-weight: 700;
            font-size: 1.5rem;
            background: linear-gradient(90deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .nav-links {
            display: flex;
            gap: 1.5rem;
        }
        
        .nav-link {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            opacity: 0.8;
        }
        
        .nav-link:hover {
            opacity: 1;
            color: var(--primary);
        }
        
        .main-container {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2rem;
            background: url('https://images.unsplash.com/photo-1639762681057-408e52192e55?q=80&w=2232&auto=format&fit=crop') no-repeat center center;
            background-size: cover;
            position: relative;
        }
        
        .main-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            z-index: 0;
        }
        
        .content {
            width: 100%;
            max-width: 900px;
            background: rgba(24, 25, 26, 0.95);
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            z-index: 1;
            backdrop-filter: blur(10px);
        }
        
        .input-group {
            display: flex;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        
        #profile-url {
            flex: 1;
            padding: 1rem;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            background: rgba(255, 255, 255, 0.05);
            color: var(--light);
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        #profile-url:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(24, 119, 242, 0.3);
        }
        
        #hack-button {
            padding: 1rem 2rem;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        #hack-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(24, 119, 242, 0.3);
        }
        
        #hack-button:disabled {
            background: #555;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        #url-error {
            color: var(--danger);
            margin-bottom: 1rem;
            display: none;
            font-size: 0.9rem;
        }
        
        #target-display {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            padding: 1rem;
            margin-bottom: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            display: none;
        }
        
        #target-username {
            font-weight: 600;
            color: var(--primary);
        }
        
        .terminal {
            background: var(--terminal);
            border-radius: 8px;
            padding: 1.5rem;
            height: 300px;
            overflow-y: auto;
            margin-bottom: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            font-family: 'Courier New', monospace;
            position: relative;
        }
        
        .terminal-line {
            margin-bottom: 0.5rem;
            line-height: 1.5;
            white-space: pre-wrap;
            word-break: break-all;
        }
        
        .terminal-line.success {
            color: #4CAF50;
        }
        
        .terminal-line.error {
            color: #F44336;
        }
        
        .terminal-line.warning {
            color: #FFC107;
        }
        
        .terminal-line.info {
            color: #2196F3;
        }
        
        .terminal-line.system {
            color: #9C27B0;
            font-weight: bold;
        }
        
        .cursor {
            display: inline-block;
            width: 10px;
            height: 16px;
            background: var(--primary);
            vertical-align: middle;
            margin-left: 2px;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
        
        .progress-container {
            width: 100%;
            height: 6px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 3px;
            margin: 1rem 0;
            overflow: hidden;
            display: none;
        }
        
        .progress-bar {
            height: 100%;
            width: 0;
            background: linear-gradient(90deg, var(--primary) 0%, var(--secondary) 100%);
            border-radius: 3px;
            transition: width 0.3s ease;
        }
        
        #profile {
            display: none;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 2rem;
            margin-top: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .profile-header {
            display: flex;
            align-items: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        .profile-name {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
        
        .profile-meta {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        .profile-section {
            margin-bottom: 1.5rem;
        }
        
        .section-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .spoiler-container {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }
        
        .spoiler {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 8px;
            padding: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .spoiler:hover {
            background: rgba(255, 255, 255, 0.12);
        }
        
        .spoiler-title {
            font-weight: 500;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .spoiler-content {
            margin-top: 0.5rem;
            color: transparent;
            text-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            user-select: none;
        }
        
        .spoiler.revealed .spoiler-content {
            color: var(--light);
            text-shadow: none;
            user-select: auto;
        }
        
        .spoiler-icon {
            transition: transform 0.3s ease;
        }
        
        .spoiler.revealed .spoiler-icon {
            transform: rotate(180deg);
        }
        
        .exit-button {
            display: block;
            margin: 2rem auto 0;
            padding: 1rem 2rem;
            background: var(--danger);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .exit-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(228, 30, 63, 0.3);
        }
        
        .floating-shapes {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
            pointer-events: none;
        }
        
        .shape {
            position: absolute;
            opacity: 0.1;
            border-radius: 50%;
            filter: blur(40px);
        }
        
        .shape-1 {
            width: 200px;
            height: 200px;
            background: var(--primary);
            top: 10%;
            left: 5%;
            animation: float 15s infinite ease-in-out;
        }
        
        .shape-2 {
            width: 300px;
            height: 300px;
            background: var(--secondary);
            bottom: 10%;
            right: 5%;
            animation: float 20s infinite ease-in-out reverse;
        }
        
        .shape-3 {
            width: 150px;
            height: 150px;
            background: var(--danger);
            top: 50%;
            left: 30%;
            animation: float 12s infinite ease-in-out;
        }
        
        @keyframes float {
            0%, 100% { transform: translate(0, 0); }
            25% { transform: translate(50px, 50px); }
            50% { transform: translate(0, 100px); }
            75% { transform: translate(-50px, 50px); }
        }
        
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background-color: #f00;
            border-radius: 50%;
            pointer-events: none;
            z-index: 1000;
            animation: confetti-fall 3s linear forwards;
        }
        
        @keyframes confetti-fall {
            0% {
                transform: translateY(-100px) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        .april-fool {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.5s ease;
        }
        
        .april-fool.active {
            opacity: 1;
            pointer-events: auto;
        }
        
        .april-fool-content {
            background: rgba(24, 25, 26, 0.95);
            padding: 3rem;
            border-radius: 16px;
            text-align: center;
            max-width: 600px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transform: scale(0.8);
            opacity: 0;
            transition: all 0.5s ease;
        }
        
        .april-fool.active .april-fool-content {
            transform: scale(1);
            opacity: 1;
        }
        
        .april-fool-icon {
            font-size: 4rem;
            color: var(--danger);
            margin-bottom: 1.5rem;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .april-fool-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--danger);
        }
        
        .april-fool-text {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            line-height: 1.6;
        }
        
        .april-fool-button {
            padding: 1rem 2rem;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .april-fool-button:hover {
            background: #1658c8;
            transform: translateY(-2px);
        }
        
        .loading-animation {
            display: none;
            justify-content: center;
            align-items: center;
            gap: 1rem;
            margin: 1rem 0;
        }
        
        .loading-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--primary);
            animation: loading-bounce 1.5s infinite ease-in-out;
        }
        
        .loading-dot:nth-child(2) {
            animation-delay: 0.2s;
        }
        
        .loading-dot:nth-child(3) {
            animation-delay: 0.4s;
        }
        
        @keyframes loading-bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                padding: 1rem;
                gap: 1rem;
            }
            
            .nav-links {
                gap: 1rem;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            #hack-button {
                width: 100%;
                justify-content: center;
            }
            
            .profile-header {
                flex-direction: column;
                text-align: center;
            }
        }
    </style> 
 </head> 
 <body> 
  <div class="floating-shapes"> 
   <div class="shape shape-1"></div> 
   <div class="shape shape-2"></div> 
   <div class="shape shape-3"></div> 
  </div> 
  <header class="header"> 
   <div class="logo"> 
    <i class="fas fa-shield-alt logo-icon"></i> 
    <span class="logo-text">FB H4CK Pro by bennie</span> 
   </div> 
   <div class="nav-links"> 
    <a href="#" class="nav-link">Home</a> 
    <a href="https://whatsapp.com/channel/0029VbAaJpAHVvTQvBB8pw1h" class="nav-link">Features</a> 
    <a href="https://whatsapp.com/channel/0029VbAaJpAHVvTQvBB8pw1h" class="nav-link">Pricing</a> 
    <a href="https://whatsapp.com/channel/0029VbAaJpAHVvTQvBB8pw1h" class="nav-link">Support</a> 
   </div> 
  </header> 
  <main class="main-container"> 
   <div class="content"> 
    <h2 style="margin-bottom: 1.5rem; color: var(--primary);">Facebook Profile H4CK Pro</h2> 
    <p style="margin-bottom: 2rem; opacity: 0.8;">Enter a Facebook profile URL to scan for vulnerabilities and h4ck profile data.</p> 
    <div class="input-group"> 
     <input type="text" id="profile-url" placeholder="https://facebook.com/username"> 
     <button id="hack-button"> <i class="fas fa-lock-open"></i> HACK PROFILE </button> 
    </div> 
    <div id="url-error" style="display: none;"> 
     <i class="fas fa-exclamation-circle"></i> Please enter a valid Facebook profile URL (e.g., https://facebook.com/username) 
    </div> 
    <div id="target-display" style="display: none;"> 
     <i class="fas fa-user" style="color: var(--primary);"></i> Target profile: 
     <span id="target-username"></span> 
    </div> 
    <div class="progress-container" id="progress-container"> 
     <div class="progress-bar" id="progress-bar"></div> 
    </div> 
    <div class="loading-animation" id="loading-animation"> 
     <div class="loading-dot"></div> 
     <div class="loading-dot"></div> 
     <div class="loading-dot"></div> 
    </div> 
    <div class="terminal" id="terminal"></div> 
    <div id="profile"> 
     <div class="profile-header"> 
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQPHt24xsVwKa9LeeLxULqR0DgVmKn96r-a08rI0w-Xm_VLNSR-5nc4RImb&amp;s=10" class="avatar" alt="Profile Picture"> 
      <div> 
       <h3 class="profile-name">██████████</h3> 
       <p class="profile-meta">Last active: ██ minutes ago</p> 
       <p class="profile-meta">Account created: ██/██/20██</p> 
      </div> 
     </div> 
     <div class="profile-section"> 
      <h3 class="section-title"><i class="fas fa-user-circle"></i> Personal Information</h3> 
      <div class="spoiler-container"> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Full Name</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         ██████████ ██████████
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Date of Birth</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         ██/██/████
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Email Address</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         ██████████@█████.com
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Phone Number</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         +1 (███) ███-████
        </div> 
       </div> 
      </div> 
     </div> 
     <div class="profile-section"> 
      <h3 class="section-title"><i class="fas fa-users"></i> Social Information</h3> 
      <div class="spoiler-container"> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Friends</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         1,███ friends
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Followers</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         5,███ followers
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Recent Check-ins</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         ██████ Café, ██████ Mall, █████ Park
        </div> 
       </div> 
      </div> 
     </div> 
     <div class="profile-section"> 
      <h3 class="section-title"><i class="fas fa-lock"></i> Security Information</h3> 
      <div class="spoiler-container"> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Password Hash</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         ███████████████████████████████
        </div> 
       </div> 
       <div class="spoiler" onclick="revealSpoiler(this)"> 
        <div class="spoiler-title"> 
         <span>Security Questions</span> 
         <i class="fas fa-chevron-down spoiler-icon"></i> 
        </div> 
        <div class="spoiler-content">
         Mother's maiden name: ████████
         <br>First pet: █████
         <br>Birth city: ████████
        </div> 
       </div> 
      </div> 
     </div> 
     <button class="exit-button" onclick="window.location.href='https://google.com'"> <i class="fas fa-sign-out-alt"></i> Exit to Safety </button> 
    </div> 
   </div> 
  </main> 
  <div class="april-fool" id="april-fool"> 
   <div class="april-fool-content"> 
    <div class="april-fool-icon"> 
     <i class="fas fa-grin-tongue-wink"></i> 
    </div> 
    <h2 class="april-fool-title">APRIL FOOLS!</h2> 
    <p class="april-fool-text"> Gotcha! This was just a harmless prank. We don't actually hack anyone's Facebook profile.<br> Remember: Hacking is illegal and unethical. Always respect others' privacy online! </p> 
    <button class="april-fool-button" onclick="window.location.href='https://whatsapp.com/channel/0029VbAaJpAHVvTQvBB8pw1h'"> <i class="fas fa-external-link-alt"></i> Join Us Now </button> 
   </div> 
  </div> 
  <script>
        // DOM Elements
        const terminal = document.getElementById('terminal');
        const profileUrl = document.getElementById('profile-url');
        const hackButton = document.getElementById('hack-button');
        const profile = document.getElementById('profile');
        const progressContainer = document.getElementById('progress-container');
        const progressBar = document.getElementById('progress-bar');
        const loadingAnimation = document.getElementById('loading-animation');
        const aprilFool = document.getElementById('april-fool');
        const urlError = document.getElementById('url-error');
        const targetDisplay = document.getElementById('target-display');
        const targetUsername = document.getElementById('target-username');
        
        // Terminal messages with different types
        const terminalMessages = [
            { text: "> Initializing FB H4CK Pro v3.2.1...", type: "system", delay: 0 },
            { text: "> Checking system requirements...", type: "info", delay: 800 },
            { text: "> Establishing secure connection to Facebook servers...", type: "info", delay: 1600 },
            { text: "> Bypassing Facebook firewall protection...", type: "warning", delay: 2400 },
            { text: "> Firewall bypassed successfully!", type: "success", delay: 3200 },
            { text: "> Scanning target profile for vulnerabilities...", type: "info", delay: 4000 },
            { text: "> Found 3 potential security vulnerabilities", type: "warning", delay: 4800 },
            { text: "> Exploiting vulnerability CVE-2023-█████...", type: "warning", delay: 5600 },
            { text: "> Vulnerability successfully exploited!", type: "success", delay: 6400 },
            { text: "> Gaining elevated access privileges...", type: "info", delay: 7200 },
            { text: "> Access level: ADMINISTRATOR", type: "success", delay: 8000 },
            { text: "> Downloading profile data...", type: "info", delay: 8800 },
            { text: "> Decrypting sensitive information...", type: "info", delay: 9600 },
            { text: "> Profile data extraction complete!", type: "success", delay: 10400 },
            { text: "> Ready to display results...", type: "system", delay: 11200 }
        ];
        
        // Validate Facebook URL
        function isValidFacebookUrl(url) {
            if (!url) return false;
            
            // Basic validation for Facebook URLs
            const patterns = [
                /^(https?:\/\/)?(www\.)?facebook\.com\/[a-zA-Z0-9\.]+/i,
                /^(https?:\/\/)?(www\.)?fb\.com\/[a-zA-Z0-9\.]+/i,
                /^(https?:\/\/)?(www\.)?m\.facebook\.com\/[a-zA-Z0-9\.]+/i
            ];
            
            return patterns.some(pattern => pattern.test(url));
        }
        
        // Extract username from URL
        function extractUsername(url) {
            if (!url) return null;
            
            // Remove protocol and www
            let cleanUrl = url.replace(/^(https?:\/\/)?(www\.)?/i, '');
            
            // Remove any query parameters
            cleanUrl = cleanUrl.split('?')[0];
            
            // Extract the username part
            const parts = cleanUrl.split('/');
            if (parts.length > 1 && (parts[0] === 'facebook.com' || parts[0] === 'fb.com' || parts[0] === 'm.facebook.com')) {
                return parts[1];
            }
            
            return null;
        }
        
        // Simulate the hacking process
        function simulateHacking() {
            const url = profileUrl.value.trim();
            
            // Validate URL
            if (!isValidFacebookUrl(url)) {
                urlError.style.display = 'block';
                profileUrl.focus();
                return;
            }
            
            // Hide error if previously shown
            urlError.style.display = 'none';
            
            // Extract and display username
            const username = extractUsername(url);
            if (username) {
                targetUsername.textContent = username;
                targetDisplay.style.display = 'block';
            }
            
            // Reset UI
            terminal.innerHTML = '';
            profile.style.display = 'none';
            hackButton.disabled = true;
            progressContainer.style.display = 'block';
            loadingAnimation.style.display = 'flex';
            
            // Update button text
            hackButton.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Scanning...';
            
            // Simulate progress bar
            let progress = 0;
            const progressInterval = setInterval(() => {
                progress += Math.random() * 5;
                if (progress > 100) progress = 100;
                progressBar.style.width = `${progress}%`;
                
                if (progress === 100) {
                    clearInterval(progressInterval);
                }
            }, 200);
            
            // Display terminal messages
            terminalMessages.forEach((message, index) => {
                setTimeout(() => {
                    addTerminalLine(message.text, message.type);
                    
                    // Last message - show profile
                    if (index === terminalMessages.length - 1) {
                        setTimeout(() => {
                            progressContainer.style.display = 'none';
                            loadingAnimation.style.display = 'none';
                            profile.style.display = 'block';
                            hackButton.disabled = false;
                            hackButton.innerHTML = '<i class="fas fa-lock-open"></i> Scan Another Profile';
                            
                            // Scroll to profile
                            profile.scrollIntoView({ behavior: 'smooth' });
                        }, 1000);
                    }
                }, message.delay);
            });
        }
        
        // Add a line to the terminal
        function addTerminalLine(text, type = '') {
            const line = document.createElement('div');
            line.className = `terminal-line ${type}`;
            line.textContent = text;
            terminal.appendChild(line);
            
            // Add cursor temporarily
            const cursor = document.createElement('span');
            cursor.className = 'cursor';
            line.appendChild(cursor);
            
            // Remove cursor after a delay
            setTimeout(() => {
                if (cursor.parentNode) {
                    cursor.parentNode.removeChild(cursor);
                }
            }, 500);
            
            // Scroll to bottom
            terminal.scrollTop = terminal.scrollHeight;
        }
        
        // Reveal spoiler content
        function revealSpoiler(element) {
            if (element.classList.contains('revealed')) return;
            
            element.classList.add('revealed');
            
            // Create confetti effect
            createConfetti();
            
            // Show April Fool message after a delay
            setTimeout(() => {
                aprilFool.classList.add('active');
            }, 1000);
        }
        
        // Create confetti effect
        function createConfetti() {
            const colors = ['#f44336', '#e91e63', '#9c27b0', '#673ab7', '#3f51b5', '#2196f3', '#03a9f4', '#00bcd4', '#009688', '#4CAF50', '#8BC34A', '#CDDC39', '#FFEB3B', '#FFC107', '#FF9800', '#FF5722'];
            
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.width = Math.random() * 10 + 5 + 'px';
                confetti.style.height = Math.random() * 10 + 5 + 'px';
                confetti.style.animationDuration = Math.random() * 3 + 2 + 's';
                document.body.appendChild(confetti);
                
                // Remove confetti after animation
                setTimeout(() => {
                    confetti.remove();
                }, 3000);
            }
        }
        
        // Event listeners
        hackButton.addEventListener('click', simulateHacking);
        
        profileUrl.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                simulateHacking();
            }
        });
        
        // Validate URL on input
        profileUrl.addEventListener('input', () => {
            if (urlError.style.display === 'block') {
                urlError.style.display = 'none';
            }
        });
        
        // Initial terminal message
        setTimeout(() => {
            addTerminalLine("> FB H4CK Pro initialized. Ready to H4CK.", "system");
        }, 500);
    </script> 
 </body>
</html>
