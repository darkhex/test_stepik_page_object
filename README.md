## Автоматизация тестирования с помощью Selenium и Python
>[Курс stepik "Автоматизация тестирования с помощью Selenium и Python"](https://stepik.org/course/575/syllabus)
---
### Структура
```
├── README.md
├── __init__.py
├── conftest.py
├── pages
│   ├── base_page.py
│   ├── basket_page.py
│   ├── locators.py
│   ├── login_page.py
│   ├── main_page.py
│   └── product_page.py
├── pytest.ini
├── requirements.txt
├── test_main_page.py
└── test_product_page.py
```
### Шаги для проверки 
- Скопировать репозиторий 
- Настроить virtualenv
```
pip install virtualenv
cd dir 
virtualenv venv
source venv/bin/activate
```
- Установить пакеты 
`pip install -r test_stepik_page_object/requirements.txt`
- Запустить команду
`pytest -v --tb=line --language=en -m need_review`

---
### Equipment:
- OS: Mac OS 11.2.3
- Python: Python 3.9.4