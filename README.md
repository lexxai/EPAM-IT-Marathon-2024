# EPAM-IT-Marathon-2024
IT Marathon 2024 from EPAM.  Backend : .NET (C#), FastAPI (Python). Frontend: Angular (JavaScript). DevOPS: (Azure Cloud)

## Опис
<details>
  <summary>Click to expand</summary>
  
![зображення](https://github.com/user-attachments/assets/bed21e23-67b9-423b-b1ee-99d3720097fd)

Онлайн-воркшопи заплановані кожного робочого дня з 23.09 по 04.10 (крім 1.10), початок о 17:00, тривалість — приблизно по 2 години. Один день — один напрям. Трансляція та всі записи будуть доступні до перегляду на YouTube. Зберігайте розклад ;) 

✍️ Участь в ІТ-Марафоні передбачає, що після деяких тем у вас будуть домашні завдання. Результати виконання ми будемо збирати через форми опитування. Після аналізу відповідей ми надамо загальні рекомендації в цьому чаті. 

Після прослуховування всіх воркшопів у вас буде дві опції: 

  1️⃣ Закінчення Марафону через реалізацію проєкту (передбачає отримання диплому про успішне проходження на 60 годин).
  
  2️⃣ Закінчення Марафону через успішне складання фінального тесту (передбачає отримання диплому про успішне завершення на 40 годин). 

  🔗 Посилання на ваш проєкт, а також посилання на репозиторій потрібно буде надати через форму тесту — для цього в опитуванні будуть передбачені відповідні питання. Результат технічного тесту буде відправлено вам на пошту одразу після його проходження. Для отримання диплому про завершення треба набрати 60% або вище. Самі дипломи будуть відправлені трохи пізніше. 

 📌 Правила проходження тесту: 
 
  🔹Кількість спроб: ОДНА❗️
  
  🔹Тип питань: Закриті питання з варіантами відповідей (на основі інформації з воркшопів) 
  
  🔹Кількість питань: 25 
  
  🔹Час: 60 хвилин 

 📌 Вимоги до проєкту: 
   
  🔹Унікальне посилання на ваш веб-додаток. 
  
  🔹Унікальне посилання на репозиторій із вихідним кодом. 
  
  🔹Проєкт розміщено у хмарі. 
  
  🔹Тема проєкту відповідає темі марафону. 
  
  🔹Можна використовувати будь-які мови програмування. 

Ми оберемо найкращі проєкти та покажемо їх на фінальній зустрічі, а також на авторів найцікавіших робіт чекають приємні призи від EPAM Campus! 🎁

</details>


## Домашні завдання 
<details>
  <summary>Click to expand</summary>

### 1. UX/UI Design
<details>
  <summary>Click to expand</summary>
  
![зображення](https://github.com/user-attachments/assets/eaaff3b0-41ad-4677-883b-fe8de60716da)

#### Завдання
  Створіть сторінку 🐶 тваринки для нашого проєкту. 
  
*Вимоги*: 
- Використовуйте компоненти
- Використовуйте Auto layout 
- Використовуйте існуючі шрифти та кольори, щоб ваш дизайн був консистентним.

🖼 Приклади екранів: [Figma file](https://www.figma.com/design/n3NerFxT8TyGzlosEbbE0e/homework_it_marathon?node-id=0-1&node-type=canvas&t=vzkuVaX8Li0OGC23-0)

#### Рішення:

  [Figma file](https://www.figma.com/design/Vo3844B2pQXppfY6OGp45f/homework_it_marathon-(lexxai)?node-id=0-1&t=93DZnEBqlmfCGQ4s-1)

#### Зворотній зв'язок:
  [![зображення](https://github.com/user-attachments/assets/d2b68d1c-12da-4ab3-b416-785a30760db1)](https://shelled-baker-894.notion.site/homework_feed-11740c272e7380f49115dcde5c264a6f)

  
</details>

### 2. Software Architecture. Cloud
<details>
<summary>Click to expand</summary>

![зображення](https://github.com/user-attachments/assets/572b5c41-cfdc-4afa-8917-f59a9919a9a2)

#### Завдання:

1. Створити та налаштувати Azure-акаунт.
2. Ознайомитися з сервісами:
   
- 📌Azure [Web App](https://azure.microsoft.com/en-us/products/app-service/webhttps://azure.microsoft.com/en-us/products/app-service/web)
- 📌Azure [Storage Account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview)
- 📌Azure [DevOps](https://azure.microsoft.com/en-us/products/devops)
- 📌Azure [Mysql Flexible Server](https://learn.microsoft.com/en-us/azure/mysql/flexible-server/overview) 

#### Рішення:

![зображення](https://github.com/user-attachments/assets/6ee23e24-98ee-4301-b731-acad0ec1291d)
</details>


### 3. Web API on .NET

<details>
<summary>Click to expand</summary>

![зображення](https://github.com/user-attachments/assets/21b1015e-9da6-4854-a6bb-d08201e42c64)

#### Завдання:

Реалізувати REST endpoint отримання оголошень з фільтруванням, сортуванням і посторінковим завантаженням. 
 
В ProposalsController реалізувати метод: 
```csharp
   public async Task<ActionResult<DataPage<ProposalDto>>> GetAllProposals( 
       FromQuery(Name = "$top") int? top, 
       FromQuery(Name = "$skip") int? skip, 
       FromQuery(Name = "$filter") string? filter, 
       FromQuery(Name = "$orderby") string? orderby) 
 ```
Цей метод повинен зчитувати з бази даних оголошення, використовуючи надані параметри: 
- `top` - повертає тільки задану кількість перших записів
- `skip` - пропускає задану кількість записів
- `filter` - фільтрує записи (формат фільтра OData)
- `orderby` - сортує записи (формат сортування OData) 
 
Додатково до цього повинна вираховуватись загальна кількість записів, що проходить фільтр. Це потрібно для вирахування кількості сторінок посторінкового завантаження. 

#### Рішення:
[https://github.com/lexxai/it-marathon-v4-net-workshop](https://github.com/lexxai/it-marathon-v4-net-workshop/tree/dev?tab=readme-ov-file#%D1%80%D0%B5%D0%B0%D0%BB%D1%96%D0%B7%D0%B0%D1%86%D1%96%D1%8F)

![зображення](https://github.com/user-attachments/assets/b426df76-5b7c-468a-902d-d32263fde0da)

#### Зворотній зв'язок:

![зображення](https://github.com/user-attachments/assets/25bb6d59-302e-4039-a0f8-6a3f7eb9344f)


</details>

### 4. API Development with Python
<details>
<summary>Click to expand</summary>
  
![зображення](https://github.com/user-attachments/assets/e20988a5-adf0-44ad-9f36-554b58b5cfb3)

  
#### Завдання:

Сконфігурувати та розробити механізм логування подій для чинного функціоналу авторизації в додатку Pet World. 

Треба зробити так, щоб кожен запит до нашого мікросервісу потрапляв у текстовий файл, а також мав в собі час, який витрачено на виконання запиту.

#### Рішення:

[https://github.com/lexxai/EPAM-2024-petworld-python](https://github.com/lexxai/EPAM-2024-petworld-python?tab=readme-ov-file#homework)

![зображення](https://github.com/user-attachments/assets/5adaaf53-b1e1-47f8-aa24-5160a14f7634)

#### Зворотній зв'язок:
...

</details>


### 5. Web Programming
<details>
<summary>Click to expand</summary>
  
![зображення](https://github.com/user-attachments/assets/f7f44258-fadd-4fe0-9b1d-8cdab8962e4f)
  
#### Завдання:
Реалізувати Login сторінку

#### Рішення:

[https://github.com/lexxai/epam-marathon_v4-frontend_homework](https://github.com/lexxai/epam-marathon_v4-frontend_homework?tab=readme-ov-file#home-work)

![зображення](https://github.com/user-attachments/assets/b9142b0e-244b-45b0-8d70-d5ce7c1f502d)

#### Зворотній зв'язок:
![зображення](https://github.com/user-attachments/assets/8e9aed37-e998-4664-8080-560586d3f500)


</details>


### 6. Cloud
<details>
<summary>Click to expand</summary>

![зображення](https://github.com/user-attachments/assets/0f7d409b-82c5-41b0-826e-da469653cc89)

#### Завдання:

Збираємо усе, дописуємо, піднімаємо проєкт.

#### Рішення:

[Див. проєкт.](https://github.com/lexxai/EPAM-IT-Marathon-2024/edit/main/README.md#%D0%BF%D1%80%D0%BE%D1%94%D0%BA%D1%82)

![зображення](https://github.com/user-attachments/assets/939a7836-ce4f-4bd4-9df6-0a8381d02b8f)

</details>
</details>

## Examinator
<details>
<summary>Click to expand</summary>

#### Завдання:

На платформі Examinator обовʼязково потрібно вказати коректні дані в опитнику Survey IT Marathon — імʼя та прізвище 🇬🇧 англійською мовою. Саме ця інформація буде вписана в диплом, тож поставтесь до цього пункту відповідально 🫡

📌 Правила проходження тесту:
- Кількість спроб: одна
- Кількість питань: 25
- Закриті питання з варіантами відповідей
- Час: 60 хвилин
- Для отримання диплому достатньо набрати 60% 

#### Рішення:
![зображення](https://github.com/user-attachments/assets/70f93f81-b089-4ade-b681-d83e96995b15)

</details>

## Проєкт
<details>
<summary>Click to expand</summary>
  
#### Завдання:
📌 Вимоги до проєкту:
1. Унікальне посилання на ваш веб-додаток, а також посилання на репозиторій із вихідним кодом. Нагадуємо, для проєкту можна використовувати будь-які мови програмування.
2. Проєкт розміщено у хмарі.
3. Тема проєкту відповідає темі Марафону.

🎁 Ми оберемо найкращі проєкти. І звісно ж, на авторів найкращих робіт чекають приємні подарунки від [EPAM Campus!](https://t.me/epamuniprogua)

#### Рішення:
##### DevOps:
This directory contains the DevOps components for the IT Marathon project, focusing on infrastructure as code and deployment automation.

The DevOps setup for this project includes:

1. Infrastructure as Code (IaC). 
    <details>  
    <summary>Click to expand</summary>

    Terraform - [https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/terraform](https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/terraform/README_HW.md)

    ![зображення](https://github.com/user-attachments/assets/f427e14f-64d1-4017-af78-5d8776df1ae6)
    </details>

2. Continuous Integration and Continuous Deployment (CI/CD) using Azure DevOps
     <details>  
      <summary>Click to expand</summary>

      Azure DevOps - [https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/azure-devops](https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/azure-devops/README-HW-CICD.md)
   
     ![зображення](https://github.com/user-attachments/assets/217a8406-1c42-4f7f-a576-e90ab92f3259)
     ![зображення](https://github.com/user-attachments/assets/55bc0175-9263-4380-84e3-e270a60b51d0)
     ![зображення](https://github.com/user-attachments/assets/81118090-547d-4dca-9c56-2c1f81212b1f)



     </details>
4. Monitoring and logging setups:
   
    <details>  
    <summary>Click to expand</summary>
    
    - ![зображення](https://github.com/user-attachments/assets/baea3964-f337-465e-ae1b-659f13eeaf52)
    - ![зображення](https://github.com/user-attachments/assets/a0eddffe-2174-4acb-9d88-48ad58be0287)
    - ![зображення](https://github.com/user-attachments/assets/c18c779d-3b10-4a21-9d0d-3a3e1db80924)
    </details>


##### Cайт:
1. Готовий сайт розвернуто з унікальним ім'ям: [https://stitmarathonlexxaiprod.z16.web.core.windows.net](https://stitmarathonlexxaiprod.z16.web.core.windows.net)
     <details>  
      <summary>Click to expand</summary>
      
      ![зображення](https://github.com/user-attachments/assets/7c5143c7-26bd-4ac8-a00c-896152efe004)
      ![зображення](https://github.com/user-attachments/assets/0a559fb8-a219-4c3d-a251-aa91b08c6c44)
      ![зображення](https://github.com/user-attachments/assets/43b69dbb-eba1-435b-9ee3-97efbd3b8a69)
      [Інше...](https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/azure-devops/README-HW-CICD.md#web-site)
     </details>

2. Проєкт розміщено у хмарі Azure.


3. Тема проєкту "Pet World"
4. Проєкт об'єднано з 4-х репозиторіїв котрі були використанні у домашніх завданнях відповідно для:
    - Backend:
      - [.NET (C#)](https://github.com/lexxai/it-marathon-v4-net-workshop)
      - [FastAPI (Python)](https://github.com/lexxai/EPAM-2024-petworld-python)
    - Frontend:
      - [Angular (JavaScript)](https://github.com/lexxai/epam-marathon_v4-frontend_homework)
    - DevOps:
      - [Azure Cloud](https://github.com/lexxai/EPAM-2024-devops/blob/dev/devops/azure-devop)

</details>


#DevOps #Azure #dotNEt #CSHARP #Python #FastAPI #SQL #Terraform #Cloud #Git #CICD #Windows #Linux #Docker #BASH #EPAM #IaC #VM #Grafana #MySQL #pipeline 
