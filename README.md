<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nhập Họ Tên</title>
    <style>
        body {
            font-family: Arial;, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            text-align: center;
            padding: 20px;
        }
        #image {
            display: none;
            margin-top: 20px;
            position: relative;
        }
        #name {
            position: absolute; top: 280px; left: 50px;
            bottom: 10px;
            left: 70%;
            transform: translateX(-50%);
            font-size: 30px;
            color: black; /* Màu chữ */
            background-color: rgba(0, 0, 0, 0); /* Nền trong suốt cho chữ */
            padding: 5px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>Nhập Họ Tên Của Bạn</h1>
    <input type="text" id="nameInput" placeholder="Họ tên của bạn" required>
    <button onclick="displayImage()">Xem Ảnh</button>

    <div id="image">
        <img id="backgroundImage" src="17.png" alt="Ảnh" style="width: 1000px;">
        <div id="name"></div>
    </div>

    <script>
        function displayImage() {
            const nameInput = document.getElementById('nameInput').value;
            const nameDisplay = document.getElementById('name');
            const imageDiv = document.getElementById('image');

            if (nameInput) {
                nameDisplay.textContent = nameInput;
                imageDiv.style.display = 'block';
            } else {
                alert("Vui lòng nhập họ tên!");
            }
        }
    </script>
</body>
</html>
