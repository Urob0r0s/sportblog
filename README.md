# SportBlog

![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=green)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

Веб-приложение для спортивного блога, построенное на Django. Платформа позволяет публиковать статьи, управлять категориями и предоставляет систему пользователей с различными уровнями доступа.

## 🚀 Основные возможности

*   **Публикация статей:** Создание и редактирование спортивных статей
*   **Система категорий:** Организация статей по спортивным категориям
*   **Система пользователей:** Регистрация, авторизация и управление профилями
*   **Комментарии:** Возможность комментирования статей зарегистрированными пользователями
*   **Панель администратора:** Полный контроль над контентом через Django Admin
*   **Адаптивный дизайн:** Удобный интерфейс для всех устройств

## 🛠️ Технологический стек

*   **Backend:** Django 4.2+ (Python)
*   **Frontend:** HTML, CSS, JavaScript, Bootstrap
*   **База данных:** SQLite (разработка) / Готова к переходу на PostgreSQL
*   **Аутентификация:** Django Session Authentication
*   **Текстовый редактор:** CKEditor для редактирования контента

## 📦 Установка и запуск

### Предварительные требования

*   Python 3.8+
*   pip (менеджер пакетов Python)

### Шаги установки

1.  **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/Urob0r0s/sportblog.git
    cd sportblog
    ```

2.  **Создайте и активируйте виртуальное окружение:**
    ```bash
    python -m venv venv
    # Для Windows:
    venv\Scripts\activate
    # Для Linux/macOS:
    source venv/bin/activate
    ```

3.  **Установите зависимости:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Примените миграции базы данных:**
    ```bash
    python manage.py migrate
    ```

5.  **Создайте суперпользователя:**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Соберите статические файлы:**
    ```bash
    python manage.py collectstatic
    ```

7.  **Запустите сервер для разработки:**
    ```bash
    python manage.py runserver
    ```

8.  **Откройте приложение:**
    Перейдите по адресу [http://127.0.0.1:8000](http://127.0.0.1:8000) в вашем браузере.
    
    **Панель администратора:** [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)


👥 Управление пользователями

Обычные пользователи: Могут комментировать статьи и редактировать свой профиль

Авторы: Могут создавать и редактировать свои статьи

Администраторы: Полный доступ ко всем функциям через админ-панель


## 📁 Структура проекта

```plaintext
sportblog/
│
├── blog/                          # Основное приложение блога
│   ├── migrations/                # Файлы миграций базы данных
│   ├── templates/blog/            # HTML шаблоны блога
│   │   ├── base.html             # Базовый шаблон
│   │   ├── index.html            # Главная страница
│   │   ├── post_detail.html      # Детальная страница статьи
│   │   ├── category.html         # Страница категории
│   │   └── includes/             # Включаемые шаблоны
│   ├── static/blog/              # Статические файлы блога
│   │   ├── css/
│   │   ├── js/
│   │   └── images/
│   ├── __init__.py
│   ├── admin.py                  # Настройки админ-панели
│   ├── apps.py                   # Конфигурация приложения
│   ├── models.py                 # Модели данных (Post, Category, Comment)
│   ├── tests.py                  # Тесты
│   ├── urls.py                   # Маршруты приложения
│   ├── views.py                  # Представления (логика)
│   └── forms.py                  # Формы Django
│
├── users/                         # Приложение пользователей
│   ├── migrations/               # Миграции пользователей
│   ├── templates/users/          # Шаблоны аутентификации
│   │   ├── login.html           # Страница входа
│   │   ├── register.html        # Страница регистрации
│   │   └── profile.html         # Страница профиля
│   ├── __init__.py
│   ├── models.py                # Модель Profile
│   ├── views.py                 # Логика пользователей
│   └── forms.py                 # Формы регистрации и профиля
│
├── sportblog/                    # Настройки проекта
│   ├── __init__.py
│   ├── asgi.py                  # ASGI конфигурация
│   ├── settings.py              # Основные настройки
│   ├── urls.py                  # Корневые маршруты
│   └── wsgi.py                  # WSGI конфигурация
│
├── templates/                    # Глобальные шаблоны
│   └── base.html               # Основной шаблон сайта
│
├── static/                      # Глобальные статические файлы
│   ├── css/
│   ├── js/
│   └── images/
│
├── media/                       # Медиа файлы (изображения статей)
│   ├── post_images/
│   └── profile_pics/
│
├── requirements.txt             # Зависимости проекта
├── manage.py                    # Утилита управления Django
├── db.sqlite3                   # База данных SQLite
└── README.md                    # Документация проекта

🤝 Вклад в проект
Вклады приветствуются! Если у вас есть предложения по улучшению:

1.Сделайте fork проекта.
2.Создайте ветку для вашей фичи (git checkout -b feature/AmazingFeature).
3.Закоммитьте изменения (git commit -m 'Add some AmazingFeature').
4.Запушите ветку (git push origin feature/AmazingFeature).
5.Откройте Pull Request.