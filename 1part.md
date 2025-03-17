<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Главная страница</title>
    <style>
        body {
            background-image: url('images/background.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            transition: background-color 0.5s;
            color: black;
        }

        .logo {
            width: 200px;
            position: absolute;
            top: 20px;
            left: 20px;
            opacity: 0;
            transform: scale(0.5);
            animation: fadeIn 1s ease-in-out forwards;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: scale(0.5);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        @media (max-width: 768px) {
            .logo {
                width: 150px;
                top: 10px;
                left: 10px;
            }
        }

        .news {
            padding: 20px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
        }

        .dark-theme {
            background-color: #121212;
            color: white;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgb(0,0,0);
            background-color: rgba(0,0,0,0.4);
            padding-top: 60px;
        }

        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Логотип сайта" class="logo" loading="lazy" id="logo">
        <nav>
            <ul>
                <li><a href="index.html">Главная</a></li>
                <li><a href="news.html">Новости</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <button id="toggle-theme">Переключить тему</button>
        <h1>Добро пожаловать на наш сайт!</h1>
    </main>

    <div id="modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <p>Вы кликнули на логотип!</p>
        </div>
    </div>

    <section class="news">
        <article>
            <h2>Обновление игры!</h2>
            <p>Сегодня вышло новое обновление с новыми персонажами!</p>
        </article>
        <article>
            <h2>Скоро новый контент!</h2>
            <p>Готовьтесь к новому контенту, который выйдет в следующем месяце!</p>
        </article>
        <section class="comments">
            <h3>Комментарии</h3>
            <form id="comment-form">
                <textarea id="comment" placeholder="Ваш комментарий..." required></textarea>
                <button type="submit">Отправить</button>
            </form>
            <div id="comments-list"></div>
        </section>
    </section>

    <script>
        // Переключение темного и светлого режима
        const toggleButton = document.getElementById('toggle-theme');
        toggleButton.addEventListener('click', () => {
            document.body.classList.toggle('dark-theme');
        });

        // Модальное окно при клике на логотип
        const logo = document.getElementById('logo');
                const modal = document.getElementById('modal');
        const closeModal = document.getElementsByClassName('close')[0];

        logo.addEventListener('click', () => {
            modal.style.display = 'block';
        });

        closeModal.onclick = function() {
            modal.style.display = 'none';
        }

        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        }

        // Система комментариев
        const commentForm = document.getElementById('comment-form');
        const commentsList = document.getElementById('comments-list');

        if (commentForm) {
            commentForm.addEventListener('submit', function(event) {
                event.preventDefault();
                const commentText = document.getElementById('comment').value;
                const newComment = document.createElement('p');
                newComment.textContent = commentText;
                commentsList.appendChild(newComment);
                commentForm.reset();
            });
        }
    </script>
</body>
</html>

