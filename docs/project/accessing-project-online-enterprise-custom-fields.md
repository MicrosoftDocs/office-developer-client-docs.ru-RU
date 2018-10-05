---
title: Доступ к корпоративным настраиваемым полям Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online — это служба Office 365, компаний можно расширить для удовлетворения потребностей бизнеса. Одной области расширения — корпоративных настраиваемых полей (ECFs). ECFs, типизированное значение поля, которые можно добавить в проекты, ресурсы и задачи. В следующей таблице перечислены ECFs, связанные с проектами, ресурсы и задачи и обеспечивает пример значение для экземпляра, ECF:'
ms.openlocfilehash: 978fdfbf4ba75382ad85b9f92f8ac4df5c7f97c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401155"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Доступ к корпоративным настраиваемым полям Project Online

Project Online — это служба Office 365, компаний можно расширить для удовлетворения потребностей бизнеса. Одной области расширения — корпоративных настраиваемых полей (ECFs). ECFs, типизированное значение поля, которые можно добавить в проекты, ресурсы и задачи. В следующей таблице перечислены ECFs, связанные с проектами, ресурсы и задачи и обеспечивает пример значение для экземпляра, ECF:
  
|Имя ECF|Тип ECF|Association|Пример значения|
|:-----|:-----|:-----|:-----|
|Выравнивание  <br/> |ТЕКСТ  <br/> |Project  <br/> |Конечный пользователь записи основных статистических и данными о работоспособности, с результатами, которые включают в себя оценки работоспособности и конкретные действия плана достигло предельного лучше работоспособности.  <br/> |
|Оценка риска  <br/> |ТЕКСТ  <br/> |Project  <br/> |Low  <br/> |
|РЕНТАБЕЛЬНОСТЬ ИНВЕСТИЦИЙ  <br/> |НОМЕР  <br/> |Project  <br/> |2.10  <br/> |
|Общие расходы  <br/> |СТОИМОСТЬ  <br/> |Project  <br/> |$1,031,514  <br/> |
|Запуск команды  <br/> |ТЕКСТ  <br/> |Resources  <br/> |Да  <br/> |
|Положение роли  <br/> |ТЕКСТ  <br/> |Resources  <br/> |Инженер-испытатель  <br/> |
|Состояние отметки  <br/> |ФЛАГ  <br/> |Task  <br/> |Нет  <br/> |
|Работоспособности  <br/> |ТЕКСТ  <br/> |Task  <br/> |Не указан  <br/> |
   
ECFs определяются на экземпляр приложения Web Project (PWA), внешние из любого проекта, ресурсу или задаче. Еще они могут стать связанный с проектом, ресурсов или задач. В этой статье представлены вводные взгляд на настраиваемых полей, с помощью примера приложения и основное внимание уделяется извлечение значений ECF. 
  
Вы можете загрузить полный пример в https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
Кроме того Project Online поддерживает локальные настраиваемые поля как только для чтения объектов, относящихся к определенному проекту, ресурсу или задаче. Дополнительные сведения о локальном настраиваемые поля, см https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Фон материалы (en)

Предыдущая статья, [Разработка приложения Project Online с помощью клиентской объектной модели](developing-a-project-online-application-using-the-client-side-object-model.md), представлены основные сведения и начальную ориентацию для разработки приложений с помощью CSOM. Обратитесь в этой статье для следующих элементов:
  
- Общие сведения о проекте, изолированной и облачная выпуски 
    
- Среда разработки (выпуски Visual Studio и библиотеки программного обеспечения)
    
- Проекта установки Visual Studio для приложений .NET с помощью библиотеки CSOM
    
- Подключение к службе Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Начальные сведения (объявления на уровне класса)

Класс для этого приложения определяет два элемента данных: контекст проекта и pwaECF словаря.
  
Объект context проект является частью CSOM проекта и подключается приложение и экземпляр веб-клиента Project. Все запросы к службе использовать контекст проекта.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

Контекст должен конечную точку подключения для создания экземпляра приложения. Конечная точка подключения — это URL-адрес экземпляра веб-клиента Project. 
  
Словарь pwaECF сохранение проекта, ECFs определенные на уровне веб-клиента Project. Словарь использует ECF. Внутреннееимя как ключ и объект CustomField как значение. Словарь появится в методе ListPWACustomFields и затем используется как ссылка в методе Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Метод Main

