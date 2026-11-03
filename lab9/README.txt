Лабораторная работа №8 — Playwright UI E2E

Файлы:
- delivery.html — учебная форма расчёта доставки
- conftest.py — открывает страницу перед каждым тестом
- test_delivery_ui.py — 12 тестовых случаев

Запуск в Windows PowerShell из папки проекта:

1. Создать виртуальное окружение:
   py -m venv .venv

2. Установить Playwright для pytest:
   .venv\Scripts\python.exe -m pip install pytest-playwright

3. Установить браузер Chromium:
   .venv\Scripts\python.exe -m playwright install chromium

4. В первом терминале запустить сервер и оставить его работающим:
   .venv\Scripts\python.exe -m http.server 8000 --bind 127.0.0.1

5. Во втором терминале проверить тесты:
   .venv\Scripts\python.exe -m pytest --collect-only -q

6. Запустить тесты с диагностикой:
   .venv\Scripts\python.exe -m pytest -v --browser chromium --screenshot only-on-failure --tracing retain-on-failure --output test-results --junitxml=report.xml

Ожидаемый результат: 12 passed.
