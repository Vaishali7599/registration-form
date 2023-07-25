<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Professional Registration Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
    }
    label, input {
      display: block;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>
  <h2>Professional Registration Form</h2>
  <form id="registrationForm" onsubmit="return validateForm()">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>

    <input type="submit" value="Register">
  </form>

  <script>
    function validateForm() {
      const nameInput = document.getElementById('name');
      const emailInput = document.getElementById('email');
      const passwordInput = document.getElementById('password');

      // Basic validation - check if fields are filled
      if (!nameInput.value || !emailInput.value || !passwordInput.value) {
        alert('Please fill out all fields.');
        return false;
      }

      // Additional validation can be added here, e.g., email format validation, password strength check, etc.

      return true;
    }
  </script>
</body>
</html>
