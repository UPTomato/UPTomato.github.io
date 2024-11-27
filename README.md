<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Barry 63's Games</title>
    <style>
        /* Reset and global styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: white;
            text-align: center;
        }

        h1, h2 {
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 2rem;
        }

        h2 {
            font-size: 1.5rem;
            margin: 1.5rem 0;
        }

        a {
            text-decoration: none;
        }

        button {
            background: #ff5f6d;
            background: linear-gradient(135deg, #ff5f6d, #ffc371);
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            color: white;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s ease, box-shadow 0.2s ease, background 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        button:hover {
            background: linear-gradient(135deg, #ffc371, #ff5f6d);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
            transform: translateY(-2px);
        }

        button:active {
            transform: translateY(2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        /* Responsive design */
        @media (max-width: 768px) {
            h1, h2 {
                font-size: 1.5rem;
            }

            button {
                font-size: 1rem;
                padding: 12px 20px;
            }
        }
    </style>
</head>
<body>
    <h1>Press this button to go to Barry 63's games</h1>
    <a href="https://sites.google.com/view/unblocked-games-oli/home?authuser=0" target="_blank">
        <button id="gamesButton">Barry 63's Games</button>
    </a>

    <h2>Press this button to go straight to the fullscreen web app</h2>
    <a href="https://retrobowlbarry63sgames.w3spaces.com" target="_blank">
        <button id="fullscreenButton">Fullscreen Web App</button>
    </a>

    <script>
        // Add a click animation effect
        const buttons = document.querySelectorAll('button');

        buttons.forEach(button => {
            button.addEventListener('click', () => {
                button.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    button.style.transform = 'scale(1)';
                }, 150);
            });
        });
    </script>
</body>
</html>
