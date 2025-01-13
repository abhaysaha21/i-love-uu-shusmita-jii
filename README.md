
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I Love You Jii</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            color: white;
            text-align: center;
        }
        .slide {
            display: none;
            padding: 50px;
        }
        .slide.active {
            display: block;
        }
        .button {
            background-color: #ff66cc;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 25px;
        }
        .button:hover {
            background-color: #ff3385;
        }
    </style>
</head>
<body>

    <div id="slide1" class="slide active">
        <h2>Do you love me? Yes or No</h2>
        <button class="button" id="yes-btn">Yes</button>
        <button class="button" id="no-btn">No</button>
    </div>

    <div id="slide2" class="slide">
        <h2>I love you Jii very much ❤️❤️</h2>
        <button class="button" id="continue-btn">Continue</button>
    </div>

    <div id="slide3" class="slide">
        <h2>You are my world Jii, and please accept my proposal Sushmita Jii.</h2>
        <button class="button" id="accept-btn">Accept Proposal</button>
    </div>

    <script>
        // Slide navigation
        const slide1 = document.getElementById("slide1");
        const slide2 = document.getElementById("slide2");
        const slide3 = document.getElementById("slide3");

        const yesButton = document.getElementById("yes-btn");
        const noButton = document.getElementById("no-btn");
        const continueButton = document.getElementById("continue-btn");
        const acceptButton = document.getElementById("accept-btn");

        // Event listener for the "No" button
        noButton.addEventListener("click", function() {
            // Show message when "No" is clicked
            alert("You clicked 'No', but don't worry, we'll change it to 'Yes' automatically!");
            
            // Automatically change "No" to "Yes"
            yesButton.click();  // This simulates clicking the "Yes" button
        });

        // Event listener for the "Yes" button
        yesButton.addEventListener("click", function() {
            // Slide 1: Hide it and show slide 2
            slide1.classList.remove("active");
            slide2.classList.add("active");
        });

        // Event listener for the "Continue" button
        continueButton.addEventListener("click", function() {
            // Slide 2: Hide it and show slide 3
            slide2.classList.remove("active");
            slide3.classList.add("active");
        });

        // Event listener for the "Accept Proposal" button
        acceptButton.addEventListener("click", function() {
            // Display a message or handle the final step (if necessary)
            alert("Proposal Accepted! ❤️💍");
        });
    </script>

</body>
</html>
