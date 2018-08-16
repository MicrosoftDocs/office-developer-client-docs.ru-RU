---
title: Обновление настраиваемых полей в пакетном режиме и создание сайтов проектов в Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Чтобы помочь пользователям в эффективной Project Online, связанных с нашей службы расширяемость и гибкость, мы добавили два метода для клиентской объектной модели, которые можно использовать в Project Online приложений и рабочих процессов.
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812942"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Пакетное обновление настраиваемых полей и создание сайтов проектов из рабочего процесса в Project Online

Чтобы помочь пользователям в эффективной Project Online, связанных с нашей службы расширяемость и гибкость, мы добавили два метода для клиентской объектной модели, которые можно использовать в Project Online приложений и рабочих процессов.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Массовое обновление настраиваемых полей проекта. Для Project Online только. Доступно только в API-Интерфейс REST.  <br/> |
|**CreateProjectSite** <br/> | Создание сайта проекта. Для Project Online только. Доступно в API-Интерфейс REST, управляемая клиентская объектная модель и JavaScript клиентской объектной модели.  <br/> |
   
Помимо большая гибкость, эти методы также предоставляют значительное улучшение производительности при сохранение и публикация проектов в рабочем процессе. В этой статье описывается, как использовать методы в API-Интерфейс REST и содержит инструкции по созданию рабочего процесса, массового обновления настраиваемых полей и рабочего процесса, который создает сайта проекта.
  
