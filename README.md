- 👋 Hi, I’m @bhushan-spek
- 👀 I’m interested in ...
- 🌱 I need to learn work ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
bhushan-spek/bhushan-spek is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vista.Ai - Login</title>
    <!-- SweetAlert2 CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.min.css">
    <style>
        /* Basic Styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #232323; /* Matte Black */
            color: #fff; /* Text color for better contrast */
        }
        body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: url('background.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #fff;
}
        /* Top Navigation Buttons */
        .top-nav {
            position: absolute;
            top: 10px;
            right: 10px;
            display: flex;
            gap: 10px;
        }
        .top-nav button {
            padding: 10px 15px;
            background: #00bcd4;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }
        .top-nav button:hover {
            background: #0097a7;
        }
        /* Welcome Message */
        .welcome-message {
            font-size: 2rem;
            font-weight: bold;
            color: #00bcd4; /* Light blue for contrast */
            margin-bottom: 1.5rem;
            text-align: center;
        }
        /* Small Login Form */
        .small-login-form {
            background: #333; /* Dark background for the form */
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
            width: 100%;
            max-width: 320px;
        }
        .small-login-form h2 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            text-align: center;
            color: #fff;
        }
        .small-login-form label {
            font-size: 0.9rem;
            display: block;
            margin-bottom: 0.5rem;
            color: #ddd; /* Lighter text for visibility */
        }
        .small-login-form input {
            width: 100%;
            padding: 0.7rem;
            margin-bottom: 1rem;
            border: 1px solid #444;
            border-radius: 5px;
            background: #232323;
            color: #fff;
        }
        .small-login-form button {
            width: 100%;
            padding: 0.8rem;
            background: #00bcd4;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .small-login-form button:hover {
            background: #0097a7;
        }
        /* Forgotten Password Link */
        .forgot-password {
            margin-top: 10px;
            text-align: center;
        }
        .forgot-password a {
            color: #00bcd4;
            text-decoration: none;
        }
        .forgot-password a:hover {
            text-decoration: underline;
        }
        /* Create New Account Button */
        .create-account {
            margin-top: 20px;
            text-align: center;
        }
        .create-account button {
            padding: 0.8rem 1.5rem;
            background: #4caf50; /* Green color */
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }
        .create-account button:hover {
            background: #388e3c;
        }
    </style>
</head>
<body>
    <!-- Top Navigation Buttons -->
    <div class="top-nav">
        <button onclick="showAbout()">About</button>
        <button onclick="showService()">Service</button>
        <button onclick="showContact()">Contact Us</button>
    </div>
    <!-- Welcome Message -->
    <div class="welcome-message">Welcome to Vista.Ai</div>
    <!-- Small Login Form -->
    <div class="small-login-form">
        <h2>Login</h2>
        <form id="loginForm">
            <label for="username">Username</label>
            <input type="text" id="username" name="username" placeholder="Enter your username" required>
            <label for="password">Password</label>
            <input type="password" id="password" name="password" placeholder="Enter your password" required>
            <button type="button" id="loginButton">Login</button>
        </form>
        <div class="forgot-password">
            <a id="forgotPasswordLink" href="#">Forgotten Password?</a>
        </div>
        <!-- Create New Account Button -->
        <div class="create-account">
            <button id="createAccountButton">Create New Account</button>
        </div>
    </div>
    <!-- SweetAlert2 JS -->
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
    <script>
        // Top Navigation Button Functions
        function showAbout() {
            Swal.fire({
                title: "About Us",
                text: "Vista.Ai is your trusted partner in innovation.",
            });
        }
        function showService() {
            Swal.fire({
                title: "Our Services",
                text: "We provide top-notch IT solutions tailored to your needs.",
            });
        }
        function showContact() {
            Swal.fire({
                title: "Contact Us",
                text: "Email: bhushankumar10817@gmail.com\nPhone: +91-1231234567",
            });
        }
        // Handle Login Button Click
        document.getElementById("loginButton").addEventListener("click", function () {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            if (username === "" || password === "") {
                Swal.fire("Oops...", "Please fill in all fields!", "warning");
            } else {
                Swal.fire("Login Successful", `Welcome, ${username}!`, "success").then(() => {
                    window.location.href = "SOLUTION-VISTA.html"; // Replace with your dashboard URL
                });
            }
        });
        // Forgot Password Functionality
        document.getElementById("forgotPasswordLink").addEventListener("click", function () {
            Swal.fire({
                title: "Reset Password",
                input: "email",
                inputLabel: "Enter your registered email",
                inputPlaceholder: "yourname@example.com",
                showCancelButton: true,
                confirmButtonText: "Submit",
                preConfirm: (email) => {
                    if (!email) {
                        Swal.showValidationMessage("Email is required!");
                    }
                    return new Promise((resolve) => setTimeout(() => resolve(true), 1000)); // Simulate delay
                }
            }).then((result) => {
                if (result.isConfirmed) {
                    Swal.fire("Success", "Password reset link has been sent to your email.", "success");
                }
            });
        });
        // Create New Account
        document.getElementById("createAccountButton").addEventListener("click", function () {
            Swal.fire("Create Account", "         ", "info").then(() => {
                window.location.href = "upsign123123.html"; // Replace with your registration URL
            });
        });
    </script>
    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Vista.Ai Solutions. All rights reserved.</p>
    </footer>
</body>
</html>
