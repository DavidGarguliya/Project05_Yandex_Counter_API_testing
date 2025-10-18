# 🚀 Проект: Тестирование API сервиса **Яндекс.Прилавок**

![Проект](https://img.shields.io/badge/Проект-Яндекс.Прилавок-orange)  
![Спринт](https://img.shields.io/badge/Спринт-5-blue)  
![Статус](https://img.shields.io/badge/Статус-Завершён-brightgreen)  
![Платформа](https://img.shields.io/badge/Платформа-API-lightgrey)  
![Баги](https://img.shields.io/badge/Найдено_багов-29-red)  
![Критические](https://img.shields.io/badge/Критические-19-red)  
![Блокирующие](https://img.shields.io/badge/Блокирующие-10-darkred)  

---

## 📝 Описание

Проект выполнен в рамках **5-го спринта курса “Инженер по тестированию: от новичка до автоматизатора” (Яндекс Практикум)**.  
Задача — протестировать новую версию **API Яндекс.Прилавок (v3.3.1)** после обновления функциональности: работа с наборами, корзиной и доставкой.

Цель тестирования:
- Проверить корректность реализации новых эндпоинтов;
- Провести функциональное и негативное тестирование;
- Зафиксировать найденные дефекты и подготовить итоговый отчёт.

---

## 📎 Артефакты

| Тип документа | Ссылка |
|----------------|--------|
| 📑 Требования к бэкенду | [PDF](https://code.s3.yandex.net/qa/files/backend_requirements.pdf) |
| ✅ Чек-лист тестирования | [Google Sheets](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=2006427015#gid=2006427015&range=A1:E1) |
| 🐞 Таблица баг-репортов (29 дефектов) | [Google Sheets](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A1:K1) |
| 📄 Отчёт о тестировании | [GitHub](./Test_Report.md) |

---

## 🔍 Этапы тестирования

### 🔹 Этап 1. Подготовка
- Изучена документация API (Swagger / Apidoc);
- Определены тестовые данные и сценарии;
- Составлен функциональный чек-лист.

### 🔹 Этап 2. Проведение тестирования
- Выполнено 150 проверок в Postman;
- Зафиксировано 29 дефектов (10 блокирующих, 19 критических).

### 🔹 Этап 3. Анализ результатов
- Проведена классификация багов по приоритетам;
- Оценена готовность API к релизу;
- Подготовлен отчёт и рекомендации по ретесту.

---

## 📊 Результаты тестирования

- Всего проверок: **150**  
- Пройдено успешно: **50**  
- Не пройдено: **100**

| Приоритет | Кол-во | Примеры |
|------------|--------|----------|
| 🔴 **Блокирующие** | 10 | [BUG_01](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A3), [BUG_04](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A6), [BUG_05](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A7), [BUG_07](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A9), [BUG_10](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A12), [BUG_26](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A28) |
| 🔴 **Критические** | 19 | [BUG_02](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A4), [BUG_03](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A5), [BUG_06](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A8), [BUG_09](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A11), [BUG_15](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A17), [BUG_21](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A23) |
| ⚪ **Обычные / Низкие** | 0 | – |

---

## 🧩 Основные найденные проблемы

- Ошибки 500 при невалидных параметрах запросов;
- Отсутствие обязательных валидаций (`quantity`, `id`, `kitId`);
- Дублирование корзин при создании;
- Некорректная структура JSON и несоответствие документации;
- Ошибки при обработке XML-тел запросов в ручке доставки.

---

## 🚀 Выводы

- Найдено **29 дефектов**, включая **10 блокирующих** и **19 критических**;  
- Продукт не готов к продакшн-релизу без доработки;  
- После исправления дефектов требуется провести **повторное регрессионное тестирование**.

---

## 👤 Автор

**Давид Гаргулия**  
QA Engineer | 32-я когорта, Яндекс Практикум  
📅 Октябрь 2025