> [!NOTE]
> Для получения дополнительных сведений о вызове API-интерфейсы REST из рабочих процессов SharePoint 2013, видеть [служб с помощью SharePoint REST из рабочего процесса с помощью метода POST](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) и [вызов API SharePoint 2013 Rest из рабочего процесса SharePoint Designer](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Массовое обновление проекта настраиваемых полей из рабочего процесса
<a name="BulkUpdateCustomFields"> </a>

Ранее состояние рабочего процесса может только один настраиваемого поля за раз. Обновление проекта настраиваемого поля во время может привести к низкого уровня для конечных пользователей при пользователей перехода между страницы сведений о проекте. Каждое обновление требуется запроса на отдельном сервере, с использованием действие **Задать поля проекта** , и обновления нескольких настраиваемых полей на высоким уровнем задержки, низкой пропускной способностью сети вызвал необычный накладные расходы. Чтобы устранить эту проблему, мы добавили метод **UpdateCustomFields** API-Интерфейс REST, что позволяет вам массовое обновление настраиваемых полей. Чтобы использовать **UpdateCustomFields**, передайте словарь, содержащий имена и значения настраиваемых полей, которые необходимо обновить.
  
Метод REST, можно найти в следующих конечной точки:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Замените `<site-url>` заполнитель в разделе примеры URL-адрес сайта Project Web App (PWA) и `<guid>` заполнитель с проектом ИД пользователя. 
  
В этом разделе описывается создание рабочего процесса, что массовое обновление настраиваемых полей для проекта. Рабочий процесс выполняет следующие высокоуровневые действия:
  
- Подождите для проекта, который необходимо обновить для получения возврата
    
- Создание набора данных, который определяет все обновления настраиваемого поля проекта
    
- Извлечение проекта
    
- Вызовите **UpdateCustomFields** , чтобы применить обновления настраиваемого поля в проект 
    
- Выполните вход информацию в списке журнала рабочего процесса (если необходимо)
    
- Публикация проекта
    
- Возврат проекта
    
Окончательный начала до конца рабочих процессов выглядит следующим образом:
  
![Рабочий процесс начала до конца] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Рабочий процесс начала до конца")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Создание рабочего процесса, что массовое обновление настраиваемых полей

1. Необязательный атрибут. Сохраните полный URL-адрес проекта в переменной, которые можно использовать во всем рабочего процесса.
    
    ![Хранилище URL-адрес project в переменной] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Хранилище URL-адрес project в переменной")
  
2. Добавление действия **Ожидание события проекта** в рабочем процессе и выберите событие, **при возврате проекта** . 
    
    ![Дождитесь проекта для возврата] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Дождитесь проекта для возврата")
  
3. Создайте словарь **requestHeader** , с помощью действие при **построении словаря** . Для всех вызовов веб-службы в этом рабочем процессе используется один и тот же заголовок запроса. 
    
    ![Создание словаря requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Создание словаря requestHeader")
  
4. Добавьте следующие два элемента словаря.
    
    |Имя|Тип|Значение|
    |:-----|:-----|:-----|
    |Accept  <br/> |Строка  <br/> |приложение/json; OData = verbose  <br/> |
    |Content-Type  <br/> |Строка  <br/> |приложение/json; OData = verbose  <br/> |
   
    ![Добавление заголовков Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Добавление заголовков Accept")
  
5. Создайте словарь **requestBody** , с помощью действие при **построении словаря** . Данным словарем хранит все обновления поля, которые нужно применить. 
    
    Каждое обновление настраиваемого поля требуется четыре строки: (1) метаданных типа поля, ключ (2), (3) значение и тип значения (4).
    
    - **__metadata/тип** Тип поля метаданных. Эта запись не изменяется и используются следующие значения: 
    
       - Имя: customFieldDictionary (i) / __metadata/типа (где **i** — индекс каждого настраиваемого поля в словаре, начиная с 0) 
            
       - Тип: String
            
       - Значение: SP. KeyValue
    
       ![Определение обновления настраиваемого поля] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Определение обновления настраиваемого поля")
  
    - **Ключ** Внутреннее имя настраиваемого поля, в формате: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Внутреннее имя настраиваемого поля можно найти, перейдя к конечной **внутреннееимя** :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       При создании настраиваемых полей вручную, значения будут отличаться от сайта для сайта. Если вы планируете повторно использовать рабочий процесс на нескольких сайтах, убедитесь, что настраиваемого поля идентификаторы верны.
    
    - **Значение** Значение, задаваемое для настраиваемого поля. Для настраиваемых полей, связанных с таблицами подстановки необходимо использовать вместо фактического значения таблицы внутренних имен записей в таблице подстановки. 
    
       Внутреннее имя записи таблицы подстановки можно найти на следующих конечной точки:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Если у вас есть настраиваемого поля таблицы подстановки настроен на прием несколько значений, используйте `;#` для объединения значения (как показано в примере словаре ниже). 
    
    - **Тип значения** Тип настраиваемого поля, которую требуется обновить. 
    
       - Для полей, текст, длительность, флаг и LookupTable используйте Edm.String
    
       - Для полей число используйте Edm.Int32, Edm.Double или любой другой принятия OData числовой тип
    
       - Для поля даты используйте Edm.DateTime
    
       Ниже примере словаря определяет обновления для трех настраиваемых полей. Во-первых, для нескольких значение настраиваемого поля таблицы подстановки, второй — для числового поля и третий — для поля даты. Примечание как шагом **customFieldDictionary** индекса. 
    
       > [!NOTE]
       > Эти значения — только для иллюстрации. Пары ключ значение, которые будут использоваться зависят от данных веб-клиента Project. 
  
       |Имя|Тип|Значение|
       |:-----|:-----|:-----|
       |Тип/__metadata/customFieldDictionary (0)  <br/> |Строка  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (0) аудио- и ключа  <br/> |Строка  <br/> |Настраиваемые\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0) / стоимости  <br/> |Строка  <br/> |Запись\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0) или тип значения  <br/> |Строка  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1) / __metadata/тип  <br/> |Строка  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (1) запись реестра  <br/> |Строка  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) и значений  <br/> |Строка  <br/> |90.5  <br/> |
       |customFieldDictionary (1) или тип значения  <br/> |Строка  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2) / __metadata/тип  <br/> |Строка  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (2) запись реестра  <br/> |Строка  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2)-значение  <br/> |Строка  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2) / тип значения  <br/> |Строка  <br/> |Edm.DateTime  <br/> |
   
       ![Словарь, который определяет обновления настраиваемых полей] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Словарь, который определяет обновления настраиваемых полей")
  
6. Добавление действия **Вызова веб-службы HTTP** для извлечения проекта. 
    
    ![Вызовите метод Checkout] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Вызовите метод Checkout")
  
7. Изменение свойств вызова веб-службы для указания заголовка запроса. Чтобы открыть диалоговое окно " **Свойства** ", щелкните правой кнопкой мыши действие и выберите **Свойства**.
    
    ![Вызов свойства укажите заголовка запроса в веб-службе] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Вызов свойства укажите заголовка запроса в веб-службе")
  
