<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#050b18">

<title>Alislamiah 465 | شبكة الإسلامية الرقمية</title>

<meta name="description" content="Alislamiah 465، بوابتك الموحدة لاكتشاف جميع مواقع وتطبيقات وخدمات شبكة الإسلامية الرقمية.">
<meta name="robots" content="index, follow">

<link rel="icon" href="icon.png" type="image/png">

<style>
:root {
    --bg: #050914;
    --panel: #0b1427;
    --panel2: #101d35;
    --blue: #1677ff;
    --cyan: #31d7ff;
    --text: #f4f7ff;
    --muted: #a3b2cc;
    --border: rgba(100,160,255,.17);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    font-family: Arial, Tahoma, sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.9;
    overflow-x: hidden;
}

a {
    color: inherit;
    text-decoration: none;
}

button {
    font: inherit;
}

button:focus-visible,
a:focus-visible {
    outline: 2px solid var(--cyan);
    outline-offset: 4px;
}

/* الخلفية */

body::before {
    content: "";
    position: fixed;
    inset: 0;
    z-index: -1;
    pointer-events: none;
    background:
        radial-gradient(ellipse at 15% 5%,
            rgba(0,100,255,.15), transparent 38%),
        radial-gradient(ellipse at 90% 40%,
            rgba(0,200,255,.07), transparent 35%),
        #050914;
}

/* الشريط العلوي */

header {
    position: sticky;
    top: 0;
    z-index: 100;
    height: 76px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 6%;
    background: rgba(5,9,20,.94);
    border-bottom: 1px solid var(--border);
    backdrop-filter: blur(18px);
}

.brand {
    display: flex;
    align-items: center;
    gap: 12px;
}

.brand img {
    width: 46px;
    height: 46px;
    object-fit: contain;
    border-radius: 13px;
}

.brand-name {
    font-size: 19px;
    font-weight: 900;
    letter-spacing: .3px;
}

.brand-name span {
    color: var(--cyan);
}

.menu-button {
    width: 45px;
    height: 43px;
    border: 1px solid var(--border);
    background: var(--panel);
    color: white;
    border-radius: 12px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
}

.menu-button span {
    width: 21px;
    height: 2px;
    background: var(--cyan);
    border-radius: 5px;
}

/* القائمة الجانبية */

.overlay {
    position: fixed;
    inset: 0;
    z-index: 150;
    background: rgba(0,0,0,.65);
    opacity: 0;
    visibility: hidden;
    transition: .25s;
}

.overlay.active {
    opacity: 1;
    visibility: visible;
}

.sidebar {
    position: fixed;
    z-index: 151;
    top: 0;
    right: 0;
    height: 100%;
    height: 100dvh;
    width: min(310px, 85vw);
    padding: 25px 20px;
    background: #081225;
    border-left: 1px solid var(--border);
    transform: translateX(105%);
    transition: transform .3s ease;
    overflow-y: auto;
}

.sidebar.active {
    transform: translateX(0);
}

.sidebar-head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 25px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 20px;
}

.sidebar-brand {
    display: flex;
    align-items: center;
    gap: 10px;
    font-weight: bold;
}

.sidebar-brand img {
    width: 42px;
    height: 42px;
    object-fit: contain;
    border-radius: 10px;
}

.close-button {
    background: var(--panel2);
    color: white;
    border: 1px solid var(--border);
    border-radius: 10px;
    width: 39px;
    height: 39px;
    font-size: 22px;
    cursor: pointer;
}

.menu-label {
    color: #7187a8;
    font-size: 12px;
    margin: 20px 10px 8px;
}

.sidebar a {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 13px 12px;
    border-radius: 12px;
    margin-bottom: 7px;
    color: #dce8ff;
    transition: background .2s, color .2s;
}

.sidebar a:hover {
    background: #122747;
    color: var(--cyan);
}

.menu-icon {
    width: 35px;
    height: 35px;
    border-radius: 10px;
    background: #102441;
    display: grid;
    place-items: center;
    font-size: 18px;
}

/* القسم الرئيسي */

.hero {
    max-width: 1000px;
    margin: auto;
    padding: 85px 22px 55px;
    text-align: center;
}

.hero-logo {
    width: 104px;
    height: 104px;
    object-fit: contain;
    border-radius: 27px;
    padding: 7px;
    background: rgba(17,34,62,.8);
    border: 1px solid rgba(49,215,255,.28);
    box-shadow: 0 0 38px rgba(22,119,255,.18);
    margin-bottom: 25px;
}

.badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(22,119,255,.10);
    border: 1px solid rgba(49,215,255,.22);
    color: #8bdfff;
    padding: 5px 15px;
    border-radius: 50px;
    font-size: 13px;
    margin-bottom: 18px;
}

.badge-dot {
    width: 7px;
    height: 7px;
    background: var(--cyan);
    border-radius: 50%;
}

.hero h1 {
    font-size: clamp(34px, 7vw, 65px);
    line-height: 1.3;
    font-weight: 900;
    margin-bottom: 15px;
}

.hero h1 span {
    background: linear-gradient(100deg, #3d8bff, #37e2ff);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero-description {
    max-width: 680px;
    margin: auto;
    color: var(--muted);
    font-size: 16px;
}

.hero-buttons {
    margin-top: 30px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 12px;
}

.btn {
    min-height: 48px;
    padding: 11px 22px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 9px;
    border-radius: 12px;
    font-weight: bold;
    font-size: 14px;
    transition: background .2s, border-color .2s;
}

.btn-primary {
    color: white;
    background: linear-gradient(110deg, #1264ee, #168be9);
    border: 1px solid transparent;
}

.btn-primary:hover {
    background: linear-gradient(110deg, #287aff, #20b2ef);
}

.btn-secondary {
    background: #0c1629;
    border: 1px solid var(--border);
    color: #e4edff;
}

.btn-secondary:hover {
    border-color: var(--cyan);
}

/* الفاصل */

.section {
    max-width: 1160px;
    margin: auto;
    padding: 40px 22px 55px;
}

.section-heading {
    text-align: center;
    margin-bottom: 30px;
}

.section-heading .eyebrow {
    color: var(--cyan);
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 1px;
}

.section-heading h2 {
    font-size: clamp(25px, 4vw, 36px);
    margin-top: 5px;
}

.section-heading p {
    color: var(--muted);
    font-size: 14px;
    margin-top: 5px;
}

/* التعريف بالشبكة */

.about-box {
    position: relative;
    overflow: hidden;
    padding: 28px;
    background: linear-gradient(130deg, #0c1930, #091121);
    border: 1px solid var(--border);
    border-radius: 22px;
}

.about-box::before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    width: 4px;
    height: 100%;
    background: linear-gradient(var(--blue), var(--cyan));
}

.about-title {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 13px;
}

.about-title-icon {
    width: 45px;
    height: 45px;
    border-radius: 13px;
    background: rgba(22,119,255,.15);
    display: grid;
    place-items: center;
    font-size: 23px;
}

.about-title h3 {
    font-size: 21px;
}

.about-box p {
    color: #b4c3db;
    font-size: 15px;
    line-height: 2.1;
}

/* بطاقات الخدمات */

.services-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 18px;
}

.service-card {
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    min-width: 0;
    padding: 25px;
    background: linear-gradient(145deg, #0d192d, #09111f);
    border: 1px solid var(--border);
    border-radius: 20px;
    transition: border-color .2s, background .2s;
}

.service-card:hover {
    border-color: rgba(49,215,255,.5);
    background: linear-gradient(145deg, #10213d, #0a1426);
}

.card-top {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 12px;
    margin-bottom: 17px;
}

.service-icon {
    width: 58px;
    height: 58px;
    flex-shrink: 0;
    display: grid;
    place-items: center;
    border-radius: 16px;
    font-size: 29px;
    background: linear-gradient(145deg, #112e54, #0b1a31);
    border: 1px solid rgba(70,150,255,.2);
}

.card-number {
    color: #7188a9;
    font-size: 12px;
    background: rgba(255,255,255,.035);
    border: 1px solid var(--border);
    padding: 3px 10px;
    border-radius: 50px;
}

.service-card h3 {
    font-size: 20px;
    margin-bottom: 8px;
}

.service-card p {
    color: var(--muted);
    font-size: 14px;
    line-height: 2;
    margin-bottom: 22px;
    flex-grow: 1;
}

.service-link {
    width: 100%;
    min-height: 46px;
    padding: 10px 14px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 8px;
    border-radius: 11px;
    background: #102442;
    border: 1px solid rgba(65,142,255,.2);
    color: #bfeeff;
    font-size: 13px;
    font-weight: bold;
    transition: background .2s;
}

.service-link:hover {
    background: #153963;
}

.service-link .arrow {
    font-size: 19px;
}

/* شريط ختامي */

.closing {
    max-width: 1116px;
    margin: 5px auto 55px;
    padding: 30px 22px;
    width: calc(100% - 44px);
    text-align: center;
    border: 1px solid var(--border);
    border-radius: 20px;
    background: linear-gradient(110deg, #0b1930, #0c1224);
}

.closing h2 {
    font-size: 24px;
    margin-bottom: 7px;
}

.closing p {
    color: var(--muted);
    font-size: 14px;
    margin-bottom: 18px;
}

/* التذييل */

footer {
    padding: 28px 20px;
    text-align: center;
    border-top: 1px solid var(--border);
    background: rgba(4,8,17,.8);
}

.footer-brand {
    font-size: 18px;
    font-weight: 900;
    margin-bottom: 7px;
}

.footer-brand span {
    color: var(--cyan);
}

footer p {
    color: #8292ac;
    font-size: 12px;
}

.footer-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin: 14px 0;
    font-size: 13px;
    color: #bdcbe0;
}

.footer-links a:hover {
    color: var(--cyan);
}

/* الهاتف */

@media (max-width: 650px) {
    header {
        height: 68px;
        padding: 0 17px;
    }

    .brand img {
        width: 40px;
        height: 40px;
    }

    .brand-name {
        font-size: 17px;
    }

    .hero {
        padding: 58px 20px 35px;
    }

    .hero-logo {
        width: 88px;
        height: 88px;
    }

    .hero-description {
        font-size: 14px;
    }

    .section {
        padding: 30px 15px 40px;
    }

    .services-grid {
        grid-template-columns: 1fr;
        gap: 14px;
    }

    .service-card {
        padding: 21px;
    }

    .about-box {
        padding: 23px 19px;
    }

    .closing {
        margin-bottom: 35px;
    }
}

@media (prefers-reduced-motion: reduce) {
    html {
        scroll-behavior: auto;
    }

    *, *::before, *::after {
        transition-duration: .01ms !important;
    }
}
</style>
</head>

<body>

<!-- الشريط العلوي -->
<header>
    <a href="#home" class="brand" aria-label="Alislamiah 465 - الصفحة الرئيسية">
        <img src="icon.png" alt="شعار الإسلامية">
        <div class="brand-name">Alislamiah <span>465</span></div>
    </a>

    <button class="menu-button" id="menuButton"
            aria-label="فتح القائمة"
            aria-expanded="false"
            aria-controls="sidebar">
        <span></span>
        <span></span>
        <span></span>
    </button>
</header>

<!-- خلفية القائمة -->
<div class="overlay" id="overlay"></div>

<!-- القائمة الجانبية -->
<aside class="sidebar" id="sidebar"
       aria-label="القائمة الرئيسية"
       aria-hidden="true">

    <div class="sidebar-head">
        <div class="sidebar-brand">
            <img src="icon.png" alt="">
            <span>Alislamiah 465</span>
        </div>

        <button class="close-button" id="closeButton"
                aria-label="إغلاق القائمة">×</button>
    </div>

    <div class="menu-label">القائمة الرئيسية</div>

    <a href="#home" class="menu-link">
        <span class="menu-icon">⌂</span>
        <span>الرئيسية</span>
    </a>

    <a href="#about" class="menu-link">
        <span class="menu-icon">◈</span>
        <span>عن الإسلامية</span>
    </a>

    <a href="#services" class="menu-link">
        <span class="menu-icon">▦</span>
        <span>خدمات الإسلامية</span>
    </a>

    <div class="menu-label">روابط شبكة الإسلامية</div>

    <a href="https://mohamedmadoui5195.github.io/Alislamiah-services/">
        <span class="menu-icon">🌐</span>
        <span>خدمات الإسلامية</span>
    </a>

    <a href="https://mohamedmadoui5195.github.io/Alislamiah-_net/">
        <span class="menu-icon">ℹ️</span>
        <span>عن Alislamiah</span>
    </a>
</aside>

<!-- الواجهة الرئيسية -->
<main>

<section class="hero" id="home">

    <img class="hero-logo" src="icon.png" alt="أيقونة شبكة الإسلامية">

    <div>
        <span class="badge">
            <span class="badge-dot"></span>
            بوابتك إلى العالم الرقمي
        </span>
    </div>

    <h1>
        عالمك الرقمي<br>
        <span>مع Alislamiah 465</span>
    </h1>

    <p class="hero-description">
        اكتشف جميع مواقع وتطبيقات وخدمات شبكة الإسلامية من مكان واحد.
        بوابة موحدة تجمع التعليم والبحث والتصفح والفيديوهات والخرائط
        والذكاء الاصطناعي والبريد الإلكتروني والتخزين السحابي.
    </p>

    <div class="hero-buttons">
        <a href="#services" class="btn btn-primary">
            اكتشف خدماتنا <span>←</span>
        </a>

        <a href="#about" class="btn btn-secondary">
            تعرّف على الشبكة
        </a>
    </div>

</section>

<!-- عن الإسلامية -->
<section class="section" id="about">

    <div class="section-heading">
        <div class="eyebrow">ABOUT ALISLAMIAH</div>
        <h2>عن Alislamiah</h2>
        <p>تعرّف على رؤيتنا ومجال خدماتنا الرقمية</p>
    </div>

    <div class="about-box">

        <div class="about-title">
            <div class="about-title-icon">🌐</div>
            <h3>شبكة الإسلامية الرقمية</h3>
        </div>

        <p>
            الإسلامية هي شبكة رقمية توفر خدمات متعددة، منها منصة تعليمية
            متكاملة ومتصفح آمن خالٍ من الإباحيات، بالإضافة إلى مجموعة من
            المنصات والخدمات الرقمية التي تهدف إلى توفير تجربة تقنية آمنة
            ومفيدة للمستخدمين.
        </p>

    </div>
</section>

<!-- المواقع والتطبيقات -->
<section class="section" id="services">

    <div class="section-heading">
        <div class="eyebrow">OUR DIGITAL ECOSYSTEM</div>
        <h2>مواقعنا وخدماتنا وتطبيقاتنا</h2>
        <p>ثماني خدمات رقمية في بوابة واحدة</p>
    </div>

    <div class="services-grid">

        <!-- 1: المنصة التعليمية -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">📚</div>
                <span class="card-number">01 / 08</span>
            </div>

            <h3>منصة تعليمية</h3>

            <p>
                تقدم لكم الإسلامية منصة تعليمية مجانية،
                تهدف إلى تسهيل الوصول إلى المحتوى التعليمي
                والخدمات المعرفية.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Alislamiah-_net/">
                <span>الانتقال إلى Alislamiah-_net</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 2: محرك البحث -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">🔎</div>
                <span class="card-number">02 / 08</span>
            </div>

            <h3>محرك بحث</h3>

            <p>
                توفر الإسلامية محرك بحث يهدف إلى توفير
                تجربة بحث آمنة وموثوقة، مع التركيز على
                الوصول إلى محتوى مناسب للمستخدمين.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Alislamiah-AI/">
                <span>الانتقال إلى Alislamiah AI</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 3: المتصفح -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">🌐</div>
                <span class="card-number">03 / 08</span>
            </div>

            <h3>متصفح Alislamiah Bing</h3>

            <p>
                توفر الإسلامية تجربة رقمية أخرى تناسب
                محبي الحداثة والتطور التكنولوجي،
                من خلال واجهة مخصصة للبحث والتصفح.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Alislamiah/">
                <span>الانتقال إلى Alislamiah Bing</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 4: منصة الفيديوهات -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">▶️</div>
                <span class="card-number">04 / 08</span>
            </div>

            <h3>منصة فيديوهات</h3>

            <p>
                ولم تكتفِ الإسلامية بمحركات البحث فقط،
                بل توفر أيضًا Alislamiah Tube، منصة
                لمشاهدة الفيديوهات مع التركيز على
                المحتوى المفيد والملائم.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Alislamiah-Tube/">
                <span>الانتقال إلى Alislamiah Tube</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 5: الخرائط -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">🗺️</div>
                <span class="card-number">05 / 08</span>
            </div>

            <h3>تطبيق الخرائط</h3>

            <p>
                طورت شبكة Alislamiah أيضًا تطبيق
                Alislamiah Maps لاستكشاف الأماكن
                والمواقع والاستفادة من خدمات الخرائط.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Alislamiah-Maps/">
                <span>الانتقال إلى Alislamiah Maps</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 6: المساعد الرقمي -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">✦</div>
                <span class="card-number">06 / 10</span>
            </div>

            <h3>المساعد الرقمي Gemalot</h3>

            <p>
                توفر شبكة الإسلامية مساعدًا رقميًا
                يرافقك ويساندك في مهامك، ضمن تجربة
                تقنية مخصصة للمساعدة والإنتاجية.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Gemalot/">
                <span>الانتقال إلى Gemalot</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 7: البريد الإلكتروني -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">✉️</div>
                <span class="card-number">07 / 10</span>
            </div>

            <h3>البريد الإلكتروني Eisen Mail</h3>

            <p>
                إلى جانب ذلك، تشمل تطبيقات الإسلامية
                خدمة Eisen Mail للبريد الإلكتروني،
                للتواصل وإدارة الرسائل عبر الإنترنت.
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Eisen-mail/">
                <span>الانتقال إلى Eisen Mail</span>
                <span class="arrow">←</span>
            </a>

        </article>

        <!-- 8: التخزين السحابي -->
        <article class="service-card">

    <div class="card-top">
        <div class="service-icon">☁️</div>
        <span class="card-number">08 / 10</span>
    </div>

    <h3>التخزين السحابي Bingot</h3>

    <p>
        وختمت الإسلامية مشاريعها بتطبيق Bingot للتخزين السحابي،
        الذي يوفر مساحة لحفظ الملفات والصور والفيديوهات
        والوصول إليها عبر الإنترنت.
    </p>

    <a class="service-link"
       href="https://mohamedmadoui5195.github.io/Bingot/">
        <span>الانتقال إلى Bingot</span>
        <span class="arrow">←</span>
    </a>

</article>

 <!-- 9: التقويم -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">🔎</div>
                <span class="card-number">09 / 09</span>
            </div>

            <h3>التقويم </h3>

            <p>
                توفر الإسلامية  تطبيق تقويم أيضا 
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Eisen.Calendar/">
                <span>الانتقال إلى  Eisen Calandar</span>
                <span class="arrow">←</span>
            </a>

        </article>

<!-- 9: التقويم -->
        <article class="service-card">

            <div class="card-top">
                <div class="service-icon">🔎</div>
                <span class="card-number">10 / 10</span>
            </div>

            <h3>التقويم </h3>

            <p>
                توفر الإسلامية تطبيق ميت وإجتماعات
            </p>

            <a class="service-link"
               href="https://mohamedmadoui5195.github.io/Eisen.metting/">
                <span>الانتقال إلى  Eisen Meeting</span>
                <span class="arrow">←</span>
            </a>

        </article>



</div>
</section>

<!-- الوصول إلى بقية خدمات الشبكة -->
<section class="closing">

    <h2>الإسلامية، عالم رقمي متكامل</h2>

    <p>
        اكتشف المزيد من الخدمات والمنصات التي تقدمها شبكة الإسلامية.
    </p>

    <a class="btn btn-primary"
       href="https://mohamedmadoui5195.github.io/Alislamiah-services/">
        استكشف خدمات الإسلامية <span>←</span>
    </a>

</section>

</main>

<!-- التذييل -->
<footer>

    <div class="footer-brand">
        Alislamiah <span>465</span>
    </div>

    <div class="footer-links">

        <a href="#home">الرئيسية</a>

        <a href="#about">عن الإسلامية</a>

        <a href="https://mohamedmadoui5195.github.io/Alislamiah-services/">
            خدمات الإسلامية
        </a>

        <a href="#services">جميع التطبيقات</a>

    </div>

    <p>
        جميع الحقوق محفوظة لشبكة الإسلامية ©
        <span id="year"></span>
    </p>

</footer>

<script>
(function () {
    "use strict";

    const menuButton = document.getElementById("menuButton");
    const closeButton = document.getElementById("closeButton");
    const sidebar = document.getElementById("sidebar");
    const overlay = document.getElementById("overlay");

    function openMenu() {
        sidebar.classList.add("active");
        overlay.classList.add("active");

        sidebar.setAttribute("aria-hidden", "false");
        menuButton.setAttribute("aria-expanded", "true");

        document.body.style.overflow = "hidden";
        closeButton.focus();
    }

    function closeMenu() {
        sidebar.classList.remove("active");
        overlay.classList.remove("active");

        sidebar.setAttribute("aria-hidden", "true");
        menuButton.setAttribute("aria-expanded", "false");

        document.body.style.overflow = "";
    }

    menuButton.addEventListener("click", function () {
        if (sidebar.classList.contains("active")) {
            closeMenu();
        } else {
            openMenu();
        }
    });

    closeButton.addEventListener("click", closeMenu);
    overlay.addEventListener("click", closeMenu);

    document.querySelectorAll(".sidebar a").forEach(function (link) {
        link.addEventListener("click", closeMenu);
    });

    document.addEventListener("keydown", function (event) {
        if (event.key === "Escape") {
            closeMenu();
        }
    });

    document.getElementById("year").textContent =
        new Date().getFullYear();

})();
</script>

</body>
</html>