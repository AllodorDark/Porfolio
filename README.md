# 🧪 Тестирование REST API — Restful-Booker

Практический пет-проект по функциональному и негативному тестированию REST API сервиса бронирования отелей **[Restful-Booker]([https://herokuapp.com](https://restful-booker.herokuapp.com/apidoc/index.html))**.

Цель проекта — продемонстрировать полный цикл работы QA-инженера: от анализа API-документации и проектирования тест-кейсов до запросов в Postman и заведения баг-репортов.

---

## 🛠 Стек и инструменты
* **Тест-менеджмент:** Testit
* **Тестирование API:** Postman
* **Баг-трекинг:** Kaiten
* **Форматы и протоколы:** HTTP/HTTPS, REST, JSON

---

## 📋 Что было сделано

### 1. Анализ документации и тест-дизайн (Testit)
Изучена спецификация эндпоинтов и спроектировано **13 тест-кейсов** с применением техник тест-дизайна (эквивалентное разделение, граничные значения, негативное тестирование, базовые проверки безопасности):
* **`Auth - CreateToken` (`POST /auth`):** 5 тест-кейсов (валидная авторизация, неверный логин, неверный пароль, пустые значения полей, пустой JSON-объект `{}`).
* **`Booking - GetBookingIds` (`GET /booking`):** 8 тест-кейсов (получение списка всех ID, фильтрация по имени и фамилии, поиск по несуществующим данным, пустые Query-параметры, спецсимволы и SQL-инъекция).
> 📂 [Ссылка на Test IT](https://team-pp9r.testit.software/projects/1/tests?isolatedSection=047b38f6-c7d7-4504-8592-0edc3c7c0378)
<img width="300" alt="image" src="https://github.com/user-attachments/assets/166b35c5-928f-4784-b315-4b214b7376fc" />
<img width="600" alt="image" src="https://github.com/user-attachments/assets/5ffb8f73-2547-41b5-bf94-86f11168fc1c" />
<img width="600" alt="image" src="https://github.com/user-attachments/assets/507a0756-24ec-40d5-b762-7d207c5d9ebe" />

---

### 2. Тестирование API в Postman
Собрана и структурирована коллекция запросов, полностью повторяющая структуру тест-кейсов из Testit:
* Настроены HTTP-методы, заголовки (`Content-Type: application/json`, `Accept: application/json`), Query-параметры и JSON-тела запросов.
* Проверены статус-коды ответов, структура и типы данных возвращаемого JSON.

> 📂 **[Скачать Postman-коллекцию (`collection.json`)](./collection.json))**
<img width="450" alt="image" src="https://github.com/user-attachments/assets/c1f04ca7-c96d-4b96-a4bd-558f4d2b26ea" />

---

### 3. Баг-репортинг (Kaiten)
В ходе тестирования эндпоинта авторизации выявлены несоответствия стандартам REST API (сервер возвращает статус `200 OK` вместо `400 Bad Request` / `401 Unauthorized` при передаче невалидных или пустых учетных данных).

По результатам проверок заведено **3 подробных баг-репорта** в Kaiten с указанием предусловий, шагов воспроизведения, ожидаемого и фактического результатов, а также приложенными скриншотами ответов сервера.
<img width="570" alt="image" src="https://github.com/user-attachments/assets/5a6ff87c-8ce9-4104-93de-7bbcd9bff6fa" />
<img width="570" alt="image" src="https://github.com/user-attachments/assets/2286242d-93c1-44eb-8be8-60aa0cf0a302" />
<img width="570" alt="image" src="https://github.com/user-attachments/assets/c8ec2b30-147d-4a39-b050-a92ecb6f9561" />
<img width="570" alt="image" src="https://github.com/user-attachments/assets/a5cdbda9-1412-4d8d-848e-e854066c4495" />
---

## 👤 Контакты
* **Имя Фамилия** — Александр П.
* **Telegram:** `@Krot190`
