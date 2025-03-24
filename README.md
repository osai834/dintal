<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عيادة مطروح للأسنان</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            direction: rtl;
            background-color: #f8f8f8;
        }
        .container {
            width: 50%;
            margin: auto;
            background: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            margin-top: 50px;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>مرحبًا بكم في عيادة مطروح للأسنان</h2>
        <p>الموقع: أمام صيدلية صالح</p>
        <p>📞 رقم الهاتف: <strong>+201203388305</strong></p>

        <h3>احجز موعدك الآن</h3>
        <input type="text" id="name" placeholder="أدخل اسمك" required>
        <textarea id="request" placeholder="أدخل طلبك" rows="4" required></textarea>
        <button onclick="sendToWhatsApp()">إرسال عبر واتساب</button>
    </div>

    <script>
        function sendToWhatsApp() {
            var name = document.getElementById("name").value;
            var request = document.getElementById("request").value;
            var phoneNumber = "+201203388305";

            if (name.trim() === "" || request.trim() === "") {
                alert("يرجى إدخال جميع البيانات قبل الإرسال.");
                return;
            }

            var message = "مرحبا، أنا " + name + " وأرغب في: " + request;
            var whatsappUrl = "https://wa.me/" + phoneNumber + "?text=" + encodeURIComponent(message);

            window.open(whatsappUrl, "_blank");
        }
    </script>

</body>
</html>
