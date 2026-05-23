# Лабораторная работа #2 по теме "Работа с основными сервисами AWS и развёртывание веб-приложения"

## Цель работы
Познакомиться с основными вычислительными сервисами AWS, научиться создавать и настраивать виртуальные машины (EC2), а также развёртывать простые веб-приложения.

## Процесс выполнения работы
Прикрепляю скриншоты постепенного выполнения, по шагам. Выполнял все внутри курсов, а не в оригинальном AWS, там уже были предсозданы IAM группы и пользователь. В 6-ом заданиии выполнил все три пункта a, b, c.

## Задание 1. Создание IAM группы и пользователя
<img width="1920" height="995" alt="1_1" src="https://github.com/user-attachments/assets/ca181ca8-fcad-4b05-8092-2d001020bc4a" />

<img width="1319" height="944" alt="1_2" src="https://github.com/user-attachments/assets/026ddb3a-22cd-4814-aba0-45469825dc42" />

<img width="1315" height="946" alt="1_3" src="https://github.com/user-attachments/assets/0b07a11e-1acd-4cc2-8438-6e07266489e0" />

<img width="1316" height="945" alt="1_4" src="https://github.com/user-attachments/assets/b8e99602-1881-4112-9fdc-5316a7cc8231" />

<img width="1316" height="996" alt="1_5" src="https://github.com/user-attachments/assets/b6691e15-0c39-4739-b17e-ef531912a459" />

- **Вопрос**: Что делает политика AdministratorAccess? - Политика AdministratorAccess предоставляет полный доступ ко всем сервисам и ресурсам AWS без ограничений.

---
## Задание 2. Настройка Zero-Spend Budget
После создания бюджета система AWS начала отслеживать расходы аккаунта и отправлять уведомления при превышении лимита расходов в $0.

<img width="1315" height="948" alt="2_1" src="https://github.com/user-attachments/assets/ccf1f18e-fdd9-4cc9-bf13-e0da20dfb12a" />

<img width="1315" height="991" alt="2_2" src="https://github.com/user-attachments/assets/428072e7-7342-48be-a4de-90e0596ef946" />

<img width="1315" height="946" alt="2_3" src="https://github.com/user-attachments/assets/3e92e720-092a-476a-9683-c0d517f816f4" />

---
## Задание 3. Создание и запуск EC2 экземпляра
Для запуска и настройки виртуальной машины используется сервис Amazon EC2.

<img width="1316" height="994" alt="3_1" src="https://github.com/user-attachments/assets/8337e367-e078-4c7c-8b87-9b4f90550fb1" />

<img width="1315" height="947" alt="3_2" src="https://github.com/user-attachments/assets/b8654b5e-4e97-44da-b374-b6a055eed48e" />

<img width="1315" height="944" alt="3_3" src="https://github.com/user-attachments/assets/97b858a9-8460-40e2-b264-9d80b95dc13f" />

<img width="1316" height="945" alt="3_4" src="https://github.com/user-attachments/assets/8d1a73b0-57c3-4cef-9de3-b0e50a9f54c0" />

<img width="1316" height="946" alt="3_5" src="https://github.com/user-attachments/assets/973683f8-765a-43ef-9259-d78391e73f10" />

<img width="1315" height="446" alt="3_6" src="https://github.com/user-attachments/assets/c1dd17db-7ab8-40e7-a73e-f32534451108" />

<img width="1314" height="911" alt="3_7" src="https://github.com/user-attachments/assets/b802048e-8733-4849-899e-ab2739195334" />

<img width="1316" height="995" alt="3_8" src="https://github.com/user-attachments/assets/dbaa3154-0fe1-4898-9574-3ecaf8d61b0c" />

<img width="1315" height="431" alt="3_9" src="https://github.com/user-attachments/assets/3390fff7-4c23-4a1e-ad7c-8f161a77b1c2" />

- **Вопрос**: Что такое User Data и какую роль выполняет данный скрипт? - User Data - это механизм автоматического выполнения команд при первом запуске EC2-инстанса. С помощью данного скрипта автоматически обновлялась система, устанавливались утилиты и запускался веб-сервер Nginx.

- **Вопрос**: Для чего используется nginx? - Nginx используется как веб-сервер для обработки HTTP-запросов и публикации веб-сайтов.

## Задание 4. Логирование и мониторинг
Мониторинг - это важная часть обеспечения надёжности, доступности и производительности ваших экземпляров Amazon EC2 и решений в AWS.

<img width="1315" height="992" alt="4_1" src="https://github.com/user-attachments/assets/119d9662-23ec-4c6a-be2a-253c8f72cd10" />

<img width="1314" height="938" alt="4_2" src="https://github.com/user-attachments/assets/56cceeff-2062-4efb-b05b-5824663fbd77" />

