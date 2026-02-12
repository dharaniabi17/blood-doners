<!DOCTYPE html>
<html>
<head>
    <title>Google Classroom - School</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #4285F4, #34A853);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background: white;
            padding: 30px;
            border-radius: 10px;
            width: 350px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            display: none;
        }

        .container h2 {
            text-align: center;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
        }

        button {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            background: #4285F4;
            color: white;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background: #2c6adf;
        }

        .link-btn {
            background: #34A853;
        }

        .google-btn {
            background: #DB4437;
        }

        #signup { display: block; }
    </style>
</head>
<body>

<!-- SIGN UP PAGE -->
<div class="container" id="signup">
    <h2>Sign Up</h2>
    <input type="email" placeholder="Enter Email">
    <input type="password" placeholder="Enter Password">
    <button onclick="showLogin()">Sign Up</button>
</div>

<!-- LOGIN PAGE -->
<div class="container" id="login">
    <h2>Login</h2>
    <input type="text" placeholder="Register Number / Username">
    <input type="password" placeholder="Password">
    <button onclick="showUpload()">Login</button>
    <button class="google-btn">Sign in with Google</button>
    <button class="link-btn" onclick="showSignup()">Create a New Account</button>
</div>

<!-- ASSIGNMENT UPLOAD PAGE -->
<div class="container" id="upload">
    <h2>Upload Assignment</h2>
    <input type="file">
    <button>Upload File</button>
</div>

<script>
    function showLogin() {
        document.getElementById("signup").style.display = "none";
        document.getElementById("login").style.display = "block";
        document.getElementById("upload").style.display = "none";
    }

    function showSignup() {
        document.getElementById("signup").style.display = "block";
        document.getElementById("login").style.display = "none";
        document.getElementById("upload").style.display = "none";
    }

    function showUpload() {
        document.getElementById("signup").style.display = "none";
        document.getElementById("login").style.display = "none";
        document.getElementById("upload").style.display = "block";
    }
</script>

</body>
</html>
