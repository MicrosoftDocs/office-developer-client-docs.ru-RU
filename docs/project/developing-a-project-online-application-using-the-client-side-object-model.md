---
title: Разработка с помощью клиентской объектной модели приложения Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: В этой статье описываются Microsoft Project Online разработки приложений для настольных приложений с помощью .NET Framework 4.0. Приложения, описанного в данной статье извлекает сведения из внешнего размещения сервера.
ms.openlocfilehash: a65dbbdedb371fae9b8f0b99ea113ae38cbaffb5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572881"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>Разработка с помощью клиентской объектной модели приложения Project Online

В этой статье описываются Microsoft Project Online разработки приложений для настольных приложений с помощью .NET Framework 4.0. Приложения, описанного в данной статье извлекает сведения из внешнего размещения сервера. 
  
## <a name="background"></a>Общие сведения

Microsoft Project работы в качестве приложения для настольных систем в начале 1990-х годов. В настоящее время проекта — гораздо более как подтверждающим ее несколько видов:
  
- Project standard edition — это приложения для настольных систем, на котором выполняется как автономное приложение.
    
- Профессиональный выпуск Project — это настольное приложение, которое может взаимодействовать и общего доступа к данным с сервера на больший размер, а также выполнять функциональные возможности, обнаруженных в Project Стандартный выпуск.
    
- Project Online — служба размещенных на ресурсах Майкрософт, которая предоставляет компании с PMO решения по координации усилий и управление проектов, программ и портфелей. Различные предложения, чем выпусков для настольных компьютеров, Project Online для обслуживания и отслеживания сведений о проекте в течение всего жизненного цикла проекта. 
    
- Project Server — это службы, размещенной в enterprise в котором предприятия управляет и защищает сервер, содержащий проект, программы и сведения о портфеля. Project Server, поскольку они защита внутренних, server предлагает проекта, программы и компоненты портфеля ориентированную на внешне размещаемые Project Online в больше возможностей для настройки.
    
Project Online включает три online наборов API: объектной модели со стороны клиента (CSOM), объектная модель JavaScript (JSOM) и представлений состояния (REST). 
  
- Реализация .NET CSOM является предпочтительным интерфейса при разработке приложений Windows, которые взаимодействуют с Project Online клиентов. Типичная сред для приложения, ориентированные на пользователя включают настольных компьютеров Windows и Microsoft Surface устройств. Приложения серверной написан с использованием .NET CSOM могут подключаться к другим серверам для бизнеса логики и источники данных, которые являются внешними по отношению к Project Online. Запросы на извлечение для Project Online используйте систему LINQ как запрос, который содержит ряд улучшений извлечения основные функции.
    
- Интерфейс объектной модели JavaScript (JSOM) обеспечивает поддержку браузеров для надстройки Project Online. Надстройка — это веб-приложения, которые хранятся в Project Online для клиентов. Если требуется запустить надстройку, код для надстройки файлы для загрузки и запущен в браузере на компьютере пользователя. 
    
- Этот интерфейс REST/Odata модель предоставляет связи на основе HTTP, рекомендуется для приложений в средах, отличных от Windows. Конечные точки обмена данными — это объекты на сайте приложения Web Project (PWA). Результаты предоставляют стандартные коды состояния HTTP.
    
В этой статье основное внимание уделяется приложение, использующее интерфейс .NET CSOM.
  
## <a name="prerequisites"></a>Необходимые разрешения

Начать с базовой системы под управлением Windows 10 и добавьте следующие элементы:
  
- .NET framework 4.0 или более поздней версии--используют структуру завершена. Сайт загрузки — это https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- Visual Studio 2013 или более поздней версии — любой выпуск приемлем. Сообщество выпуск Visual Studio 2015 использовалась для разработки учебное приложение. Выпуск сообщества доступном по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- SharePoint Client Components SDK--Project Online и Project Server находятся на основе SharePoint и SharePoint сборки. Клиентские компоненты SharePoint в Visual Studio Professional и корпоративные выпуски включены. Если вы используете Visual Studio сообщества edition, последней версии пакета SDK средств разработчика Office доступна на следующем сайте: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Project Online учетной записи — это предоставляет доступ для размещения сайта. Дополнительные сведения о получении учетной записи Project Online можно https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Проекты на узле размещения, которые заполняются сведения
    
