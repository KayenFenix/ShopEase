# 🛒 ShopEase — E-Commerce Web Store

ShopEase — это полнофункциональный интернет-магазин, разработанный на основе Java Spring Boot с классической многослойной архитектурой. Проект предоставляет полноценный пользовательский путь: от просмотра каталога до оформления заказа и отслеживания его статуса, а также содержит удобную панель администратора для управления товарами, категориями и заказами.

📌 Основные возможности

👤 Для покупателей (CUSTOMER):

Аутентификация: Регистрация и вход в систему с защищенным хэшированием паролей (BCrypt).

Каталог товаров: Просмотр списка товаров с пагинацией, фильтрация по категориям и поиск по названию.

Карточка товара: Детальное описание, наличие на складе, актуальная цена и возможность добавления в корзину.

Корзина: Добавление, удаление, изменение количества товаров и динамический подсчет итоговой стоимости.

Оформление заказа: Указание деталей доставки, автоматическое уменьшение остатков на складе.

История заказов: Отслеживание статуса текущих и прошлых заказов (NEW, PAID, SHIPPED, DELIVERED, CANCELLED).

⚙️ Для администраторов (ADMIN):

Управление каталогом: Добавление, редактирование, удаление товаров и категорий.

Управление остатками: Изменение количества товаров на складе и цен.

Управление заказами: Просмотр всех заказов пользователей и сменяемость их статусов.

🛠 Стек технологий

Backend: Java 17, Spring Boot, Spring MVC, Spring Security, Spring Data JPA, Hibernate, Lombok, Spring Validation

Frontend: Thymeleaf (Server-Side Rendering), HTML5, CSS3, JavaScript (Fetch API)

База данных: PostgreSQL

Сборка и зависимость: Maven

Тестирование: JUnit, Mockito, Postman

Дизайн: Figma

🏛 Архитектура приложения

Проект использует классическую многослойную архитектуру (Layered Architecture):

$$\text{Client (Thymeleaf / JS)} \longleftrightarrow \text{Controller} \longleftrightarrow \text{Service} \longleftrightarrow \text{Repository} \longleftrightarrow \text{PostgreSQL}$$

Frontend: Отображение Thymeleaf-шаблонов и обработка динамических запросов через JS.

Controller: Обработка HTTP-запросов (ProductController, CartController, OrderController, AuthController, AdminController).

Service: Бизнес-логика (расчет суммы заказа, контроль остатков на складе, смена статуса заказа).

Repository: Взаимодействие с базами данных с помощью Spring Data JPA (ProductRepository, UserRepository, OrderRepository).

Entity / DTO: Модели данных (User, Role, Category, Product, Cart, CartItem, Order, OrderItem).

📂 Структура проекта

com.shopease
 ├── config/          # Конфигурация Spring Security и приложения
 ├── controller/      # MVC и REST контроллеры
 ├── dto/             # Data Transfer Objects
 ├── entity/          # JPA Сущности
 ├── exception/       # Обработка исключений
 ├── repository/      # Репозитории Spring Data JPA
 └── service/         # Сервисный слой бизнес-логики


🚀 Запуск проекта локально

Требования:

Java 17 или выше

Maven 3.8+

Установленный и запущенный PostgreSQL

Шаги для запуска:

Клонируйте репозиторий:

git clone https://github.com/your-username/shopease.git
cd shopease


Настройте подключение к БД:
Отредактируйте файл src/main/resources/application.properties (или application.yml):

spring.datasource.url=jdbc:postgresql://localhost:5432/shopease_db
spring.datasource.username=YOUR_POSTGRES_USER
spring.datasource.password=YOUR_POSTGRES_PASSWORD
spring.jpa.hibernate.ddl-auto=update


Соберите и запустите проект:

mvn clean install
mvn spring-boot:run


Откройте в браузере:
Перейдите по адресу http://localhost:8080

👥 Команда разработки

[Студент 1 — Имя Фамилия] — Backend & Database Developer (Проектирование БД, сущности JPA, бизнес-логика, репозитории, JUnit тесты).

[Студент 2 — Имя Фамилия] — Frontend & Integration Developer (Прототип Figma, Thymeleaf-шаблоны, Spring Security, контроллеры, Postman тесты).

🎨 Ссылки и ресурсы

🎨 Прототип в Figma: [Вставить ссылку на Figma]

📄 Документация / План проекта: [Вставить ссылку, если есть]
