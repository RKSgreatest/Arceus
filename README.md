<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Family Group Website</title>
    <style>
        body { font-family: Arial, sans-serif; }
        .container { max-width: 800px; margin: auto; padding: 20px; }
        .hidden { display: none; }
        .content { display: none; }
        .password-section { text-align: center; margin-top: 100px; }
        .password-section input { padding: 10px; margin: 10px; }
        .password-section button { padding: 10px; background-color: #4CAF50; color: white; border: none; cursor: pointer; }
        .password-section button:hover { background-color: #45a049; }
    </style>
</head>
<body>

<div class="container">
    <!-- Password protection section -->
    <div class="password-section" id="passwordSection">
        <h2>Enter Password to Access the Site</h2>
        <input type="password" id="password" placeholder="Enter Password">
        <button onclick="checkPassword()">Enter</button>
        <p id="errorMessage" class="hidden" style="color: red;">Incorrect password, please try again.</p>
    </div>

    <!-- Content that appears after password is entered -->
    <div class="content" id="contentSection">
        <h1>Welcome to the Family Group Website!</h1>
        <h2>Game Recommendations</h2>
        <div>
            <h3>Game 1: Game Name</h3>
            <img src="game-image.jpg" alt="Game Image" style="width: 300px;">
            <p>Description of Game 1</p>
        </div>
        <div>
            <h3>Game 2: Another Game</h3>
            <img src="another-game-image.jpg" alt="Another Game Image" style="width: 300px;">
            <p>Description of Game 2</p>
        </div>

        <h2>Movie Recommendations</h2>
        <div>
            <h3>Movie 1: Movie Name</h3>
            <img src="movie-image.jpg" alt="Movie Image" style="width: 300px;">
            <p>Description of Movie 1</p>
        </div>
        <div>
            <h3>Movie 2: Another Movie</h3>
            <img src="another-movie-image.jpg" alt="Another Movie Image" style="width: 300px;">
            <p>Description of Movie 2</p>
        </div>
    </div>
</div>

<script>
    function checkPassword() {
        var enteredPassword = document.getElementById("password").value;
        var correctPassword = "family123"; // Change to your desired password
        
        if (enteredPassword === correctPassword) {
            document.getElementById("passwordSection").style.display = "none";
            document.getElementById("contentSection").style.display = "block";
        } else {
            document.getElementById("errorMessage").classList.remove("hidden");
        }
    }
</script>

</body>
</html>
