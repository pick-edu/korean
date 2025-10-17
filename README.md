<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PICK: Грант в Корею. Программа подготовки к поступлению</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap" rel="stylesheet">
    <style>
        /* Custom CSS to match the deep black/blue block style from the PDF */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #101010; /* Very deep dark background, nearly black */
            color: #ffffff; /* Bright white text for maximum contrast */
        }
        .hero-bg {
            background-color: #1e293b; /* Dark Slate/Navy for the Hero area */
            border-bottom: 4px solid #3b82f6; /* Blue dividing line */
        }
        .cta-button {
            transition: background-color 0.2s, box-shadow 0.2s;
            background-color: #3b82f6; /* Vibrant Blue accent */
            color: #ffffff;
            font-weight: 700;
            border: 2px solid #3b82f6;
        }
        .cta-button:hover {
            background-color: #2563eb;
            box-shadow: 0 4px 15px rgba(59, 130, 246, 0.5); 
        }
        .secondary-cta {
             background-color: #ffffff;
             color: #101010;
        }
        .secondary-cta:hover {
             background-color: #e2e8f0;
        }
        .section-heading {
            border-bottom: 4px solid #3b82f6; /* Blue underline */
            padding-bottom: 8px;
            display: inline-block;
            color: #ffffff;
        }
        .process-card {
            background-color: #1f2937; /* Darker card background (Slate-800) */
            border-radius: 8px; /* Slightly less rounded corners for block style */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
            transition: border 0.3s;
            border-left: 4px solid transparent;
        }
        .process-card:hover {
            border-left: 4px solid #3b82f6; /* Blue border hover effect */
        }
        .step-number {
            color: #3b82f6; /* Vibrant Blue number */
        }
        .input-style {
            background-color: #1f2937;
            color: #ffffff;
            border: 1px solid #374151;
            padding: 1rem;
            border-radius: 0.5rem;
            width: 100%;
        }
        .result-card {
            background-color: #101010;
            border: 1px solid #374151;
            padding: 1.5rem;
            border-radius: 0.75rem;
            text-align: left; /* Ensure text alignment is left for the response */
        }
        .modal-input-style {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 1px solid #d1d5db;
            border-radius: 0.5rem;
            color: #1f2937;
            background-color: #ffffff;
            transition: border-color 0.15s, box-shadow 0.15s;
        }
        .modal-input-style:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.5);
        }

        /* Spinner for loading state */
        .spinner {
            border: 4px solid rgba(255, 255, 255, 0.3);
            border-top: 4px solid #ffffff;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        /* Style for Markdown Headings and lists in the output */
        #resultOutput h2 {
            font-size: 1.5rem; /* Equivalent to text-2xl */
            font-weight: 700; /* Equivalent to font-bold */
            margin-top: 1.5rem;
            margin-bottom: 0.5rem;
            color: #3b82f6; /* Blue heading for structure */
        }
        #resultOutput ul {
            list-style-type: disc;
            margin-left: 1.5rem;
            padding-left: 0;
            margin-bottom: 1rem;
        }
        #resultOutput p {
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        /* Mobile adjustment */
        @media (max-width: 640px) {
            .hero-text-container {
                padding-top: 4rem;
                padding-bottom: 6rem;
            }
        }
    </style>
