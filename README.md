# JobFinder

JobFinder — это веб-приложение для поиска и управления вакансиями. Пользователи могут просматривать вакансии, сохранять их, а также управлять своей активностью через удобный интерфейс.

## Основные функции

- **Работа с вакансиями**:
  - Просмотр списка вакансий
  - Сохранение вакансий
  - Управление откликами

- **Управление данными пользователя**:
  - Регистрация и авторизация
  - Хранение пользовательской активности

## Технологии

- Бэкенд: FastAPI
- Фронтенд: React.js
- База данных: PostgreSQL
- Аутентификация: JWT

## Запуск проекта

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/AlekseyAmp/JobFinder-FastAPI-React
    cd JobFinder-FastAPI-React
    ```

2. Создайте файл `.env` в папке `server` и заполните его:
    ```env
    DATABASE_URL=postgresql://postgres:1@localhost:5432/JobFinder
    DATABASE_NAME=JobFinder

    JWT_ALGORITHM=RS256
    ACCESS_TOKEN_EXPIRES_IN=60
    REFRESH_TOKEN_EXPIRES_IN=15

    CLIENT_ORIGIN=http://localhost:3000

    JWT_PRIVATE_KEY=...
    JWT_PUBLIC_KEY=...
    ```

3. Запустите backend:
    ```bash
    cd server

    python -m venv venv

    # Linux / MacOS
    source venv/bin/activate

    # Windows
    venv\Scripts\activate

    pip install -r requirements.txt
    uvicorn main:app --reload
    ```

4. Запустите frontend (в отдельном терминале):
    ```bash
    cd client
    npm install
    npm start
    ```
