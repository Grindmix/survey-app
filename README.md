Survey app
===

Survey app это приложение позволяющие создавать опросы и проходить их и включает в себя систему аутентификации.

---
Как использовать:
---

1. Закиньте survey в папку проекта

2. Добавьте survey в INSTALLED_APPS:
```python
    INSTALLED_APPS = [
        'survey.apps.SurveyConfig',
    ]
```

3. Добавьте survey в URLConf:
```python
    path('survey/', include('survey.urls')),
```
4. Запустите: `` python manage.py migrate ``

---
Опросы создаются в админ панели django так что не забудьте сделать суперпользователя (`` python manage.py createsuperuser ``).

Опросы, вопросы, и их параметры создаются и редактируются среди моделей **Surveys**.

Варианты выбора создаются и редактируются в моделях **Questions** (Есть поиск по названию опроса).

**Survey Results** это модели результатов опроса.