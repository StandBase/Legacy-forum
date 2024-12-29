<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Legacy Forum</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #1e1e2f;
            color: #ffffff;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #121212;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        header a {
            color: #ffffff;
            text-decoration: none;
            margin: 0 15px;
            font-size: 18px;
            font-weight: bold;
        }

        header a:hover {
            text-decoration: underline;
        }

        .content {
            text-align: center;
            padding: 20px;
        }

        .server-buttons {
            margin-top: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .server-buttons button {
            background: linear-gradient(to right, #ff7b7b, #ff3b3b);
            border: none;
            color: white;
            padding: 15px 30px;
            margin: 10px 0;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            width: 80%;
            max-width: 300px;
        }

        .server-buttons button:hover {
            background: linear-gradient(to right, #ff3b3b, #ff7b7b);
        }

        .modal {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #2a2a3d;
            padding: 20px;
            border-radius: 8px;
            width: 90%;
            max-width: 600px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.5);
            z-index: 1000;
        }

        .modal h3 {
            color: #ff7b7b;
        }

        .modal p {
            text-align: left;
            margin: 10px 0;
        }

        .modal button {
            margin-top: 15px;
            padding: 10px 20px;
            border: none;
            background: linear-gradient(to right, #4caf50, #2e7d32);
            color: white;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        .modal button:hover {
            background: linear-gradient(to right, #2e7d32, #4caf50);
        }

        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 999;
        }

    </style>
</head>
<body>
    <header>
        <a href="https://standbase.github.io/Legacy/">Главное</a>
        <a href="https://standbase.github.io/Legacy-shop/">Магазин</a>
        <a href="#">Форум</a>
    </header>

    <div class="content">
        <div class="server-buttons">
            <button onclick="openModal('server1')">Сервер №1 [Legacy]</button>
            <button onclick="openModal('server2')">Сервер №2 [Legacy]</button>
        </div>
    </div>

    <div id="modal" class="modal">
        <h3>Как стать админом</h3>
        <p>Доброго времени суток, уважаемые игроки сервера Legacy!<br>
        У Вас есть отличная возможность попасть на пост хелпера на нашем сервере!</p>
        <p><b>Требования к кандидатам:</b><br>
        - Быть грамотным, адекватным, коммуникабельным, ответственным;<br>
        - Знать правила сервера;<br>
        - Общий онлайн в игре от 22 часов в неделю;<br>
        - Иметь игровой уровень 20+;<br>
        - Возраст 14+.</p>
        <p><b>Правила подачи заявки:</b><br>
        - Аккаунт должен быть зарегистрирован до открытия заявок и быть активным.<br>
        - Форумный аккаунт должен быть зарегистрирован за 15 дней до открытия заявок.<br>
        - Отказы выдаются без объяснения причин.<br>
        - Запрещено создавать заявки с использованием VPN.<br>
        - Следует помнить: обман администрации карается баном.<br>
        </p>
        <p><b>[Важно!]</b> Прежде чем подать заявление на пост хелпера, обдумайте это несколько раз и решите, нужно ли это вам или нет.</p>
        <button onclick="window.open('https://t.me/Legacyrpserver', '_blank')">Подать заявку</button>
        <button onclick="closeModal()">Закрыть</button>
    </div>

    <div id="modal-overlay" class="modal-overlay" onclick="closeModal()"></div>

    <script>
        function openModal(server) {
            const modal = document.getElementById('modal');
            const overlay = document.getElementById('modal-overlay');
            modal.style.display = 'block';
            overlay.style.display = 'block';
            modal.querySelector('h3').textContent = server === 'server1' ? 'Как стать админом на сервере №1' : 'Как стать админом на сервере №2';
        }

        function closeModal() {
            const modal = document.getElementById('modal');
            const overlay = document.getElementById('modal-overlay');
            modal.style.display = 'none';
            overlay.style.display = 'none';
        }
    </script>
</body>
</html>
