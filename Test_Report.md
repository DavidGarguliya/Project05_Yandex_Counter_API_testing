# 🧪 Отчёт о тестировании API сервиса **Яндекс.Прилавок**

![Проект](https://img.shields.io/badge/Проект-Яндекс.Прилавок-orange)  
![Спринт](https://img.shields.io/badge/Спринт-5-blue)  
![Статус](https://img.shields.io/badge/Статус-Тестирование_завершено-brightgreen)  
![Тип теста](https://img.shields.io/badge/Тип_тестирования-Функциональное_+_Негативное-green)  
![Версия](https://img.shields.io/badge/Версия-v3.3.1-blue)  
![Дата](https://img.shields.io/badge/Дата-Октябрь_2025-lightgrey)  
![Баги](https://img.shields.io/badge/Найдено_багов-29-red)  
![Критические](https://img.shields.io/badge/Критические-19-red)  
![Блокирующие](https://img.shields.io/badge/Блокирующие-10-darkred)  

---

## 📝 Цель тестирования
Проверка стабильности и корректности новой функциональности **API Яндекс.Прилавок**, включающей работу с наборами, корзинами и курьерской доставкой.  
Тестирование проводилось после добавления новых эндпоинтов в бэкенд.

---

## 🔍 Объект тестирования

**Тестируемая версия API:** `v3.3.1`  
**Тестовый стенд:** `https://{id}.serverhub.praktikum-services.ru/`  
**Документация:** `https://{id}.serverhub.praktikum-services.ru/docs/`

---

## ⚙️ Тестовое окружение

| Параметр | Значение |
|-----------|-----------|
| ОС | macOS 15.4 (24E248) |
| Среда тестирования | Postman |
| Тестовый стенд | https://{id}.serverhub.praktikum-services.ru/ |
| Версия API | 3.3.1 |
| Документация | Swagger / Apidoc |
| Инструменты | Postman, Requests |

---

## 🕒 Временные затраты

| Этап | Ожидаемое время | Фактическое время |
|------|------------------|------------------|
| Выполнение работы | 16 часов | 10 часов |

---

## 🧾 Артефакты

- ✅ [Чек-лист функционального тестирования](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=2006427015#gid=2006427015&range=A1:E1)
- ✅ [Таблица баг-репортов (29 дефектов)](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A1:K1)
- ✅ [Требования к бэкенду](https://code.s3.yandex.net/qa/files/backend_requirements.pdf)
- ✅ [Коллекция Postman](https://drive.google.com/file/d/1EATbRFp18yEosUguT6HFxg02nOz1R7k4/view?usp=drive_link)
- ✅ Тестовый отчёт (данный документ)

---

## 📊 Результаты тестирования

- Всего проверок: **150**  
- Пройдено успешно: **50**  
- Не пройдено: **100**

---

## 🧩 Проверенные модули

| Модуль | Проверки | Результат |
|---------|-----------|------------|
| Работа с наборами (`/api/v1/kits/{id}/products`) | 40 | ❌ 27 Не пройдено |
| Работа с корзиной (`/api/v1/orders/:id`) | 70 | ❌ 52 Не пройдено |
| Работа с курьерской доставкой (`/fast-delivery/v3.1.1/calculate-delivery.xml`) | 40 | ❌ 21 Не пройдено |
| Авторизация и вспомогательные ручки | - | не проверялись по условиям задачи |

---

## 🐞 Список обнаруженных дефектов

### 🔴 Блокирующие дефекты (10)
| ID | Название | Приоритет |
|----|-----------|------------|
| [BUG_01](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A3) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке пустого массива [ ] в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_04](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A6) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `id`, содержащим строку с английскими буквами "tomato" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_05](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A7) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `id`, содержащим массив [1,2,3] | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_07](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A9) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity`, содержащим дробное число 1.5 | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_10](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A12) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity`, содержащим массив [1,2,3] | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_11](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A13) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку возможности доставки без элемента потомка `productsCount` | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_18](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A20) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с параметром `id`, содержащим строку с англисйкими буквами "tomato" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_19](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A21) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с параметром `productList`, содержащим строку с числом "123" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_26](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A28) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity`, содержащим число за пределами int "9999999999" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_28](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A30) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в набор с параметром `quantity`, содержащим число за пределами int "9999999999" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |

---

### 🔴 Критические дефекты (19)
| ID | Название | Приоритет |
|----|-----------|------------|
| [BUG_02](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A4) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` без элемента потомка `id` на добавление продуктов в набор | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_03](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A5) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продукта с несуществующим `id` в набор | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_06](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A8) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity`, содержащим отрицательное число -1 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_08](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A10) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity` = 0 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_09](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A11) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром `quantity`, содержащим строку с числом "12" | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_12](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A14) | Отсутствует тело ответа при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки в нерабочее время | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_13](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A15) | Отсутствует тело ответа при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -3 в параметре `deliveryTime` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_14](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A16) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с числом ввиде строки "20" в параметре `deliveryTime` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_15](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A17) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -3 в параметре `productsCount` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_16](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A18) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -3 в параметре `productsWeight` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_17](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A19) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину пустым массивом в `productList` [ ] | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_20](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A22) | ![409 Conflict](https://img.shields.io/badge/409_Conflict-darkorange) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину без элемента потомка id | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_21](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A23) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину пустым массивом в `productList` [ ] | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_22](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A24) | ![409 Conflict](https://img.shields.io/badge/409_Conflict-darkorange) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с отрицательным числом `id` -1 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_23](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A25) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с числом в виде строки в `id` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_24](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A26) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину отрицательным `quantity` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_25](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A27) | ![404 Not Found](https://img.shields.io/badge/404_Not_Found-red) при отправке при отправке ![DELETE](https://img.shields.io/badge/DELETE-red) запроса `/api/v1/orders/id` на удаление корзины с существующим `id` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_27](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A29) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину без элемента родителя `productList` | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_29](https://docs.google.com/spreadsheets/d/1pdwNDj-F-vK2SajkGFImVc1kID8EhSguqjFkqux8Ibw/edit?gid=400522582#gid=400522582&range=A31) | ![409 Conflict](https://img.shields.io/badge/409_Conflict-darkorange) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину `quantity` содержащим числом за пределами int (9999999999) | ![Критический](https://img.shields.io/badge/Критический-red) |

---

## 📊 Распределение дефектов по приоритетам

| Приоритет | Кол-во | Примеры |
|------------|--------|----------|
| 🔴 **Блокирующие** | 10 | BUG_01, BUG_04, BUG_05, BUG_07, BUG_10, BUG_11, BUG_18, BUG_19, BUG_26, BUG_28 |
| 🟠 **Критические** | 19 | BUG_02–BUG_03, BUG_06–BUG_09, BUG_12–BUG_25, BUG_27, BUG_29 |
| ⚪ **Высокие / Стандартные** | 0 | – |

---

## 🔍 Рекомендации по повторному тестированию

После исправления дефектов рекомендуется:

- Повторно проверить обработку поля `quantity` в наборах и корзинах.  
- Перепроверить структуру ответов JSON на соответствие документации.  
- Провести smoke-тест всех эндпоинтов после фиксов.  
- Проверить корректность XML-валидации для ручки `/fast-delivery/v3.1.1/calculate-delivery.xml`.

---

## 📌 Итоги

- Критические и блокирующие дефекты **затрагивают ключевые пользовательские сценарии**.  
- API не готово к выпуску — требуется доработка бэкенда и повторное тестирование.  
- После фиксов необходимо выполнить **регрессионное тестирование**.

---

## 👤 Автор отчёта

**Давид Гаргулия**  
QA Engineer | Яндекс Практикум  
📅 Октябрь 2025
