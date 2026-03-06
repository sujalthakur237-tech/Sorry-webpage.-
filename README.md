<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm Sorry 💖</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ffeef8 0%, #fff0f6 50%, #ffe6f0 100%);
            overflow: hidden;
        }

        /* Floral Background Animation */
        .flower {
            position: absolute;
            opacity: 0.6;
            font-size: 3rem;
            animation: float 6s ease-in-out infinite;
        }

        .flower:nth-child(1) {
            top: 10%;
            left: 5%;
            animation-delay: 0s;
        }

        .flower:nth-child(2) {
            top: 15%;
            right: 8%;
            animation-delay: 1s;
            font-size: 2.5rem;
        }

        .flower:nth-child(3) {
            bottom: 15%;
            left: 10%;
            animation-delay: 2s;
            font-size: 2rem;
        }

        .flower:nth-child(4) {
            bottom: 10%;
            right: 5%;
            animation-delay: 1.5s;
            font-size: 2.5rem;
        }

        .flower:nth-child(5) {
            top: 50%;
            left: 2%;
            animation-delay: 0.5s;
            font-size: 2rem;
        }

        .flower:nth-child(6) {
            top: 30%;
            right: 3%;
            animation-delay: 2.5s;
            font-size: 2.2rem;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        /* Main Container */
        .container {
            position: relative;
            z-index: 10;
            text-align: center;
            background: rgba(255, 255, 255, 0.95);
            padding: 3rem 2rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
            max-width: 500px;
            width: 90%;
            backdrop-filter: blur(10px);
        }

        h1 {
            color: #d4547b;
            margin-bottom: 1.5rem;
            font-size: 2.5rem;
            letter-spacing: 1px;
        }

        .emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }

        .subtitle {
            color: #888;
            font-size: 0.95rem;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        /* Sorry Button */
        .sorry-btn {
            background: linear-gradient(135deg, #ff6b9d 0%, #d4547b 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            box-shadow: 0 10px 25px rgba(255, 107, 157, 0.4);
            margin-bottom: 2rem;
        }

        .sorry-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(255, 107, 157, 0.6);
        }

        .sorry-btn:active {
            transform: translateY(-1px);
        }

        /* Message Box */
        .message-box {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.6s ease, opacity 0.6s ease;
            opacity: 0;
        }

        .message-box.show {
            max-height: 600px;
            opacity: 1;
        }

        .message-text {
            background: linear-gradient(135deg, #ffe6f0 0%, #fff0f6 100%);
            border-left: 4px solid #ff6b9d;
            padding: 2rem;
            border-radius: 10px;
            color: #555;
            line-height: 1.8;
            font-size: 1rem;
            text-align: left;
            margin-top: 1rem;
        }

        .message-text p {
            margin-bottom: 1rem;
        }

        .message-text p:last-child {
            margin-bottom: 0;
        }

        .signature {
            margin-top: 1.5rem;
            color: #d4547b;
            font-style: italic;
            font-weight: 600;
        }

        /* Footer */
        .footer {
            position: fixed;
            bottom: 20px;
            right: 20px;
            font-size: 0.85rem;
            color: #999;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .container {
                padding: 2rem 1.5rem;
                margin: 20px;
            }

            h1 {
                font-size: 2rem;
            }

            .emoji {
                font-size: 2.5rem;
            }

            .sorry-btn {
                padding: 12px 30px;
                font-size: 1rem;
            }

            .message-text {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Floral Background -->
    <div class="flower">🌸</div>
    <div class="flower">🌹</div>
    <div class="flower">🌺</div>
    <div class="flower">🌼</div>
    <div class="flower">🌻</div>
    <div class="flower">🌷</div>

    <!-- Main Container -->
    <div class="container">
        <span class="emoji">💖</span>
        <h1>I'm Sorry</h1>
        <p class="subtitle">I want to apologize sincerely. Please hear me out.</p>
        
        <button class="sorry-btn" onclick="toggleMessage()">Let me explain...</button>

        <!-- Hidden Message -->
        <div class="message-box" id="messageBox">
            <div class="message-text">
                <p>I'm really sorry…</p>

                <p>Whatever mistake I made, I sincerely apologize from the bottom of my heart. I never intended to hurt you. Sometimes a person says or does something without thinking, and later realizes how much it might have hurt someone.</p>
                
                <p>I will make sure that something like this never happens again, and I won't let it happen in the future.</p>
                
                <p>That's all I want to say… I am truly sorry.</p>
                
                <div class="signature">With all my sincerity,<br>Someone who cares about you 💕</div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        Made with 💖
    </div>

    <!-- JavaScript -->
    <script>
        function toggleMessage() {
            const messageBox = document.getElementById('messageBox');
            const btn = document.querySelector('.sorry-btn');
            
            if (messageBox.classList.contains('show')) {
                messageBox.classList.remove('show');
                btn.textContent = 'Let me explain...';
            } else {
                messageBox.classList.add('show');
                btn.textContent = 'Hide message';
            }
        }
    </script>
</body>
</html>