> [!NOTE]
> Стандартный .NET Framework (4.0 или более поздняя версия) — это правильный framework для использования. Не используйте для клиентского профиля .NET Framework 4. 
  
## <a name="develop-the-application"></a>Разработка приложения

При разработке приложения для настольных систем для SharePoint, основной интерфейс — это проект клиентской объектной модели (CSOM). 
  
Вы можете загрузить полный пример в https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.
  
В первых двух разделах рассматриваются основные проблемы: Создание проекта Visual Studio с помощью соответствующего пространства имен и сборки и доступ к серверу размещения. Остальные разделы работают с извлечением информации о через CSOM, из одной и количество объектов. 
  
Получение сведений из узла — это процесс два действия из клиентских приложений. Во-первых приложение указывает и отправляет запросы на извлечение одного или нескольких серверов. Во-вторых приложение выдает уведомление для выполнения запросов, отправленных на сервер. Сервер отвечает, отправляя результаты запроса на клиенте.
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, связывания соответствующие сборки и объявление необходимых пространств имен. Visual Studio содержит несколько типов проектов разработки. 
  
#### <a name="select-a-visual-studio-project"></a>Выбор проекта Visual Studio

1. Запустите Visual Studio и выберите команду **Начать новый проект** на начальной странице. 
    
   Диалоговое окно Новый проект отображает шаблоны доступных приложений и поля данных для любого выбранного шаблона. 
    
2. Для этого приложения укажите следующие элементы. Ключевые слова, на экране иметь атрибут полужирного шрифта:
    
   1. Установленные шаблоны в левой области выберите **C#** => **Windows** => **классического рабочего стола**. 
    
   2. В верхней области центра установите **.NET Framework 4**. 
    
   3. В списке типов приложения в центральной области выберите пункт **Консольное приложение**. 
    
   4. В нижней части укажите имя и расположение проекта и имя решения. 
    
   5. Также в нижней части установите флажок **Создать каталог для решения** . 
    
3. Нажмите **кнопку ОК** , чтобы создать исходный проект. 
    
#### <a name="add-assemblies"></a>Добавление сборок

Решения VS должен сборки ProjectServerClient из Project 2013 SDK, несколько сборки .NET Framework System.Security и сборки из пакета SDK SharePoint.
  
1. В обозревателе решений VS щелкните правой кнопкой мыши элемент ссылки и выберите команду **Добавить ссылку** в контекстном меню. 
    
2. Установите флажок **Microsoft.ProjectServer.Client.dll**. 
    
   При необходимости нажмите кнопку **Обзор...** кнопки в нижней части диалогового окна и перейдите в каталог установки пакета SDK Project 2013 для обнаружения сборки. 
    
3. Нажмите кнопку **ОК**. 
    
4. Добавление пространства имен клиента PrjoctServer CS-файл.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Добавьте пакет SDK для SharePoint 2013 сборки, с помощью консоли диспетчер пакетов NuGet. 
  
1. Выберите в меню Сервис и выберите следующие меню: **средства =\> диспетчер пакетов NuGet =\> консоли диспетчера пакетов**. 
    
2. В консоли диспетчера пакетов, введите следующую команду и нажмите клавишу \<ввод\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   В **Консоли диспетчера пакетов** с описанием результатов команды; и в ссылки проекта в обозревателе решений VS отображаются сборки SharePoint. 
    
3. Добавьте в файл .cs пространств имен:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

System.Security сборка является частью .NET Framework и была установлена с помощью платформы. Пример приложения должен один дополнительные пространство имен, содержащее зашифрованную строку для размещения системы проверки подлинности. После проверки подлинности для доступа проектов для размещения системы. Добавьте пространство имен System.Security файл .cs таким образом:
  
1. В обозревателе решений VS щелкните правой кнопкой мыши элемент ссылки и выберите команду **Добавить ссылку** в контекстном меню. 
    
2. Выберите **сборки =\> Framework** в левой области диалогового окна Диспетчер справочные материалы, после чего проверьте **System.Security**. 
    
3. Нажмите кнопку **ОК**. 
    
4. Добавьте пространство имен System.Security CS-файл:
    
   ```cs
    using System.Security;
   ```

Начало CS-файл должен содержать следующие пространства имен:
  
- Системный
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Подключения к системе узла

