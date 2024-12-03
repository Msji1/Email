<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Welcome Form</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-color: #7e1126; /* Background color */
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      color: white;
    }

    .container {
      text-align: center;
      background-color: #821835;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    }

    h1 {
      font-size: 36px;
      margin-bottom: 20px;
    }

    input[type="text"], input[type="email"] {
      width: 80%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 4px;
      font-size: 16px;
    }

    button {
      background-color: #e63946; /* Button color */
      color: white;
      border: none;
      padding: 10px 30px;
      font-size: 13px;
      font-weight: bold;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 10px;
    }

    button:hover {
      background-color: #d62828;
    }

    p {
      font-size: 14px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Welcome</h1>
    <form id="submit-form">
      <input type="text" id="name" name="name" placeholder="Enter your name" required>
      <input type="email" id="email" name="email" placeholder="Enter your email" required>
      <button type="submit">Submit</button>
    </form>
    <p>Visit the official website after submit the form</p>
  </div>

  <script>
    const scriptURL = 'https://script.google.com/macros/s/AKfycbzY8dXD4jzhDNLFw7tuX6KRNJ6ngogM4wjxJNkyl10WbCIDmvJkYp_DpbccBGgvzOyZjA/exec'; // Replace with your Google Apps Script URL
    const form = document.getElementById('submit-form');

    form.addEventListener('submit', e => {
      e.preventDefault();
      const formData = new FormData(form);

      fetch(scriptURL, { method: 'POST', body: formData })
        .then(response => {
          window.location.href = 'https://76e7991dvael5yfmuc6815pm27.hop.clickbank.net/?&creative=Neo'; // Replace with your redirect URL
        })
        .catch(error => console.error('Error!', error.message));
    });
  </script>
</body>
</html>
