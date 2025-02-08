<!DOCTYPE html>
<html lang="fa" dir="rtl">

<head>
    <meta charset="UTF-8">
    <title>رزومه سمانه سلیمانی</title>

    <!-- فونت فارسی (دلخواه) -->
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;500;700&display=swap" rel="stylesheet">

    <!-- آیکون های Font Awesome (در صورت تمایل) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" integrity="sha512-acNqULYIt2MUpGW1JRcUWw/X2wSn3ZirRgu6wbA4pOT4bLN8xCl9P5k98z5jYqS1S3QeuRMbN7lf2Qy0E8VOow==" crossorigin="anonymous" referrerpolicy="no-referrer"
    />

    <style>
        /* ===== ریست و تنظیمات پایه ===== */
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
            /* پیمایش نرم */
        }
        
        body {
            font-family: 'Vazirmatn', Tahoma, sans-serif;
            background: #fafafa;
            color: #333;
            line-height: 1.6;
            direction: rtl;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        ul {
            list-style: none;
        }
        /* ===== رنگ های اصلی در این طرح ===== */
        
         :root {
            --main-color: #6c63ff;
            /* رنگ اصلی قالب */
            --sec-color: #b45de2;
            /* رنگ ثانویه (صورتی مایل به بنفش) */
            --bg-color: #fafafa;
            --text-color: #333;
            --white: #fff;
        }
        /* ===== هدر (ناوبری) ===== */
        
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: var(--main-color);
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
            z-index: 999;
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            height: 60px;
        }
        
        .nav-logo {
            font-size: 18px;
            font-weight: 700;
            color: var(--white);
        }
        
        .nav-menu {
            display: flex;
            gap: 20px;
        }
        
        .nav-menu a {
            font-size: 14px;
            font-weight: 500;
            color: var(--white);
            transition: color 0.3s;
        }
        
        .nav-menu a:hover {
            color: #ddd;
        }
        /* آیکون همبرگری در موبایل */
        
        .hamburger {
            display: none;
            font-size: 24px;
            color: var(--white);
            cursor: pointer;
        }
        /* ===== ناوبری موبایل ===== */
        
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
                /* مخفی‌سازی منوی دسکتاپ در موبایل */
                flex-direction: column;
                background: var(--main-color);
                position: absolute;
                top: 60px;
                right: 0;
                width: 100%;
                padding: 10px 20px;
            }
            .nav-menu.active {
                display: flex;
                /* وقتی کلاس active بگیرد، نمایش داده می‌شود */
            }
            .hamburger {
                display: block;
                /* همبرگری فقط در موبایل نمایش داده شود */
            }
            .nav-menu a {
                padding: 10px 0;
                border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            }
        }
        /* ===== سکشن هرو (بالای سایت) ===== */
        
        .hero {
            height: 100vh;
            width: 100%;
            background: url('hero-bg.jpg') no-repeat center center/cover;
            /* اگر تصویر hero ندارید، یا گرادیان بگذارید: background: linear-gradient(135deg, #8E2DE2, #4A00E0); */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding-top: 60px;
            /* فضای هدر */
            text-align: center;
            position: relative;
        }
        
        .hero-overlay {
            background: rgba(0, 0, 0, 0.3);
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 0;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            color: #fff;
            padding: 20px;
        }
        
        .profile-img {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            border: 3px solid #fff;
            overflow: hidden;
            margin: 0 auto 20px;
            background: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .hero h1 {
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 10px;
        }
        
        .hero p {
            font-size: 16px;
            font-weight: 300;
        }
        /* ===== بخش عمومی سکشن‌ها ===== */
        
        section {
            max-width: 1000px;
            margin: 60px auto;
            padding: 0 20px;
        }
        
        section h2.section-title {
            font-size: 22px;
            font-weight: 700;
            color: var(--main-color);
            margin-bottom: 20px;
            position: relative;
            text-align: center;
        }
        
        section h2.section-title i {
            margin-left: 5px;
            color: var(--sec-color);
        }
        
        section h2.section-title::after {
            content: "";
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--sec-color);
            margin: 10px auto 0;
        }
        
        .section-box {
            background: var(--white);
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            padding: 30px 25px;
        }
        /* ===== سکشن درباره ===== */
        
        #about p {
            line-height: 1.7;
        }
        /* ===== سکشن مهارت‌ها (استفاده از نوار پیشرفت) ===== */
        
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 10px;
        }
        
        .skill-item {
            flex: 1 1 200px;
            margin-bottom: 15px;
        }
        
        .skill-name {
            font-size: 14px;
            margin-bottom: 5px;
            font-weight: 600;
        }
        
        .skill-bar {
            width: 100%;
            height: 8px;
            background: #eaeaea;
            border-radius: 4px;
            overflow: hidden;
            position: relative;
        }
        
        .skill-bar-fill {
            height: 100%;
            background: var(--main-color);
            width: 50%;
            /* درصد پیشرفت */
        }
        /* ===== سکشن سوابق یا تجربه ===== */
        
        .experience-list ul {
            padding-right: 20px;
        }
        
        .experience-list li {
            margin-bottom: 15px;
            line-height: 1.6;
        }
        
        .experience-list li strong {
            display: inline-block;
            margin-bottom: 3px;
            color: var(--sec-color);
            font-weight: 700;
        }
        /* ===== سکشن تحصیلات ===== */
        
        .education-list ul {
            padding-right: 20px;
        }
        
        .education-list li {
            margin-bottom: 15px;
            line-height: 1.6;
        }
        
        .education-list li strong {
            display: inline-block;
            margin-bottom: 3px;
            color: var(--sec-color);
            font-weight: 700;
        }
        /* ===== سکشن پروژه‌ها ===== */
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .project-card {
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }
        
        .project-card h3 {
            font-size: 16px;
            margin-bottom: 10px;
            color: var(--main-color);
        }
        
        .project-card p {
            flex: 1;
            font-size: 14px;
            margin-bottom: 10px;
            line-height: 1.6;
        }
        
        .project-card a {
            margin-top: auto;
            align-self: flex-start;
            padding: 8px 14px;
            background: var(--main-color);
            color: #fff;
            border-radius: 4px;
            font-size: 13px;
            transition: background 0.3s;
        }
        
        .project-card a:hover {
            background: var(--sec-color);
        }
        /* ===== سکشن تماس ===== */
        
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 15px;
        }
        
        .contact-form input,
        .contact-form textarea {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
            font-size: 14px;
        }
        
        .contact-form button {
            background: var(--main-color);
            color: var(--white);
            border: none;
            padding: 12px 24px;
            border-radius: 4px;
            cursor: pointer;
            transition: background 0.3s;
            font-size: 14px;
            font-weight: 600;
            align-self: flex-start;
        }
        
        .contact-form button:hover {
            background: var(--sec-color);
        }
        /* ===== فوتر ===== */
        
        footer {
            background: var(--main-color);
            color: var(--white);
            text-align: center;
            padding: 20px;
            margin-top: 60px;
        }
        
        footer p {
            font-size: 14px;
            margin-bottom: 5px;
        }
        
        footer .social-links a {
            display: inline-block;
            margin: 0 8px;
            color: var(--white);
            font-size: 18px;
            transition: color 0.3s;
        }
        
        footer .social-links a:hover {
            color: var(--sec-color);
        }
        /* ===== واکنش گرایی ===== */
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 20px;
            }
            .hero p {
                font-size: 14px;
            }
            .profile-img {
                width: 100px;
                height: 100px;
            }
            section {
                margin: 30px auto;
            }
        }
    </style>
