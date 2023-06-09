![image](https://user-images.githubusercontent.com/78702396/228333319-acc64c22-4400-48a4-b2d0-799bf1328ade.png)

# UAI_Team
Рады вас приветствовать! Это наш проект про разработке системы Аудиосопровождения для людей с нарушением зрения в рамках хакатона True Tech Hack. Мы предлагаем вам пройти увлекательный путь по нашему решению. Вы точно не собьётесь с пути если будете следовать нашему повествованию.


# Links
<a href="https://github.com/Aleshka5/video_hosting_website">Ссылка на репозиторий с сайтом на Flask</a> [1] - тут вы можете познакомиться с технической частью разработки нашего веб сервиса.<br>
<a href="http://91.185.84.94:5000">Наш сайт-плеер.</a> [2]<br>
<a href="https://colab.research.google.com/drive/12g97sgxS4suIZHFURT2iG9hGSduUnvzW#scrollTo=WozCs7AZuEUW">Colaboratory</a> [3]


# Intro
Если вы это читаете, значит мы уже высыпаемся после бессонных ночей. И это не может не радовать. Задача которая была поставлена перед нашей командой:<br>
Создать инструмент, который поможет людям с нарушением зрения понимать, что происходит в той или иной сцене фильма, не прерывая ход повествования. 
Решение этой задачи мы будем рассказывать по блокам, чтобы ничего не упустить.<br>
Задачу мы условно поделили на два больших этапа: 
  1. Создание алгоритма на основе нейросети (или нескольких нейросетей) для разметки видео, генерации комментариев и их озвучивания.<br>
  2. Создание сайта (то есть интерфейса взаимодействия с пользователем).<br>

# First Step (AI)
Более подробно вы можете рассмотреть нашу систему в нашей презентации: <a href="https://docs.google.com/presentation/d/1NDOTi7RWrr821zwFZXV0hywr4nAt6Wk7/edit?usp=sharing&ouid=101188216251655793371&rtpof=true&sd=true">Презентация Tiflo_system</a><br>
Здесь я расскажу в целом про архитектуру нашего решения:

Мы анализируем как визуальную так и аудио составляющие исходного фильма. И получаем самые временные промежутки в которые идеально подойдёт аудиосопровождение без нарушения исходного повествования.
![Архитектура markup](https://user-images.githubusercontent.com/78702396/228350523-9644b8ea-a2b6-461f-b131-0fbe6324e7c7.jpg)

Каждый участок анализируется отдельно, чтобы более получить более подробную информацию о происходящем на экране.
![Архитектура генерация текста](https://user-images.githubusercontent.com/78702396/228355518-dc0a5f65-224c-4172-a7b0-72e1965b2649.jpg)

Сгенерированные аудио дорожки с описанием происходящего подгоняются по темпу речи под размер имеющегося промежутка в диалоге.
![Архитектура генерация аудио](https://user-images.githubusercontent.com/78702396/228359374-f7e58ecc-e9d5-492b-9e02-28b50e5f7ee7.jpg)

В качестве уникальной особенности нашего решения мы выбрали контекстное сохранение информации о героях. Так, наше решение может не только рассказать что происходит вне диалогов, но и о том кто не посредственно сейчас разговаривает.
![Архитектура распознования персонажей](https://user-images.githubusercontent.com/100163713/229601924-5d52cc29-4c03-4121-8ff8-8636180fbefb.jpg)


# Second Step (Web App)
Более подробно вы можете рассмотреть наш сайт в репозитории: <a href="">[1]</a><br>

## Просмотр видео для людей с ограничениями по зрению, Искользуемые технологии

## Frontend
- <a href="https://github.com/vuejs">Vue</a>
- <a href="https://www.typescriptlang.org">TypeScript</a>
- <a href="https://github.com/videojs/video.js">Video.js</a> для воспроизведения видео
## Backend
- <a href="https://www.python.org/">Python</a>
- <a href="https://github.com/pallets/flask">Flask</a>
- <a href="https://github.com/sqlalchemy/sqlalchemy">SQLAlchemy</a>

# Quick Start
Для проверки работоспособности нашей системы для генерации тифлокомментариев вы можете выполнить простой код в ноутбуке <a href="https://colab.research.google.com/drive/12g97sgxS4suIZHFURT2iG9hGSduUnvzW#scrollTo=WozCs7AZuEUW">[3]</a>


# Our Team
 - Филенков Алексей: <a href="https://github.com/Aleshka5">Aleshka5</a><br>
 - Князев Александр: <a href="https://github.com/Squderini">Squderini</a><br>
- Шахлин Виталий: <a href="https://github.com/vshakhlin">vshakhlin</a><br>
- Глебов Павел: <a href="https://github.com/Pavel-hb">Pavel-hb</a><br>
- Мартынович Степан: <a href="https://github.com/Stedjey">Stedjey</a><br>

![team](https://user-images.githubusercontent.com/100163713/229600856-9db9442d-517c-4431-bbe0-ebba5a2ea1eb.png)
