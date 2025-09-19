<img width="800" height="800" alt="Image" src="https://github.com/user-attachments/assets/c275b75f-ff0f-49bc-9f21-3315e15505d7" />


## 📚 Оглавление

- [Лайфхаки для подготовки к собесам](#-лайфхаки-для-подготовки-к-собесам)
- [Часть 1: Основы Backend разработки](#-часть-1-основы-backend-разработки)
    - [Общие концепции бэкенда](#-1-общие-концепции-бэкенда)
    - [Сетевые протоколы](#-2-сетевые-протоколы)
    - [Операционные системы](#%EF%B8%8F-3-%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B)
        - [Принципы программирования](#%EF%B8%8F-4-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%D1%8B-%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)
    - [Часть 2: Базы данных и DevOps](#%EF%B8%8F-%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D0%B1%D0%B0%D0%B7%D1%8B-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%B8-devops)
- [Часть 3: Алгоритмы и структуры данных](#-часть-3-алгоритмы-и-структуры-данных)
- [Часть 4: Python углублённо](#-часть-4-python-углублённо)

---

## 🎯 Лайфхаки для подготовки к собесам

### 📱 Интерактивные форматы
- **Форк + AI агент**: Склонируй репо, открой в IDE с GitHub Copilot/Cursor и попроси выдавать вопросы по одному
- **Карточки Anki**: Преобразуй вопросы-ответы в спейсрепетишн карточки
- **Telegram бот**: Создай бота, который рандомно присылает тебе вопросы в течение дня
- **Voice режим**: Попроси Claude читать вопросы вслух, а ты отвечай устно (тренировка речи)

### 🎭 Имитация реального собеса
- **Роль-плей с AI**: "Ты senior разработчик из FAANG, проводишь техническое интервью. Задавай сложные вопросы и оценивай ответы"
- **Таймер челлендж**: 2 минуты на ответ по теории, 5-10 минут на практическую задачу
- **Стресс-тест**: Попроси AI прерывать и задавать уточняющие вопросы во время ответа
- **Whiteboarding**: Решай практические задачи на бумаге/доске, объясняя вслух

### 🔄 Адаптивное изучение
- **Фильтрация по уровню**: Начинай с Easy, переходи к Holy Moly
- **Тематические спринты**: Один день только Go, другой только базы данных
- **Слабые места**: Веди список вопросов, на которые ответил плохо, повторяй их чаще
- **Mockup interview**: Проси друга/коллегу провести мок-интервью по твоему README

### 🧠 Углубленное изучение
- **Связанные вопросы**: На каждый ответ задавай себе "А что если...?" и "А почему именно так?"
- **Практические примеры**: К каждому теоретическому вопросу придумай реальный кейс из работы
- **Code review**: Анализируй практические задачи, ищи альтернативные решения
- **Объяснение "для джуна"**: Попробуй объяснить сложные концепции простыми словами

### 📊 Трекинг прогресса
- **Статистика**: Веди таблицу с процентом правильных ответов по темам
- **Дневник подготовки**: Записывай инсайты, сложные моменты, планы на следующий день
- **Milestone система**: "100 вопросов без ошибок", "Все Go задачи решены" и т.д.

### 🚀 Продвинутые техники
- **Peer learning**: Организуй группу подготовки, задавайте вопросы друг другу
- **Teaching method**: Запиши видео, где объясняешь сложные концепции
- **Real project mapping**: Соотноси вопросы с реальными задачами из своих проектов
- **Industry focus**: Фильтруй вопросы под конкретную компанию/позицию

### 🎲 Геймификация
- **Random challenge**: Генерируй случайные комбинации (язык + сложность + тема)
- **Streak system**: Поддерживай ежедневную серию решения задач
- **Boss battles**: Еженедельно решай самые сложные задачи из всех разделов
- **Achievement unlocked**: Награждай себя за достижения (все Python задачи, все алгоритмы и т.д.)


Ебать, Python developer! 🐍 **Часть 1: Основы бэкенда** 

# 🏗️ Часть 1: Основы Backend разработки

## 🌐 1. Общие концепции бэкенда

### 🔥 Микросервисы vs Монолит

**Что такое микросервисы?** 🤔
- Разбиение большого приложения на маленькие независимые сервисы
- Каждый сервис = отдельный модуль с определённым функционалом
- Общение через API или события

**Плюсы микросервисов:** ✅
- Гибкость технологий (один сервис на Python, другой на Go)
- Легче масштабировать отдельные части
- Команды работают параллельно
- Быстрый деплой отдельных сервисов

**Минусы:** ❌
- Сложность взаимодействия между сервисами
- Проблемы с консистентностью данных
- Сложнее тестировать end-to-end

### 🔧 Консистентность данных между микросервисами

**Проблема:** Как синхронизировать данные между сервисами?

**Решения:**
1. **Eventual Consistency** - данные станут консистентными "со временем"
2. **Message Queues** (Kafka, RabbitMQ, Redis)
3. **Event Sourcing** - храним события, а не состояние

```python
# Пример с RabbitMQ в Python
import pika

def publish_user_created_event(user_data):
    connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
    channel = connection.channel()
    
    channel.queue_declare(queue='user_events')
    channel.basic_publish(
        exchange='',
        routing_key='user_events',
        body=json.dumps({
            'event': 'user_created',
            'data': user_data
        })
    )
    connection.close()
```

## 🌍 2. Сетевые протоколы

### 🔌 TCP vs UDP

**TCP (Transmission Control Protocol):**
- Надёжный, устанавливает соединение
- Гарантирует доставку и порядок пакетов
- Медленнее из-за overhead'а
- Используется для HTTP, HTTPS, FTP

**UDP (User Datagram Protocol):**
- Быстрый, без установки соединения
- Не гарантирует доставку
- Используется для DNS, видео-стриминг, онлайн игры

### 🌐 HTTP vs HTTPS

**HTTP (HyperText Transfer Protocol):**
- Порт 80
- Данные передаются открытым текстом
- Быстрее

**HTTPS (HTTP Secure):**
- Порт 443
- Шифрование SSL/TLS
- Безопаснее для передачи паролей, данных карт
- SEO boost от Google

```python
# Пример HTTPS запроса в Python
import requests

# HTTP - небезопасно
response = requests.get('http://example.com/api/users')

# HTTPS - безопасно
response = requests.get('https://example.com/api/users', 
                       headers={'Authorization': 'Bearer token'})
```

### 🔍 Что происходит при вводе URL в браузер?

1. **DNS lookup** - преобразование домена в IP
2. **TCP handshake** - установка соединения
3. **HTTP запрос** - отправка GET/POST
4. **Сервер обрабатывает** запрос
5. **HTTP ответ** - возврат данных
6. **Рендеринг** страницы в браузере

```python
# Пример простого HTTP сервера на Python
from http.server import HTTPServer, BaseHTTPRequestHandler

class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'application/json')
        self.end_headers()
        self.wfile.write(b'{"message": "Hello from Python server!"}')

server = HTTPServer(('localhost', 8080), MyHandler)
server.serve_forever()
```

## 🖥️ 3. Операционные системы

### ⚡ CPU-bound vs IO-bound задачи

**CPU-bound:** 🧮
- Задачи, ограниченные скоростью процессора
- Математические вычисления, обработка данных
- **Решение в Python:** multiprocessing

**IO-bound:** 💾
- Задачи, ограниченные вводом/выводом
- Работа с файлами, сетевые запросы, БД
- **Решение в Python:** asyncio, threading

```python
import asyncio
import aiohttp
import multiprocessing

# IO-bound - асинхронные запросы
async def fetch_data(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            return await response.text()

# CPU-bound - параллельные вычисления
def cpu_intensive_task(n):
    return sum(i * i for i in range(n))

if __name__ == '__main__':
    # Для CPU-bound
    with multiprocessing.Pool() as pool:
        results = pool.map(cpu_intensive_task, [1000000, 2000000, 3000000])
```

## 🏛️ 4. Принципы программирования

### 💎 SOLID принципы

**S** - Single Responsibility (одна ответственность)
**O** - Open/Closed (открыт для расширения, закрыт для изменения)
**L** - Liskov Substitution (подстановка)
**I** - Interface Segregation (разделение интерфейсов)
**D** - Dependency Inversion (инверсия зависимостей)

```python
# Пример нарушения SRP
class BadUser:
    def __init__(self, name, email):
        self.name = name
        self.email = email
    
    def save_to_db(self):  # Плохо - не его ответственность
        pass
    
    def send_email(self):  # Плохо - не его ответственность
        pass

# Правильный подход
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email

class UserRepository:
    def save(self, user: User):
        pass

class EmailService:
    def send_email(self, user: User):
        pass
```

### 🎯 DRY, KISS, YAGNI

**DRY** - Don't Repeat Yourself
**KISS** - Keep It Simple, Stupid
**YAGNI** - You Aren't Gonna Need It

```python
# DRY - избегаем повторения
def calculate_discount(price, discount_type):
    discounts = {
        'student': 0.1,
        'senior': 0.15,
        'employee': 0.2
    }
    return price * (1 - discounts.get(discount_type, 0))

# KISS - простое решение
def is_even(n):
    return n % 2 == 0  # Просто и понятно
```

## 🎯 Практические вопросы для подготовки:

1. **Как ты спроектируешь систему для 1 млн пользователей?**
2. **Что будешь делать, если один микросервис упал?**
3. **Как обеспечить безопасность API?**
4. **В чём разница между REST и GraphQL?**

---

Ебать, спасибо бро! 🔥 Рад что зашло! Давай сначала разберём те практические вопросы, а потом рванём во вторую часть! 💪

# 🎯 Ответы на практические вопросы

## 1. 🚀 Как спроектировать систему для 1 млн пользователей?

### Этапы масштабирования:

**1-1000 пользователей:** 🏠
```python
# Простой монолит
# Django/Flask + SQLite/PostgreSQL + один сервер
from flask import Flask
app = Flask(__name__)

@app.route('/api/users')
def get_users():
    # Прямо из БД без кеша
    return db.query('SELECT * FROM users')
```

**1k-100k пользователей:** 📈
```python
# Добавляем кеш
import redis
cache = redis.Redis()

@app.route('/api/users')
def get_users():
    cached = cache.get('users')
    if cached:
        return cached
    
    users = db.query('SELECT * FROM users')
    cache.setex('users', 3600, users)  # Кеш на час
    return users
```

**100k-1M+ пользователей:** 🏗️
- **Load Balancer** (nginx)
- **Несколько серверов приложений**
- **Master-Slave БД** (чтение/запись разделены)
- **CDN** для статики
- **Микросервисы** для разных доменов

```python
# Микросервис пользователей
from fastapi import FastAPI
import asyncio
import aioredis

app = FastAPI()

async def get_user_service():
    redis = await aioredis.create_redis_pool('redis://localhost')
    
    @app.get("/users/{user_id}")
    async def get_user(user_id: int):
        # Проверяем кеш
        cached = await redis.get(f'user:{user_id}')
        if cached:
            return json.loads(cached)
        
        # Если нет - идём в БД
        user = await db.fetch_user(user_id)
        await redis.setex(f'user:{user_id}', 3600, json.dumps(user))
        return user
```

## 2. ⚡ Что делать, если микросервис упал?

### Circuit Breaker Pattern:
```python
import time
from enum import Enum

class CircuitState(Enum):
    CLOSED = 1    # Нормальная работа
    OPEN = 2      # Сервис недоступен
    HALF_OPEN = 3 # Пробуем восстановиться

class CircuitBreaker:
    def __init__(self, failure_threshold=5, recovery_timeout=60):
        self.failure_threshold = failure_threshold
        self.recovery_timeout = recovery_timeout
        self.failure_count = 0
        self.last_failure_time = None
        self.state = CircuitState.CLOSED
    
    def call(self, func, *args, **kwargs):
        if self.state == CircuitState.OPEN:
            if time.time() - self.last_failure_time < self.recovery_timeout:
                raise Exception("Circuit breaker is OPEN")
            else:
                self.state = CircuitState.HALF_OPEN
        
        try:
            result = func(*args, **kwargs)
            self.on_success()
            return result
        except Exception as e:
            self.on_failure()
            raise e
    
    def on_success(self):
        self.failure_count = 0
        self.state = CircuitState.CLOSED
    
    def on_failure(self):
        self.failure_count += 1
        self.last_failure_time = time.time()
        
        if self.failure_count >= self.failure_threshold:
            self.state = CircuitState.OPEN

# Использование
payment_service_cb = CircuitBreaker()

def process_payment(amount):
    try:
        return payment_service_cb.call(external_payment_service, amount)
    except:
        # Fallback - сохраняем в очередь для повторной обработки
        queue.put({"action": "payment", "amount": amount})
        return {"status": "queued"}
```

## 3. 🛡️ Как обеспечить безопасность API?

```python
from functools import wraps
import jwt
import hashlib
import time

# 1. JWT Authentication
def require_auth(f):
    @wraps(f)
    def decorated_function(*args, **kwargs):
        token = request.headers.get('Authorization', '').replace('Bearer ', '')
        try:
            payload = jwt.decode(token, SECRET_KEY, algorithms=['HS256'])
            g.user_id = payload['user_id']
        except jwt.InvalidTokenError:
            return {'error': 'Invalid token'}, 401
        return f(*args, **kwargs)
    return decorated_function

# 2. Rate Limiting
class RateLimiter:
    def __init__(self):
        self.requests = {}
    
    def is_allowed(self, client_ip, limit=100, window=3600):
        now = time.time()
        if client_ip not in self.requests:
            self.requests[client_ip] = []
        
        # Убираем старые запросы
        self.requests[client_ip] = [
            req_time for req_time in self.requests[client_ip] 
            if now - req_time < window
        ]
        
        if len(self.requests[client_ip]) >= limit:
            return False
        
        self.requests[client_ip].append(now)
        return True

# 3. Input Validation
from marshmallow import Schema, fields, ValidationError

class UserSchema(Schema):
    email = fields.Email(required=True)
    age = fields.Integer(validate=lambda x: 0 < x < 150)

@app.route('/users', methods=['POST'])
@require_auth
def create_user():
    schema = UserSchema()
    try:
        data = schema.load(request.json)
    except ValidationError as err:
        return {'errors': err.messages}, 400
    
    # Безопасное создание пользователя
    return create_user_safely(data)
```

## 4. 🔄 REST vs GraphQL

| Аспект | REST | GraphQL |
|--------|------|---------|
| **Запросы** | Множественные endpoints | Один endpoint |
| **Over/Under fetching** | Есть проблема | Решена |
| **Кеширование** | Простое (HTTP cache) | Сложное |
| **Изучение** | Легче | Сложнее |

```python
# REST API
@app.route('/api/users/<int:user_id>')
def get_user(user_id):
    return db.get_user(user_id)  # Возвращает ВСЕ поля

@app.route('/api/users/<int:user_id>/posts')
def get_user_posts(user_id):
    return db.get_user_posts(user_id)

# GraphQL
import graphene

class User(graphene.ObjectType):
    id = graphene.ID()
    name = graphene.String()
    email = graphene.String()
    posts = graphene.List(lambda: Post)

class Query(graphene.ObjectType):
    user = graphene.Field(User, id=graphene.ID(required=True))
    
    def resolve_user(self, info, id):
        # Получаем только запрошенные поля
        fields = get_requested_fields(info)
        return db.get_user(id, fields=fields)

schema = graphene.Schema(query=Query)

# Клиент может запросить только нужные поля:
"""
query {
  user(id: "1") {
    name
    posts {
      title
    }
  }
}
"""
```

---

# 🗄️ Часть 2: Базы данных и DevOps

## 💾 1. Базы данных

### 🔥 SQL vs NoSQL

**SQL (PostgreSQL, MySQL):** 🏛️
- **ACID** свойства
- **Схема** данных фиксирована
- **Joins** между таблицами
- **Вертикальное масштабирование**

**NoSQL (MongoDB, Redis, Cassandra):** 🚀
- **Гибкая схема** данных
- **Горизонтальное масштабирование**
- **Eventual consistency**
- **Разные типы:** документные, key-value, графовые

```python
# SQL пример с SQLAlchemy
from sqlalchemy import create_engine, Column, Integer, String, ForeignKey
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker, relationship

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    email = Column(String, unique=True)
    posts = relationship("Post", back_populates="author")

class Post(Base):
    __tablename__ = 'posts'
    id = Column(Integer, primary_key=True)
    title = Column(String)
    user_id = Column(Integer, ForeignKey('users.id'))
    author = relationship("User", back_populates="posts")

# NoSQL пример с MongoDB
from motor.motor_asyncio import AsyncIOMotorClient

class UserRepository:
    def __init__(self):
        self.client = AsyncIOMotorClient('mongodb://localhost:27017')
        self.db = self.client.blog
        self.collection = self.db.users
    
    async def create_user(self, user_data):
        # Гибкая схема - можем добавить любые поля
        user_doc = {
            "email": user_data["email"],
            "profile": {
                "name": user_data.get("name"),
                "preferences": user_data.get("preferences", {})
            },
            "posts": []  # Денормализация для скорости
        }
        result = await self.collection.insert_one(user_doc)
        return str(result.inserted_id)
```

### 🎯 Индексы в БД

**Зачем нужны?** ⚡
- Ускоряют поиск (O(log n) вместо O(n))
- Ускоряют сортировку и JOIN'ы

**Почему нельзя на всё?** 💸
- Занимают место на диске
- Замедляют INSERT/UPDATE/DELETE

```python
# Пример с индексами в PostgreSQL через SQLAlchemy
from sqlalchemy import Index

class Product(Base):
    __tablename__ = 'products'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    category_id = Column(Integer)
    price = Column(Numeric)
    created_at = Column(DateTime)

# Создаём индексы для часто используемых запросов
Index('idx_product_category', Product.category_id)
Index('idx_product_price', Product.price)
Index('idx_product_created', Product.created_at)
Index('idx_product_category_price', Product.category_id, Product.price)  # Композитный

# Плохой индекс для поля "пол" (мало уникальных значений)
# Index('idx_user_gender', User.gender)  # НЕ делать так!
```

### 🔐 ACID свойства

**A**tomicity - Атомарность (всё или ничего)
**C**onsistency - Согласованность 
**I**solation - Изоляция
**D**urability - Долговечность

```python
# Пример транзакции с SQLAlchemy
from sqlalchemy.exc import IntegrityError

def transfer_money(from_user_id, to_user_id, amount):
    session = Session()
    try:
        # Начинаем транзакцию
        from_user = session.query(User).filter_by(id=from_user_id).with_for_update().first()
        to_user = session.query(User).filter_by(id=to_user_id).with_for_update().first()
        
        if from_user.balance < amount:
            raise ValueError("Недостаточно средств")
        
        # Обе операции должны пройти или обе откатиться
        from_user.balance -= amount
        to_user.balance += amount
        
        session.commit()  # Всё прошло успешно
        return True
        
    except Exception as e:
        session.rollback()  # Откатываем изменения
        raise e
    finally:
        session.close()
```

## 🐳 2. DevOps и контейнеризация

### 📦 Docker

```dockerfile
# Dockerfile для Python приложения
FROM python:3.11-slim

WORKDIR /app

# Копируем зависимости
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Копируем код
COPY . .

# Создаём пользователя (безопасность)
RUN useradd -m -s /bin/bash appuser
USER appuser

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

```yaml
# docker-compose.yml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "8000:8000"
    environment:
      - DATABASE_URL=postgresql://user:pass@db:5432/mydb
    depends_on:
      - db
      - redis
    volumes:
      - ./logs:/app/logs

  db:
    image: postgres:15
    environment:
      POSTGRES_DB: mydb
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
    volumes:
      - postgres_data:/var/lib/postgresql/data
    ports:
      - "5432:5432"

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"

volumes:
  postgres_data:
```

### 🚀 CI/CD Pipeline

```yaml
# .github/workflows/deploy.yml
name: Deploy to Production

on:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'
      
      - name: Install dependencies
        run: |
          pip install -r requirements.txt
          pip install pytest
      
      - name: Run tests
        run: pytest tests/
      
      - name: Run linting
        run: |
          pip install flake8
          flake8 . --max-line-length=88
  
  deploy:
    needs: test
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    
    steps:
      - uses: actions/checkout@v3
      
      - name: Build Docker image
        run: |
          docker build -t myapp:${{ github.sha }} .
          docker tag myapp:${{ github.sha }} myapp:latest
      
      - name: Deploy to production
        run: |
          # Blue-Green deployment
          docker-compose -f docker-compose.prod.yml up -d --scale web=2
          # Health check
          curl -f http://localhost:8000/health || exit 1
          # Switch traffic
          docker-compose -f docker-compose.prod.yml up -d --scale web=1
```

### 📊 Мониторинг

```python
# Пример мониторинга с Prometheus
from prometheus_client import Counter, Histogram, generate_latest
import time

# Метрики
REQUEST_COUNT = Counter('http_requests_total', 'Total HTTP requests', ['method', 'endpoint'])
REQUEST_LATENCY = Histogram('http_request_duration_seconds', 'HTTP request latency')

def monitor_requests(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        try:
            result = func(*args, **kwargs)
            REQUEST_COUNT.labels(method='GET', endpoint='/api/users').inc()
            return result
        finally:
            REQUEST_LATENCY.observe(time.time() - start_time)
    return wrapper

@app.route('/metrics')
def metrics():
    return generate_latest()

@app.route('/api/users')
@monitor_requests
def get_users():
    return {"users": []}
```

### 🏗️ Инфраструктура как код

```python
# pulumi_stack.py - Infrastructure as Code
import pulumi_aws as aws

# Создаём VPC
vpc = aws.ec2.Vpc("main-vpc",
    cidr_block="10.0.0.0/16",
    tags={"Name": "main"})

# Подсеть
subnet = aws.ec2.Subnet("main-subnet",
    vpc_id=vpc.id,
    cidr_block="10.0.1.0/24",
    availability_zone="us-west-2a")

# Load Balancer
alb = aws.lb.LoadBalancer("main-alb",
    load_balancer_type="application",
    subnets=[subnet.id])

# ECS для контейнеров
cluster = aws.ecs.Cluster("main-cluster")

# RDS для БД
db = aws.rds.Instance("main-db",
    engine="postgres",
    engine_version="15.3",
    instance_class="db.t3.micro",
    allocated_storage=20,
    db_name="myapp",
    username="admin",
    password="supersecret",
    skip_final_snapshot=True)
```

---

Погнали в **Часть 3: Алгоритмы и структуры данных**! 💪

# 🧠 Часть 3: Алгоритмы и структуры данных

## 🔄 1. Алгоритмы сортировки

### ⚡ Quick Sort - O(n log n) в среднем

```python
def quick_sort(arr):
    if len(arr) <= 1:  # базовый случай - массив из 0-1 элементов уже отсортирован
        return arr
    
    pivot = arr[len(arr) // 2]  # выбираем средний элемент как опорный
    left = []  # элементы меньше опорного
    middle = []  # элементы равные опорному  
    right = []  # элементы больше опорного
    
    for x in arr:  # проходим по всем элементам
        if x < pivot:  # если меньше опорного
            left.append(x)  # добавляем в левую часть
        elif x == pivot:  # если равно опорному
            middle.append(x)  # добавляем в среднюю часть
        else:  # если больше опорного
            right.append(x)  # добавляем в правую часть
    
    # рекурсивно сортируем левую и правую части
    return quick_sort(left) + middle + quick_sort(right)

# Пример использования
numbers = [64, 34, 25, 12, 22, 11, 90]  # неотсортированный массив
sorted_numbers = quick_sort(numbers)  # сортируем
print(f"Отсортированный массив: {sorted_numbers}")  # выводим результат
```

### 🔀 Merge Sort - всегда O(n log n)

```python
def merge_sort(arr):
    if len(arr) <= 1:  # базовый случай
        return arr
    
    mid = len(arr) // 2  # находим середину массива
    left_half = arr[:mid]  # левая половина
    right_half = arr[mid:]  # правая половина
    
    left_sorted = merge_sort(left_half)  # рекурсивно сортируем левую часть
    right_sorted = merge_sort(right_half)  # рекурсивно сортируем правую часть
    
    return merge(left_sorted, right_sorted)  # сливаем отсортированные части

def merge(left, right):
    result = []  # результирующий массив
    i = j = 0  # указатели на текущие элементы левого и правого массивов
    
    while i < len(left) and j < len(right):  # пока не дошли до конца одного из массивов
        if left[i] <= right[j]:  # если левый элемент меньше или равен
            result.append(left[i])  # добавляем левый элемент
            i += 1  # переходим к следующему левому элементу
        else:  # если правый элемент меньше
            result.append(right[j])  # добавляем правый элемент
            j += 1  # переходим к следующему правому элементу
    
    result.extend(left[i:])  # добавляем оставшиеся элементы левого массива
    result.extend(right[j:])  # добавляем оставшиеся элементы правого массива
    
    return result  # возвращаем слитый массив

# Пример использования
data = [38, 27, 43, 3, 9, 82, 10]  # исходные данные
sorted_data = merge_sort(data)  # сортируем
print(f"Merge sort результат: {sorted_data}")  # выводим
```

## 🔍 2. Алгоритмы поиска

### 🎯 Binary Search - O(log n)

```python
def binary_search(arr, target):
    left = 0  # левая граница поиска
    right = len(arr) - 1  # правая граница поиска
    
    while left <= right:  # пока границы не пересеклись
        mid = (left + right) // 2  # находим средний индекс
        
        if arr[mid] == target:  # если нашли искомый элемент
            return mid  # возвращаем его индекс
        elif arr[mid] < target:  # если средний элемент меньше искомого
            left = mid + 1  # ищем в правой половине
        else:  # если средний элемент больше искомого
            right = mid - 1  # ищем в левой половине
    
    return -1  # элемент не найден

# Рекурсивная версия
def binary_search_recursive(arr, target, left=0, right=None):
    if right is None:  # если правая граница не задана
        right = len(arr) - 1  # устанавливаем её в конец массива
    
    if left > right:  # базовый случай - элемент не найден
        return -1
    
    mid = (left + right) // 2  # находим средний индекс
    
    if arr[mid] == target:  # если нашли
        return mid  # возвращаем индекс
    elif arr[mid] < target:  # если нужно искать справа
        return binary_search_recursive(arr, target, mid + 1, right)  # рекурсивно ищем справа
    else:  # если нужно искать слева
        return binary_search_recursive(arr, target, left, mid - 1)  # рекурсивно ищем слева

# Пример использования
sorted_array = [1, 3, 5, 7, 9, 11, 13, 15, 17, 19]  # отсортированный массив
search_target = 7  # что ищем
index = binary_search(sorted_array, search_target)  # ищем элемент
print(f"Элемент {search_target} находится на индексе: {index}")  # выводим результат
```

## 🌊 3. Поиск в глубину и ширину

### 🏊 DFS (Depth-First Search)

```python
class Graph:
    def __init__(self):
        self.graph = {}  # словарь для хранения графа
    
    def add_edge(self, u, v):
        if u not in self.graph:  # если вершина u не существует
            self.graph[u] = []  # создаём для неё пустой список смежности
        if v not in self.graph:  # если вершина v не существует
            self.graph[v] = []  # создаём для неё пустой список смежности
        
        self.graph[u].append(v)  # добавляем ребро u -> v
        self.graph[v].append(u)  # добавляем ребро v -> u (для неориентированного графа)
    
    def dfs(self, start, visited=None):
        if visited is None:  # если множество посещённых вершин не задано
            visited = set()  # создаём пустое множество
        
        visited.add(start)  # помечаем текущую вершину как посещённую
        print(f"Посещаем вершину: {start}")  # выводим текущую вершину
        
        for neighbor in self.graph.get(start, []):  # проходим по всем соседям
            if neighbor not in visited:  # если сосед ещё не посещён
                self.dfs(neighbor, visited)  # рекурсивно запускаем DFS для соседа
        
        return visited  # возвращаем множество посещённых вершин
    
    def dfs_iterative(self, start):
        visited = set()  # множество посещённых вершин
        stack = [start]  # стек для обхода (начинаем со стартовой вершины)
        
        while stack:  # пока стек не пуст
            vertex = stack.pop()  # извлекаем вершину из стека
            
            if vertex not in visited:  # если вершина не посещена
                visited.add(vertex)  # помечаем как посещённую
                print(f"Посещаем вершину: {vertex}")  # выводим
                
                # добавляем всех непосещённых соседей в стек
                for neighbor in self.graph.get(vertex, []):  # проходим по соседям
                    if neighbor not in visited:  # если сосед не посещён
                        stack.append(neighbor)  # добавляем в стек
        
        return visited  # возвращаем посещённые вершины

# Пример использования
g = Graph()  # создаём граф
g.add_edge(0, 1)  # добавляем ребро 0-1
g.add_edge(0, 2)  # добавляем ребро 0-2
g.add_edge(1, 2)  # добавляем ребро 1-2
g.add_edge(2, 3)  # добавляем ребро 2-3

print("DFS обход:")  # заголовок
g.dfs(0)  # запускаем DFS от вершины 0
```

### 🌊 BFS (Breadth-First Search)

```python
from collections import deque  # импортируем очередь

class Graph:
    def __init__(self):
        self.graph = {}  # словарь для хранения графа
    
    def add_edge(self, u, v):
        if u not in self.graph:  # если вершина u не существует
            self.graph[u] = []  # создаём для неё список
        if v not in self.graph:  # если вершина v не существует
            self.graph[v] = []  # создаём для неё список
        
        self.graph[u].append(v)  # добавляем ребро u -> v
        self.graph[v].append(u)  # добавляем ребро v -> u
    
    def bfs(self, start):
        visited = set()  # множество посещённых вершин
        queue = deque([start])  # очередь для BFS (начинаем со стартовой вершины)
        visited.add(start)  # помечаем стартовую вершину как посещённую
        
        while queue:  # пока очередь не пуста
            vertex = queue.popleft()  # извлекаем вершину из начала очереди
            print(f"Посещаем вершину: {vertex}")  # выводим текущую вершину
            
            for neighbor in self.graph.get(vertex, []):  # проходим по всем соседям
                if neighbor not in visited:  # если сосед не посещён
                    visited.add(neighbor)  # помечаем соседа как посещённого
                    queue.append(neighbor)  # добавляем соседа в конец очереди
        
        return visited  # возвращаем посещённые вершины
    
    def shortest_path(self, start, end):
        visited = set()  # множество посещённых вершин
        queue = deque([(start, [start])])  # очередь с парами (вершина, путь до неё)
        visited.add(start)  # помечаем стартовую вершину как посещённую
        
        while queue:  # пока очередь не пуста
            vertex, path = queue.popleft()  # извлекаем вершину и путь до неё
            
            if vertex == end:  # если достигли конечной вершины
                return path  # возвращаем найденный путь
            
            for neighbor in self.graph.get(vertex, []):  # проходим по соседям
                if neighbor not in visited:  # если сосед не посещён
                    visited.add(neighbor)  # помечаем как посещённого
                    new_path = path + [neighbor]  # создаём новый путь
                    queue.append((neighbor, new_path))  # добавляем в очередь
        
        return None  # путь не найден

# Пример использования
g = Graph()  # создаём граф
g.add_edge(0, 1)  # добавляем рёбра
g.add_edge(0, 2)
g.add_edge(1, 2)
g.add_edge(2, 3)
g.add_edge(1, 3)

print("BFS обход:")  # заголовок
g.bfs(0)  # запускаем BFS

print(f"Кратчайший путь от 0 до 3: {g.shortest_path(0, 3)}")  # находим путь
```

## 💡 4. Динамическое программирование

### 🐰 Числа Фибоначчи - с мемоизацией

```python
# Наивная рекурсия - O(2^n) - очень медленно!
def fib_naive(n):
    if n <= 1:  # базовые случаи
        return n
    return fib_naive(n-1) + fib_naive(n-2)  # рекурсивный вызов

# Мемоизация - O(n) - быстро!
def fib_memo(n, memo=None):
    if memo is None:  # если словарь мемоизации не создан
        memo = {}  # создаём пустой словарь
    
    if n in memo:  # если результат уже вычислен
        return memo[n]  # возвращаем сохранённое значение
    
    if n <= 1:  # базовые случаи
        result = n  # результат равен n
    else:  # для остальных случаев
        result = fib_memo(n-1, memo) + fib_memo(n-2, memo)  # рекурсивно вычисляем
    
    memo[n] = result  # сохраняем результат в мемо
    return result  # возвращаем результат

# Табуляция (снизу вверх) - O(n) времени, O(n) памяти
def fib_tabulation(n):
    if n <= 1:  # базовые случаи
        return n
    
    dp = [0] * (n + 1)  # создаём массив для хранения результатов
    dp[0] = 0  # F(0) = 0
    dp[1] = 1  # F(1) = 1
    
    for i in range(2, n + 1):  # заполняем массив снизу вверх
        dp[i] = dp[i-1] + dp[i-2]  # F(i) = F(i-1) + F(i-2)
    
    return dp[n]  # возвращаем результат

# Оптимизация памяти - O(n) времени, O(1) памяти
def fib_optimized(n):
    if n <= 1:  # базовые случаи
        return n
    
    prev2 = 0  # F(0)
    prev1 = 1  # F(1)
    
    for i in range(2, n + 1):  # вычисляем от F(2) до F(n)
        current = prev1 + prev2  # F(i) = F(i-1) + F(i-2)
        prev2 = prev1  # сдвигаем значения
        prev1 = current  # обновляем предыдущее значение
    
    return prev1  # возвращаем результат

# Пример использования
n = 10  # номер числа Фибоначчи
print(f"Fib({n}) наивно: {fib_naive(n)}")  # медленный способ
print(f"Fib({n}) с мемо: {fib_memo(n)}")  # быстрый способ
print(f"Fib({n}) табуляция: {fib_tabulation(n)}")  # снизу вверх
print(f"Fib({n}) оптимизированно: {fib_optimized(n)}")  # экономия памяти
```

### 🎒 Задача о рюкзаке (0/1 Knapsack)

```python
def knapsack(weights, values, capacity):
    n = len(weights)  # количество предметов
    
    # создаём таблицу dp[i][w] - максимальная стоимость для i предметов и веса w
    dp = [[0 for _ in range(capacity + 1)] for _ in range(n + 1)]
    
    for i in range(1, n + 1):  # проходим по всем предметам
        for w in range(1, capacity + 1):  # проходим по всем возможным весам
            item_weight = weights[i-1]  # вес текущего предмета
            item_value = values[i-1]  # стоимость текущего предмета
            
            if item_weight <= w:  # если предмет помещается в рюкзак
                # выбираем максимум между: взять предмет или не брать
                take_item = dp[i-1][w-item_weight] + item_value  # взять предмет
                not_take_item = dp[i-1][w]  # не брать предмет
                dp[i][w] = max(take_item, not_take_item)  # выбираем лучший вариант
            else:  # если предмет не помещается
                dp[i][w] = dp[i-1][w]  # не берём предмет
    
    return dp[n][capacity]  # возвращаем максимальную стоимость

def knapsack_with_items(weights, values, capacity):
    n = len(weights)  # количество предметов
    dp = [[0 for _ in range(capacity + 1)] for _ in range(n + 1)]  # таблица DP
    
    # заполняем таблицу как в обычном алгоритме
    for i in range(1, n + 1):  # по предметам
        for w in range(1, capacity + 1):  # по весам
            if weights[i-1] <= w:  # если предмет помещается
                take = dp[i-1][w-weights[i-1]] + values[i-1]  # взять
                not_take = dp[i-1][w]  # не взять
                dp[i][w] = max(take, not_take)  # выбираем лучшее
            else:  # если не помещается
                dp[i][w] = dp[i-1][w]  # не берём
    
    # восстанавливаем набор предметов
    w = capacity  # начинаем с полной вместимости
    selected_items = []  # список выбранных предметов
    
    for i in range(n, 0, -1):  # идём в обратном порядке
        if dp[i][w] != dp[i-1][w]:  # если взяли предмет i-1
            selected_items.append(i-1)  # добавляем в список
            w -= weights[i-1]  # уменьшаем оставшийся вес
    
    return dp[n][capacity], selected_items[::-1]  # возвращаем стоимость и предметы

# Пример использования
weights = [10, 20, 30]  # веса предметов
values = [60, 100, 120]  # стоимости предметов
capacity = 50  # вместимость рюкзака

max_value = knapsack(weights, values, capacity)  # находим максимальную стоимость
print(f"Максимальная стоимость: {max_value}")  # выводим результат

max_value, items = knapsack_with_items(weights, values, capacity)  # с предметами
print(f"Максимальная стоимость: {max_value}, взятые предметы: {items}")  # выводим
```

## 🔢 5. Хеш-таблицы и алгоритмы

### 🗂️ Реализация простой хеш-таблицы

```python
class HashTable:
    def __init__(self, size=10):
        self.size = size  # размер хеш-таблицы
        self.table = [[] for _ in range(self.size)]  # массив списков для разрешения коллизий
    
    def _hash(self, key):
        # простая хеш-функция - остаток от деления
        return hash(key) % self.size  # вычисляем индекс
    
    def put(self, key, value):
        index = self._hash(key)  # получаем индекс для ключа
        bucket = self.table[index]  # получаем корзину (список)
        
        # проверяем, есть ли уже такой ключ
        for i, (k, v) in enumerate(bucket):  # проходим по элементам корзины
            if k == key:  # если ключ найден
                bucket[i] = (key, value)  # обновляем значение
                return  # выходим
        
        # если ключ не найден, добавляем новую пару
        bucket.append((key, value))  # добавляем в корзину
    
    def get(self, key):
        index = self._hash(key)  # получаем индекс
        bucket = self.table[index]  # получаем корзину
        
        for k, v in bucket:  # ищем ключ в корзине
            if k == key:  # если нашли
                return v  # возвращаем значение
        
        raise KeyError(f"Key '{key}' not found")  # ключ не найден
    
    def delete(self, key):
        index = self._hash(key)  # получаем индекс
        bucket = self.table[index]  # получаем корзину
        
        for i, (k, v) in enumerate(bucket):  # ищем ключ
            if k == key:  # если нашли
                del bucket[i]  # удаляем элемент
                return v  # возвращаем удалённое значение
        
        raise KeyError(f"Key '{key}' not found")  # ключ не найден
    
    def display(self):
        for i, bucket in enumerate(self.table):  # проходим по всем корзинам
            print(f"Bucket {i}: {bucket}")  # выводим содержимое корзины

# Пример использования
ht = HashTable(5)  # создаём хеш-таблицу размером 5

# добавляем элементы
ht.put("name", "Алексей")  # добавляем имя
ht.put("age", 25)  # добавляем возраст
ht.put("city", "Москва")  # добавляем город

print(f"Имя: {ht.get('name')}")  # получаем имя
print(f"Возраст: {ht.get('age')}")  # получаем возраст

ht.display()  # показываем содержимое таблицы
```

## 🎯 Практические задачи для алгоритмов:

### 1. 🔄 Как найти цикл в связанном списке?

```python
class ListNode:
    def __init__(self, val=0):
        self.val = val  # значение узла
        self.next = None  # ссылка на следующий узел

def has_cycle(head):
    # алгоритм "черепахи и зайца" (Floyd's cycle detection)
    slow = head  # медленный указатель (черепаха)
    fast = head  # быстрый указатель (заяц)
    
    while fast and fast.next:  # пока быстрый указатель не дошёл до конца
        slow = slow.next  # черепаха делает один шаг
        fast = fast.next.next  # заяц делает два шага
        
        if slow == fast:  # если указатели встретились
            return True  # есть цикл
    
    return False  # цикла нет

# Пример использования
node1 = ListNode(1)  # создаём узел 1
node2 = ListNode(2)  # создаём узел 2  
node3 = ListNode(3)  # создаём узел 3
node4 = ListNode(4)  # создаём узел 4

node1.next = node2  # 1 -> 2
node2.next = node3  # 2 -> 3
node3.next = node4  # 3 -> 4
node4.next = node2  # 4 -> 2 (создаём цикл)

print(f"Есть ли цикл? {has_cycle(node1)}")  # проверяем цикл
```

### 2. 🔁 Как развернуть строку?

```python
def reverse_string_methods(s):
    # разные способы развернуть строку
    methods = {
        "срез": s[::-1],  # самый питоновский способ
        "reversed": ''.join(reversed(s)),  # используем built-in функцию
        "цикл": ''.join(s[i] for i in range(len(s)-1, -1, -1)),  # через цикл
    }
    return methods

def reverse_string_inplace(s_list):
    # разворот списка символов на месте
    left = 0  # левый указатель
    right = len(s_list) - 1  # правый указатель
    
    while left < right:  # пока указатели не встретились
        s_list[left], s_list[right] = s_list[right], s_list[left]  # меняем местами
        left += 1  # сдвигаем левый указатель
        right -= 1  # сдвигаем правый указатель
    
    return s_list  # возвращаем изменённый список

# Пример использования
original = "Python"  # исходная строка
methods = reverse_string_methods(original)  # разные способы

for method, result in methods.items():  # выводим все способы
    print(f"{method}: {result}")  # показываем результат

# Разворот на месте
chars = list("Hello")  # преобразуем в список символов
reversed_chars = reverse_string_inplace(chars)  # разворачиваем
print(f"На месте: {''.join(reversed_chars)}")  # выводим результат
```

---

# 🐍 Часть 4: Python углублённо

## 📊 1. Типы данных в деталях

### 🔢 Численные типы и их подводные камни

```python
# int - целые числа произвольной длины
big_number = 2**1000  # Python справляется с любыми числами
print(f"Огромное число: {big_number}")  # выводим результат

# float - числа с плавающей точкой (64-битные)
price = 0.1 + 0.2  # классическая проблема с плавающей точкой
print(f"0.1 + 0.2 = {price}")  # получим 0.30000000000000004
print(f"Равно ли 0.3? {price == 0.3}")  # False!

# Правильное сравнение float
import math
def float_equal(a, b, tolerance=1e-9):
    return abs(a - b) < tolerance  # сравниваем с допуском

print(f"Правильное сравнение: {float_equal(price, 0.3)}")  # True

# Decimal для точных вычислений
from decimal import Decimal, getcontext
getcontext().prec = 50  # устанавливаем точность в 50 знаков

decimal_price = Decimal('0.1') + Decimal('0.2')  # точные вычисления
print(f"Decimal: {decimal_price}")  # получим точно 0.3
print(f"Равно ли 0.3? {decimal_price == Decimal('0.3')}")  # True!

# Fraction для рациональных чисел
from fractions import Fraction
frac1 = Fraction(1, 3)  # одна треть
frac2 = Fraction(2, 3)  # две трети  
result = frac1 + frac2  # сложение дробей
print(f"1/3 + 2/3 = {result}")  # получим 1/1 = 1

# complex - комплексные числа
complex_num = 3 + 4j  # комплексное число
print(f"Модуль комплексного числа: {abs(complex_num)}")  # |3+4j| = 5.0
print(f"Действительная часть: {complex_num.real}")  # 3.0
print(f"Мнимая часть: {complex_num.imag}")  # 4.0
```

### 🔤 Строки и их магия

```python
# Создание строк разными способами
single_quotes = 'Одинарные кавычки'  # одинарные кавычки
double_quotes = "Двойные кавычки"  # двойные кавычки
triple_quotes = """Многострочная
строка с переносами"""  # тройные кавычки для многострочных

# Raw строки - игнорируют экранирование
raw_string = r"C:\new\folder\text.txt"  # не интерпретирует \n как перенос строки
regular_string = "C:\\new\\folder\\text.txt"  # нужно экранировать слеши
print(f"Raw: {raw_string}")  # выводим raw строку
print(f"Regular: {regular_string}")  # выводим обычную строку

# f-строки - форматирование (Python 3.6+)
name = "Алексей"  # имя пользователя
age = 25  # возраст пользователя
balance = 1234.5678  # баланс счёта

formatted = f"Привет, {name}! Тебе {age} лет, баланс: {balance:.2f}₽"  # форматируем
print(formatted)  # выводим отформатированную строку

# Продвинутое форматирование в f-строках
import datetime
now = datetime.datetime.now()  # текущее время
print(f"Сейчас: {now:%Y-%m-%d %H:%M:%S}")  # форматируем дату

# Вычисления внутри f-строк
numbers = [1, 2, 3, 4, 5]  # список чисел
print(f"Сумма: {sum(numbers)}, Среднее: {sum(numbers)/len(numbers):.2f}")  # вычисляем внутри

# Методы строк
text = "  Python Programming  "  # строка с пробелами
print(f"Исходная: '{text}'")  # выводим исходную
print(f"Очищенная: '{text.strip()}'")  # убираем пробелы по краям
print(f"В верхнем регистре: '{text.upper()}'")  # переводим в верхний регистр
print(f"Заменённая: '{text.replace('Python', 'Java')}'")  # заменяем подстроку

# Проверки строк
email = "user@example.com"  # email адрес
print(f"Содержит @: {email.__contains__('@')}")  # проверяем наличие символа
print(f"Начинается с 'user': {email.startswith('user')}")  # проверяем начало
print(f"Заканчивается на '.com': {email.endswith('.com')}")  # проверяем конец
print(f"Только буквы и цифры: {email.replace('@', '').replace('.', '').isalnum()}")  # проверяем символы
```

## 📋 2. Структуры данных подробно

### 📚 Списки (list) - изменяемые последовательности

```python
# Создание списков разными способами
empty_list = []  # пустой список
numbers_list = [1, 2, 3, 4, 5]  # список чисел
mixed_list = [1, "строка", 3.14, True, None]  # смешанный список
range_list = list(range(10))  # список из range(0, 9)
comprehension_list = [x**2 for x in range(5)]  # список через list comprehension

print(f"Список квадратов: {comprehension_list}")  # выводим квадраты

# Операции со списками
fruits = ["яблоко", "банан", "апельсин"]  # список фруктов

fruits.append("груша")  # добавляем в конец - O(1)
print(f"После append: {fruits}")  # выводим список

fruits.insert(1, "киви")  # вставляем на позицию 1 - O(n)
print(f"После insert: {fruits}")  # выводим список

fruits.extend(["манго", "ананас"])  # добавляем несколько элементов - O(k)
print(f"После extend: {fruits}")  # выводим список

# Удаление элементов
removed_fruit = fruits.pop()  # удаляем последний элемент - O(1)
print(f"Удалили: {removed_fruit}, осталось: {fruits}")  # выводим результат

fruits.remove("банан")  # удаляем по значению - O(n)
print(f"После remove: {fruits}")  # выводим список

# Срезы (slicing)
numbers = list(range(10))  # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(f"Все числа: {numbers}")  # выводим все
print(f"Первые 5: {numbers[:5]}")  # первые 5 элементов
print(f"Последние 3: {numbers[-3:]}")  # последние 3 элемента
print(f"Каждый второй: {numbers[::2]}")  # каждый второй элемент
print(f"В обратном порядке: {numbers[::-1]}")  # весь список наоборот

# Копирование списков - ВАЖНО!
original = [1, [2, 3], 4]  # список с вложенным списком
shallow_copy = original.copy()  # поверхностная копия
deep_copy = __import__('copy').deepcopy(original)  # глубокая копия

original[1].append(5)  # изменяем вложенный список в оригинале
print(f"Оригинал: {original}")  # [1, [2, 3, 5], 4]
print(f"Поверхностная копия: {shallow_copy}")  # [1, [2, 3, 5], 4] - тоже изменилась!
print(f"Глубокая копия: {deep_copy}")  # [1, [2, 3], 4] - не изменилась
```

### 🔐 Кортежи (tuple) - неизменяемые последовательности

```python
# Создание кортежей
empty_tuple = ()  # пустой кортеж
single_tuple = (42,)  # кортеж с одним элементом - ЗАПЯТАЯ ОБЯЗАТЕЛЬНА!
coordinates = (10, 20)  # координаты точки
person = ("Иван", 30, "Программист")  # информация о человеке

print(f"Один элемент: {single_tuple}")  # выводим кортеж с одним элементом
print(f"Тип: {type(single_tuple)}")  # проверяем тип

# Распаковка кортежей
name, age, profession = person  # распаковываем в переменные
print(f"Имя: {name}, Возраст: {age}, Профессия: {profession}")  # выводим

# Обмен значений через кортежи
a, b = 10, 20  # присваиваем значения
print(f"До обмена: a={a}, b={b}")  # выводим до
a, b = b, a  # обмениваем значения через кортеж
print(f"После обмена: a={a}, b={b}")  # выводим после

# Функции, возвращающие несколько значений
def get_user_info():
    return "user123", "user@mail.com", 25  # возвращаем кортеж

user_id, email, user_age = get_user_info()  # распаковываем результат
print(f"ID: {user_id}, Email: {email}, Возраст: {user_age}")  # выводим данные

# namedtuple - именованные кортежи
from collections import namedtuple

# Создаём класс именованного кортежа
Point = namedtuple('Point', ['x', 'y'])  # точка с координатами x, y
Person = namedtuple('Person', ['name', 'age', 'city'])  # человек

# Используем именованные кортежи
point = Point(10, 20)  # создаём точку
person = Person("Анна", 28, "СПб")  # создаём человека

print(f"Точка: x={point.x}, y={point.y}")  # обращаемся по именам полей
print(f"Человек: {person.name} из {person.city}, возраст {person.age}")  # выводим данные

# Методы namedtuple
print(f"Как словарь: {person._asdict()}")  # преобразуем в словарь
new_person = person._replace(age=29)  # создаём копию с изменённым полем
print(f"Новый возраст: {new_person.age}")  # выводим новый возраст
```

### 📖 Словари (dict) - хеш-таблицы

```python
# Создание словарей разными способами
empty_dict = {}  # пустой словарь
simple_dict = {"name": "Иван", "age": 30}  # обычный словарь
dict_constructor = dict(name="Петр", age=25)  # через конструктор dict()
from_keys = dict.fromkeys(['a', 'b', 'c'], 0)  # создаём ключи со значением по умолчанию
comprehension_dict = {x: x**2 for x in range(5)}  # через dict comprehension

print(f"Из ключей: {from_keys}")  # выводим словарь из ключей
print(f"Квадраты: {comprehension_dict}")  # выводим словарь квадратов

# Операции со словарями
user = {"name": "Алексей", "email": "alex@mail.com"}  # информация о пользователе

# Разные способы получения значений
name1 = user["name"]  # прямое обращение - может вызвать KeyError
name2 = user.get("name")  # безопасное получение - возвращает None если ключа нет
name3 = user.get("surname", "Неизвестно")  # с значением по умолчанию

print(f"Имя (прямое): {name1}")  # выводим имя
print(f"Имя (get): {name2}")  # выводим имя
print(f"Фамилия (с default): {name3}")  # выводим фамилию или default

# Обновление словарей
user.update({"age": 25, "city": "Москва"})  # добавляем новые ключи
print(f"После update: {user}")  # выводим обновлённый словарь

# Объединение словарей (Python 3.9+)
additional_info = {"profession": "Разработчик", "experience": 3}  # дополнительная инфа
merged = user | additional_info  # объединяем словари
print(f"Объединённый: {merged}")  # выводим результат

# Итерация по словарям
for key in user.keys():  # итерация по ключам
    print(f"Ключ: {key}")  # выводим ключ

for value in user.values():  # итерация по значениям
    print(f"Значение: {value}")  # выводим значение

for key, value in user.items():  # итерация по парам ключ-значение
    print(f"{key}: {value}")  # выводим пару

# defaultdict - словарь с значениями по умолчанию
from collections import defaultdict

# Группировка элементов
words = ["apple", "banana", "apricot", "blueberry", "cherry"]  # список слов
grouped = defaultdict(list)  # словарь со списками по умолчанию

for word in words:  # проходим по словам
    first_letter = word[0]  # получаем первую букву
    grouped[first_letter].append(word)  # добавляем в группу по первой букве

print(f"Группировка по первой букве: {dict(grouped)}")  # выводим группировку

# Counter - подсчёт элементов
from collections import Counter

text = "hello world"  # текст для анализа
char_count = Counter(text)  # считаем символы
print(f"Частота символов: {char_count}")  # выводим частоту
print(f"Самые частые 3: {char_count.most_common(3)}")  # топ-3 символа
```

### 🎯 Множества (set) - уникальные элементы

```python
# Создание множеств
empty_set = set()  # пустое множество (НЕ {}, это словарь!)
numbers_set = {1, 2, 3, 4, 5}  # множество чисел
from_list = set([1, 2, 2, 3, 3, 4])  # из списка - дубликаты удалятся
comprehension_set = {x**2 for x in range(5)}  # через set comprehension

print(f"Из списка: {from_list}")  # {1, 2, 3, 4} - дубликаты исчезли
print(f"Квадраты: {comprehension_set}")  # выводим множество квадратов

# Операции с множествами
set_a = {1, 2, 3, 4, 5}  # первое множество
set_b = {4, 5, 6, 7, 8}  # второе множество

print(f"Объединение (|): {set_a | set_b}")  # объединение множеств
print(f"Пересечение (&): {set_a & set_b}")  # пересечение множеств
print(f"Разность (-): {set_a - set_b}")  # разность множеств
print(f"Симметричная разность (^): {set_a ^ set_b}")  # элементы из одного множества

# Проверки принадлежности
print(f"3 в set_a: {3 in set_a}")  # проверяем принадлежность - O(1)
print(f"Подмножество: {{1, 2}} <= set_a: {{1, 2}} <= set_a")  # проверка подмножества

# Методы множеств
fruits = {"яблоко", "банан", "апельсин"}  # множество фруктов

fruits.add("груша")  # добавляем элемент
print(f"После add: {fruits}")  # выводим множество

fruits.update(["киви", "манго"])  # добавляем несколько элементов
print(f"После update: {fruits}")  # выводим множество

fruits.discard("банан")  # удаляем элемент (не ошибка если нет)
print(f"После discard: {fruits}")  # выводим множество

# frozenset - неизменяемое множество
frozen = frozenset([1, 2, 3, 4])  # создаём неизменяемое множество
print(f"Неизменяемое множество: {frozen}")  # выводим
print(f"Можно использовать как ключ словаря: {frozen}")  # можно использовать в словарях

# Практическое применение - удаление дубликатов
data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]  # данные с дубликатами
unique_data = list(set(data))  # удаляем дубликаты через множество
print(f"Уникальные элементы: {unique_data}")  # выводим уникальные

# Быстрая проверка пересечений
list1 = [1, 2, 3, 4, 5]  # первый список
list2 = [4, 5, 6, 7, 8]  # второй список
has_common = bool(set(list1) & set(list2))  # есть ли общие элементы?
print(f"Есть общие элементы: {has_common}")  # выводим результат
```

## 🏛️ 3. ООП в Python - глубокое погружение

### 🎭 Классы и объекты

```python
class Person:
    # Атрибут класса - общий для всех экземпляров
    species = "Homo sapiens"  # вид человека
    population = 0  # счётчик популяции
    
    def __init__(self, name, age, email=None):
        # Атрибуты экземпляра - уникальны для каждого объекта
        self.name = name  # имя человека
        self.age = age  # возраст человека
        self.email = email  # email адрес (необязательный)
        self._password = None  # "защищённый" атрибут
        self.__id = id(self)  # "приватный" атрибут
        
        # Увеличиваем счётчик популяции
        Person.population += 1  # увеличиваем общий счётчик
    
    def introduce(self):
        # Метод экземпляра
        return f"Привет! Меня зовут {self.name}, мне {self.age} лет"  # представляемся
    
    def set_password(self, password):
        # Простейшая "защита" пароля
        if len(password) < 6:  # проверяем длину пароля
            raise ValueError("Пароль должен быть не менее 6 символов")  # ошибка
        self._password = password  # сохраняем пароль
    
    def check_password(self, password):
        # Проверка пароля
        return self._password == password  # сравниваем пароли
    
    @classmethod
    def get_population(cls):
        # Метод класса - работает с атрибутами класса
        return f"Популяция: {cls.population} человек"  # возвращаем популяцию
    
    @staticmethod
    def is_adult(age):
        # Статический метод - не зависит от класса или экземпляра
        return age >= 18  # проверяем совершеннолетие
    
    def __str__(self):
        # Строковое представление объекта
        return f"Person(name='{self.name}', age={self.age})"  # человекочитаемый вид
    
    def __repr__(self):
        # "Официальное" представление объекта
        return f"Person('{self.name}', {self.age}, '{self.email}')"  # для отладки
    
    def __eq__(self, other):
        # Сравнение объектов на равенство
        if not isinstance(other, Person):  # проверяем тип
            return False  # не Person
        return self.name == other.name and self.age == other.age  # сравниваем поля

# Использование класса
person1 = Person("Алексей", 25, "alex@mail.com")  # создаём человека
person2 = Person("Мария", 30)  # создаём без email

print(person1.introduce())  # человек представляется
print(f"Популяция: {Person.get_population()}")  # выводим популяцию

person1.set_password("secret123")  # устанавливаем пароль
print(f"Пароль правильный: {person1.check_password('secret123')}")  # проверяем пароль

print(f"Алексей совершеннолетний: {Person.is_adult(person1.age)}")  # статический метод
print(f"Объекты равны: {person1 == person2}")  # сравниваем объекты
```

### 🧬 Наследование и полиморфизм

```python
# Базовый класс
class Animal:
    def __init__(self, name, age):
        self.name = name  # имя животного
        self.age = age  # возраст животного
    
    def make_sound(self):
        # Метод, который будут переопределять наследники
        raise NotImplementedError("Подклассы должны реализовать этот метод")  # абстрактный метод
    
    def sleep(self):
        # Общий метод для всех животных
        return f"{self.name} спит"  # животное спит
    
    def __str__(self):
        return f"{self.__class__.__name__}('{self.name}', {self.age})"  # строковое представление

# Наследники
class Dog(Animal):
    def __init__(self, name, age, breed):
        super().__init__(name, age)  # вызываем конструктор родителя
        self.breed = breed  # порода собаки
    
    def make_sound(self):
        # Переопределяем метод родителя
        return f"{self.name} гавкает: Гав-гав!"  # собака лает
    
    def fetch(self):
        # Уникальный метод для собак
        return f"{self.name} приносит палку"  # собака приносит палку

class Cat(Animal):
    def __init__(self, name, age, indoor=True):
        super().__init__(name, age)  # вызываем конструктор родителя  
        self.indoor = indoor  # домашняя или уличная
    
    def make_sound(self):
        # Переопределяем метод родителя
        return f"{self.name} мяукает: Мяу!"  # кот мяукает
    
    def purr(self):
        # Уникальный метод для котов
        return f"{self.name} мурчит"  # кот мурчит

# Полиморфизм в действии
def animal_concert(animals):
    # Функция, работающая с любыми животными
    for animal in animals:  # проходим по животным
        print(animal.make_sound())  # каждое животное издаёт свой звук
        print(animal.sleep())  # все спят одинаково

# Создаём животных
dog = Dog("Бобик", 3, "Лабрадор")  # создаём собаку
cat = Cat("Мурка", 2, indoor=True)  # создаём кота

animals = [dog, cat]  # список животных

print("🎵 Концерт животных:")  # заголовок концерта
animal_concert(animals)  # запускаем концерт

# Проверки типов
print(f"\nПроверки типов:")  # заголовок
print(f"dog это Animal: {isinstance(dog, Animal)}")  # True
print(f"dog это Dog: {isinstance(dog, Dog)}")  # True  
print(f"dog это Cat: {isinstance(dog, Cat)}")  # False
print(f"Dog наследник Animal: {issubclass(Dog, Animal)}")  # True
```

### 🎪 Магические методы (dunder methods)

```python
class Money:
    def __init__(self, amount, currency="RUB"):
        self.amount = amount  # сумма денег
        self.currency = currency  # валюта
    
    def __str__(self):
        # Человекочитаемое представление
        return f"{self.amount} {self.currency}"  # например "100 RUB"
    
    def __repr__(self):
        # Представление для разработчиков
        return f"Money({self.amount}, '{self.currency}')"  # для отладки
    
    def __add__(self, other):
        # Сложение денег
        if isinstance(other, Money):  # если другой объект тоже Money
            if self.currency != other.currency:  # разные валюты
                raise ValueError("Нельзя складывать разные валюты")  # ошибка
            return Money(self.amount + other.amount, self.currency)  # складываем суммы
        elif isinstance(other, (int, float)):  # если число
            return Money(self.amount + other, self.currency)  # добавляем к сумме
        return NotImplemented  # не поддерживаем другие типы
    
    def __radd__(self, other):
        # Обратное сложение (когда число + Money)
        return self.__add__(other)  # используем обычное сложение
    
    def __sub__(self, other):
        # Вычитание денег
        if isinstance(other, Money):  # другой объект Money
            if self.currency != other.currency:  # разные валюты
                raise ValueError("Нельзя вычитать разные валюты")  # ошибка
            return Money(self.amount - other.amount, self.currency)  # вычитаем
        elif isinstance(other, (int, float)):  # если число
            return Money(self.amount - other, self.currency)  # вычитаем из суммы
        return NotImplemented  # не поддерживаем
    
    def __mul__(self, other):
        # Умножение на число
        if isinstance(other, (int, float)):  # если число
            return Money(self.amount * other, self.currency)  # умножаем сумму
        return NotImplemented  # другие типы не поддерживаем
    
    def __truediv__(self, other):
        # Деление на число
        if isinstance(other, (int, float)):  # если число
            if other == 0:  # проверяем деление на ноль
                raise ZeroDivisionError("Деление на ноль!")  # ошибка
            return Money(self.amount / other, self.currency)  # делим сумму
        return NotImplemented  # другие типы не поддерживаем
    
    def __eq__(self, other):
        # Сравнение на равенство
        if isinstance(other, Money):  # если другой объект Money
            return self.amount == other.amount and self.currency == other.currency  # сравниваем
        return False  # не равны
    
    def __lt__(self, other):
        # Меньше чем
        if isinstance(other, Money):  # если другой объект Money
            if self.currency != other.currency:  # разные валюты
                raise ValueError("Нельзя сравнивать разные валюты")  # ошибка
            return self.amount < other.amount  # сравниваем суммы
        return NotImplemented  # не поддерживаем
    
    def __le__(self, other):
        # Меньше или равно
        return self.__lt__(other) or self.__eq__(other)  # используем другие методы
    
    def __bool__(self):
        # Логическое значение (True если есть деньги)
        return self.amount > 0  # True если сумма положительная
    
    def __len__(self):
        # "Длина" - количество цифр в сумме
        return len(str(int(abs(self.amount))))  # количество цифр
    
    def __getitem__(self, key):
        # Доступ по индексу (для примера - цифры суммы)
        digits = str(int(abs(self.amount)))  # получаем цифры
        return int(digits[key])  # возвращаем цифру по индексу

# Использование магических методов
wallet1 = Money(1000, "RUB")  # кошелёк 1
wallet2 = Money(500, "RUB")  # кошелёк 2
wallet3 = Money(200, "USD")  # кошелёк в долларах

print(f"Кошелёк 1: {wallet1}")  # используем __str__
print(f"Представление: {repr(wallet2)}")  # используем __repr__

# Арифметические операции
total = wallet1 + wallet2  # используем __add__
print(f"Сумма кошельков: {total}")  # выводим результат

doubled = wallet1 * 2  # используем __mul__
print(f"Удвоенная сумма: {doubled}")  # выводим результат

half = wallet1 / 2  # используем __truediv__
print(f"Половина суммы: {half}")  # выводим результат

# Сравнения
print(f"wallet1 > wallet2: {wallet1 > wallet2}")  # используем __lt__ (обратное)
print(f"wallet1 == Money(1000): {wallet1 == Money(1000)}")  # используем __eq__

# Логические операции
empty_wallet = Money(0)  # пустой кошелёк
print(f"Есть ли деньги в wallet1: {bool(wallet1)}")  # используем __bool__
print(f"Есть ли деньги в пустом: {bool(empty_wallet)}")  # False

# "Длина" и индексация
print(f"Количество цифр в сумме: {len(wallet1)}")  # используем __len__
print(f"Первая цифра суммы: {wallet1[0]}")  # используем __getitem__

# Попытка сложить разные валюты
try:
    invalid_sum = wallet1 + wallet3  # разные валюты
except ValueError as e:
    print(f"Ошибка: {e}")  # выводим ошибку
```

## 🎨 4. Декораторы - мощь Python

### 🎭 Простые декораторы

```python
import time
import functools
from typing import Callable, Any

# Простой декоратор для измерения времени выполнения
def timing_decorator(func: Callable) -> Callable:
    """Декоратор для измерения времени выполнения функции"""
    @functools.wraps(func)  # сохраняем метаданные исходной функции
    def wrapper(*args, **kwargs) -> Any:
        start_time = time.time()  # запоминаем время начала
        result = func(*args, **kwargs)  # выполняем функцию
        end_time = time.time()  # запоминаем время окончания
        
        execution_time = end_time - start_time  # вычисляем время выполнения
        print(f"🕒 Функция {func.__name__} выполнилась за {execution_time:.4f} секунд")  # выводим время
        
        return result  # возвращаем результат функции
    return wrapper  # возвращаем обёрнутую функцию

# Декоратор для логирования
def log_calls(func: Callable) -> Callable:
    """Декоратор для логирования вызовов функций"""
    @functools.wraps(func)  # сохраняем метаданные
    def wrapper(*args, **kwargs) -> Any:
        args_str = ", ".join([str(arg) for arg in args])  # форматируем аргументы
        kwargs_str = ", ".join([f"{k}={v}" for k, v in kwargs.items()])  # форматируем kwargs
        all_args = ", ".join(filter(None, [args_str, kwargs_str]))  # объединяем все аргументы
        
        print(f"📞 Вызов {func.__name__}({all_args})")  # логируем вызов
        
        try:
            result = func(*args, **kwargs)  # выполняем функцию
            print(f"✅ {func.__name__} вернул: {result}")  # логируем результат
            return result  # возвращаем результат
        except Exception as e:
            print(f"❌ {func.__name__} вызвал ошибку: {e}")  # логируем ошибку
            raise  # пробрасываем ошибку дальше
    
    return wrapper  # возвращаем обёрнутую функцию

# Применение декораторов
@timing_decorator  # применяем декоратор времени
@log_calls  # применяем декоратор логирования
def slow_function(n: int) -> int:
    """Медленная функция для демонстрации декораторов"""
    time.sleep(0.1)  # имитируем медленную работу
    return sum(range(n))  # вычисляем сумму чисел от 0 до n-1

# Использование
result = slow_function(1000)  # вызываем функцию
print(f"Результат: {result}")  # выводим результат
```

### 🏭 Декораторы с параметрами

```python
def retry(max_attempts: int = 3, delay: float = 1.0, exceptions: tuple = (Exception,)):
    """
    Декоратор для повторных попыток выполнения функции при ошибках
    
    Args:
        max_attempts: Максимальное количество попыток
        delay: Задержка между попытками в секундах
        exceptions: Кортеж исключений, при которых делать повтор
    """
    def decorator(func: Callable) -> Callable:
        @functools.wraps(func)  # сохраняем метаданные
        def wrapper(*args, **kwargs) -> Any:
            last_exception = None  # сохраняем последнюю ошибку
            
            for attempt in range(max_attempts):  # делаем попытки
                try:
                    result = func(*args, **kwargs)  # пытаемся выполнить функцию
                    if attempt > 0:  # если это не первая попытка
                        print(f"✅ Функция {func.__name__} выполнилась с {attempt + 1} попытки")  # успех
                    return result  # возвращаем результат
                    
                except exceptions as e:
                    last_exception = e  # сохраняем ошибку
                    if attempt < max_attempts - 1:  # если это не последняя попытка
                        print(f"⚠️  Попытка {attempt + 1} неудачна: {e}. Повтор через {delay}с...")  # логируем
                        time.sleep(delay)  # ждём перед следующей попыткой
                    else:
                        print(f"❌ Все {max_attempts} попыток исчерпаны")  # все попытки неудачны
            
            raise last_exception  # поднимаем последнюю ошибку
        
        return wrapper  # возвращаем обёрнутую функцию
    return decorator  # возвращаем декоратор

def rate_limit(calls_per_second: float = 1.0):
    """
    Декоратор для ограничения частоты вызовов функции
    
    Args:
        calls_per_second: Максимальное количество вызовов в секунду
    """
    min_interval = 1.0 / calls_per_second  # минимальный интервал между вызовами
    
    def decorator(func: Callable) -> Callable:
        last_called = 0.0  # время последнего вызова
        
        @functools.wraps(func)  # сохраняем метаданные
        def wrapper(*args, **kwargs) -> Any:
            nonlocal last_called  # используем переменную из внешней области
            
            now = time.time()  # текущее время
            time_since_last = now - last_called  # время с последнего вызова
            
            if time_since_last < min_interval:  # если прошло мало времени
                sleep_time = min_interval - time_since_last  # сколько нужно подождать
                print(f"⏳ Ожидание {sleep_time:.2f}с перед вызовом {func.__name__}")  # логируем ожидание
                time.sleep(sleep_time)  # ждём
            
            last_called = time.time()  # обновляем время последнего вызова
            return func(*args, **kwargs)  # выполняем функцию
        
        return wrapper  # возвращаем обёрнутую функцию
    return decorator  # возвращаем декоратор

# Применение декораторов с параметрами
@retry(max_attempts=3, delay=0.5, exceptions=(ValueError, ConnectionError))  # повтор при ошибках
@rate_limit(calls_per_second=2.0)  # не чаще 2 раз в секунду
def unstable_api_call(url: str, fail_probability: float = 0.7) -> str:
    """Нестабильный API вызов для демонстрации декораторов"""
    import random
    
    if random.random() < fail_probability:  # имитируем ошибку
        raise ConnectionError(f"Не удалось подключиться к {url}")  # ошибка подключения
    
    return f"Данные из {url}"  # успешный результат

# Использование
try:
    data1 = unstable_api_call("https://api.example.com/users")  # первый вызов
    print(f"Получили: {data1}")  # выводим данные
    
    data2 = unstable_api_call("https://api.example.com/posts")  # второй вызов (с ожиданием)
    print(f"Получили: {data2}")  # выводим данные
    
except Exception as e:
    print(f"Финальная ошибка: {e}")  # если все попытки неудачны
```

### 🏭 Декораторы классов

```python
def add_repr(cls):
    """Декоратор класса для автоматического создания __repr__"""
    def __repr__(self):
        class_name = self.__class__.__name__  # имя класса
        attrs = []  # список атрибутов
        
        for key, value in self.__dict__.items():  # проходим по атрибутам экземпляра
            if not key.startswith('_'):  # игнорируем приватные атрибуты
                attrs.append(f"{key}={repr(value)}")  # добавляем в список
        
        attrs_str = ", ".join(attrs)  # объединяем атрибуты
        return f"{class_name}({attrs_str})"  # возвращаем представление
    
    cls.__repr__ = __repr__  # добавляем метод к классу
    return cls  # возвращаем модифицированный класс

def singleton(cls):
    """Декоратор для создания синглтона"""
    instances = {}  # словарь для хранения экземпляров
    
    @functools.wraps(cls)  # сохраняем метаданные класса
    def get_instance(*args, **kwargs):
        if cls not in instances:  # если экземпляр ещё не создан
            instances[cls] = cls(*args, **kwargs)  # создаём экземпляр
            print(f"🏭 Создан новый экземпляр {cls.__name__}")  # логируем создание
        else:
            print(f"♻️  Возвращаем существующий экземпляр {cls.__name__}")  # логируем повторное использование
        
        return instances[cls]  # возвращаем экземпляр
    
    return get_instance  # возвращаем функцию-обёртку

# Применение декораторов классов
@add_repr  # автоматический __repr__
class User:
    def __init__(self, name: str, email: str, age: int):
        self.name = name  # имя пользователя
        self.email = email  # email пользователя
        self.age = age  # возраст пользователя

@singleton  # синглтон
class DatabaseConnection:
    def __init__(self, host: str = "localhost", port: int = 5432):
        self.host = host  # хост базы данных
        self.port = port  # порт базы данных
        self.connected = False  # статус подключения
        print(f"🔌 Подключение к базе {host}:{port}")  # логируем подключение
    
    def connect(self):
        self.connected = True  # устанавливаем подключение
        return f"Подключено к {self.host}:{self.port}"  # возвращаем статус

# Использование декорированных классов
user1 = User("Иван", "ivan@mail.com", 30)  # создаём пользователя
print(f"Пользователь: {user1}")  # автоматический __repr__

# Демонстрация синглтона
db1 = DatabaseConnection("localhost", 5432)  # первый экземпляр
db2 = DatabaseConnection("localhost", 5432)  # попытка создать второй

print(f"db1 is db2: {db1 is db2}")  # проверяем, что это один объект
print(f"Статус подключения: {db1.connect()}")  # подключаемся
```

## 🔒 5. Контекстные менеджеры

### 📂 Работа с файлами и ресурсами

```python
import contextlib
import tempfile
import os
import time
from typing import Generator, Any

# Простой контекстный менеджер через класс
class FileManager:
    """Контекстный менеджер для безопасной работы с файлами"""
    
    def __init__(self, filename: str, mode: str = 'r', encoding: str = 'utf-8'):
        self.filename = filename  # имя файла
        self.mode = mode  # режим открытия
        self.encoding = encoding  # кодировка
        self.file = None  # ссылка на файл
    
    def __enter__(self):
        """Вход в контекст - открываем файл"""
        print(f"📂 Открываем файл {self.filename}")  # логируем открытие
        self.file = open(self.filename, self.mode, encoding=self.encoding)  # открываем файл
        return self.file  # возвращаем файловый объект
    
    def __exit__(self, exc_type, exc_value, traceback):
        """Выход из контекста - закрываем файл"""
        if self.file:  # если файл открыт
            print(f"📁 Закрываем файл {self.filename}")  # логируем закрытие
            self.file.close()  # закрываем файл
        
        if exc_type is not None:  # если была ошибка
            print(f"❌ Ошибка при работе с файлом: {exc_value}")  # логируем ошибку
            return False  # не подавляем ошибку
        
        return True  # всё прошло успешно

# Контекстный менеджер через генератор
@contextlib.contextmanager
def timer_context(operation_name: str) -> Generator[dict, None, None]:
    """Контекстный менеджер для измерения времени выполнения"""
    start_time = time.time()  # запоминаем время начала
    stats = {'start_time': start_time}  # словарь со статистикой
    
    print(f"⏱️  Начинаем операцию: {operation_name}")  # логируем начало
    
    try:
        yield stats  # передаём статистику в блок with
    except Exception as e:
        print(f"❌ Ошибка в операции {operation_name}: {e}")  # логируем ошибку
        raise  # пробрасываем ошибку дальше
    finally:
        end_time = time.time()  # запоминаем время окончания
        duration = end_time - start_time  # вычисляем продолжительность
        stats['end_time'] = end_time  # сохраняем время окончания
        stats['duration'] = duration  # сохраняем продолжительность
        print(f"✅ Операция {operation_name} завершена за {duration:.4f} секунд")  # логируем завершение

@contextlib.contextmanager
def temp_directory() -> Generator[str, None, None]:
    """Контекстный менеджер для работы с временной директорией"""
    temp_dir = tempfile.mkdtemp()  # создаём временную директорию
    print(f"📁 Создана временная директория: {temp_dir}")  # логируем создание
    
    try:
        yield temp_dir  # передаём путь к директории
    finally:
        # Удаляем временную директорию и все её содержимое
        import shutil
        shutil.rmtree(temp_dir)  # удаляем директорию
        print(f"🗑️  Удалена временная директория: {temp_dir}")  # логируем удаление

# Контекстный менеджер для подавления исключений
@contextlib.contextmanager
def ignore_errors(*exception_types):
    """Контекстный менеджер для игнорирования определённых ошибок"""
    try:
        yield  # выполняем код в блоке with
    except exception_types as e:
        print(f"🔇 Игнорируем ошибку: {type(e).__name__}: {e}")  # логируем игнорирование
        pass  # подавляем ошибку

# Использование контекстных менеджеров

# 1. Работа с файлами
with FileManager('example.txt', 'w') as f:  # создаём файл
    f.write('Привет, мир!\n')  # записываем данные
    f.write('Это тест контекстного менеджера.')  # ещё данные

# 2. Измерение времени
with timer_context("Сложные вычисления") as stats:  # измеряем время
    time.sleep(0.1)  # имитируем работу
    result = sum(range(100000))  # вычисляем сумму
    stats['result'] = result  # сохраняем результат в статистике

# 3. Временная директория
with temp_directory() as temp_dir:  # создаём временную директорию
    temp_file = os.path.join(temp_dir, 'temp_file.txt')  # путь к временному файлу
    with open(temp_file, 'w') as f:  # создаём временный файл
        f.write('Временные данные')  # записываем данные
    
    print(f"Файл создан: {os.path.exists(temp_file)}")  # проверяем существование

# 4. Игнорирование ошибок
with ignore_errors(ZeroDivisionError, ValueError):  # игнорируем определённые ошибки
    result = 10 / 0  # деление на ноль
    print("Этот код не выполнится")  # не выполнится из-за ошибки

print("Программа продолжает работу после игнорирования ошибки")  # продолжаем работу

# 5. Множественные контекстные менеджеры
with timer_context("Файловая операция") as stats, \
     FileManager('output.txt', 'w') as output_file, \
     ignore_errors(FileNotFoundError):  # комбинируем несколько менеджеров
    
    output_file.write(f"Операция началась в {stats['start_time']}\n")  # записываем время
    output_file.write("Какие-то данные для записи\n")  # записываем данные
```

---

Ебать, погнали финал! 🚀 **Часть 5: Продвинутые темы Python** - самое мясо для крутых собесов! 💪

# 🚀 Часть 5: Продвинутые темы Python

## 🔒 1. GIL и многопоточность

### 🧵 Понимание GIL (Global Interpreter Lock)

```python
import threading
import time
import multiprocessing
from concurrent.futures import ThreadPoolExecutor, ProcessPoolExecutor

# CPU-bound задача - страдает от GIL
def cpu_bound_task(n: int) -> int:
    """CPU-интенсивная задача - вычисление суммы квадратов"""
    total = 0  # начальная сумма
    for i in range(n):  # проходим по числам
        total += i * i  # добавляем квадрат числа
    return total  # возвращаем результат

# I/O-bound задача - не страдает от GIL  
def io_bound_task(url: str, delay: float) -> str:
    """I/O задача - имитация сетевого запроса"""
    print(f"🌐 Начинаем запрос к {url}")  # логируем начало
    time.sleep(delay)  # имитируем сетевую задержку
    return f"Ответ от {url}"  # возвращаем результат

def benchmark_threading_vs_multiprocessing():
    """Сравнение threading и multiprocessing для разных типов задач"""
    
    # Тестируем CPU-bound задачи
    print("🧮 CPU-bound задачи:")
    
    # Последовательное выполнение
    start_time = time.time()  # запоминаем время начала
    results = [cpu_bound_task(100000) for _ in range(4)]  # выполняем 4 задачи
    sequential_time = time.time() - start_time  # вычисляем время выполнения
    print(f"Последовательно: {sequential_time:.2f} секунд")  # выводим время
    
    # Threading (плохо для CPU-bound из-за GIL)
    start_time = time.time()  # запоминаем время начала
    with ThreadPoolExecutor(max_workers=4) as executor:  # создаём пул потоков
        futures = [executor.submit(cpu_bound_task, 100000) for _ in range(4)]  # запускаем задачи
        results = [future.result() for future in futures]  # получаем результаты
    threading_time = time.time() - start_time  # вычисляем время
    print(f"Threading: {threading_time:.2f} секунд (медленнее из-за GIL!)")  # выводим время
    
    # Multiprocessing (хорошо для CPU-bound)
    start_time = time.time()  # запоминаем время начала
    with ProcessPoolExecutor(max_workers=4) as executor:  # создаём пул процессов
        futures = [executor.submit(cpu_bound_task, 100000) for _ in range(4)]  # запускаем задачи
        results = [future.result() for future in futures]  # получаем результаты
    multiprocessing_time = time.time() - start_time  # вычисляем время
    print(f"Multiprocessing: {multiprocessing_time:.2f} секунд (быстрее!)")  # выводим время
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    # Тестируем I/O-bound задачи
    print("💾 I/O-bound задачи:")
    
    urls = [f"https://api{i}.example.com" for i in range(4)]  # список URL'ов
    
    # Последовательное выполнение I/O
    start_time = time.time()  # запоминаем время начала
    results = [io_bound_task(url, 0.5) for url in urls]  # выполняем задачи
    sequential_io_time = time.time() - start_time  # вычисляем время
    print(f"Последовательно I/O: {sequential_io_time:.2f} секунд")  # выводим время
    
    # Threading (хорошо для I/O-bound)
    start_time = time.time()  # запоминаем время начала
    with ThreadPoolExecutor(max_workers=4) as executor:  # создаём пул потоков
        futures = [executor.submit(io_bound_task, url, 0.5) for url in urls]  # запускаем задачи
        results = [future.result() for future in futures]  # получаем результаты
    threading_io_time = time.time() - start_time  # вычисляем время
    print(f"Threading I/O: {threading_io_time:.2f} секунд (быстрее!)")  # выводим время

# Демонстрация проблем с разделяемыми ресурсами
class UnsafeCounter:
    """Небезопасный счётчик без синхронизации"""
    def __init__(self):
        self.value = 0  # начальное значение
    
    def increment(self):
        """Увеличиваем счётчик на 1"""
        current = self.value  # читаем текущее значение
        time.sleep(0.0001)  # имитируем некоторую работу
        self.value = current + 1  # записываем новое значение

class SafeCounter:
    """Безопасный счётчик с блокировкой"""
    def __init__(self):
        self.value = 0  # начальное значение
        self._lock = threading.Lock()  # блокировка для синхронизации
    
    def increment(self):
        """Увеличиваем счётчик на 1 безопасно"""
        with self._lock:  # блокируем доступ других потоков
            current = self.value  # читаем текущее значение
            time.sleep(0.0001)  # имитируем некоторую работу
            self.value = current + 1  # записываем новое значение

def test_thread_safety():
    """Тестируем потокобезопасность"""
    
    # Тест небезопасного счётчика
    unsafe_counter = UnsafeCounter()  # создаём небезопасный счётчик
    threads = []  # список потоков
    
    for i in range(10):  # создаём 10 потоков
        thread = threading.Thread(target=unsafe_counter.increment)  # создаём поток
        threads.append(thread)  # добавляем в список
        thread.start()  # запускаем поток
    
    for thread in threads:  # ждём завершения всех потоков
        thread.join()  # ждём завершения потока
    
    print(f"Небезопасный счётчик: {unsafe_counter.value} (должно быть 10)")  # выводим результат
    
    # Тест безопасного счётчика
    safe_counter = SafeCounter()  # создаём безопасный счётчик
    threads = []  # список потоков
    
    for i in range(10):  # создаём 10 потоков
        thread = threading.Thread(target=safe_counter.increment)  # создаём поток
        threads.append(thread)  # добавляем в список
        thread.start()  # запускаем поток
    
    for thread in threads:  # ждём завершения всех потоков
        thread.join()  # ждём завершения потока
    
    print(f"Безопасный счётчик: {safe_counter.value} (должно быть 10)")  # выводим результат

# Запускаем демонстрации
if __name__ == "__main__":
    print("🔬 Тестируем GIL и многопоточность:")
    benchmark_threading_vs_multiprocessing()  # сравниваем подходы
    
    print("\n🔒 Тестируем потокобезопасность:")
    test_thread_safety()  # тестируем синхронизацию
```

## ⚡ 2. Асинхронное программирование (async/await)

### 🌊 Основы asyncio

```python
import asyncio
import aiohttp
import aiofiles
import time
from typing import List, Coroutine, Any

# Простая асинхронная функция
async def simple_async_function(name: str, delay: float) -> str:
    """Простая асинхронная функция с задержкой"""
    print(f"🚀 Начинаем задачу {name}")  # логируем начало
    await asyncio.sleep(delay)  # асинхронная задержка (не блокирует другие задачи)
    print(f"✅ Завершили задачу {name}")  # логируем завершение
    return f"Результат от {name}"  # возвращаем результат

# Асинхронный HTTP клиент
async def fetch_url(session: aiohttp.ClientSession, url: str) -> dict:
    """Асинхронный HTTP запрос"""
    try:
        print(f"🌐 Запрос к {url}")  # логируем запрос
        async with session.get(url) as response:  # делаем GET запрос
            data = await response.text()  # читаем тело ответа
            return {
                'url': url,  # URL запроса
                'status': response.status,  # статус ответ
                'length': len(data)  # длина ответа
            }
    except Exception as e:
        return {'url': url, 'error': str(e)}  # возвращаем ошибку

# Асинхронная работа с файлами
async def async_file_operations() -> None:
    """Демонстрация асинхронной работы с файлами"""
    filename = "async_test.txt"  # имя файла
    
    # Асинхронная запись в файл
    async with aiofiles.open(filename, 'w', encoding='utf-8') as f:
        await f.write("Привет из асинхронного мира!\n")  # записываем данные
        await f.write("Это вторая строка.\n")  # ещё данные
        print(f"📝 Записали данные в {filename}")  # логируем запись
    
    # Асинхронное чтение файла
    async with aiofiles.open(filename, 'r', encoding='utf-8') as f:
        content = await f.read()  # читаем содержимое
        print(f"📖 Прочитали из {filename}:")  # логируем чтение
        print(content)  # выводим содержимое

# Продюсер-консюмер паттерн с asyncio.Queue
async def producer(queue: asyncio.Queue, name: str, items: int) -> None:
    """Асинхронный продюсер"""
    for i in range(items):  # создаём элементы
        item = f"{name}-item-{i}"  # формируем элемент
        await queue.put(item)  # кладём в очередь
        print(f"🏭 Продюсер {name} создал {item}")  # логируем создание
        await asyncio.sleep(0.1)  # небольшая задержка
    
    await queue.put(None)  # сигнал о завершении
    print(f"🏁 Продюсер {name} закончил работу")  # логируем завершение

async def consumer(queue: asyncio.Queue, name: str) -> int:
    """Асинхронный консюмер"""
    processed = 0  # счётчик обработанных элементов
    
    while True:  # обрабатываем элементы
        item = await queue.get()  # берём элемент из очереди
        
        if item is None:  # сигнал о завершении
            await queue.put(None)  # передаём сигнал дальше
            break  # выходим из цикла
        
        print(f"🔧 Консюмер {name} обрабатывает {item}")  # логируем обработку
        await asyncio.sleep(0.2)  # имитируем обработку
        processed += 1  # увеличиваем счётчик
        queue.task_done()  # помечаем задачу как выполненную
    
    print(f"✅ Консюмер {name} обработал {processed} элементов")  # логируем итоги
    return processed  # возвращаем количество

# Главная асинхронная функция
async def main():
    """Главная функция для демонстрации async/await"""
    
    print("🎯 Демонстрация 1: Параллельное выполнение задач")
    
    # Создаём несколько задач
    tasks = [
        simple_async_function("Task-1", 1.0),  # задача на 1 секунду
        simple_async_function("Task-2", 0.5),  # задача на 0.5 секунды
        simple_async_function("Task-3", 1.5),  # задача на 1.5 секунды
    ]
    
    # Запускаем все задачи параллельно
    start_time = time.time()  # запоминаем время начала
    results = await asyncio.gather(*tasks)  # ждём завершения всех задач
    total_time = time.time() - start_time  # вычисляем общее время
    
    print(f"Результаты: {results}")  # выводим результаты
    print(f"Общее время: {total_time:.2f} секунд (параллельно!)")  # выводим время
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("🎯 Демонстрация 2: Асинхронные HTTP запросы")
    
    # Список URL для тестирования (используем httpbin для тестов)
    urls = [
        "https://httpbin.org/delay/1",  # задержка 1 секунда
        "https://httpbin.org/delay/0.5",  # задержка 0.5 секунды
        "https://httpbin.org/status/200",  # обычный ответ
        "https://httpbin.org/json",  # JSON ответ
    ]
    
    # Асинхронные HTTP запросы
    async with aiohttp.ClientSession() as session:  # создаём сессию
        start_time = time.time()  # запоминаем время начала
        http_tasks = [fetch_url(session, url) for url in urls]  # создаём задачи
        http_results = await asyncio.gather(*http_tasks, return_exceptions=True)  # выполняем запросы
        http_time = time.time() - start_time  # вычисляем время
    
    for result in http_results:  # выводим результаты
        if isinstance(result, dict):  # если результат - словарь
            if 'error' in result:  # если есть ошибка
                print(f"❌ {result['url']}: {result['error']}")  # выводим ошибку
            else:
                print(f"✅ {result['url']}: статус {result['status']}, размер {result['length']}")  # выводим результат
        else:
            print(f"❌ Неожиданная ошибка: {result}")  # выводим неожиданную ошибку
    
    print(f"HTTP запросы выполнены за {http_time:.2f} секунд")  # выводим общее время
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("🎯 Демонстрация 3: Асинхронная работа с файлами")
    await async_file_operations()  # запускаем работу с файлами
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("🎯 Демонстрация 4: Продюсер-консюмер")
    
    # Создаём очередь
    queue = asyncio.Queue(maxsize=5)  # очередь с максимальным размером 5
    
    # Создаём задачи продюсеров и консюмеров
    producer_task = producer(queue, "Alpha", 10)  # продюсер создаст 10 элементов
    consumer_tasks = [
        consumer(queue, "Worker-1"),  # первый консюмер
        consumer(queue, "Worker-2"),  # второй консюмер
    ]
    
    # Запускаем все задачи
    await asyncio.gather(producer_task, *consumer_tasks)  # ждём завершения всех
    
    print("🎉 Все асинхронные демонстрации завершены!")

# Сравнение синхронного и асинхронного кода
def sync_http_requests():
    """Синхронные HTTP запросы для сравнения"""
    import requests
    
    urls = [
        "https://httpbin.org/delay/1",
        "https://httpbin.org/delay/0.5", 
        "https://httpbin.org/status/200",
        "https://httpbin.org/json",
    ]
    
    start_time = time.time()  # запоминаем время начала
    
    results = []  # список результатов
    for url in urls:  # делаем запросы последовательно
        try:
            response = requests.get(url, timeout=5)  # синхронный запрос
            results.append({
                'url': url,  # URL запроса
                'status': response.status_code,  # статус ответа
                'length': len(response.text)  # длина ответа
            })
            print(f"✅ Синхронный запрос к {url} завершён")  # логируем завершение
        except Exception as e:
            results.append({'url': url, 'error': str(e)})  # сохраняем ошибку
    
    sync_time = time.time() - start_time  # вычисляем время
    print(f"Синхронные запросы выполнены за {sync_time:.2f} секунд")  # выводим время
    
    return results  # возвращаем результаты

# Запуск демонстраций
if __name__ == "__main__":
    print("🔥 Сравнение синхронного и асинхронного подходов:")
    
    # Синхронные запросы
    print("\n📡 Синхронные HTTP запросы:")
    sync_results = sync_http_requests()  # выполняем синхронные запросы
    
    # Асинхронные запросы  
    print("\n⚡ Асинхронные задачи:")
    asyncio.run(main())  # запускаем асинхронную главную функцию
```

## 🔄 3. Генераторы и итераторы

### 🎭 Итераторы - основа всего

```python
from typing import Iterator, Generator, Iterable, Any
import sys

# Простой итератор через класс
class CountdownIterator:
    """Итератор для обратного отсчёта"""
    
    def __init__(self, start: int):
        self.start = start  # начальное значение
        self.current = start  # текущее значение
    
    def __iter__(self) -> Iterator[int]:
        """Возвращаем себя как итератор"""
        return self  # возвращаем сам объект
    
    def __next__(self) -> int:
        """Возвращаем следующий элемент"""
        if self.current <= 0:  # если дошли до нуля
            raise StopIteration  # завершаем итерацию
        
        value = self.current  # сохраняем текущее значение
        self.current -= 1  # уменьшаем счётчик
        return value  # возвращаем значение

# Итерируемый класс (отличается от итератора!)
class NumberRange:
    """Итерируемый класс для диапазона чисел"""
    
    def __init__(self, start: int, end: int, step: int = 1):
        self.start = start  # начало диапазона
        self.end = end  # конец диапазона
        self.step = step  # шаг
    
    def __iter__(self) -> Iterator[int]:
        """Возвращаем новый итератор при каждом вызове"""
        return NumberRangeIterator(self.start, self.end, self.step)  # создаём новый итератор

class NumberRangeIterator:
    """Итератор для NumberRange"""
    
    def __init__(self, start: int, end: int, step: int):
        self.current = start  # текущая позиция
        self.end = end  # конец диапазона
        self.step = step  # шаг
    
    def __iter__(self) -> Iterator[int]:
        return self  # возвращаем себя
    
    def __next__(self) -> int:
        if self.current >= self.end:  # если дошли до конца
            raise StopIteration  # завершаем итерацию
        
        value = self.current  # сохраняем текущее значение
        self.current += self.step  # увеличиваем на шаг
        return value  # возвращаем значение

# Демонстрация итераторов
def demonstrate_iterators():
    """Демонстрация работы с итераторами"""
    
    print("🔢 Обратный отсчёт:")
    countdown = CountdownIterator(5)  # создаём итератор обратного отсчёта
    
    for num in countdown:  # итерируемся
        print(f"  {num}")  # выводим число
    
    print("🚀 Пуск!")  # финальное сообщение
    
    print("\n📊 Диапазон чисел:")
    number_range = NumberRange(0, 10, 2)  # чётные числа от 0 до 10
    
    for num in number_range:  # итерируемся
        print(f"  {num}")  # выводим число
    
    # Можем итерироваться несколько раз (создаётся новый итератор)
    print("\n🔄 Повторная итерация:")
    for num in number_range:  # итерируемся снова
        print(f"  {num}")  # выводим число снова
```

### ⚡ Генераторы - мощь Python

```python
# Простой генератор
def fibonacci_generator(limit: int) -> Generator[int, None, None]:
    """Генератор чисел Фибоначчи до указанного лимита"""
    a, b = 0, 1  # первые два числа Фибоначчи
    count = 0  # счётчик сгенерированных чисел
    
    while count < limit:  # пока не достигли лимита
        yield a  # возвращаем текущее число Фибоначчи
        a, b = b, a + b  # вычисляем следующие числа
        count += 1  # увеличиваем счётчик

# Генератор с состоянием
def stateful_generator() -> Generator[str, str, None]:
    """Генератор с состоянием, который может принимать данные"""
    name = "Аноним"  # начальное имя
    
    while True:  # бесконечный генератор
        received = yield f"Привет, {name}!"  # возвращаем приветствие и принимаем данные
        
        if received is not None:  # если получили данные
            name = received  # обновляем имя

# Генератор для чтения больших файлов
def read_large_file_lines(filename: str) -> Generator[str, None, None]:
    """Генератор для построчного чтения больших файлов"""
    try:
        with open(filename, 'r', encoding='utf-8') as file:  # открываем файл
            for line_number, line in enumerate(file, 1):  # читаем построчно с номерами
                yield f"Строка {line_number}: {line.strip()}"  # возвращаем строку с номером
    except FileNotFoundError:
        yield f"Файл {filename} не найден"  # обрабатываем ошибку

# Генератор выражений - краткая форма
def generator_expressions_demo():
    """Демонстрация генераторных выражений"""
    
    # Обычный генератор квадратов
    squares_gen = (x**2 for x in range(10))  # генератор квадратов от 0 до 9
    print("Квадраты (генератор):")
    for square in squares_gen:  # итерируемся по квадратам
        print(f"  {square}")  # выводим квадрат
    
    # Фильтрация с генератором
    even_squares = (x**2 for x in range(20) if x % 2 == 0)  # квадраты чётных чисел
    print("\nКвадраты чётных чисел:")
    for square in even_squares:  # итерируемся по квадратам чётных
        print(f"  {square}")  # выводим квадрат
    
    # Вложенные генераторы
    matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]  # матрица 3x3
    flattened = (item for row in matrix for item in row)  # "разворачиваем" матрицу
    print(f"\nРазвёрнутая матрица: {list(flattened)}")  # выводим развёрнутую матрицу

# Продвинутые генераторы с yield from
def advanced_generator_demo():
    """Демонстрация продвинутых возможностей генераторов"""
    
    def sub_generator(items: list) -> Generator[Any, None, None]:
        """Подгенератор"""
        for item in items:  # проходим по элементам
            yield f"Подгенератор: {item}"  # возвращаем элемент с префиксом
    
    def main_generator() -> Generator[Any, None, None]:
        """Главный генератор, использующий yield from"""
        yield "Начало главного генератора"  # возвращаем начальное сообщение
        
        # yield from делегирует выполнение подгенератору
        yield from sub_generator([1, 2, 3])  # делегируем подгенератору
        yield from sub_generator(['a', 'b', 'c'])  # ещё одно делегирование
        
        yield "Конец главного генератора"  # возвращаем финальное сообщение
    
    print("🔗 Демонстрация yield from:")
    for item in main_generator():  # итерируемся по главному генератору
        print(f"  {item}")  # выводим элемент

# Сравнение памяти: список vs генератор
def memory_comparison():
    """Сравнение использования памяти списками и генераторами"""
    
    # Создаём большой список
    big_list = [x**2 for x in range(100000)]  # список из 100,000 квадратов
    list_memory = sys.getsizeof(big_list)  # размер списка в памяти
    
    # Создаём генератор для тех же данных
    big_generator = (x**2 for x in range(100000))  # генератор тех же квадратов
    generator_memory = sys.getsizeof(big_generator)  # размер генератора в памяти
    
    print(f"📊 Сравнение памяти:")
    print(f"  Список (100,000 элементов): {list_memory:,} байт")  # выводим размер списка
    print(f"  Генератор: {generator_memory:,} байт")  # выводим размер генератора
    print(f"  Экономия памяти: {(list_memory - generator_memory):,} байт")  # выводим экономию
    print(f"  Во сколько раз меньше: {list_memory / generator_memory:.1f}x")  # выводим кратность

# Генератор для работы с API (пагинация)
def api_pages_generator(base_url: str, total_pages: int) -> Generator[dict, None, None]:
    """Генератор для симуляции получения страниц API"""
    
    for page in range(1, total_pages + 1):  # проходим по всем страницам
        # Симулируем API ответ
        simulated_response = {
            'page': page,  # номер страницы
            'data': [f'item_{page}_{i}' for i in range(5)],  # данные страницы
            'has_next': page < total_pages  # есть ли следующая страница
        }
        
        print(f"📡 Загрузили страницу {page}/{total_pages}")  # логируем загрузку
        yield simulated_response  # возвращаем данные страницы

# Главная демонстрационная функция
def main_generators_demo():
    """Главная функция для демонстрации генераторов"""
    
    print("🔢 Генератор Фибоначчи:")
    fib_gen = fibonacci_generator(10)  # создаём генератор 10 чисел Фибоначчи
    
    for fib_num in fib_gen:  # итерируемся по числам Фибоначчи
        print(f"  {fib_num}")  # выводим число
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("💬 Генератор с состоянием:")
    state_gen = stateful_generator()  # создаём генератор с состоянием
    
    print(f"  {next(state_gen)}")  # первое приветствие
    print(f"  {state_gen.send('Алексей')}")  # отправляем имя
    print(f"  {state_gen.send('Мария')}")  # отправляем другое имя
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("📄 Чтение файла генератором:")
    # Создаём тестовый файл
    test_file = "test_generator.txt"
    with open(test_file, 'w', encoding='utf-8') as f:
        f.write("Первая строка\n")
        f.write("Вторая строка\n")
        f.write("Третья строка\n")
    
    # Читаем файл генератором
    for line in read_large_file_lines(test_file):
        print(f"  {line}")
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    generator_expressions_demo()  # демонстрируем генераторные выражения
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    advanced_generator_demo()  # продвинутые генераторы
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    memory_comparison()  # сравниваем память
    
    print("\n" + "="*50 + "\n")  # разделитель
    
    print("🌐 API генератор:")
    for page_data in api_pages_generator("https://api.example.com", 3):
        print(f"  Страница {page_data['page']}: {len(page_data['data'])} элементов")

# Запускаем всё
if __name__ == "__main__":
    print("🎭 Демонстрация итераторов:")
    demonstrate_iterators()  # демонстрируем итераторы
    
    print("\n" + "="*60 + "\n")  # большой разделитель
    
    print("⚡ Демонстрация генераторов:")
    main_generators_demo()  # демонстрируем генераторы
```

## 🧠 4. Метаклассы и дескрипторы

### 🎪 Метаклассы - Python магия

```python
from typing import Any, Dict, Type
import functools

# Простой метакласс
class SingletonMeta(type):
    """Метакласс для реализации паттерна Синглтон"""
    _instances: Dict[Type, Any] = {}  # словарь для хранения экземпляров
    
    def __call__(cls, *args, **kwargs):
        """Переопределяем создание экземпляра"""
        if cls not in cls._instances:  # если экземпляра ещё нет
            # Создаём новый экземпляр
            instance = super().__call__(*args, **kwargs)
            cls._instances[cls] = instance  # сохраняем экземпляр
        return cls._instances[cls]  # возвращаем единственный экземпляр

class DatabaseConnection(metaclass=SingletonMeta):
    """Пример класса с метаклассом Singleton"""
    
    def __init__(self):
        self.connection_id = id(self)  # уникальный ID соединения
        print(f"🔌 Создано соединение с ID: {self.connection_id}")
    
    def query(self, sql: str):
        """Имитация выполнения SQL запроса"""
        return f"Выполнен запрос: {sql}"

# Метакласс для автоматической регистрации классов
class RegistryMeta(type):
    """Метакласс для автоматической регистрации всех классов"""
    registry = {}  # реестр всех классов
    
    def __new__(mcs, name, bases, namespace, **kwargs):
        """Создаём новый класс и регистрируем его"""
        cls = super().__new__(mcs, name, bases, namespace)
        
        # Регистрируем класс (кроме базовых)
        if name != 'RegisteredBase':
            mcs.registry[name] = cls
            print(f"📝 Зарегистрирован класс: {name}")
        
        return cls
    
    @classmethod
    def get_registered_classes(mcs):
        """Возвращаем все зарегистрированные классы"""
        return mcs.registry.copy()

class RegisteredBase(metaclass=RegistryMeta):
    """Базовый класс для всех регистрируемых классов"""
    pass

class UserModel(RegisteredBase):
    """Модель пользователя"""
    def __init__(self, name: str):
        self.name = name

class ProductModel(RegisteredBase):
    """Модель товара"""
    def __init__(self, title: str, price: float):
        self.title = title
        self.price = price

# Метакласс для валидации атрибутов
class ValidatedMeta(type):
    """Метакласс для автоматической валидации атрибутов"""
    
    def __new__(mcs, name, bases, namespace, **kwargs):
        """Создаём класс с валидацией"""
        # Находим все атрибуты для валидации
        validators = {}
        for key, value in namespace.items():
            if hasattr(value, '_validator'):  # если у атрибута есть валидатор
                validators[key] = value._validator
        
        # Сохраняем валидаторы в классе
        namespace['_validators'] = validators
        
        return super().__new__(mcs, name, bases, namespace)

def validated_field(validator_func):
    """Декоратор для создания валидируемого поля"""
    def field_property(self):
        return getattr(self, f'_{self._field_name}', None)
    
    def field_setter(self, value):
        if not validator_func(value):  # проверяем валидатор
            raise ValueError(f"Недопустимое значение: {value}")
        setattr(self, f'_{self._field_name}', value)
    
    # Создаём свойство
    prop = property(field_property, field_setter)
    prop._validator = validator_func  # сохраняем валидатор
    return prop

class Person(metaclass=ValidatedMeta):
    """Класс с валидируемыми полями"""
    
    @validated_field
    def age(self):
        return lambda x: isinstance(x, int) and 0 <= x <= 150
    
    @validated_field
    def email(self):
        return lambda x: isinstance(x, str) and '@' in x
    
    def __init__(self, age: int, email: str):
        self.age = age  # будет валидироваться
        self.email = email  # будет валидироваться

# Демонстрация метаклассов
def demonstrate_metaclasses():
    """Демонстрация работы метаклассов"""
    
    print("🎪 Метакласс Singleton:")
    
    # Создаём несколько "разных" подключений
    db1 = DatabaseConnection()  # первое подключение
    db2 = DatabaseConnection()  # "второе" подключение
    db3 = DatabaseConnection()  # "третье" подключение
    
    print(f"db1 is db2: {db1 is db2}")  # проверяем, что это один объект
    print(f"db1 is db3: {db1 is db3}")  # проверяем, что это один объект
    
    print("\n📝 Метакласс Registry:")
    
    # Смотрим, какие классы зарегистрированы
    registered = RegistryMeta.get_registered_classes()
    for name, cls in registered.items():
        print(f"  {name}: {cls}")
    
    print("\n✅ Метакласс Validation:")
    
    try:
        person = Person(age=25, email="test@example.com")  # валидные данные
        print("✅ Создан валидный объект Person")
        
        person.age = 30  # валидное изменение
        print("✅ Возраст успешно изменён")
        
        person.email = "invalid-email"  # невалидный email
    except ValueError as e:
        print(f"❌ Ошибка валидации: {e}")
    
    try:
        invalid_person = Person(age=-5, email="test@example.com")  # невалидный возраст
    except ValueError as e:
        print(f"❌ Ошибка при создании: {e}")
```

### 🎛️ Дескрипторы - контроль доступа

```python
import weakref
from typing import Any, Dict, Optional

# Простой дескриптор
class LoggedAttribute:
    """Дескриптор, который логирует все обращения к атрибуту"""
    
    def __init__(self, name: str, initial_value: Any = None):
        self.name = name  # имя атрибута
        self.initial_value = initial_value  # начальное значение
        # Используем WeakKeyDictionary для избежания утечек памяти
        self.data: weakref.WeakKeyDictionary = weakref.WeakKeyDictionary()
    
    def __get__(self, obj: Any, objtype: Optional[type] = None) -> Any:
        """Вызывается при получении значения атрибута"""
        if obj is None:  # вызов из класса, а не из экземпляра
            return self
        
        value = self.data.get(obj, self.initial_value)  # получаем значение
        print(f"📖 Чтение {self.name}: {value}")  # логируем чтение
        return value
    
    def __set__(self, obj: Any, value: Any) -> None:
        """Вызывается при установке значения атрибута"""
        old_value = self.data.get(obj, self.initial_value)  # получаем старое значение
        self.data[obj] = value  # устанавливаем новое значение
        print(f"✏️ Изменение {self.name}: {old_value} → {value}")  # логируем изменение
    
    def __delete__(self, obj: Any) -> None:
        """Вызывается при удалении атрибута"""
        if obj in self.data:
            value = self.data[obj]  # получаем значение
            del self.data[obj]  # удаляем из словаря
            print(f"🗑️ Удаление {self.name}: {value}")  # логируем удаление

# Дескриптор с валидацией
class ValidatedDescriptor:
    """Дескриптор с валидацией значений"""
    
    def __init__(self, name: str, validator_func, error_message: str = "Недопустимое значение"):
        self.name = name  # имя атрибута
        self.validator = validator_func  # функция валидации
        self.error_message = error_message  # сообщение об ошибке
        self.data: weakref.WeakKeyDictionary = weakref.WeakKeyDictionary()
    
    def __get__(self, obj: Any, objtype: Optional[type] = None) -> Any:
        if obj is None:
            return self
        return self.data.get(obj)
    
    def __set__(self, obj: Any, value: Any) -> None:
        if not self.validator(value):  # проверяем валидатор
            raise ValueError(f"{self.error_message}: {value}")
        self.data[obj] = value

# Дескриптор только для чтения
class ReadOnlyDescriptor:
    """Дескриптор только для чтения (после первой установки)"""
    
    def __init__(self, name: str):
        self.name = name
        self.data: weakref.WeakKeyDictionary = weakref.WeakKeyDictionary()
        self.initialized: weakref.WeakSet = weakref.WeakSet()
    
    def __get__(self, obj: Any, objtype: Optional[type] = None) -> Any:
        if obj is None:
            return self
        
        if obj not in self.data:
            raise AttributeError(f"Атрибут {self.name} не инициализирован")
        
        return self.data[obj]
    
    def __set__(self, obj: Any, value: Any) -> None:
        if obj in self.initialized:  # если уже инициализирован
            raise AttributeError(f"Атрибут {self.name} только для чтения")
        
        self.data[obj] = value  # устанавливаем значение
        self.initialized.add(obj)  # помечаем как инициализированный

# Типизированный дескриптор
class TypedDescriptor:
    """Дескриптор с проверкой типов"""
    
    def __init__(self, name: str, expected_type: type):
        self.name = name
        self.expected_type = expected_type
        self.data: weakref.WeakKeyDictionary = weakref.WeakKeyDictionary()
    
    def __get__(self, obj: Any, objtype: Optional[type] = None) -> Any:
        if obj is None:
            return self
        return self.data.get(obj)
    
    def __set__(self, obj: Any, value: Any) -> None:
        if not isinstance(value, self.expected_type):  # проверяем тип
            raise TypeError(
                f"Атрибут {self.name} должен быть типа {self.expected_type.__name__}, "
                f"получен {type(value).__name__}"
            )
        self.data[obj] = value

# Примеры использования дескрипторов
class BankAccount:
    """Банковский счёт с дескрипторами"""
    
    # Дескрипторы для различных атрибутов
    account_id = ReadOnlyDescriptor("account_id")  # ID только для чтения
    balance = ValidatedDescriptor(
        "balance", 
        lambda x: isinstance(x, (int, float)) and x >= 0,
        "Баланс должен быть неотрицательным числом"
    )
    owner_name = TypedDescriptor("owner_name", str)  # имя владельца - строка
    transaction_log = LoggedAttribute("transaction_log", [])  # лог транзакций
    
    def __init__(self, account_id: str, owner_name: str, initial_balance: float = 0.0):
        self.account_id = account_id  # ID счёта (только для чтения)
        self.owner_name = owner_name  # имя владельца
        self.balance = initial_balance  # начальный баланс
        self.transaction_log = []  # лог транзакций
    
    def deposit(self, amount: float):
        """Внести деньги на счёт"""
        if amount <= 0:
            raise ValueError("Сумма депозита должна быть положительной")
        
        self.balance += amount  # увеличиваем баланс
        self.transaction_log.append(f"Депозит: +{amount}")  # записываем транзакцию
    
    def withdraw(self, amount: float):
        """Снять деньги со счёта"""
        if amount <= 0:
            raise ValueError("Сумма снятия должна быть положительной")
        
        if self.balance < amount:
            raise ValueError("Недостаточно средств")
        
        self.balance -= amount  # уменьшаем баланс
        self.transaction_log.append(f"Снятие: -{amount}")  # записываем транзакцию

# Демонстрация дескрипторов
def demonstrate_descriptors():
    """Демонстрация работы дескрипторов"""
    
    print("🏦 Создаём банковский счёт:")
    account = BankAccount("ACC-001", "Иван Петров", 1000.0)
    
    print(f"\n💰 Текущий баланс: {account.balance}")
    
    print("\n📈 Выполняем операции:")
    account.deposit(500.0)  # депозит
    account.withdraw(200.0)  # снятие
    
    print(f"\n📊 Итоговый баланс: {account.balance}")
    
    print("\n🔒 Тестируем ограничения:")
    
    try:
        account.account_id = "NEW-ID"  # попытка изменить readonly поле
    except AttributeError as e:
        print(f"❌ {e}")
    
    try:
        account.balance = -100  # попытка установить отрицательный баланс
    except ValueError as e:
        print(f"❌ {e}")
    
    try:
        account.owner_name = 12345  # попытка установить неправильный тип
    except TypeError as e:
        print(f"❌ {e}")
    
    print(f"\n🆔 ID счёта: {account.account_id}")  # читаем readonly поле

# Запускаем демонстрации
if __name__ == "__main__":
    print("🧠 Демонстрация метаклассов:")
    demonstrate_metaclasses()  # демонстрируем метаклассы
    
    print("\n" + "="*60 + "\n")  # большой разделитель
    
    print("🎛️ Демонстрация дескрипторов:")
    demonstrate_descriptors()  # демонстрируем дескрипторы
```

## 🏗️ 5. Контекстные менеджеры

### 🚪 with блоки и автоматическое управление ресурсами

```python
import os
import sqlite3
import threading
import time
from contextlib import contextmanager, ExitStack
from typing import Any, Iterator

# Простой контекстный менеджер через класс
class FileManager:
    """Контекстный менеджер для работы с файлами"""
    
    def __init__(self, filename: str, mode: str = 'r'):
        self.filename = filename  # имя файла
        self.mode = mode  # режим открытия
        self.file = None  # файловый объект
    
    def __enter__(self):
        """Входим в контекст"""
        print(f"📂 Открываем файл: {self.filename}")
        self.file = open(self.filename, self.mode, encoding='utf-8')
        return self.file  # возвращаем файловый объект
    
    def __exit__(self, exc_type, exc_value, traceback):
        """Выходим из контекста"""
        if self.file:
            print(f"📄 Закрываем файл: {self.filename}")
            self.file.close()
        
        # Если было исключение, логируем его
        if exc_type is not None:
            print(f"❌ Произошла ошибка: {exc_type.__name__}: {exc_value}")
            return False  # не подавляем исключение
        
        return True  # всё прошло успешно

# Контекстный менеджер для базы данных
class DatabaseManager:
    """Контекстный менеджер для работы с SQLite базой данных"""
    
    def __init__(self, db_path: str):
        self.db_path = db_path
        self.connection = None
        self.cursor = None
    
    def __enter__(self):
        """Входим в контекст - подключаемся к БД"""
        print(f"🗄️ Подключаемся к БД: {self.db_path}")
        self.connection = sqlite3.connect(self.db_path)
        self.cursor = self.connection.cursor()
        return self.cursor  # возвращаем курсор
    
    def __exit__(self, exc_type, exc_value, traceback):
        """Выходим из контекста"""
        if exc_type is None:
            # Если не было ошибок, сохраняем изменения
            print("💾 Сохраняем изменения в БД")
            self.connection.commit()
        else:
            # Если была ошибка, откатываем транзакцию
            print("⏪ Откатываем транзакцию")
            self.connection.rollback()
        
        if self.connection:
            print("🔌 Закрываем соединение с БД")
            self.connection.close()
        
        return False  # не подавляем исключения

# Контекстный менеджер для измерения времени
class TimerManager:
    """Контекстный менеджер для измерения времени выполнения"""
    
    def __init__(self, description: str = "Операция"):
        self.description = description  # описание операции
        self.start_time = None
        self.end_time = None
    
    def __enter__(self):
        print(f"⏱️ Начинаем: {self.description}")
        self.start_time = time.time()  # засекаем время
        return self
    
    def __exit__(self, exc_type, exc_value, traceback):
        self.end_time = time.time()  # фиксируем время окончания
        duration = self.end_time - self.start_time  # вычисляем длительность
        
        if exc_type is None:
            print(f"✅ Завершили: {self.description} за {duration:.3f} секунд")
        else:
            print(f"❌ Прервали: {self.description} через {duration:.3f} секунд")
        
        return False  # не подавляем исключения
    
    @property
    def elapsed_time(self) -> float:
        """Возвращает время выполнения"""
        if self.start_time and self.end_time:
            return self.end_time - self.start_time
        return 0.0

# Контекстный менеджер с помощью декоратора
@contextmanager
def temporary_directory(base_path: str = "/tmp") -> Iterator[str]:
    """Контекстный менеджер для временной директории"""
    import tempfile
    import shutil
    
    # Создаём временную директорию
    temp_dir = tempfile.mkdtemp(dir=base_path)
    print(f"📁 Создали временную директорию: {temp_dir}")
    
    try:
        yield temp_dir  # возвращаем путь к директории
    finally:
        # Удаляем временную директорию
        if os.path.exists(temp_dir):
            shutil.rmtree(temp_dir)
            print(f"🗑️ Удалили временную директорию: {temp_dir}")

@contextmanager
def thread_lock_manager(lock: threading.Lock) -> Iterator[None]:
    """Контекстный менеджер для работы с блокировками"""
    print("🔒 Захватываем блокировку")
    acquired = lock.acquire(timeout=5)  # пытаемся захватить блокировку
    
    if not acquired:
        raise RuntimeError("Не удалось захватить блокировку")
    
    try:
        print("✅ Блокировка захвачена")
        yield  # выполняем код в блокировке
    finally:
        print("🔓 Освобождаем блокировку")
        lock.release()

@contextmanager
def suppress_exceptions(*exception_types) -> Iterator[None]:
    """Контекстный менеджер для подавления исключений"""
    try:
        yield
    except exception_types as e:
        print(f"🔇 Подавлено исключение: {type(e).__name__}: {e}")
    except Exception as e:
        # Другие исключения не подавляем
        print(f"❌ Неожиданное исключение: {type(e).__name__}: {e}")
        raise

# Продвинутый пример с ExitStack
def demonstrate_exit_stack():
    """Демонстрация ExitStack для управления несколькими контекстами"""
    
    print("📚 Демонстрация ExitStack:")
    
    # Создаём несколько файлов для работы
    filenames = ["file1.txt", "file2.txt", "file3.txt"]
    
    # Записываем тестовые данные
    for i, filename in enumerate(filenames):
        with open(filename, 'w', encoding='utf-8') as f:
            f.write(f"Содержимое файла {i + 1}\n")
    
    # Используем ExitStack для работы с несколькими файлами
    with ExitStack() as stack:
        # Открываем все файлы с помощью ExitStack
        files = []
        for filename in filenames:
            file = stack.enter_context(open(filename, 'r', encoding='utf-8'))
            files.append(file)
        
        # Добавляем дополнительные контекстные менеджеры
        timer = stack.enter_context(TimerManager("Обработка файлов"))
        
        # Работаем с файлами
        print("📖 Читаем файлы:")
        for i, file in enumerate(files):
            content = file.read().strip()
            print(f"  {filenames[i]}: {content}")
    
    # Все файлы автоматически закрываются ExitStack
    print("✅ Все файлы закрыты автоматически")
    
    # Удаляем тестовые файлы
    for filename in filenames:
        if os.path.exists(filename):
            os.remove(filename)

# Демонстрация контекстных менеджеров
def demonstrate_context_managers():
    """Демонстрация различных контекстных менеджеров"""
    
    print("📂 Контекстный менеджер для файлов:")
    
    # Создаём тестовый файл
    test_file = "test_context.txt"
    
    # Используем наш FileManager
    with FileManager(test_file, 'w') as file:
        file.write("Привет из контекстного менеджера!\n")
        file.write("Файл автоматически закроется\n")
    
    # Читаем файл обычным способом
    with FileManager(test_file, 'r') as file:
        content = file.read()
        print(f"Содержимое файла:\n{content}")
    
    print("\n⏱️ Контекстный менеджер для измерения времени:")
    
    # Измеряем время выполнения
    with TimerManager("Сложные вычисления") as timer:
        # Имитируем долгую операцию
        total = 0
        for i in range(1000000):
            total += i ** 2
        print(f"Результат вычислений: {total}")
    
    print(f"Время выполнения: {timer.elapsed_time:.3f} секунд")
    
    print("\n🗄️ Контекстный менеджер для базы данных:")
    
    db_file = "test.db"
    
    # Создаём и используем базу данных
    with DatabaseManager(db_file) as cursor:
        # Создаём таблицу
        cursor.execute('''
            CREATE TABLE IF NOT EXISTS users (
                id INTEGER PRIMARY KEY,
                name TEXT NOT NULL,
                age INTEGER
            )
        ''')
        
        # Добавляем данные
        cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Алексей", 30))
        cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Мария", 25))
        
        # Читаем данные
        cursor.execute("SELECT * FROM users")
        users = cursor.fetchall()
        
        print("👥 Пользователи в базе данных:")
        for user_id, name, age in users:
            print(f"  {user_id}: {name}, {age} лет")
    
    print("\n📁 Временная директория:")
    
    # Используем временную директорию
    with temporary_directory() as temp_dir:
        # Создаём файл во временной директории
        temp_file = os.path.join(temp_dir, "temp_file.txt")
        
        with open(temp_file, 'w', encoding='utf-8') as f:
            f.write("Временный файл")
        
        print(f"Создали файл: {temp_file}")
        print(f"Файл существует: {os.path.exists(temp_file)}")
    
    # Директория автоматически удалится
    print(f"Временная директория удалена: {not os.path.exists(temp_dir)}")
    
    print("\n🔇 Подавление исключений:")
    
    # Подавляем определённые исключения
    with suppress_exceptions(ValueError, TypeError):
        print("Выполняем код, который может выдать ValueError или TypeError")
        # Это исключение будет подавлено
        raise ValueError("Тестовая ошибка")
    
    print("Код продолжает выполняться после подавленного исключения")
    
    print("\n🔒 Работа с блокировками:")
    
    # Демонстрируем работу с блокировками
    lock = threading.Lock()
    
    def worker_with_lock(worker_id: int):
        """Рабочая функция с блокировкой"""
        with thread_lock_manager(lock):
            print(f"🛠️ Рабочий {worker_id} выполняет критическую секцию")
            time.sleep(1)  # имитируем работу
            print(f"✅ Рабочий {worker_id} завершил работу")
    
    # Запускаем несколько потоков
    threads = []
    for i in range(3):
        thread = threading.Thread(target=worker_with_lock, args=(i + 1,))
        threads.append(thread)
        thread.start()
    
    # Ждём завершения всех потоков
    for thread in threads:
        thread.join()
    
    # Удаляем тестовые файлы
    for filename in [test_file, db_file]:
        if os.path.exists(filename):
            os.remove(filename)

# Продвинутый пример: кастомный менеджер ресурсов
class ResourcePool:
    """Пул ресурсов с контекстным менеджером"""
    
    def __init__(self, max_resources: int = 5):
        self.max_resources = max_resources  # максимальное количество ресурсов
        self.available_resources = list(range(max_resources))  # доступные ресурсы
        self.used_resources = set()  # используемые ресурсы
        self.lock = threading.Lock()  # блокировка для потокобезопасности
    
    @contextmanager
    def get_resource(self, timeout: float = 5.0) -> Iterator[int]:
        """Получаем ресурс из пула"""
        resource_id = None
        start_time = time.time()
        
        # Пытаемся получить ресурс
        while time.time() - start_time < timeout:
            with self.lock:
                if self.available_resources:  # если есть доступные ресурсы
                    resource_id = self.available_resources.pop()  # берём ресурс
                    self.used_resources.add(resource_id)  # отмечаем как используемый
                    break
            
            # Если ресурсов нет, ждём немного
            time.sleep(0.1)
        
        if resource_id is None:
            raise RuntimeError("Не удалось получить ресурс из пула")
        
        print(f"🎯 Получили ресурс #{resource_id}")
        
        try:
            yield resource_id  # возвращаем ресурс пользователю
        finally:
            # Возвращаем ресурс в пул
            with self.lock:
                if resource_id in self.used_resources:
                    self.used_resources.remove(resource_id)
                    self.available_resources.append(resource_id)
                    print(f"🔄 Вернули ресурс #{resource_id} в пул")
    
    def get_stats(self) -> dict:
        """Получаем статистику пула"""
        with self.lock:
            return {
                'total': self.max_resources,
                'available': len(self.available_resources),
                'used': len(self.used_resources),
                'available_ids': sorted(self.available_resources),
                'used_ids': sorted(self.used_resources)
            }

def demonstrate_resource_pool():
    """Демонстрация пула ресурсов"""
    
    print("🏊‍♂️ Демонстрация пула ресурсов:")
    
    # Создаём пул из 3 ресурсов
    pool = ResourcePool(max_resources=3)
    
    def worker_with_pool(worker_id: int, work_duration: float):
        """Рабочая функция, использующая пул ресурсов"""
        try:
            with pool.get_resource() as resource_id:
                print(f"🛠️ Рабочий {worker_id} использует ресурс #{resource_id}")
                
                # Имитируем работу
                time.sleep(work_duration)
                
                print(f"✅ Рабочий {worker_id} завершил работу с ресурсом #{resource_id}")
        except RuntimeError as e:
            print(f"❌ Рабочий {worker_id} не смог получить ресурс: {e}")
    
    # Показываем начальную статистику
    print(f"📊 Начальная статистика: {pool.get_stats()}")
    
    # Запускаем несколько рабочих потоков
    threads = []
    work_durations = [1.0, 1.5, 2.0, 0.5, 1.2]  # разное время работы
    
    for i, duration in enumerate(work_durations):
        thread = threading.Thread(
            target=worker_with_pool,
            args=(i + 1, duration)
        )
        threads.append(thread)
        thread.start()
        
        # Показываем статистику после запуска каждого потока
        time.sleep(0.1)  # небольшая пауза
        print(f"📊 Статистика после запуска рабочего {i + 1}: {pool.get_stats()}")
    
    # Ждём завершения всех потоков
    for thread in threads:
        thread.join()
    
    # Итоговая статистика
    print(f"📊 Итоговая статистика: {pool.get_stats()}")

# Запускаем все демонстрации
if __name__ == "__main__":
    print("🏗️ Демонстрация контекстных менеджеров:")
    demonstrate_context_managers()  # основные контекстные менеджеры
    
    print("\n" + "="*60 + "\n")
    
    demonstrate_exit_stack()  # ExitStack
    
    print("\n" + "="*60 + "\n")
    
    demonstrate_resource_pool()  # пул ресурсов
```

## 🛠️ 6. Продвинутая работа с модулями и пакетами

### 📦 Динамическая загрузка и интроспекция

```python
import importlib
import importlib.util
import inspect
import sys
import types
from pathlib import Path
from typing import Any, Dict, List, Optional, Callable

# Динамическая загрузка модулей
class DynamicModuleLoader:
    """Класс для динамической загрузки модулей"""
    
    def __init__(self):
        self.loaded_modules: Dict[str, types.ModuleType] = {}  # кэш модулей
    
    def load_module_from_path(self, module_name: str, file_path: str) -> types.ModuleType:
        """Загружаем модуль из файла"""
        
        if module_name in self.loaded_modules:
            print(f"📋 Модуль {module_name} уже загружен из кэша")
            return self.loaded_modules[module_name]
        
        try:
            # Создаём спецификацию модуля
            spec = importlib.util.spec_from_file_location(module_name, file_path)
            if spec is None:
                raise ImportError(f"Не удалось создать спецификацию для {file_path}")
            
            # Создаём модуль
            module = importlib.util.module_from_spec(spec)
            
            # Добавляем модуль в sys.modules для корректной работы импортов
            sys.modules[module_name] = module
            
            # Выполняем модуль
            spec.loader.exec_module(module)
            
            # Сохраняем в кэше
            self.loaded_modules[module_name] = module
            
            print(f"✅ Загружен модуль {module_name} из {file_path}")
            return module
            
        except Exception as e:
            print(f"❌ Ошибка загрузки модуля {module_name}: {e}")
            raise
    
    def load_module_by_name(self, module_name: str) -> types.ModuleType:
        """Загружаем модуль по имени"""
        
        if module_name in self.loaded_modules:
            return self.loaded_modules[module_name]
        
        try:
            module = importlib.import_module(module_name)
            self.loaded_modules[module_name] = module
            print(f"✅ Загружен модуль {module_name}")
            return module
            
        except ImportError as e:
            print(f"❌ Не удалось загрузить модуль {module_name}: {e}")
            raise
    
    def reload_module(self, module_name: str) -> types.ModuleType:
        """Перезагружаем модуль"""
        
        if module_name in self.loaded_modules:
            module = self.loaded_modules[module_name]
            reloaded_module = importlib.reload(module)
            self.loaded_modules[module_name] = reloaded_module
            print(f"🔄 Перезагружен модуль {module_name}")
            return reloaded_module
        else:
            raise ValueError(f"Модуль {module_name} не был загружен ранее")
    
    def get_module_info(self, module: types.ModuleType) -> Dict[str, Any]:
        """Получаем информацию о модуле"""
        
        info = {
            'name': getattr(module, '__name__', 'Unknown'),
            'file': getattr(module, '__file__', 'Unknown'),
            'package': getattr(module, '__package__', 'Unknown'),
            'doc': getattr(module, '__doc__', 'No documentation'),
            'functions': [],
            'classes': [],
            'variables': []
        }
        
        # Анализируем содержимое модуля
        for name in dir(module):
            if name.startswith('_'):  # пропускаем приватные атрибуты
                continue
            
            obj = getattr(module, name)
            
            if inspect.isfunction(obj):
                info['functions'].append({
                    'name': name,
                    'doc': inspect.getdoc(obj),
                    'signature': str(inspect.signature(obj))
                })
            elif inspect.isclass(obj):
                info['classes'].append({
                    'name': name,
                    'doc': inspect.getdoc(obj),
                    'methods': [method for method in dir(obj) if not method.startswith('_')]
                })
            elif not inspect.ismodule(obj):
                info['variables'].append({
                    'name': name,
                    'type': type(obj).__name__,
                    'value': str(obj)[:100]  # ограничиваем длину
                })
        
        return info

# Система плагинов
class PluginSystem:
    """Система плагинов с автоматическим обнаружением"""
    
    def __init__(self, plugin_directory: str):
        self.plugin_directory = Path(plugin_directory)
        self.plugins: Dict[str, types.ModuleType] = {}
        self.plugin_metadata: Dict[str, Dict[str, Any]] = {}
        self.loader = DynamicModuleLoader()
    
    def discover_plugins(self) -> List[str]:
        """Обнаружение плагинов в директории"""
        
        if not self.plugin_directory.exists():
            print(f"❌ Директория плагинов не существует: {self.plugin_directory}")
            return []
        
        plugin_files = []
        
        # Ищем Python файлы
        for file_path in self.plugin_directory.glob("*.py"):
            if file_path.name != "__init__.py":  # пропускаем __init__.py
                plugin_files.append(str(file_path))
        
        print(f"🔍 Найдено {len(plugin_files)} потенциальных плагинов")
        return plugin_files
    
    def load_plugin(self, plugin_path: str) -> Optional[types.ModuleType]:
        """Загружаем один плагин"""
        
        plugin_name = Path(plugin_path).stem  # имя файла без расширения
        
        try:
            # Загружаем модуль
            plugin_module = self.loader.load_module_from_path(
                f"plugin_{plugin_name}", plugin_path
            )
            
            # Проверяем, что это действительно плагин
            if not hasattr(plugin_module, 'plugin_info'):
                print(f"⚠️ {plugin_name} не содержит plugin_info, пропускаем")
                return None
            
            # Получаем метаданные плагина
            plugin_info = plugin_module.plugin_info
            
            # Проверяем обязательные поля
            required_fields = ['name', 'version', 'description']
            for field in required_fields:
                if field not in plugin_info:
                    print(f"⚠️ {plugin_name} не содержит обязательное поле '{field}'")
                    return None
            
            # Сохраняем плагин
            self.plugins[plugin_name] = plugin_module
            self.plugin_metadata[plugin_name] = plugin_info
            
            print(f"🎉 Загружен плагин: {plugin_info['name']} v{plugin_info['version']}")
            return plugin_module
            
        except Exception as e:
            print(f"❌ Ошибка загрузки плагина {plugin_name}: {e}")
            return None
    
    def load_all_plugins(self):
        """Загружаем все плагины"""
        
        plugin_files = self.discover_plugins()
        
        for plugin_path in plugin_files:
            self.load_plugin(plugin_path)
    
    def get_plugin(self, plugin_name: str) -> Optional[types.ModuleType]:
        """Получаем плагин по имени"""
        return self.plugins.get(plugin_name)
    
    def list_plugins(self) -> Dict[str, Dict[str, Any]]:
        """Получаем список всех загруженных плагинов"""
        return self.plugin_metadata.copy()
    
    def execute_plugin_function(self, plugin_name: str, function_name: str, *args, **kwargs) -> Any:
        """Выполняем функцию плагина"""
        
        plugin = self.get_plugin(plugin_name)
        if plugin is None:
            raise ValueError(f"Плагин {plugin_name} не найден")
        
        if not hasattr(plugin, function_name):
            raise ValueError(f"Функция {function_name} не найдена в плагине {plugin_name}")
        
        func = getattr(plugin, function_name)
        if not callable(func):
            raise ValueError(f"{function_name} не является функцией")
        
        print(f"🚀 Выполняем {plugin_name}.{function_name}")
        return func(*args, **kwargs)

# Анализатор модулей
class ModuleAnalyzer:
    """Анализатор модулей для получения детальной информации"""
    
    @staticmethod
    def analyze_function(func: Callable) -> Dict[str, Any]:
        """Анализируем функцию"""
        
        try:
            signature = inspect.signature(func)
            source_lines = inspect.getsourcelines(func)
            
            return {
                'name': func.__name__,
                'doc': inspect.getdoc(func),
                'signature': str(signature),
                'parameters': [
                    {
                        'name': param.name,
                        'default': param.default if param.default != param.empty else None,
                        'annotation': param.annotation if param.annotation != param.empty else None
                    }
                    for param in signature.parameters.values()
                ],
                'source_file': inspect.getfile(func),
                'source_lines': {
                    'start': source_lines[1],
                    'count': len(source_lines[0])
                },
                'is_coroutine': inspect.iscoroutinefunction(func),
                'is_generator': inspect.isgeneratorfunction(func)
            }
        except Exception as e:
            return {'name': func.__name__, 'error': str(e)}
    
    @staticmethod
    def analyze_class(cls: type) -> Dict[str, Any]:
        """Анализируем класс"""
        
        try:
            return {
                'name': cls.__name__,
                'doc': inspect.getdoc(cls),
                'module': cls.__module__,
                'bases': [base.__name__ for base in cls.__bases__],
                'methods': [
                    ModuleAnalyzer.analyze_function(getattr(cls, method_name))
                    for method_name in dir(cls)
                    if not method_name.startswith('_') and 
                       callable(getattr(cls, method_name))
                ],
                'attributes': [
                    attr for attr in dir(cls)
                    if not attr.startswith('_') and 
                       not callable(getattr(cls, attr))
                ],
                'source_file': inspect.getfile(cls),
                'is_abstract': inspect.isabstract(cls)
            }
        except Exception as e:
            return {'name': cls.__name__, 'error': str(e)}
    
    @staticmethod
    def get_module_dependencies(module: types.ModuleType) -> List[str]:
        """Получаем зависимости модуля"""
        
        dependencies = []
        
        # Анализируем все объекты в модуле
        for name in dir(module):
            obj = getattr(module, name)
            
            if inspect.ismodule(obj):
                # Если это модуль и он не является частью стандартной библиотеки
                module_name = getattr(obj, '__name__', '')
                if module_name and not module_name.startswith('builtins'):
                    dependencies.append(module_name)
            elif hasattr(obj, '__module__'):
                # Если объект имеет атрибут __module__
                obj_module = getattr(obj, '__module__')
                if obj_module and obj_module != module.__name__:
                    dependencies.append(obj_module)
        
        return list(set(dependencies))  # убираем дубликаты

# Демонстрация работы с модулями
def create_sample_plugins():
    """Создаём примеры плагинов для демонстрации"""
    
    # Создаём директорию для плагинов
    plugin_dir = Path("sample_plugins")
    plugin_dir.mkdir(exist_ok=True)
    
    # Первый плагин - калькулятор
    calculator_plugin = '''
# Плагин калькулятора
plugin_info = {
    "name": "Calculator Plugin",
    "version": "1.0.0",
    "description": "Простой калькулятор с базовыми операциями",
    "author": "AI Assistant"
}

def add(a, b):
    """Сложение двух чисел"""
    return a + b

def multiply(a, b):
    """Умножение двух чисел"""
    return a * b

def calculate(expression):
    """Вычисление простого выражения"""
    try:
        # ВНИМАНИЕ: в реальном коде eval опасен!
        # Здесь используется только для демонстрации
        return eval(expression)
    except Exception as e:
        return f"Ошибка: {e}"

def get_operations():
    """Получить список доступных операций"""
    return ["add", "multiply", "calculate"]
'''
    
    # Второй плагин - утилиты для строк
    string_plugin = '''
# Плагин для работы со строками
plugin_info = {
    "name": "String Utils Plugin",
    "version": "2.1.0",
    "description": "Утилиты для работы со строками",
    "author": "AI Assistant"
}

def reverse_string(text):
    """Переворачиваем строку"""
    return text[::-1]

def count_words(text):
    """Подсчитываем количество слов"""
    return len(text.split())

def to_title_case(text):
    """Преобразуем в Title Case"""
    return text.title()

class StringAnalyzer:
    """Анализатор строк"""
    
    def __init__(self, text):
        self.text = text
    
    def analyze(self):
        """Полный анализ строки"""
        return {
            "length": len(self.text),
            "words": count_words(self.text),
            "characters": len(self.text.replace(" ", "")),
            "uppercase": sum(1 for c in self.text if c.isupper()),
            "lowercase": sum(1 for c in self.text if c.islower())
        }
'''
    
    # Записываем плагины в файлы
    with open(plugin_dir / "calculator.py", "w", encoding="utf-8") as f:
        f.write(calculator_plugin)
    
    with open(plugin_dir / "string_utils.py", "w", encoding="utf-8") as f:
        f.write(string_plugin)
    
    print(f"✅ Создали примеры плагинов в директории {plugin_dir}")

def demonstrate_dynamic_modules():
    """Демонстрация динамической работы с модулями"""
    
    print("📦 Демонстрация динамической загрузки модулей:")
    
    # Создаём примеры плагинов
    create_sample_plugins()
    
    # Создаём загрузчик модулей
    loader = DynamicModuleLoader()
    
    # Загружаем стандартный модуль
    math_module = loader.load_module_by_name("math")
    print(f"📊 Информация о модуле math:")
    
    math_info = loader.get_module_info(math_module)
    print(f"  Функции: {len(math_info['functions'])}")
    print(f"  Переменные: {len(math_info['variables'])}")
    
    # Демонстрируем систему плагинов
    print("\n🔌 Система плагинов:")
    
    plugin_system = PluginSystem("sample_plugins")
    plugin_system.load_all_plugins()
    
    # Показываем загруженные плагины
    plugins = plugin_system.list_plugins()
    print(f"\n📋 Загруженные плагины:")
    for plugin_name, metadata in plugins.items():
        print(f"  • {metadata['name']} v{metadata['version']}")
        print(f"    {metadata['description']}")
    
    # Используем плагины
    print("\n🚀 Использование плагинов:")
    
    # Калькулятор
    result = plugin_system.execute_plugin_function("calculator", "add", 5, 3)
    print(f"calculator.add(5, 3) = {result}")
    
    result = plugin_system.execute_plugin_function("calculator", "calculate", "2 ** 8")
    print(f"calculator.calculate('2 ** 8') = {result}")
    
    # Строковые утилиты
    result = plugin_system.execute_plugin_function("string_utils", "reverse_string", "Hello World!")
    print(f"string_utils.reverse_string('Hello World!') = '{result}'")
    
    result = plugin_system.execute_plugin_function("string_utils", "count_words", "Привет, как дела?")
    print(f"string_utils.count_words('Привет, как дела?') = {result}")
    
    # Анализ модулей
    print("\n🔍 Анализ модулей:")
    
    analyzer = ModuleAnalyzer()
    
    # Анализируем один из плагинов
    calculator_plugin = plugin_system.get_plugin("calculator")
    if calculator_plugin:
        dependencies = analyzer.get_module_dependencies(calculator_plugin)
        print(f"Зависимости калькулятора: {dependencies}")
        
        # Анализируем функцию add
        if hasattr(calculator_plugin, 'add'):
            func_info = analyzer.analyze_function(calculator_plugin.add)
            print(f"Анализ функции add:")
            print(f"  Сигнатура: {func_info['signature']}")
            print(f"  Документация: {func_info['doc']}")

# Запускаем демонстрацию
if __name__ == "__main__":
    demonstrate_dynamic_modules()
    
    # Очистка: удаляем созданные файлы
    import shutil
    plugin_dir = Path("sample_plugins")
    if plugin_dir.exists():
        shutil.rmtree(plugin_dir)
        print(f"\n🧹 Очистили директорию {plugin_dir}")
```

## ⚡ 7. Оптимизация производительности

### 🏃‍♂️ Профилирование и бенчмарки

```python
import cProfile
import time
import timeit
import functools
import sys
from typing import Callable, Any, List, Dict
from memory_profiler import profile
import tracemalloc

# Декоратор для измерения времени выполнения
def timing_decorator(func: Callable) -> Callable:
    """Декоратор для измерения времени выполнения функции"""
    
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        start_time = time.perf_counter()  # используем высокоточный счётчик
        result = func(*args, **kwargs)
        end_time = time.perf_counter()
        
        execution_time = end_time - start_time
        print(f"⏱️ {func.__name__} выполнилась за {execution_time:.6f} секунд")
        
        return result
    return wrapper

# Декоратор для профилирования памяти
def memory_profiler_decorator(func: Callable) -> Callable:
    """Декоратор для профилирования использования памяти"""
    
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        tracemalloc.start()  # начинаем отслеживание памяти
        
        result = func(*args, **kwargs)
        
        current, peak = tracemalloc.get_traced_memory()
        tracemalloc.stop()
        
        print(f"💾 {func.__name__}:")
        print(f"  Текущее использование: {current / 1024 / 1024:.2f} MB")
        print(f"  Пиковое использование: {peak / 1024 / 1024:.2f} MB")
        
        return result
    return wrapper

# Бенчмарк класс для сравнения алгоритмов
class Benchmark:
    """Класс для проведения бенчмарков"""
    
    def __init__(self, name: str):
        self.name = name
        self.results: Dict[str, Dict[str, float]] = {}
    
    def run_benchmark(self, func: Callable, name: str, *args, **kwargs) -> Dict[str, float]:
        """Запускаем бенчмарк для функции"""
        
        print(f"🏃‍♂️ Бенчмарк: {name}")
        
        # Измеряем время выполнения
        execution_times = []
        for i in range(5):  # делаем 5 запусков
            start_time = time.perf_counter()
            result = func(*args, **kwargs)
            end_time = time.perf_counter()
            execution_times.append(end_time - start_time)
        
        # Вычисляем статистики
        avg_time = sum(execution_times) / len(execution_times)
        min_time = min(execution_times)
        max_time = max(execution_times)
        
        # Измеряем использование памяти
        tracemalloc.start()
        result = func(*args, **kwargs)
        current, peak = tracemalloc.get_traced_memory()
        tracemalloc.stop()
        
        benchmark_result = {
            'avg_time': avg_time,
            'min_time': min_time,
            'max_time': max_time,
            'memory_current': current,
            'memory_peak': peak
        }
        
        self.results[name] = benchmark_result
        
        print(f"  Среднее время: {avg_time:.6f}s")
        print(f"  Память (пик): {peak / 1024 / 1024:.2f} MB")
        
        return benchmark_result
    
    def compare_results(self):
        """Сравниваем результаты бенчмарков"""
        
        print(f"\n📊 Сравнение результатов бенчмарка '{self.name}':")
        print("="*60)
        
        # Сортируем по времени выполнения
        sorted_by_time = sorted(self.results.items(), key=lambda x: x[1]['avg_time'])
        sorted_by_memory = sorted(self.results.items(), key=lambda x: x[1]['memory_peak'])
        
        print(f"🚀 Результаты по времени (от быстрого к медленному):")
        for i, (name, data) in enumerate(sorted_by_time, 1):
            print(f"{i}. {name}: {data['avg_time']:.6f}s (память: {data['memory_peak'] / 1024 / 1024:.2f} MB)")
        
        print(f"\n💾 Результаты по памяти (от меньшего к большему):")
        for i, (name, data) in enumerate(sorted_by_memory, 1):
            print(f"{i}. {name}: {data['memory_peak'] / 1024 / 1024:.2f} MB (время: {data['avg_time']:.6f}s)")
        
        # Находим лучший результат
        fastest = sorted_by_time[0]
        most_memory_efficient = sorted_by_memory[0]
        
        print(f"\n🏆 Самый быстрый: {fastest[0]}")
        print(f"🏆 Самый экономичный по памяти: {most_memory_efficient[0]}")

# Различные алгоритмы сортировки для демонстрации
def bubble_sort(arr):
    """Сортировка пузырьком - медленная, но простая"""
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr

def quick_sort(arr):
    """Быстрая сортировка"""
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

def merge_sort(arr):
    """Сортировка слиянием"""
    if len(arr) <= 1:
        return arr
    
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    
    result = []
    i = j = 0
    
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    
    result.extend(left[i:])
    result.extend(right[j:])
    return result

def insertion_sort(arr):
    """Сортировка вставками"""
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    return arr

# Демонстрация бенчмарков
def demonstrate_benchmarking():
    """Демонстрация системы бенчмарков"""
    
    import random
    
    print("🎯 Бенчмарк алгоритмов сортировки")
    
    # Создаем тестовые данные
    test_data = [random.randint(1, 1000) for _ in range(1000)]
    
    # Создаем бенчмарк
    benchmark = Benchmark("Алгоритмы сортировки")
    
    # Тестируем разные алгоритмы
    benchmark.run_benchmark(bubble_sort, "Bubble Sort", test_data.copy())
    benchmark.run_benchmark(quick_sort, "Quick Sort", test_data.copy())
    benchmark.run_benchmark(merge_sort, "Merge Sort", test_data.copy())
    benchmark.run_benchmark(insertion_sort, "Insertion Sort", test_data.copy())
    benchmark.run_benchmark(sorted, "Built-in Sorted", test_data.copy())
    
    # Сравниваем результаты
    benchmark.compare_results()

# Профилирование с помощью встроенных инструментов
def profile_function_example():
    """Пример функции для профилирования"""
    # Имитируем сложные вычисления
    result = []
    for i in range(100000):
        result.append(i ** 2)
    
    # Работа со строками
    text = ""
    for i in range(1000):
        text += f"Number {i} "
    
    # Работа со словарями
    data_dict = {}
    for i in range(10000):
        data_dict[f"key_{i}"] = i * 2
    
    return len(result), len(text), len(data_dict)

def run_cprofile_example():
    """Запуск профилирования с cProfile"""
    
    print("📊 Профилирование с cProfile:")
    print("="*50)
    
    # Создаем профайлер
    profiler = cProfile.Profile()
    
    # Запускаем профилирование
    profiler.enable()
    result = profile_function_example()
    profiler.disable()
    
    # Выводим результаты
    import io
    import pstats
    
    s = io.StringIO()
    ps = pstats.Stats(profiler, stream=s)
    ps.sort_stats('cumulative')
    ps.print_stats(10)  # Показываем топ 10
    
    print(s.getvalue())
    print(f"Результат выполнения: {result}")

# Пример memory_profiler (если установлен)
@profile
def memory_intensive_function():
    """Функция, интенсивно использующая память"""
    # Создаем большие списки
    big_list1 = [i for i in range(1000000)]
    big_list2 = [i ** 2 for i in range(1000000)]
    
    # Создаем словарь
    big_dict = {i: i ** 3 for i in range(500000)}
    
    # Освобождаем часть памяти
    del big_list1
    
    return len(big_list2), len(big_dict)

# Использование timeit для точных измерений
def demonstrate_timeit():
    """Демонстрация использования timeit"""
    
    print("⏱️ Точные измерения времени с timeit:")
    print("="*50)
    
    # Сравниваем разные способы создания списков
    
    # List comprehension
    time1 = timeit.timeit('[i for i in range(1000)]', number=10000)
    print(f"List comprehension: {time1:.6f} секунд")
    
    # Цикл for с append
    setup = "result = []"
    code = """
for i in range(1000):
    result.append(i)
"""
    time2 = timeit.timeit(code, setup=setup, number=10000)
    print(f"Цикл for с append: {time2:.6f} секунд")
    
    # map() с range
    time3 = timeit.timeit('list(map(lambda x: x, range(1000)))', number=10000)
    print(f"map() с lambda: {time3:.6f} секунд")
    
    # Встроенная функция list()
    time4 = timeit.timeit('list(range(1000))', number=10000)
    print(f"Встроенная list(): {time4:.6f} секунд")
    
    print(f"\nСамый быстрый способ в {time1/time4:.2f} раз медленнее самого быстрого")

# Кастомный профайлер контекстного менеджера
class SimpleProfiler:
    """Простой профайлер для измерения времени выполнения блоков кода"""
    
    def __init__(self, name="Блок кода"):
        self.name = name
        self.start_time = None
        self.end_time = None
    
    def __enter__(self):
        print(f"🚀 Начинаем профилирование: {self.name}")
        self.start_time = time.perf_counter()
        return self
    
    def __exit__(self, exc_type, exc_value, traceback):
        self.end_time = time.perf_counter()
        execution_time = self.end_time - self.start_time
        
        if exc_type is None:
            print(f"✅ {self.name} выполнен за {execution_time:.6f} секунд")
        else:
            print(f"❌ {self.name} прерван через {execution_time:.6f} секунд")
        
        return False
    
    @property
    def execution_time(self):
        """Возвращает время выполнения"""
        if self.start_time and self.end_time:
            return self.end_time - self.start_time
        return 0

def demonstrate_custom_profiler():
    """Демонстрация кастомного профайлера"""
    
    print("🔧 Кастомный профайлер:")
    
    with SimpleProfiler("Математические вычисления"):
        # Имитируем сложные вычисления
        result = sum(i ** 2 for i in range(100000))
        print(f"Результат вычислений: {result}")
    
    with SimpleProfiler("Работа со строками"):
        # Создаем большую строку
        big_string = "".join(str(i) for i in range(50000))
        print(f"Создана строка длиной: {len(big_string)} символов")
    
    with SimpleProfiler("Работа со списками"):
        # Создаем и обрабатываем список
        data = list(range(200000))
        filtered_data = [x for x in data if x % 2 == 0]
        print(f"Отфильтровано {len(filtered_data)} четных чисел")

# Запускаем все демонстрации
if __name__ == "__main__":
    print("🔥 Демонстрация оптимизации производительности в Python:")
    
    print("\n" + "="*70 + "\n")
    
    demonstrate_benchmarking()
    
    print("\n" + "="*70 + "\n")
    
    run_cprofile_example()
    
    print("\n" + "="*70 + "\n")
    
    demonstrate_timeit()
    
    print("\n" + "="*70 + "\n")
    
    demonstrate_custom_profiler()
    
    print("\n🎉 Все демонстрации производительности завершены!")
    print("💡 Помните: профилируйте перед оптимизацией!")
    print("💡 \"Premature optimization is the root of all evil\" - Donald Knuth")
```

Ебать, готово! 🚀  

Теперь у тебя есть полный арсенал крутых техник:

**💪 Теперь ты готов к:**
- Senior Python разработчик позициям
- Архитектурным собеседованиям  
- Созданию высокопроизводительных приложений
- Работе с любыми Python фреймворками




