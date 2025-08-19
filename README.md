<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | محمد أحمد</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* الأساسيات */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary-color: #2D5BFF;
            --secondary-color: #FF6B35;
            --dark-color: #1E2A4A;
            --light-color: #F8F9FA;
            --gray-color: #6C757D;
        }
        
        body {
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            display: inline-block;
            margin-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary-color);
            border-radius: 2px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary-color);
            color: white;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* الشريط العلوي */
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 600;
            transition: color 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* قسم Hero */
        .hero {
            padding-top: 150px;
            padding-bottom: 80px;
            background: linear-gradient(135deg, #f5f7ff 0%, #e3e6ff 100%);
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .hero-text {
            flex: 1;
            padding-left: 30px;
        }
        
        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: var(--gray-color);
        }
        
        .hero-image {
            flex: 1;
            text-align: center;
        }
        
        .hero-image img {
            max-width: 100%;
            border-radius: 50%;
            border: 5px solid var(--primary-color);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        /* المهارات */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .skill-card:hover {
            transform: translateY(-10px);
        }
        
        .skill-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .skill-card h3 {
            margin-bottom: 15px;
        }
        
        /* المشاريع */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-img {
            height: 200px;
            background: linear-gradient(45deg, #2D5BFF, #6C8AFF);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            margin-bottom: 10px;
        }
        
        .project-content p {
            color: var(--gray-color);
            margin-bottom: 15px;
        }
        
        /* التواصل */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            margin-left: 15px;
        }
        
        .contact-text h3 {
            margin-bottom: 5px;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* الفوتر */
        footer {
            background: var(--dark-color);
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .social-links a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--primary-color);
            transform: translateY(-5px);
        }
        
        /* responsive */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column-reverse;
                text-align: center;
            }
            
            .hero-text {
                padding-left: 0;
                margin-top: 40px;
            }
            
            .hero-text h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                right: -100%;
                background: white;
                width: 80%;
                height: calc(100vh - 80px);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: all 0.3s ease;
                box-shadow: -5px 0 15px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                right: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .hero-text h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- الشريط العلوي -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">محمد</div>
                <ul class="nav-links">
                    <li><a href="#home">الرئيسية</a></li>
                    <li><a href="#skills">المهارات</a></li>
                    <li><a href="#projects">المشاريع</a></li>
                    <li><a href="#contact">التواصل</a></li>
                </ul>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- قسم Hero -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>مرحبًا، أنا محمد أحمد<br>مطور برمجيات</h1>
                    <p>أنا متخصص في تطوير البرمجيات باستخدام C++ وC# وتطوير الويب. أحب بناء حلول مبتكرة وجميلة.</p>
                    <a href="#contact" class="btn">تواصل معي</a>
                </div>
                <div class="hero-image">
                    <img src="https://via.placeholder.com/400x400" alt="صورة شخصية">
                </div>
            </div>
        </div>
    </section>

    <!-- المهارات -->
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>مهاراتي</h2>
            </div>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-cuttlefish"></i>
                    </div>
                    <h3>لغة C++</h3>
                    <p>خبرة متقدمة في البرمجة بلغة C++ وتطوير أنظمة معقدة.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>لغة C#</h3>
                    <p>تطوير تطبيقات Desktop وتطبيقات الويب باستخدام C# و.NET.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>تطوير الويب</h3>
                    <p>بناء مواقع وتطبيقات ويب تفاعلية باستخدام أحدث التقنيات.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3>تصميم واجهات المستخدم</h3>
                    <p>تصميم واجهات مستخدم جميلة وسهلة الاستخدام باستخدام Figma.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- المشاريع -->
    <section id="projects" style="background: linear-gradient(135deg, #f5f7ff 0%, #e3e6ff 100%);">
        <div class="container">
            <div class="section-title">
                <h2>مشاريعي</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <div class="project-content">
                        <h3>نظام إدارة المهام</h3>
                        <p>تطبيق لسطح المكتب لإدارة المهام باستخدام C# وWPF.</p>
                        <a href="#" class="btn">عرض المشروع</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-content">
                        <h3>متجر إلكتروني</h3>
                        <p>موقع متجر إلكتروني كامل باستخدام ASP.NET Core وReact.</p>
                        <a href="#" class="btn">عرض المشروع</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="project-content">
                        <h3>نظام تحليل البيانات</h3>
                        <p>نظام لتحليل ومعالجة البيانات باستخدام C++ ومكتبات البيانات.</p>
                        <a href="#" class="btn">عرض المشروع</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- التواصل -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>تواصل معي</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>الموقع</h3>
                            <p>الرياض، السعودية</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h3>البريد الإلكتروني</h3>
                            <p>mohamed@example.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h3>الهاتف</h3>
                            <p>+966 123 456 789</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">الاسم</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">البريد الإلكتروني</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">الرسالة</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">إرسال الرسالة</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>© 2023 محمد أحمد. جميع الحقوق محفوظة.</p>
        </div>
    </footer>

    <script>
        // تفعيل القائمة على الجوال
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // إغلاق القائمة عند النقر على رابط
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', function() {
                document.querySelector('.nav-links').classList.remove('active');
            });
        });
        
        // تأثير سلس للتمرير عند النقر على الروابط
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
