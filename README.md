![assassins-creed-logo-png-transparent](https://github.com/user-attachments/assets/fd1df0cc-5329-4906-bc47-91a13a51d5d7)

<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>О нашей игре</title>
    <p>Assassin’s Creed — медиафраншиза компании Ubisoft, основанная на серии компьютерных игр. Первая игра вышла в 2007 году, последняя — Assassin’s Creed Nexus VR вышла 16 ноября 2023. В данный момент, в разработке находится игра Assassin’s Creed Shadows, которая выйдет 20 марта 2025.</p>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            text-align: center;
        }
        .nav {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        .nav a {
            color: #FAF0E6;
            font-size: 24px;
            text-decoration: none;
            margin: 10px 30px;
            padding: 10px 20px;
            border: 2px solid #FAF0E6;
            border-radius: 5px;
            background-color: transparent;
            transition: background-color 0.3s;
            cursor: pointer;
        }
        .nav a:hover {
            background-color: #8B0000;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin: 20px 0;
        }
        .thumbnail {
            width: 100%;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .thumbnail:hover {
            transform: scale(1.05);
        }
        #full-image {
            width: 500px;
            display: block;
            margin: 20px auto;
        }
        .hidden { display: none; }
        details { margin-bottom: 10px; cursor: pointer; }
        summary { font-weight: bold; }
        form {
            margin: 20px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        label {
            margin: 10px 0;
        }
        button {
            padding: 10px 20px;
            background-color: #8B0000;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease-in-out;
        }
        button:hover {
            background: #ff6600;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
    </style>
</head>
<body>

<div class="nav">
    <a href="index.html">На главную страницу</a>
</div>

<h1>О нашей игре</h1>
<p>Это увлекательная компьютерная игра в жанре RPG с открытым миром, где вы сможете исследовать различные локации, выполнять квесты и сражаться с врагами.</p>
<img src="https://images.unsplash.com/photo-1574169208502-2f1e0c2d4a8b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" alt="Изображение из игры" class="fade-in">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ID_ВИДЕО" frameborder="0" allowfullscreen></iframe>

<h2>Галерея изображений</h2>
<div class="gallery">
    <img src="https://images.unsplash.com/photo-1590495190935-5c8a4a0c0d6d?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 1">
        <img src="https://images.unsplash.com/photo-1609694038480-5c1e1d0e1e8b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 2">
    <img src="https://images.unsplash.com/photo-1614202211404-4a9e5f5e3b9b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 3">
    <img src="https://images.unsplash.com/photo-1614202211404-4a9e5f5e3b9b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 4">
    <img src="https://images.unsplash.com/photo-1623026267991-fb9b9c2c5c7b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 5">
    <img src="https://images.unsplash.com/photo-1623026267991-fb9b9c2c5c7b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=800" class="thumbnail" alt="Изображение 6">
</div>
<img id="full-image" class="hidden" alt="Увеличенное изображение">

<script>
    document.querySelectorAll('.thumbnail').forEach(img => {
        img.addEventListener('click', function() {
            document.getElementById('full-image').src = this.src;
            document.getElementById('full-image').classList.remove('hidden');
        });
    });
</script>

<h2>Часто задаваемые вопросы (FAQ)</h2>
<details>
    <summary>Какие системные требования у игры?</summary>
    <p>Минимальные требования: 8GB RAM, GTX 1050, 50GB свободного места.</p>
</details>
<details>
    <summary>Какой жанр игры?</summary>
    <p>Игра относится к жанру RPG с открытым миром.</p>
</details>
<details>
    <summary>Когда выйдет следующая версия игры?</summary>
    <p>Следующая версия игры запланирована на конец текущего года.</p>
</details>

<h2>Форма обратной связи</h2>
<form id="contact-form">
    <label>Имя: <input type="text" id="name" required></label>
    <label>Email: <input type="email" id="email" required></label>
    <label>Сообщение: <textarea id="message" required></textarea></label>
    <button type="submit">Отправить</button>
</form>
<p id="response"></p>

<script>
    document.getElementById('contact-form').addEventListener('submit', function(event) {
        event.preventDefault();
        document.getElementById('response').innerText = "Ваше сообщение принято! Скоро мы на него ответим.";
    });
</script>

</body>
</html>

