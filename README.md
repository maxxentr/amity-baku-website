# amity-baku-website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amity Baku</title>
    <style>
        /* Основные стили */
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            color: white;
            overflow-x: hidden;
        }

        header {
            position: fixed;
            width: 100%;
            background: rgba(0, 0, 0, 0.9);
            padding: 15px;
            z-index: 1000;
        }

        nav ul {
            list-style: none;
            display: flex;
            padding: 0;
        }

        nav ul li {
            margin-right: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            padding: 10px 15px;
            transition: background 0.3s;
        }

        nav ul li a:hover {
            background: gold;
            border-radius: 5px;
        }

        /* Анимация заднего фона */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(270deg, #ff4e50, #fc913a, #f6e58d, #1dd1a1, #ff6b6b);
            background-size: 400% 400%;
            animation: flow 15s ease infinite;
            z-index: -1;
        }

        @keyframes flow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Главный экран */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .hero h1 {
            font-size: 3em;
            margin-bottom: 20px;
        }

        .cta-button {
            background: gold;
            padding: 15px 30px;
            border: none;
            border-radius: 5px;
            font-size: 1.2em;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .cta-button:hover {
            transform: scale(1.05);
        }

        section {
            padding: 80px 20px;
            background: rgba(0, 0, 0, 0.7);
            margin: 20px;
            border-radius: 15px;
        }

        h2 {
            text-align: center;
            color: gold;
        }

        /* Стили карт услуг */
        .service-card {
            background: #2a2a2a;
            border-radius: 10px;
            padding: 20px;
            margin: 15px;
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-link {
            display: inline-block;
            margin-top: 10px;
            background: gold;
            padding: 10px;
            text-decoration: none;
            color: black;
            border-radius: 5px;
        }

        /* Стили аккордеона */
        .accordion {
            margin-top: 20px;
        }

        .accordion-title {
            background: gold;
            color: black;
            padding: 15px;
            border-radius: 5px;
            cursor: pointer;
            margin-bottom: 10px;
        }

        .accordion-content {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 10px;
            margin-top: 5px;
            border-radius: 5px;
            display: none;
        }

        .info-button {
            background: gold;
            color: black;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .info-button:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body>

<header>
    <nav>
        <ul>
            <li><a href="#about">О нас</a></li>
            <li><a href="#services">Наши Услуги</a></li>
            <li><a href="#commands">Команды</a></li>
            <li><a href="#events">Мероприятия</a></li>
            <li><a href="#important">Важно знать</a></li>
            <li><a href="https://t.me/+yxzf44YeoEgwNzcy" target="_blank">Телеграм чат</a></li>
            <li><a href="https://www.instagram.com/amity.chat?igsh=eGJuNmdpbzFiZDg2" target="_blank">Инстаграм</a></li>
        </ul>
    </nav>
</header>

<!-- Главный экран -->
<div class="hero">
    <h1>Добро пожаловать в Amity Baku</h1>
    <button class="cta-button" onclick="scrollToSection('about')">Узнать больше</button>
</div>

<section id="about">
    <h2>О нас</h2>
    <p>Здесь будет информация о проекте и его миссии.</p>
</section>

<section id="services">
    <h2>Наши Услуги</h2>
    <div class="service-card">
        <h3>Консультации</h3>
        <p>Мы предлагаем индивидуальные консультации для всех участников сообщества.</p>
        <a class="service-link" href="#">Подробнее</a>
    </div>
    <div class="service-card">
        <h3>Мероприятия</h3>
        <p>Организация мероприятий и встреч для укрепления связей в сообществе.</p>
        <a class="service-link" href="#">Подробнее</a>
    </div>
</section>

<section id="commands">
    <h2>Команды</h2>
    <ul>
        <li><b>/start</b> – Начать взаимодействие с ботом.</li>
        <li><b>/help</b> – Получить список доступных команд.</li>
        <li><b>/event</b> – Узнать о предстоящих мероприятиях.</li>
        <li><b>/rules</b> – Показать правила сообщества.</li>
    </ul>
</section>

<section id="events">
    <h2>Мероприятия</h2>
    <p>Узнайте о наших предстоящих мероприятиях и активностях!</p>
</section>

<section id="important">
    <h2>Важно знать</h2>
    <button class="info-button" onclick="toggleUserAgreement()">Пользовательское соглашение</button>
    <button class="info-button">Роли</button>

    <div id="user-agreement-accordion" class="accordion" style="display: none;">
        <div>
            <h3 class="accordion-title" onclick="toggleSection(this)">Соглашение о поведении</h3>
            <div class="accordion-content">
                <p>Текст о допустимом поведении...</p>
            </div>
        </div>
        <div>
            <h3 class="accordion-title" onclick="toggleSection(this)">Соглашение с модерацией</h3>
            <div class="accordion-content">
                <p>Текст о правилах модерации...</p>
            </div>
        </div>
        <div>
            <h3 class="accordion-title" onclick="toggleSection(this)">Соглашение о безопасности</h3>
            <div class="accordion-content">
                <p>Текст о безопасности сообщества...</p>
            </div>
        </div>
    </div>
</section>

<footer>
    <p>&copy; 2024 Amity Baku</p>
</footer>

<script>
    function scrollToSection(sectionId) {
        document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
    }

    function toggleUserAgreement() {
        const accordion = document.getElementById('user-agreement-accordion');
        accordion.style.display = accordion.style.display === 'none' ? 'block' : 'none';
    }

    function toggleSection(element) {
        const content = element.nextElementSibling;
        content.style.display = content.style.display === 'block' ? 'none' : 'block';
    }
</script>

</body>
</html>
