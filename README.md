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

