#<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>The Ocean of Knowledge Coaching Academy - Admission Form</title>
  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f2f2f2;
      background-image: url('logo.png'); /* یہاں اپنی لوگو فائل کا نام یا لنک لگائیں */
      background-repeat: no-repeat;
      background-position: center center;
      background-size: 250px 250px; /* لوگو کا سائز ایڈجسٹ کریں */
      opacity: 1;
      position: relative;
    }
    /* لوگو کو تھوڑا ہلکا دکھانے کے لیے body کے اندر ایک overlay بنائیں */
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: url('logo.png') center center no-repeat;
      background-size: 250px 250px;
      opacity: 0.1;  /* لوگو کی ہلکی پن */
      pointer-events: none;
      z-index: -1;
    }
    header {
      background-color: #007BFF;
      color: white;
      padding: 25px;
      text-align: center;
      font-size: 36px;
      font-weight: 700;
      font-family: 'Time New Roman', serif;
      letter-spacing: 1.5px;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
      position: relative;
      z-index: 1;
    }
    .container {
      max-width: 700px;
      margin: 20px auto;
      background-color: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      position: relative;
      z-index: 1;
    }
    h2 {
      text-align: center;
      color: #333;
      background-color: yellow;
      border-color: black;
      border: solid black;
      border-radius: 10px;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    label {
      font-size: 16px;
      font-weight: bold;
    }
    input, select, textarea {
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      background-color: #28a745;
      color: white;
      padding: 12px;
      border: none;
      font-size: 18px;
      border-radius: 6px;
      cursor: pointer;
    }
    button:hover {
      background-color: #218838;
    }
    .success {
      color: green;
      text-align: center;
      margin-top: 10px;
      font-size: 16px;
    }
    @media (max-width: 600px) {
      label, input, button, textarea {
        font-size: 16px;
      }
    }
img{
  translate: 550px 5px;
}

}

  </style>
</head>
<body>

  <header>THE OCEAN OF KNOWLEDGE COACHING ACADEMY</header>
<header>
  <img src="logo.jpeg" alt="Academy Logo" style="height: 150px; display: block; margin: 0px auto 0px;" />
</header>
<marquee>Welcome to the Ocean of Knowledge coaching and Computer Academy Gogdara Swat</marquee>

  <div class="container">
    <h2>Admission Form</h2>
    <form id="admissionForm" onsubmit="submitForm(event)" method="post" name="google-sheet">
      <label>Full Name:</label>
      <input type="text" placeholder="Enter full name" required name="Name">

      <label>Father's Name:</label>
      <input type="text" placeholder="Enter father's name" required name="Father_Name">

      <label>Class:</label>
      <select required name="Class">
  <option value="">Select Class</option>
  <option value="6th">6th</option>
  <option value="7th">7th</option>
  <option value="8th">8th</option>
  <option value="9th">9th</option>
  <option value="10th">10th</option>
</select>

      <label>Date of Birth:</label>
      <input type="date" required name="Date_of_Birth">


      <label>Mobile Number:</label>
      <input type="tel" placeholder="e.g. 03001234567" required name="Contact_No">

      <label>Address:</label>
      <textarea rows="3" placeholder="Enter address" required name="Address"></textarea>

      <button type="submit" value="Submit">Submit Admission</button>
      <div class="success" id="successMessage"></div>
    </form>
  </div>

  <script>
            const scriptURL = 'https://script.google.com/macros/s/AKfycbwqox5izkFoLG_qxEMPxImbGmBakW2BcdC2rBhFigQQtseaIfC2qW36poT5PHIgRuG3/exec'
            const form = document.forms['google-sheet']
          
            form.addEventListener('submit', e => {
              e.preventDefault()
              fetch(scriptURL, { method: 'POST', body: new FormData(form)})
                .then(response => alert("Thanks for Contacting us..! We Will Contact You Soon..."))
                .catch(error => console.error('Error!', error.message))
            })
          </script>

</body>
</html>