</head>

<body>

    <!-- هدر + ناوبری -->
    <header>
        <div class="nav-container">
            <div class="nav-logo">Samaneh Soleimani</div>

            <!-- منوی دسکتاپ / موبایل -->
            <nav>
                <ul class="nav-menu" id="navMenu">
                    <li><a href="#about">درباره</a></li>
                    <li><a href="#skills">مهارت‌ها</a></li>
                    <li><a href="#experience">سوابق</a></li>
                    <li><a href="#education">تحصیلات</a></li>
                    <li><a href="#projects">پروژه‌ها</a></li>
                    <li><a href="#contact">تماس</a></li>
                </ul>
            </nav>

            <!-- آیکون منوی موبایل (همبرگری) -->
            <div class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- سکشن هرو (بالای سایت) -->
    <section class="hero" id="hero">
        <div class="hero-overlay"></div>
        <div class="hero-content">
            <div class="profile-img">
                <!-- عکس پروفایل - در کنار فایل HTML با نام 'profile.jpg' قرار دهید -->
                <img src="profile.jpg" alt="Samaneh Soleimani">
            </div>
            <h1>سمانه سلیمانی</h1>
            <p>دانشجوی ارشد معماری کامپیوتر | کارشناس فناوری اطلاعات</p>
            <p style="margin-top: 10px; font-size: 14px;">
                <strong>تلفن:</strong> ۰۹۱۰۵۸۸۳۰۶۴ <br>
                <strong>ایمیل:</strong>
                <a href="mailto:samanehsoleimani1379@gmail.com" style="color:#fff;text-decoration: underline;">
          samanehsoleimani1379@gmail.com
        </a>
            </p>
        </div>
    </section>

    <!-- سکشن درباره -->
    <section id="about">
        <h2 class="section-title"><i class="fas fa-user"></i> درباره</h2>
        <div class="section-box">
            <p>
                من سمانه سلیمانی هستم، متولد ۱۳۷۹/۰۴/۱۲ و دانشجوی ارشد مجازی مهندسی معماری کامپیوتر در دانشگاه شهید بهشتی. مقطع کارشناسی را در رشته مهندسی کامپیوتر در دانشگاه تهران مرکز به پایان رساندم. در حال حاضر، به‌عنوان کارشناس فناوری اطلاعات در فروشگاه کوتون فعالیت
                داشتم و به یادگیری مباحث دیتابیس و ERP علاقه‌مندم. مشتاق به پیشرفت در حوزه‌های نوین فناوری اطلاعات هستم و از چالش‌های جدید استقبال می‌کنم.
            </p>
        </div>
    </section>

    <!-- سکشن مهارت‌ها -->
    <section id="skills">
        <h2 class="section-title"><i class="fas fa-chart-bar"></i> مهارت‌ها</h2>
        <div class="section-box">
            <div class="skills-list">
                <div class="skill-item">
                    <div class="skill-name">SQL (سطح مقدماتی)</div>
                    <div class="skill-bar">
                        <div class="skill-bar-fill" style="width: 40%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">Microsoft Dynamics AX (پشتیبانی اولیه)</div>
                    <div class="skill-bar">
                        <div class="skill-bar-fill" style="width: 35%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">Microsoft Office</div>
                    <div class="skill-bar">
                        <div class="skill-bar-fill" style="width: 70%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">زبان انگلیسی (متوسط)</div>
                    <div class="skill-bar">
                        <div class="skill-bar-fill" style="width: 50%;"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- سکشن سوابق شغلی -->
    <section id="experience">
        <h2 class="section-title"><i class="fas fa-briefcase"></i> سوابق شغلی</h2>
        <div class="section-box experience-list">
            <ul>
                <li>
                    <strong>کارشناس فناوری اطلاعات در فروشگاه کوتون (۱ سال)</strong>
                    <ul>
                        <li>به‌روزرسانی پایگاه داده‌های داخلی (SQL مقدماتی)</li>
                        <li>پشتیبانی و همکاری در استفاده از Microsoft Dynamics AX</li>
                        <li>گزارش‌دهی و هماهنگی با مدیریت</li>
                    </ul>
                </li>
            </ul>
        </div>
    </section>

    <!-- سکشن تحصیلات -->
    <section id="education">
        <h2 class="section-title"><i class="fas fa-graduation-cap"></i> تحصیلات</h2>
        <div class="section-box education-list">
            <ul>
                <li>
                    <strong>کارشناسی ارشد (مجازی) مهندسی معماری کامپیوتر</strong>
                    <br>دانشگاه شهید بهشتی (در حال تحصیل)
                </li>
                <li>
                    <strong>کارشناسی مهندسی کامپیوتر</strong>
                    <br>دانشگاه تهران مرکز
                </li>
            </ul>
        </div>
    </section>




    <!-- فوتر سایت -->
    <footer>
        <p>&copy; 2025 - طراحی توسط سمانه سلیمانی</p>
        <div class="social-links">
            <!-- مثال: لینکدین یا گیت‌هاب -->
            <a href="#"><i class="fab fa-linkedin-in"></i></a>
            <a href="#"><i class="fab fa-github"></i></a>
            <!-- هر شبکه اجتماعی دیگری که دوست دارید اضافه کنید -->
        </div>
    </footer>

    <!-- اسکریپت برای پیمایش منوی موبایل و ... -->
    <script>
        const hamburger = document.getElementById('hamburger');
        const navMenu = document.getElementById('navMenu');

        hamburger.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });
    </script>
</body>

</html>