Project Online — это приложение SharePoint, поэтому с использованием проверки подлинности SharePoint — это правильный подход. В следующем фрагменте кода подготавливает получить доступ к размещенной среде.
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

Действия по подготовке получить доступ к размещенной среде включают следующие элементы:
  
1. Создать объект context для проектов — это содержится в следующем коде выше. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   Контекст наследуется от других компонентов, позволяя системы для управления контекста объектной модели проектов.
    
2. Определение сайта узла — это делается в следующем коде с выше.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   При создании экземпляра контекста проекты, приложению для предоставления корневого семейства веб-сайтов проектов. Приложение использует подстроки URL-адрес корня проектов. Моментальный снимок вложенным папкам будет выделена с красный прямоугольник на следующем рисунке. Проверка подлинности должна строку с его начала через подстроки «веб-клиента Project». В пример кода, приложение использует строку "https://XXXXXXXX.sharepoint.com/sites/pwa«.
        
   ![Изображение URL-адрес семейства сайтов проектов в рамках красной границей.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Снимок экрана URL-адрес проектов веб-сайтов семейства сайтов в пределах красной границы")
  
3. Поместите пароль в защищенной строки — это делается в следующем коде с выше.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   Учетная запись пользователя и пароль — учетные данные для доступа к сайту узла. 
    
4. Добавьте учетную запись пользователя и пароль в область учетные данные объекта контекста — это делается в следующем коде с выше.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

Контекст инициализированный проекта готова к использованию.
  
### <a name="list-all-published-projects"></a>Список всех опубликованных проектов

Project Online и ProjectServer использовать прокси-серверы для связи с сервером для создания, отчет, обновления и удаления (CRUD) операции. Сервер обрабатывает запросы эффективно и имеет клиента выполните следующие действия в связи с сервером:
  
1. Установите контекст для обмена данными. 
    
   Контекст используется коллекции проектов, а также другие объекты и коллекции через наследование, включая коллекции задачи, семейства назначений, объект рабочей области и настраиваемые поля. 
    
2. Использование объектной модели для указания объекта, семейства сайтов или данные требуется получить.
    
   Этот шаг использует LINQ, как запрос или метод. Спецификации определяет, вы получаете. Часто это действие встраивается в теле метода Load (шаг 3). 
    
3. Загрузка спецификации извлечения на предыдущем шаге, с помощью метода Load() или LoadQuery().
    
   Для загрузки коллекций и объектов, используйте Load(). Для запросов с помощью предложения, такие как «места» и «группировать», используйте LoadQuery(). 
    
4. Выполнение запроса с помощью метода ExecuteQuery().
    
   Метод ExecuteQuery() уведомляет узел, все готово для выполнения запросов. Когда узел получает уведомление, выполняет запросы и отправляет результаты клиенту. 
    
Данные на клиенте приложение может использовать его. В следующем фрагменте кода циклический перебор опубликованных проектов и печатает Id и Name для каждого опубликованного проекта на узле.
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

Выходные данные:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Для выполнения запроса

Использование действий в этом фрагменте кода, приложение получает список проектов в указанную учетную запись на узле размещения. 
  
1. Для проектов, которые перечислены указан ProjectContext. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Укажите элемента для извлечения. 
    
   ```cs
    projContext.Load(projects);
   ```

   С помощью только о том, коллекцию, сервер получает коллекции проектов, заполнение каждого проекта со значениями по умолчанию набор свойств. Доступ к свойствам, которые входят в состав набора свойств по умолчанию предоставляет успешные результаты. Доступ к свойствам, которые не являются частью по умолчанию задайте результаты исключение «Не инициализирован».
    
3. Загрузите запрос (projContext.Load).
    
   Это входит в предыдущем шаге.
    
4. Выполнение запроса (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Получение сведений высокого уровня проекта

Свойства, которые не являются свойства по умолчанию должно быть указано в запросе на сервер. В следующем фрагменте кода загружает контекста семейства проекты как в предыдущем примере. Затем спецификации запрашивает дополнительные свойства не по умолчанию, необходимо включить в результат. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

Инструкция load определяет контекст коллекции проектов и добавляет StartDate, фазы и стадии в результатах запроса. Дополнительные свойства могут быть скалярные, объектов и коллекций. Скалярные элементов возможен непосредственно. Объекты и коллекции требуют дополнительной обработки, как показано в следующем фрагменте кода.
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

Выходные данные первых трех проектов:
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a>Извлечение всех задач в проекте

Каждый проект имеет многих задач. Таким образом помещение задачи для отдельного проекта состоит из следующих компонентов:
  
1. Установите контекст коллекции проектов.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Получение сведений о проекте, включая свойства задачи.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Обратите внимание, что приложение является адресации опубликованных проектов. Контекст для текущего опубликованного проекта — pubProj. 
    
3. Установите контекст для коллекции задачи.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   `pubProj.Tasks` Свойство ссылается на задачи текущего опубликованного проекта. 
    
4. Загрузите спецификацию, чтобы получить коллекцию задач, в том числе соответствующие свойства не по умолчанию.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Выполнение запроса для извлечения коллекций задач с помощью соответствующих свойств.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Информация теперь является локальной. В следующем фрагменте кода обрабатывает семейства сайтов опубликованных задачи, написав сведения на консоль.
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

Выходные данные задачи для одного проекта:
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a>Сведения о доступе на нескольких уровнях

Каждой задачи может иметь один или несколько лиц (известной как ресурс), что обеспечивает до его завершения. Коллекции назначений и ресурсы содержат эти сведения для каждой задачи. 
  
Обработка состоит из следующих компонентов:
  
1. Получение контекста для задачи проекта.
    
2. Создание запроса и загружать запроса для назначений, которые привязаны к задаче. 
    
3. Выполнение запроса для назначений.
    
4. Создание запроса и загрузки запрос на ресурс, связанный с индивидуального назначения. 
    
5. Выполнение запроса для ресурса.
    
> [!NOTE] 
> - Семейства назначений явно запрошено данные с сервера, так как он не является свойством по умолчанию коллекции задачи. Как семейство последующие запрос выполняется для семейства сайтов с сервера по запросу. 
> - Ресурс — это объект. Запрос для назначения включает в себя имя ресурса, связанного с назначением.
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

Выходные данные для задач, 52, 75 и 76 проекта:
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a>Настраиваемые корпоративные поля доступа

Настраиваемые поля существует для Project Online. Это корпоративные поля, которые могут быть связаны с отдельными проекта. В этом разделе описывается, как получить доступ к эти поля. 
  
Настраиваемые поля не включаются в набор по умолчанию свойства, связанные с проектом. Таким образом они должны явные идентификации в спецификации извлечения. Высокоуровневое представление процесса состоит из следующих элементов:
  
1. Переход с помощью его общее имя настраиваемого поля.
    
2. Получение внутреннее имя настраиваемого поля.
    
3. Вернуться к глобального контекста и серверов запросов системы, с помощью внутреннее имя настраиваемого поля.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Переход в настраиваемых полей, извлечение внутреннего имени и используется для запроса системы

Эта задача указывает извлечения, использующего свойство не по умолчанию с помощью одного добавлены подробные сведения.
  
1. Начните с помощью контекста проектов, как описано в начале этой статьи.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Добавьте два элемента для получения запроса по извлечения коллекции проектов в дополнение к другим свойствам не по умолчанию:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   `p => p.IncludeCustomFields` Предложение определяет необходимость использования объекта проекта, который поддерживает настраиваемые поля. 
    
   `p => p.IncludeCustomFields.CustomFields` Предложение запрашивает включения настраиваемых полей базы данных в результатах запроса. Эти сведения используются после получения внутреннее имя настраиваемого поля. 
    
3. Загрузите запрос.
    
   Это входит в предыдущем шаге.
    
4. Выполнение запроса.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Эти сведения на стороне клиента создавайте запрос на извлечение настраиваемых полей, сопоставленных с текущим проектом.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Перейдите в соответствующий настраиваемого поля и получить внутреннее имя поля. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Получить внутреннее имя настраиваемого поля. Высокоуровневая элементы 1 и 2 завершены.
    
7. Вернитесь в контексте проекта и извлечения значения настраиваемого поля.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > Значения настраиваемого поля извлекаются с помощью внутреннее имя в качестве индекса. 
  
Выходные данные из трех проектов, состоящий из кода проекта, имя проекта, имя настраиваемого поля, внутреннее имя настраиваемого поля и значения настраиваемого поля.
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a>См. также

Документация и примеры, связанные с Project Online и разработки приложений с помощью CSOM в разделе [Портал проектов разработки](https://developer.microsoft.com/en-us/project).
    

