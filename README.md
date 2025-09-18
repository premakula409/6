# 6
HTML Program - 6
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>example of div</title>
</head>
<body>
    <h2>Contact Form</h2>
    <div>
        <label for ="name">Name:</label>
        <input type ="text" id="name" name="name" placeholder="Enter your name">
    </div>
    <br> 
    <div>
        <label for ="email">Email:</label>
        <input type ="email" id="email" name="email"  placeholder="Enter your email">
    </div>
    <br>
    <div>
        <label for ="phone">Phone Number:</label>
        <input type ="tel" id="phone" name="phone" placeholder="Enter your 10 digit number"
        pattern="[0-9]{10}" inputmode="numeric" required aria-required="true"
        aria-describedby="phone-error" onkeypress="restrictAlphabets(event)">
        <span id ="phone-error" role="alert" style="display: none;">numbers only.</span"></span>
    </div>
    <script>
        function restrictAlphabets(event){
            const key = event.key;
            if(!/[0-9]/.test(key) && key !== "Backspace"
            && key !== "ArrowLeft" && key !== "ArrowRight") {
                event.preventDefualt();
            }
        }

    </script>

</body>
</html>
