# justmotivation
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>justmotivation — Твой источник дисциплины</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: #0b0b0b;
            color: #e0e0e0;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            justify-content: space-between;
            align-items: center;
            padding: 40px 20px;
        }

        header {
            text-align: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            letter-spacing: 2px;
            color: #ffffff;
            text-transform: lowercase;
        }

        .logo span {
            color: #ff3b30;
        }

        main {
            max-width: 600px;
            width: 100%;
            text-align: center;
            padding: 20px;
        }

        .quote-container {
            background: #141414;
            border: 1px solid #222;
            border-radius: 12px;
            padding: 40px 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
            min-height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        #quote-text {
            font-size: 1.25rem;
            line-height: 1.6;
            color: #f5f5f7;
            font-weight: 400;
        }

        .btn {
            background-color: #ffffff;
            color: #0b0b0b;
            border: none;
            padding: 14px 28px;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            letter-spacing: 0.5px;
        }

        .btn:hover {
            background-color: #d1d1d6;
            transform: translateY(-2px);
        }

        .btn:active {
            transform: translateY(0);
        }

        footer {
            font-size: 0.85rem;
            color: #636366;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
    </p>
    </style>
</head>
<body>

    <header>
        <div class="logo">just<span>motivation</span></div>
    </header>

    <main>
        <div class="quote-container">
            <p id="quote-text">Нажми кнопку ниже, чтобы получить заряд дисциплины и энергии на сегодня.</p>
        </div>
        <button class="btn" onclick="generateQuote()">Получить мотивацию</button>
    </main>

    <footer>
        &copy; 2026 justmotivation. Все права защищены.
    </footer>

    <script>
        const quotes = [
            "Дисциплина — это выбор между тем, чего ты хочешь сейчас, и тем, чего ты хочешь больше всего.",
            "Каждый день — это еще один шанс изменить свою жизнь.",
            "Боль, которую ты чувствуешь сегодня, превратится в силу, которую ты почувствуешь завтра.",
            "Не жди идеальных условий. Создавай их.",
            "Побеждает тот, кто продолжает идти, даже когда тяжело.",
            "Твои результаты зависят только от того, что ты делаешь, когда никто не видит.",
            "Слабые ищут оправдания, сильные создают возможности.",
            "Маленькие ежедневные шаги приводят к грандиозным результатам.",
            "Сделай то, о чем завтра скажешь себе спасибо.",
            "Успех — это сумма небольших усилий, повторяющихся изо дня в день."
        ];

        function generateQuote() {
            const randomIndex = Math.floor(Math.random() * quotes.length);
            const quoteElement = document.getElementById("quote-text");
            
            // Легкая анимация смены текста
            quoteElement.style.opacity = 0;
            setTimeout(() => {
                quoteElement.textContent = quotes[randomIndex];
                quoteElement.style.opacity = 1;
            }, 150);
        }
    </script>

    <style>
        #quote-text {
            transition: opacity 0.15s ease-in-out;
        }
    </style>
</body>
</html>
