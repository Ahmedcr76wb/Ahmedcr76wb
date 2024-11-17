<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اشترك للوصول إلى الرابط</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }
        .container {
            margin: 100px auto;
            padding: 20px;
            background: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            max-width: 500px;
        }
        .btn {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            margin: 10px;
            display: inline-block;
        }
        .btn:hover {
            background-color: #0056b3;
        }
        .hidden {
            display: none;
        }
    </style>
    <script>
        let subscribed = false;

        function visitChannel() {
            alert("يجب عليك الاشتراك في القناة للوصول إلى الرابط.");
            window.open("https://t.me/pojav_lanunchr", "_blank");
            document.getElementById("verify-btn").classList.remove("hidden");
        }

        function verifySubscription() {
            if (!subscribed) {
                alert("لم يتم التحقق من الاشتراك. يرجى المحاولة مرة أخرى بعد الاشتراك.");
            } else {
                document.getElementById("download-link").classList.remove("hidden");
                document.getElementById("verify-btn").classList.add("hidden");
                alert("تم التحقق من الاشتراك! يمكنك الآن الوصول إلى الرابط.");
            }
        }

        // محاكاة التحقق (للتجربة فقط)
        setTimeout(() => {
            subscribed = true; // يتم تغيير هذا عند الاشتراك الحقيقي.
        }, 5000); // مؤقت 5 ثوانٍ
    </script>
</head>
<body>
    <div class="container">
        <h1>مرحباً بك!</h1>
        <p>للوصول إلى الملف، يجب الاشتراك في قناتنا.</p>
        <a class="btn" onclick="visitChannel()">اشترك الآن</a>
        <a id="verify-btn" class="btn hidden" onclick="verifySubscription()">تحقق من الاشتراك</a>
        <a id="download-link" class="btn hidden" href="https://www.curseforge.com/minecraft/modpacks/dreamcraft-new/files/5042444" target="_blank">الوصول إلى الملف</a>
    </div>
</body>
</html>
