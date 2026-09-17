<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الكابسولة الزمنية - اليوم الوطني 96</title>
    <!-- استيراد خط عربي أنيق -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0b3d2c 0%, #134e38 50%, #06261b 100%);
            color: #ffffff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 20px;
            padding: 40px;
            max-width: 600px;
            width: 100%;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        /* شريط زينة وطني علوي */
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 6px;
            background: linear-gradient(90deg, #16a34a, #ffffff, #16a34a);
        }

        .badge-96 {
            display: inline-block;
            background: rgba(22, 163, 74, 0.2);
            border: 1px solid #4ade80;
            color: #4ade80;
            padding: 5px 15px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }

        h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            color: #ffffff;
            font-weight: 900;
        }

        h1 span {
            color: #4ade80;
        }

        p.subtitle {
            font-size: 1rem;
            color: #cbd5e1;
            margin-bottom: 30px;
            line-height: 1.6;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: right;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #e2e8f0;
        }

        input[type="text"],
        input[type="email"],
        textarea {
            width: 100%;
            padding: 14px;
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            background: rgba(0, 0, 0, 0.3);
            color: #fff;
            font-size: 1rem;
            outline: none;
            transition: all 0.3s ease;
        }

        input:focus, textarea:focus {
            border-color: #4ade80;
            box-shadow: 0 0 10px rgba(74, 222, 128, 0.3);
        }

        textarea {
            resize: vertical;
            height: 120px;
        }

        .btn {
            background: linear-gradient(135deg, #16a34a, #15803d);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.1rem;
            font-weight: 700;
            border-radius: 10px;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(22, 163, 74, 0.4);
        }

        .btn:hover {
            background: linear-gradient(135deg, #15803d, #166534);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(22, 163, 74, 0.6);
        }

        /* رسالة النجاح */
        .success-message {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }

        .success-message h2 {
            color: #4ade80;
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .success-message p {
            color: #e2e8f0;
            line-height: 1.8;
            margin-bottom: 25px;
        }

        .capsule-icon {
            font-size: 3.5rem;
            margin-bottom: 10px;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- نموذج الإدخال -->
        <div id="capsuleFormContainer">
            <div class="capsule-icon">🇸🇦</div>
            <div class="badge-96">اليوم الوطني السعودي 96</div>
            <h1>الكابسولة الزمنية <span>للوطن</span></h1>
            <p class="subtitle">دوّن رسالتك، طموحك، أو وعدك للعام القادم.. وسنقوم بإقفالها وحفظها لتسترجعها بكل فخر!</p>
            
            <form id="timeCapsuleForm">
                <div class="form-group">
                    <label for="userName">الاسم أو اللقب:</label>
                    <input type="text" id="userName" required placeholder="مثال: فخر السعودية">
                </div>

                <div class="form-group">
                    <label for="userEmail">البريد الإلكتروني (لاستلام الرسالة لاحقاً):</label>
                    <input type="email" id="userEmail" required placeholder="name@example.com">
                </div>

                <div class="form-group">
                    <label for="userMessage">رسالتك أو طموحك للعام القادم:</label>
                    <textarea id="userMessage" required placeholder="اكتب طموحاتك أو رسالتك المعبرة هنا..."></textarea>
                </div>

                <button type="submit" class="btn">إغلاق الكابسولة الوطنية 🔒</button>
            </form>
        </div>

        <!-- شاشة النجاح بعد الإرسال -->
        <div id="successContainer" class="success-message">
            <div class="capsule-icon">💚</div>
            <h2>تم إغلاق الكابسولة بنجاح!</h2>
            <p>حُفظت رسالتك بأمان تحت راية الوطن. سنعيد فتحها وإرسالها إلى بريدك الإلكتروني في الموعد المحدّد لتسترجع هذه اللحظات الوطنية الخالدة.</p>
            <button onclick="resetForm()" class="btn" style="background: rgba(255,255,255,0.1); border: 1px solid rgba(255,255,255,0.2);">إرسال رسالة أخرى</button>
        </div>
    </div>

    <script>
        const form = document.getElementById('timeCapsuleForm');
        const formContainer = document.getElementById('capsuleFormContainer');
        const successContainer = document.getElementById('successContainer');

        form.addEventListener('submit', function(e) {
            e.preventDefault(); 

            const name = document.getElementById('userName').value;
            const email = document.getElementById('userEmail').value;
            const message = document.getElementById('userMessage').value;

            console.log("تم حفظ بيانات الكابسولة الوطنية:", { name, email, message });

            formContainer.style.display = 'none';
            successContainer.style.display = 'block';
        });

        function resetForm() {
            form.reset();
            successContainer.style.display = 'none';
            formContainer.style.display = 'block';
        }
    </script>

</body>
</html>
