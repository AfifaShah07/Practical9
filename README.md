<!DOCTYPE html>
<html>
<head>
  <title>Registration Form Validation</title>
  <script>
    function validateForm() {
      let name = document.forms["regForm"]["name"].value;
      let email = document.forms["regForm"]["email"].value;
      let phone = document.forms["regForm"]["phone"].value;
      let password = document.forms["regForm"]["password"].value;

      if (name == "") {
        alert("Name must be filled out");
        return false;
      }

      if (email == "" || !email.includes("@")) {
        alert("Please enter a valid email address");
        return false;
      }

      if (phone == "" || isNaN(phone) || phone.length != 10) {
        alert("Please enter a valid 10-digit phone number");
        return false;
      }

      if (password.length < 6) {
        alert("Password must be at least 6 characters long");
        return false;
      }

      alert("Registration Successful!");
      return true;
    }
  </script>
</head>
<body>
  <h2>Student Registration Form</h2>
  <form name="regForm" onsubmit="return validateForm()">
    Name: <input type="text" name="name"><br><br>
    Email: <input type="text" name="email"><br><br>
    Phone: <input type="text" name="phone"><br><br>
    Password: <input type="password" name="password"><br><br>
    <input type="submit" value="Register">
  </form>
</body>
</html># Practical9
admission registration page
