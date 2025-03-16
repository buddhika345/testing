@@ -0,0 +1,93 @@
 <!DOCTYPE html>
 <html lang="en">
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Login Form</title>
     <style>
         body {
             font-family: Arial, sans-serif;
             display: flex;
             justify-content: center;
             align-items: center;
             height: 100vh;
             background-color: #f4f4f4;
         }
         .login-container {
             background: white;
             padding: 20px;
             border-radius: 10px;
             box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
             width: 300px;
         }
         input {
             width: 100%;
             padding: 10px;
             margin: 10px 0;
             border: 1px solid #ccc;
             border-radius: 5px;
         }
         .toggle-password {
             cursor: pointer;
             position: absolute;
             right: 10px;
             top: 40%;
         }
         button {
             width: 100%;
             padding: 10px;
             background: #28a745;
             color: white;
             border: none;
             border-radius: 5px;
             cursor: pointer;
         }
         button:hover {
             background: #218838;
         }
         .input-group {
             position: relative;
         }
     </style>
 </head>
 <body>
 
 <div class="login-container">
     <h2>Login</h2>
     <form onsubmit="return loginUser(event)">
         <label for="email">Email:</label>
         <input type="email" id="email" required placeholder="Enter your email">
         
         <label for="password">Password:</label>
         <div class="input-group">
             <input type="password" id="password" required placeholder="Enter your password">
             <span class="toggle-password" onclick="togglePassword()">👁️</span>
         </div>
         
         <button type="submit">Login</button>
     </form>
 </div>
 
 <script>
     function togglePassword() {
         const passwordField = document.getElementById("password");
         passwordField.type = passwordField.type === "password" ? "text" : "password";
     }
 
     function loginUser(event) {
         event.preventDefault();
         const email = document.getElementById("email").value;
         const password = document.getElementById("password").value;
 
         if (!email || !password) {
             alert("Please fill in all fields.");
             return false;
         }
 
         alert("Login successful! (This is just a demo)");
         return true;
     }
 </script>
 
 </body>
 </html>