<img width="1314" height="827" alt="4_3" src="https://github.com/user-attachments/assets/305f390c-c6b1-426e-88c6-142b563d76ee" />

<img width="1313" height="993" alt="4_4" src="https://github.com/user-attachments/assets/6bb18fb7-9309-4061-a943-faa89255d4aa" />

<img width="1316" height="990" alt="4_5" src="https://github.com/user-attachments/assets/57179690-7da7-482c-bd4f-9c1b9dda801b" />

- **Вопрос**: В каких случаях важно включать детализированный мониторинг? - Детализированный мониторинг необходим в случаях, когда требуется быстрое обнаружение проблем, мониторинг высокой нагрузки или работа production-сервисов. В этом режиме метрики отправляются каждую минуту.

## Задание 5. Подключение к EC2 по SSH

<img width="1279" height="649" alt="5_1" src="https://github.com/user-attachments/assets/b02f4f1c-4d4f-4bd4-8380-ef0f866e8f2d" />

## Задание 6a. Развёртывание статического веб-сайта

<img width="1138" height="591" alt="6_a_1" src="https://github.com/user-attachments/assets/e1186d10-a07a-4f23-a3b4-dd7b211ffd95" />

<img width="976" height="770" alt="6_a_2" src="https://github.com/user-attachments/assets/40d4f849-25b1-439e-b0ec-4e50bcf0ab5c" />

<img width="553" height="331" alt="6_a_3" src="https://github.com/user-attachments/assets/02519d99-2be9-4af5-a554-f909dd56e482" />

## Задание 6b. Развёртывание веб-сайта на PHP

<img width="789" height="214" alt="6_b_1" src="https://github.com/user-attachments/assets/6c20ba8d-cac6-40ad-a374-b0e8ee845eba" />

<img width="984" height="115" alt="6_b_2" src="https://github.com/user-attachments/assets/2199cbe4-22b1-43b5-a199-f38f62e13698" />

<img width="981" height="451" alt="6_b_3" src="https://github.com/user-attachments/assets/f0b50d23-4828-4114-8de6-ca52522ce464" />

<img width="978" height="479" alt="6_b_4" src="https://github.com/user-attachments/assets/f8ef17fa-3588-4e04-80a8-61f0ee4ea1ae" />

<img width="982" height="180" alt="6_b_5 (2)" src="https://github.com/user-attachments/assets/9bb9f530-105b-4ab3-a6f9-63a2f726e08a" />

<img width="469" height="199" alt="6_b_6" src="https://github.com/user-attachments/assets/a8338015-dedd-4dc7-9818-8bc7df1214cb" />

## Задание 6c. Запуск PHP-приложения в Docker

<img width="978" height="523" alt="6_c_1" src="https://github.com/user-attachments/assets/c0be1e30-4014-4299-bd07-2b0c3edd61d9" />

<img width="978" height="103" alt="6_c_2" src="https://github.com/user-attachments/assets/6285b131-14d1-4326-93c2-07e29b2e8756" />

<img width="991" height="628" alt="6_c_3" src="https://github.com/user-attachments/assets/dae6ff5d-12e8-4eb0-a1ba-bd124dce45a5" />

<img width="987" height="820" alt="6_c_4 (2)" src="https://github.com/user-attachments/assets/ee635f73-5827-4617-95f0-23979e078b3b" />

<img width="516" height="219" alt="6_c_5" src="https://github.com/user-attachments/assets/11647549-f4d9-4010-9066-21a796761119" />

<img width="1305" height="551" alt="6_c_6" src="https://github.com/user-attachments/assets/2be3c8cf-c3bb-44ed-ae8f-460a9382ba1b" />

<img width="1310" height="488" alt="6_c_7" src="https://github.com/user-attachments/assets/79c46101-f913-4ce1-8707-e2ec2437a54f" />

## Задание 7. Завершение работы и удаление ресурсов

<img width="692" height="321" alt="7_1" src="https://github.com/user-attachments/assets/521dd997-0206-4db9-bfcd-296af4703b06" />

- **Вопрос**: Чем «Stop» отличается от «Terminate» - - Stop - виртуальная машина выключается, но все данные и настройки сохраняются. Инстанс можно запустить повторно. Terminate - виртуальная машина полностью удаляется вместе с привязанными ресурсами и восстановить её невозможно.

# Вывод

В ходе лабораторной работы были изучены основные сервисы платформы AWS, включая IAM, Billing, EC2 и CloudWatch. Были получены практические навыки создания пользователей и групп доступа, настройки бюджета для контроля расходов, запуска и администрирования виртуальных машин EC2, настройки веб-сервера Nginx и подключения к серверу по SSH.

Также были освоены базовые методы мониторинга и диагностики состояния EC2-инстансов, а также выполнено развёртывание собственного статического веб-сайта в облачной инфраструктуре AWS.
