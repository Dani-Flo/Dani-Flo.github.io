<!DOCTYPE html>
<html>

<head>
    <title>Daniels Website</title>
    <style>
        /* General body styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            /* Animated gradient background */
            background: linear-gradient(135deg, #a4508b, #5f0a87);
            background-size: 400% 400%;
            animation: gradientAnimation 10s ease infinite;
        }

        /* Gradient animation keyframes */
        @keyframes gradientAnimation {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        /* Container for the content */
        .container {
            text-align: center;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            background-color: #ffffff;
        }

        /* Heading styling */
        h1 {
            color: #333;
            margin-bottom: 20px;
        }

        /* Paragraph styling */
        p {
            color: #666;
            margin-bottom: 10px;
        }

        /* Link styling */
        a {
            color: #008cba;
            text-decoration: none;
            font-weight: bold;
            padding: 10px 20px;
            background-color: #f0f8ff;
            border: 2px solid #008cba;
            border-radius: 5px;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        /* Hover effect for link */
        a:hover {
            background-color: #008cba;
            color: #fff;
        }

        /* Styling for joke button */
        #jokeButton {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #008cba;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        /* Button hover effect */
        #jokeButton:hover {
            background-color: #005f73;
        }

        /* Styling for joke display */
        #jokeDisplay {
            margin-top: 20px;
            color: #333;
            font-weight: bold;
        }

        /* Custom cursor styling */
        .cursor {
            position: fixed;
            top: 0;
            left: 0;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 2px solid #fff;
            pointer-events: none;
            transform: translate(-50%, -50%);
            transition: background-color 0.3s ease;
            box-shadow: 0 0 10px 2px #fff;
        }
    </style>

    <script>
        // Array of funny and appropriate jokes
        const jokes = [
            "Why don't scientists trust atoms? Because they make up everything!",
            "I'm reading a book on anti-gravity. It's impossible to put down!",
            "Why don't programmers like nature? It has too many bugs.",
            "What do you call fake spaghetti? An impasta!",
            "How does a penguin build its house? Igloos it together!",
            "What do you call a bear with no teeth? A gummy bear!",
            "Why did the scarecrow win an award? Because he was outstanding in his field!",
            "What did one wall say to the other wall? I'll meet you at the corner!",
            "Why can't you trust an atom? Because they make up everything!",
            "Why do cows wear bells? Because their horns don't work!",
            "Why did the tomato turn red? Because it saw the salad dressing!",
            "What do you call a fish with no eyes? Fsh!",
            "Why don't skeletons fight each other? They don't have the guts!",
            "Why do seagulls fly over the ocean? Because if they flew over the bay, they'd be bagels!",
            "What did the grape do when it got stepped on? It let out a little wine!",
            "Why was the math book sad? It had too many problems!",
            "How do you organize a space party? You planet!",
            "Why don't eggs tell each other secrets? They might crack up!",
            "Why was the broom late? It swept in!",
            "Why don't oysters donate to charity? Because they're shellfish!",
            "What did the ocean say to the beach? Nothing, it just waved!",
            "Why don't we ever tell secrets on a farm? Because the potatoes have eyes and the corn has ears!",
            "How does a scientist freshen their breath? With experi-mints!",
            "Why was the picture sent to jail? It was framed!",
            "Why was the computer cold? It left its Windows open!",
            "Why was the cookie sad? Because its mother was a wafer too long!",
            "What do you call a dinosaur with an extensive vocabulary? A thesaurus!",
            "Why did the chicken go to the seance? To talk to the other side!",
            "What did one plate say to the other plate? Lunch is on me!",
            "What do you call cheese that isn't yours? Nacho cheese!"
        ];

        // Function to display a single random joke
        function displayRandomJoke() {
            const jokeDisplay = document.getElementById('jokeDisplay');
            // Generate one random joke and display it
            const randomIndex = Math.floor(Math.random() * jokes.length);
            jokeDisplay.innerHTML = jokes[randomIndex];
        }

        // Function to simulate a fake virus scan
        function fakeScan() {
            const scanResults = document.getElementById('scanResults');
            // Display fake scan results
            scanResults.innerHTML = "Scanning website for viruses...<br>Scan complete! No viruses found!";
        }

        // Custom cursor function
        const cursor = document.createElement('div');
        cursor.className = 'cursor';
        document.body.appendChild(cursor);

        document.addEventListener('mousemove', (e) => {
            cursor.style.top = e.clientY + 'px';
            cursor.style.left = e.clientX + 'px';
        });
    </script>
</head>

<body>
    <div class="container">
        <h1>Hallo Toni, hier findest du den Link</h1>
        <p>Klicke unten, um auf das Video zu gelangen, damit dein Vater nichts sieht</p>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">das video</a>

        <!-- Button to start the fake virus scan -->
        <button onclick="fakeScan()">Scan Website for Viruses</button>

        <!-- Display area for the scan results -->
        <div id="scanResults"></div>

        <!-- Button to generate a random joke -->
        <button id="jokeButton" onclick="displayRandomJoke()">Generate a Random Joke</button>

        <!-- Display area for the joke -->
        <div id="jokeDisplay"></div>
    </div>
</body>

</html>