Метод Main управляет потоком приложения. Как с помощью других приложений, использующих Project Online CSOM Main инициализирует контекст проекта. 
  
1. Получение и списка ECFs в Project Online веб-клиента Project.
    
   В метод ListPWACustomFields реализовать эту функцию.
    
2. Получение проектов с настраиваемыми полями и ненастраиваемых полей.
    
   При получении проектов с ECFs запрос к службе Project Online необходимо включить следующие элементы: 
    
   - **IncludeCustomFields** &ndash; Этот элемент запрашивает службу для возврата коллекции PublishedProjects, где каждый опубликованного проекта включает в себя расширение, который поддерживает настраиваемые поля. Если этот элемент не указан, Project Online возвращает объекты PublishedProject, не содержащих данных настраиваемого поля.
    
   - **IncludeCustomFields.CustomFields** &ndash; этот элемент запрашивает службу для заполнения объектов PublishedProject с данными настраиваемых полей.
    
   Следующий запрос указывает код проекта и имя, а также расширение объекта для настраиваемых полей и значения настраиваемых полей.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Проверьте каждый из проектов.
    
   Объекты проекта, которые используются в этом приложении являются PublishedProject тип, поскольку значения извлекаются и отображаются. 
    
   Если вам потребуется обновить значения данных в один или несколько проектов, выполняет обновление проекта будет извлечено и приложение будет использовать объект DraftProject для получения значения и обновлять проект.
    
4. Доступ к записи ECF для проекта
    
   Каждый экземпляр ECF разделяет значения поля из оставшейся части ECF сведения. Значение поля сохраняется как часть пары "ключ значение". Остальные сведения хранятся в объекте CustomField.
    
   Доступ к значениям ECF в проекте состоит из двух частей:
    
   - Переход по коллекции настраиваемых полей
    
   - Доступ к надлежащему запись, с помощью двух конструкций.
    
   Каждый из проектов хранятся связанные записи ECF в двух местах, перечисляемую коллекцию настраиваемых полей и и значения полей как часть пары "ключ значение". В пары "ключ значение" внутреннееимя — ключ и значение поля — это значение. Используйте словарь для хранения и доступа к значениям поля. 
    
   Свойства ECF, отличных от значений полей, хранятся в объекты CustomField один объект в проекте. Используйте коллекцию настраиваемых полей для доступа к ECFs, связанный с отдельного проекта. 
    
5. Каждый из проектов хранятся связанные ECFs в семействе сайтов, где каждой записи ECF состоит из ключа — внутреннее имя ECF--и объекта, который содержит значение ECF. Перенос словаря для отдельных операций доступа к коллекции. Объявление приводится ниже.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   Значение в записи словаря соответствует типу данных ECF. Объект для каждого ECF сопоставляется один из различных типов. Большинство ECFs используйте простые типы, которые входят в стандартный переменных. В следующем фрагменте показано, что минимальной обработки задействованных для нескольких типов:
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   В таблице подстановки ТЕКСТОВЫХ значений, тем не менее, требует дополнительной обработки. Приложение получает в таблице подстановки соответствующие из службы и выводит экземпляра ECF (с одним или несколькими значениями) путем обхода таблицы подстановки. В следующем фрагменте кода показан обработки ECFs текста, включая простого значения и с помощью таблицы подстановки: 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   Это приложение выводит просто значения; Тем не менее можно получить дополнительные значения из значения данных.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

Метод ListPWACustomFields получает и перечислены ECFs, связанных с проектами. Этот метод перечислены ECFs, зарегистрированные в экземпляре веб-клиента Project, который может быть связано с отдельные проекты. Точка входа для доступа к ECFs используется элемент настраиваемых полей проекта контекста, как показано в следующем запросе:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

Метод не проверяет, чтобы увидеть, использует ли проект конкретных ECF.
  
## <a name="see-also"></a>См. также

- [Портал проекта разработки](https://developer.microsoft.com/en-us/project)
- [Обзор: Корпоративные настраиваемые поля и таблицы подстановки](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Локальные и корпоративные настраиваемые поля](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Добавление и редактирование корпоративных настраиваемых полей в Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