</head>
<body>

    <header class="p-4 bg-gray-900 shadow-xl sticky top-0 z-20">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <a href="#">
                <img src="6.png" alt="PICK EdTech Logo" class="h-8 md:h-10" onerror="this.onerror=null;this.src='https://placehold.co/100x40/101010/ffffff?text=PICK+LOGO';">
            </a>
            
            <nav class="space-x-6 hidden sm:block font-medium">
                <a href="#process" class="text-white hover:text-blue-400 transition">Процесс</a>
                <a href="#ai-coordinator" class="text-white hover:text-blue-400 transition">AI-Координатор 🎯</a>
                <a href="#prize" class="text-white hover:text-blue-400 transition">Бесплатные Авиабилеты ✈️</a>
                <a href="#contacts" class="text-white hover:text-blue-400 transition">Контакты</a>
            </nav>
            <button id="navOpenModalBtn" class="px-5 py-2 cta-button text-sm rounded-lg shadow-md hidden sm:block">
                Записаться
            </button>
            <button class="sm:hidden text-2xl text-white">☰</button>
        </div>
    </header>

    <section class="hero-bg text-white pb-16 md:pb-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center pt-24 md:pt-32 hero-text-container">
            <p class="text-lg font-light mb-2 text-blue-400 uppercase tracking-widest">PICK EDUCATION</p>
            <h1 class="text-4xl sm:text-6xl font-extrabold mb-6 tracking-tight">
                <strong>Стипендия</strong> в Корею: Легче, чем кажется.
            </h1>
            <p class="text-xl sm:text-2xl font-light mb-10 max-w-4xl mx-auto opacity-90">
                Твой путь к <strong>100% гранту</strong>. Не просто консультации, а полноценная 2-х годовая программа с индивидуальным подходом.
            </p>
            <div class="space-y-4 sm:space-y-0 sm:space-x-6">
                <button id="heroOpenModalBtn" class="cta-button inline-block px-10 py-3 text-lg font-bold rounded-lg shadow-lg uppercase tracking-wider">
                    Сделать первый шаг
                </button>
                <a href="#process" class="secondary-cta inline-block px-10 py-3 text-lg font-bold rounded-lg shadow-lg uppercase tracking-wider text-black">
                    Узнать подробнее
                </a>
            </div>
            <div class="mt-8 text-sm font-medium opacity-80">
                Уже <strong>50+ студентов</strong> достигли своих целей вместе с PICK.
            </div>
        </div>
    </section>

    <section id="process" class="py-16 md:py-24 bg-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 section-heading mx-auto">
                Процесс работы с PICK
            </h2>
            <p class="mb-12 max-w-3xl mx-auto text-gray-400">
                PICK — это не просто консультации, это тщательно разработанная 2-х годовая программа с индивидуальным подходом для обеспечения <strong>качественного результата</strong>.
            </p>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                
                <div class="process-card p-6 text-left">
                    <div class="step-number text-5xl font-extrabold mb-3">1</div>
                    <h3 class="text-xl font-bold mb-3 text-white">TOPIK: Корейский Язык</h3>
                    <p class="text-gray-400 text-sm">
                        Гарантия гранта основана на знании корейского языка. <strong>Первый шаг</strong> — изучение языка и подготовка к экзамену TOPIK (уровень 3-4).
                    </p>
                </div>

                <div class="process-card p-6 text-left">
                    <div class="step-number text-5xl font-extrabold mb-3">2</div>
                    <h3 class="text-xl font-bold mb-3 text-white">Работа над Профайлом</h3>
                    <p class="text-gray-400 text-sm">
                        Университеты выбирают тех, кто активен. <strong>Второй шаг</strong>: внешкольная работа над профайлом для обеспечения наилучшего результата.
                    </p>
                </div>

                <div class="process-card p-6 text-left">
                    <div class="step-number text-5xl font-extrabold mb-3">3</div>
                    <h3 class="text-xl font-bold mb-3 text-white">Мотивационное Письмо &amp; Интервью</h3>
                    <p class="text-gray-400 text-sm">
                        Университет встречает студентов по письму. <strong>Третий шаг</strong>: написание мотивационного письма, стади плана и последующая подготовка к интервью.
                    </p>
                </div>

                <div class="process-card p-6 text-left">
                    <div class="step-number text-5xl font-extrabold mb-3">4</div>
                    <h3 class="text-xl font-bold mb-3 text-white">Подача в Университеты</h3>
                    <p class="text-gray-400 text-sm">
                        Чем больше вузов, тем выше шансы. <strong>Четвертый шаг</strong>: обучение всему процессу подачи через специальные сайты и выбор самого выгодного гранта.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="ai-coordinator" class="py-16 md:py-24 bg-[#1f2937]">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center section-heading mx-auto">
                AI-Координатор: Оценка Шансов на Грант 🎯
            </h2>
            <div class="bg-black p-8 rounded-xl shadow-2xl border-2 border-blue-600 space-y-6">
                <p class="text-gray-300 text-center">
                    Введите ваши текущие данные, чтобы получить **реалистичную оценку** шансов на грант и индивидуальный план повышения результата с программой PICK.
                </p>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <input type="text" id="targetMajor" placeholder="Желаемая Специальность (напр., Computer Science)" class="input-style" required>
                    <input type="text" id="currentTOPIK" placeholder="Текущий уровень TOPIK (напр., 3 или 0)" class="input-style" required>
                </div>
                <textarea id="currentGPA" placeholder="Средний балл (GPA) из аттестата/транскрипта (напр., 4.7/5.0)" rows="1" class="input-style resize-none" required></textarea>
                <textarea id="currentAchievements" placeholder="Ключевые достижения (напр., призер олимпиады, волонтерство, спорт, опыт работы)" rows="3" class="input-style resize-none" required></textarea>

                <button id="evaluateButton" class="cta-button w-full px-8 py-3 rounded-lg uppercase tracking-wider disabled:opacity-50 flex items-center justify-center">
                    <span id="buttonText">Оценить шансы и получить план</span>
                    <div id="loader" class="hidden ml-3 spinner"></div>
                </button>
                
                <div id="resultOutputContainer" class="mt-6 p-6 result-card hidden border-blue-400">
                    <h4 class="text-2xl font-bold text-blue-400 mb-4">Результаты Оценки:</h4>
                    <div id="resultOutput" class="text-gray-200 whitespace-pre-wrap leading-relaxed"></div>
                    <p class="mt-6 text-sm italic text-gray-500">
                        *Для получения полного индивидуального плана и гарантированного сопровождения запишитесь на **бесплатную консультацию** ниже.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="prize" class="py-16 md:py-24 bg-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center section-heading mx-auto">
                Бесплатные Авиабилеты: Шанс для Топ-Студентов ✈️
            </h2>
            
            <div class="flex flex-col md:flex-row items-stretch bg-[#1f2937] p-6 md:p-10 rounded-lg shadow-2xl border-2 border-blue-500">
                
                <div class="md:w-1/2 md:pr-10 mb-6 md:mb-0">
                    <h3 class="text-3xl font-extrabold text-blue-400 mb-4 flex items-center">
                        <svg class="w-8 h-8 mr-3" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2C6.477 2 2 6.477 2 12s4.477 10 10 10 10-4.477 10-10S17.523 2 12 2zm-1 15.938v-3.876h2v3.876H11zm0-4.876V6.062h2v7.001H11z"/></svg>
                        100% Оплата Авиабилетов для Топ-3
                    </h3>
                    <p class="text-lg text-gray-300 mb-6">
                        Мы поощряем выдающиеся успехи. **PICK спонсирует авиабилеты** для **трех лучших студентов** каждого семестра, которые добились 100% гранта в топовых университетах.
                    </p>
                    <ul class="space-y-3 text-gray-300">
                        <li class="flex items-center">
                            <span class="text-blue-400 text-2xl mr-3 flex-shrink-0">✈️</span>
                            <span class="font-medium"><strong>Топ-3 студента</strong>, успешно поступивших с 100% грантом.</span>
                        </li>
                        <li class="flex items-center">
                            <span class="text-blue-400 text-2xl mr-3 flex-shrink-0">🚀</span>
                            <span class="font-medium">Билеты на перелет в Корею **БЕСПЛАТНО** за счет PICK.</span>
                        </li>
                    </ul>
                </div>
                
                <div class="md:w-1/2 bg-[#101010] p-6 rounded-lg border border-gray-700 shadow-inner">
                    <h4 class="text-xl font-bold text-white mb-4">Детали Гранта Университета:</h4>
                    <p class="text-gray-400 mb-4">
                        Наша программа направлена на получение <strong>полного гранта</strong> от самого университета, который включает:
                    </p>
                    <ul class="space-y-3 text-gray-400">
                        <li class="flex items-start">
                            <span class="text-blue-500 font-bold text-lg mr-2 flex-shrink-0">✅</span>
                            <span>Покрытие <strong>100% стоимости обучения</strong> (4 года).</span>
                        </li>
                        <li class="flex items-start">
                            <span class="text-blue-500 font-bold text-lg mr-2 flex-shrink-0">✅</span>
                            <span>Ежемесячная **стипендия** на проживание и питание (зависит от вуза).</span>
                        </li>
                        <li class="flex items-start">
                            <span class="text-blue-500 font-bold text-lg mr-2 flex-shrink-0">✅</span>
                            <span>Полное сопровождение в оформлении визы D-4 / D-2.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section class="py-16 md:py-24 bg-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 section-heading mx-auto">
                Истории Успеха
            </h2>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="process-card p-6 border-t-4 border-blue-500">
                    <p class="italic text-gray-300 mb-4">"Благодаря PICK я поступила в университет <strong>Yonsei</strong>! Четкий план по TOPIK и профайлу был решающим. Это лучшая инвестиция в мое будущее."</p>
                    <p class="font-semibold text-white">— Диана, 17 лет, Алматы</p>
                </div>

                <div class="process-card p-6 border-t-4 border-blue-500">
                    <p class="italic text-gray-300 mb-4">"Сначала я думал, что сам справлюсь. Но помощь с мотивационным письмом и интервью от PICK дала мне <strong>100% уверенность</strong>. Теперь я в Сеуле!"</p>
                    <p class="font-semibold text-white">— Арман, 18 лет, Нур-Султан</p>
                </div>

                <div class="process-card p-6 border-t-4 border-blue-500">
                    <p class="italic text-gray-300 mb-4">"Уроки корейского были максимально адаптированы под сдачу <strong>TOPIK 4</strong>. Это ускорило мой процесс в разы. Рекомендую всем, кто ищет грант!"</p>
                    <p class="font-semibold text-white">— Жанна, 16 лет, Астана</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="free-trial" class="py-16 md:py-24 bg-blue-900 text-white text-center">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl sm:text-4xl font-bold mb-4">
                Начните <strong>бесплатную консультацию</strong>.
            </h2>
            <p class="text-xl font-light mb-8 opacity-90">
                Запишитесь, чтобы составить индивидуальный план поступления и узнать свой реальный шанс на грант.
            </p>
            <div class="max-w-md mx-auto">
                 <button id="footerOpenModalBtn" class="cta-button w-full sm:w-auto px-8 py-3 rounded-lg uppercase tracking-wider">
                    Записаться сейчас
                </button>
                <p class="mt-3 text-sm italic opacity-80">
                    Количество мест на бесплатную консультацию ограничено.
                </p>
            </div>
        </div>
    </section>

    <footer id="contacts" class="bg-gray-900 text-gray-400 py-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center space-y-6 md:space-y-0">
            
            <div class="text-center md:text-left">
                <a href="#" class="text-3xl font-extrabold text-white mb-2 block">PICK</a>
                <p class="text-sm">EdTech Platform &copy; 2025. Все права защищены.</p>
            </div>

            <div class="flex space-x-6 text-xl">
                <a href="#" class="hover:text-white transition" aria-label="Instagram">
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.254.15 4.79 1.488 4.95 4.95.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.16 3.461-1.7 4.798-4.95 4.95-1.265.058-1.645.068-4.849.068-3.205 0-3.584-.012-4.849-.069-3.253-.15-4.79-1.488-4.95-4.95-.058-1.265-.068-1.644-.068-4.849 0-3.204.012-3.584.069-4.849.16-3.461 1.7-4.798 4.95-4.95 1.265-.058 1.644-.068 4.849-.068zM12 4.098c-3.176 0-3.57.012-4.802.069-2.903.132-3.967 1.206-4.098 4.098-.057 1.232-.069 1.626-.069 4.801 0 3.176.012 3.57.069 4.802.132 2.903 1.206 3.967 4.098 4.098 1.232.057 1.626.069 4.802.069 3.176 0 3.57-.012 4.801-.069 2.903 
                    c1.232-.057 1.626-.069 4.801-.069 3.176 0 3.57.012 4.802.069 2.903.132 3.967 1.206 4.098 4.098.057 1.232.069 1.626.069 4.801 0 3.176-.012 3.57-.069 4.802-.132 2.903-1.206 3.967-4.098 4.098-1.232.057-1.626.069-4.802.069zM12 5.517c3.568 0 3.98.013 5.394.075 3.195.148 5.163 1.956 5.397 5.397.062 1.414.075 1.826.075 5.394 0 3.568-.013 3.98-.075 5.394-.234 3.441-2.202 5.25-5.397 5.397-1.414.062-1.826.075-5.394.075-3.568 0-3.98-.013-5.394-.075-3.195-.148-5.163-1.956-5.397-5.397-.062-1.414-.075-1.826-.075-5.394 0-3.568.013-3.98.075-5.394.234-3.441 2.202-5.25 5.397-5.397 1.414-.062 1.826-.075 5.394-.075zM12 7.625c-2.43 0-4.375 1.945-4.375 4.375s1.945 4.375 4.375 4.375 4.375-1.945 4.375-4.375-1.945-4.375-4.375-4.375zm0 7.42c-1.685 0-3.045-1.36-3.045-3.045s1.36-3.045 3.045-3.045 3.045 1.36 3.045 3.045-1.36 3.045-3.045 3.045zm5.727-8.086c.61 0 1.104.493 1.104 1.104s-.494 1.104-1.104 1.104-1.104-.494-1.104-1.104.494-1.104 1.104-1.104z"/></svg>
                </a>
                <a href="#" class="hover:text-white transition" aria-label="Telegram">
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm5.181 8.216c.15.485-.233.916-.628.718l-3.327-1.61c-.42-.204-.816-.01-1.077.348l-1.98 2.64-4.23-1.328c-.46-.145-.92-.016-1.17.387-.25.402-.036.877.424 1.022l2.97 1.018c.55.188.805.57.85 1.144l.21 2.894c.06.827.818 1.096 1.364.385l.775-1.114c.28-.403.627-.61.996-.583l2.843.896c.55.176 1.08-.236 1.08-.82l.006-6.62c.002-.54-.265-.89-.785-1.05z"/></svg>
                </a>
                <a href="#" class="hover:text-white transition" aria-label="YouTube">
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M21.543 6.495c-.328-1.298-1.34-2.31-2.638-2.638C17.514 3.5 12 3.5 12 3.5s-5.514 0-6.805.357c-1.298.328-2.31 1.34-2.638 2.638C3.5 7.846 3.5 12 3.5 12s0 4.154.357 5.445c.328 1.298 1.34 2.31 2.638 2.638C6.486 20.5 12 20.5 12 20.5s5.514 0 6.805-.357c1.298-.328 2.31-1.34 2.638-2.638C20.5 16.154 20.5 12 20.5 12s0-4.154-.357-5.445zM10 16.142V7.858L16.275 12 10 16.142z"/></svg>
                </a>
            </div>
            
            <div class="text-center md:text-right">
                <p class="font-medium text-white mb-2">Контакты:</p>
                <p>+7 701 XXX XX XX (Казахстан)</p>
                <p>pick.edu.korea@gmail.com</p>
            </div>
        </div>
    </footer>
    
    <div id="ctaModal" class="fixed inset-0 bg-black bg-opacity-80 z-50 flex items-center justify-center hidden">
        <div class="bg-white p-8 rounded-lg shadow-2xl max-w-md w-full relative">
            <button id="closeModalBtn" class="absolute top-3 right-3 text-gray-700 hover:text-gray-900 text-3xl font-light leading-none">&times;</button>
            <h3 class="text-2xl font-bold text-gray-900 mb-4">Записаться на Бесплатную Консультацию</h3>
            <p class="text-gray-600 mb-6">Получите индивидуальный план поступления и узнайте свой реальный шанс на грант в Корее.</p>

            <form id="consultationForm" class="space-y-4">
                <div>
                    <input type="text" id="modalName" placeholder="Ваше Имя" class="modal-input-style" required>
                </div>
                <div>
                    <input type="tel" id="modalPhone" placeholder="Ваш Телефон (WhatsApp)" class="modal-input-style" required>
                </div>
                <div>
                    <input type="email" id="modalEmail" placeholder="Ваш Email" class="modal-input-style">
                </div>
                <button type="submit" id="modalSubmitBtn" class="w-full px-5 py-3 cta-button text-lg rounded-lg shadow-md mt-4 flex items-center justify-center">
                    <span id="modalButtonText">Получить бесплатный план</span>
                    <div id="modalLoader" class="hidden ml-3 spinner border-white border-t-white"></div>
                </button>
                <p id="modalMessage" class="mt-3 text-center text-sm text-green-600 hidden"></p>
            </form>
            <p class="mt-4 text-xs text-gray-500 text-center">
                Нажимая на кнопку, вы соглашаетесь с обработкой персональных данных.
            </p>
        </div>
    </div>
    
    <script>
        // Modal functionality
        const modal = document.getElementById('ctaModal');
        const openModalBtns = document.querySelectorAll('#navOpenModalBtn, #heroOpenModalBtn, #footerOpenModalBtn');
        const closeModalBtn = document.getElementById('closeModalBtn');
        const form = document.getElementById('consultationForm');
        const modalSubmitBtn = document.getElementById('modalSubmitBtn');
        const modalButtonText = document.getElementById('modalButtonText');
        const modalLoader = document.getElementById('modalLoader');
        const modalMessage = document.getElementById('modalMessage');

        openModalBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                modal.classList.remove('hidden');
                document.body.style.overflow = 'hidden'; // Prevent scrolling
            });
        });

        closeModalBtn.addEventListener('click', () => {
            modal.classList.add('hidden');
            document.body.style.overflow = ''; // Restore scrolling
        });

        // Close when clicking outside the modal content
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.classList.add('hidden');
                document.body.style.overflow = '';
            }
        });

        // Mock form submission (replace with actual API call)
        form.addEventListener('submit', function(e) {
            e.preventDefault();

            // Disable button and show loader
            modalSubmitBtn.disabled = true;
            modalButtonText.textContent = 'Отправка...';
            modalLoader.classList.remove('hidden');
            modalMessage.classList.add('hidden');

            setTimeout(() => {
                // Mock success state
                modalSubmitBtn.disabled = false;
                modalButtonText.textContent = 'Получить бесплатный план';
                modalLoader.classList.add('hidden');
                modalMessage.textContent = '✅ Заявка успешно отправлена! Мы свяжемся с вами в течение 30 минут.';
                modalMessage.classList.remove('hidden');
                form.reset();
                
                // Close modal after a short delay
                setTimeout(() => {
                     modal.classList.add('hidden');
                     document.body.style.overflow = '';
                     modalMessage.classList.add('hidden');
                }, 3000);

            }, 2000); // 2-second mock delay
        });
        
        // AI Coordinator LLM Integration (UPDATED FOR TOOL CALL)
        const evaluateButton = document.getElementById('evaluateButton');
        const resultOutputContainer = document.getElementById('resultOutputContainer');
        const resultOutput = document.getElementById('resultOutput');
        const loader = document.getElementById('loader');
        const buttonText = document.getElementById('buttonText');

        evaluateButton.addEventListener('click', async function() {
            const targetMajor = document.getElementById('targetMajor').value.trim();
            const currentTOPIK = document.getElementById('currentTOPIK').value.trim();
            const currentGPA = document.getElementById('currentGPA').value.trim();
            const currentAchievements = document.getElementById('currentAchievements').value.trim();

            if (!targetMajor || !currentTOPIK || !currentGPA || !currentAchievements) {
                resultOutputContainer.classList.remove('hidden');
                resultOutput.innerHTML = `<span class="text-red-400 font-bold">⚠️ Внимание:</span> Пожалуйста, заполните все поля для точной оценки.`;
                resultOutputContainer.style.borderColor = '#ef4444';
                return;
            }
            
            // Show loading state
            evaluateButton.disabled = true;
            buttonText.textContent = 'Оцениваем...';
            loader.classList.remove('hidden');
            resultOutputContainer.classList.add('hidden');
            resultOutput.innerHTML = '';
            resultOutputContainer.style.borderColor = '#3b82f6'; // Reset border color

            const userData = `
Major: ${targetMajor}
TOPIK: ${currentTOPIK}
GPA: ${currentGPA}
Achievements: ${currentAchievements}
`;
            
            const systemInstruction = `
You are the 'PICK AI-Coordinator,' an expert educational consultant specializing in securing 100% scholarship grants to South Korean universities. Your goal is to provide a highly structured, personalized analysis to qualify a prospective student and showcase the value of the PICK EdTech program.

The user will provide their Desired Major, Current TOPIK Level, GPA, and Key Achievements.

Your response MUST be in Russian, formatted using Markdown, and strictly follow these four sections in order. Do not include any introductory or concluding text outside of these four numbered sections.

## 1. Реалистичная Оценка (Без PICK)
* State the chance is only 10-20%.
* Explain that top Korean universities (even those offering grants) look for much more than just good scores/TOPIK. They require a compelling, highly developed profile (extracurriculars, leadership, unique stories) that most students cannot build alone.

## 2. Улучшенные Шансы (С PICK)
* State that with the 2-year PICK program, chances increase to **70-85%**.
* Explain that PICK provides the structured, step-by-step guidance needed to build a winning profile: from TOPIK mastery and extracurricular strategy to polished application documents, ensuring they stand out in the hyper-competitive Korean admissions pool.

## 3. Стратегический Список Университетов
* Recommend 3-4 specific universities that are a **strategic fit** for the student's current profile and major goal.
* The list must be selected from: Chung-Ang University, Dongguk University, Inha University, Pusan National University.
* For each university, briefly explain why it is a strategic and realistic target given their profile and the grant goal.

## 4. Персональный 2-Годичный Роудмап
* Provide a high-level timeline of the 2-year program (e.g., Months 1-6, Months 7-12, Months 13-18, Months 19-24).
* Structure the roadmap based on the PICK program pillars: TOPIK, Profile Building, Documents/Interview, and Final Application.
`;
            
            try {
                const toolResult = await google.generate_content({
                    model: 'gemini-2.5-flash',
                    contents: userData,
                    system_instruction: systemInstruction
                });
                
                const aiResponse = toolResult.text;
                
                // Display result, converting newlines for better display
                resultOutputContainer.classList.remove('hidden');
                // Use innerHTML and a simple replace to handle markdown and newlines
                resultOutput.innerHTML = aiResponse.replace(/\n/g, '<br>');
                
            } catch (error) {
                console.error('Gemini API Error:', error);
                resultOutput.innerHTML = `<span class="text-red-400 font-bold">⚠️ Произошла ошибка:</span> Не удалось получить оценку от AI-Координатора. Попробуйте обновить страницу.`;
                resultOutputContainer.classList.remove('hidden');
                resultOutputContainer.style.borderColor = '#ef4444';
            } finally {
                // Restore UI state
                evaluateButton.disabled = false;
                buttonText.textContent = 'Оценить шансы и получить план';
                loader.classList.add('hidden');
            }
        });

        // Smooth scrolling logic
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                const targetId = this.getAttribute('href');
                
                if (targetId === '#') {
                    e.preventDefault();
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                    return; 
                }

                e.preventDefault();
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                } else {
                    console.error('Target element not found for ID: ' + targetId);
                }
            });
        });
    </script>
</body>
</html>
