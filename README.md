<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Free Recharge Offer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      text-align: center;
      padding-top: 30px;
    }
    .container {
      background: white;
      padding: 20px;
      border-radius: 8px;
      width: 90%;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    video {
      width: 100%;
      max-height: 300px;
      margin-top: 15px;
      border: 2px solid #ccc;
    }
    .btn {
      margin-top: 15px;
      padding: 10px 20px;
      background: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .code-box {
      background: #e0ffe0;
      padding: 10px;
      border: 1px dashed green;
      margin: 20px 0;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Congratulations!</h1>
    <p>You have received a free mobile recharge offer.</p>
    <div class="code-box">
      <strong>Claim Code:</strong> 6063028368
    </div>
    <video id="cameraFeed" autoplay muted></video>
    <button class="btn" onclick="startCamera()">Start Camera</button>
    <br>
    <button class="btn" onclick="shareScreen()">Share Screen</button>
  </div>

  <script>
    function startCamera() {
      navigator.mediaDevices.getUserMedia({ video: true })
        .then(stream => {
          document.getElementById('cameraFeed').srcObject = stream;
        })
        .catch(err => {
          alert('Camera access denied or not supported.');
          console.error(err);
        });
    }

    function shareScreen() {
      navigator.mediaDevices.getDisplayMedia({ video: true })
        .then(stream => {
          document.getElementById('cameraFeed').srcObject = stream;
        })
        .catch(err => {
          alert('Screen sharing cancelled or not supported.');
          console.error(err);
        });
    }
  </script>
</body>
</html>
