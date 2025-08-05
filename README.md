# goit-algo2-hw-08

## Завдання 1. Sliding Window Rate Limiter

### Опис
Реалізовано клас `SlidingWindowRateLimiter`, який обмежує частоту повідомлень від користувачів у чаті, використовуючи алгоритм Sliding Window.

- `window_size = 4` секунди 
- `max_requests = 1` повідомлення на користувача в межах вікна

### Реалізовані методи:
- `_cleanup_window(user_id, current_time)`
- `can_send_message(user_id)`
- `record_message(user_id)`
- `time_until_next_allowed(user_id)` 

### Результат:
Працює згідно з очікуваним прикладом — повідомлення  блокуються, якщо перевищено ліміт частоти в межах вікна.

## Завдання 2. Throttling Rate Limiter

### Опис
Реалізовано клас `ThrottlingRateLimiter`, який контролює інтервал між повідомленнями кожного користувача, використовуючи алгоритм Throttling.

- `min_interval = 10` секунд

### Реалізовані методи:
- `can_send_message(user_id)`
- `record_message(user_id)`
- `time_until_next_allowed(user_id)`

### Результат:
Перші повідомлення завжди дозволені. Наступні — лише якщо пройшло 10 секунд з попереднього.

## Як запустити
python HW_8_1.py
python HW_8_2.py