8. Добавление действия **Вызова веб-службы HTTP** для вызова метода **UpdateCustomFields** . 
    
    ![Создать действие вызова веб-службы HTTP] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Создать действие вызова веб-службы HTTP")
  
    Примечание `/Draft/` сегмента в URL-адрес службы. Полный URL-адрес должен выглядеть следующим образом:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Вызовите метод UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Вызовите метод UpdateCustomFields")
  
9. Изменение свойств вызова веб-службы для привязки параметров **RequestHeader** и **RequestContent** словарей, созданной. Кроме того, можно создать новую переменную для хранения **ResponseContent**.
    
    ![Привязка словарей для заголовка запроса и контента] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Привязка словарей для заголовка запроса и контента")
  
10. Необязательный атрибут. Чтение из словаря ответа для проверки состояния задания очереди и записи данных в списке журнала рабочего процесса.
    
    ![Настройка ведения журнала] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Настройка ведения журнала")
  
11. Добавьте вызов веб-службы в конечную точку **публикации** для публикации проекта. Всегда используйте один и тот же заголовок запроса. 
    
    ![Вызовите метод публикации] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Вызовите метод публикации")
  
    ![Вызов свойства для публикации веб-службы] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Вызов свойства для публикации веб-службы")
  
12. Добавьте последний вызов веб-службы в конечную точку **Checkin** возврат проекта. 
    
    ![Вызовите метод Checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Вызовите метод Checkin")
  
    ![Вызов свойства для возврата веб-службы] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Вызов свойства для возврата веб-службы")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Создание сайта проекта из рабочего процесса

Каждый проект может иметь собственный выделенный сайтов SharePoint, где участники группы можно совместно работать, совместно использовать документы, вызывает проблемы и т.д. Ранее, сайты могут быть созданы только автоматически в сначала опубликовать или вручную руководителем проекта в Project Professional или администратором в веб-клиента Project параметров или их может быть отключена.
  
Мы добавили метод **CreateProjectSite** , чтобы вы могли выбрать, когда следует создавать сайты проекта. Это полезно для организаций, которым требуется автоматически создавать их сайты по достижении определенного этапа предварительно определенного рабочего процесса в предложении по проекту, а не при первой публикации. Отсрочка Создание сайта проекта значительно улучшает производительность для создания проекта. 
  
**Необходимых компонентов:** Прежде чем использовать **CreateProjectSite**, параметр **Разрешить пользователям выбирать,** должен быть задан для создания сайта проекта в **Настройках веб-клиента Project** > ** подключенные сайты SharePoint ** > **Параметры**.
  
![Параметр «Разрешить пользователям выбирать» в параметрах веб-клиента Project] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Параметр Разрешить пользователям выбирать в настройках веб-клиента Project")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Создание рабочего процесса, который создает сайта проекта

1. Создание или изменение существующих рабочих процессов и выберите действие, где вы хотите создать сайтов проектов.
    
2. Создайте словарь **requestHeader** , с помощью действие при **построении словаря** . 
    
    ![Создание словаря requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Создание словаря requestHeader")
  
3. Добавьте следующие два элемента словаря.
    
    |Имя|Тип|Значение|
    |:-----|:-----|:-----|
    |Accept  <br/> |Строка  <br/> |приложение/json; OData = verbose  <br/> |
    |Content-Type  <br/> |Строка  <br/> |приложение/json; OData = verbose  <br/> |
   
    ![Добавление заголовков Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Добавление заголовков Accept")
  
4. Добавление действия **Вызова веб-службы HTTP** . Измените тип запроса для использования **POST**и задать URL-адрес в следующем формате:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Построение URI конечной точки CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Построение URI конечной точки CreateProjectSite")
  
    Передайте имя сайта проекта в метод **CreateProjectSite** как строку. Чтобы использовать имя проекта в качестве имени сайта, передайте пустую строку. Необходимо использовать уникальные имена, поэтому следующего сайта проекта, вы создаете будут работать. 
    
5. Изменение свойств вызова веб-службы для привязки параметр **RequestHeader** словаря, созданной. 
    
    ![Привязка словаря для запроса] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Привязка словаря для запроса")
  
## <a name="see-also"></a>См. также

- [Задачи программирования Project](project-programming-tasks.md)
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Рабочие процессы в SharePoint 2013](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    
