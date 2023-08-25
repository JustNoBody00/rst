<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Resignation Form</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      margin: 0;
    }

    header {
      background-color: #333;
      color: white;
      padding: 1rem;
    }

    nav ul {
      list-style: none;
      display: flex;
    }

    nav li {
      margin-right: 1rem;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    .container {
      max-width: 800px;
      margin: 2rem auto;
      padding: 2rem;
      background-color: white;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    }

    h1 {
      font-size: 24px;
      margin-bottom: 1rem;
    }

    label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: bold;
    }

    input, textarea, select {
      width: 100%;
      padding: 0.5rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      margin-bottom: 1rem;
    }

    textarea {
      resize: vertical;
    }

    button {
      background-color: #333;
      color: white;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 1rem;
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Service</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <div class="container">
    <h1>Resignation Form</h1>
    <form id="resignation-form" method="post">
      <label for="client-name">Client name</label>
      <input type="text" id="client-name" name="client-name" required>

      <label for="resignation-date">Resignation date</label>
      <input type="date" id="resignation-date" name="resignation-date" required>

      <label for="reason-for-resignation">Reason for resignation</label>
      <textarea id="reason-for-resignation" name="reason-for-resignation" rows="4" required></textarea>

      <label for="submit-option">Choose an option:</label>
      <select id="submit-option">
        <option value="submit">Submit resignation</option>
        <option value="cancel">Cancel request</option>
      </select>

      <button type="submit" id="submit-request">Submit</button>
    </form>
  </div>

  <footer>
    <!-- Add your footer content here -->
  </footer>

  <script>
    const submitRequestButton = document.getElementById("submit-request");
    const submitOptionSelect = document.getElementById("submit-option");
    const resignationForm = document.getElementById("resignation-form");

    resignationForm.addEventListener("submit", function(event) {
      event.preventDefault();

      if (submitOptionSelect.value === "submit") {
        // Logic to handle resignation submission
        alert("Resignation submitted!");
      } else if (submitOptionSelect.value === "cancel") {
        // Logic to handle cancel request
        alert("Cancel request submitted!");
      }
    });
  </script>
</body>
</html>
