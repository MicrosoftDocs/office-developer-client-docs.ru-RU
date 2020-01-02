---
title: Разработка приложений для Project Online с помощью клиентской объектной модели
manager: lindalu
ms.date: 12/18/2019
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: 'В этой статье описана разработка приложений Microsoft Project Online с помощью .NET Framework 4.0 и CSOM. '
localization_priority: Priority
ms.openlocfilehash: 33ddafe2e3a75039bf55381524accf1a25692885
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825774"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model-csom"></a>Разработка приложений для Project Online с помощью клиентской объектной модели (CSOM)

>[!NOTE] 
>В этой статье описана разработка приложений Microsoft Project Online для использования CSOM. Рекомендуется изучить способ разработки приложений с помощью [нового приложения Project в Интернете](https://developer.microsoft.com/ru-RU/office/blogs/developing-applications-and-reports-using-the-new-project/).
  
## <a name="background"></a>Общие сведения

Программа Microsoft Project стала использоваться в качестве классического приложения в начале 1990-х. На сегодня возможности Project значительно расширились, что подтверждают различные версии данной программы:
  
- Project стандартный — классическое приложение, которое работает как автономное.
    
- Project профессиональный — классическое приложение, которое предоставляет возможности совместного использования данных с сервера и взаимодействия с ними в крупных масштабах, а также может выполнять функции Project стандартный.
    
- Project Online — служба, размещаемая на серверах корпорации Майкрософт, которая предоставляет компаниям решение уровня проектного офиса (PMO) для согласования и управления проектами, программами и портфелями. В отличии от выпусков для настольных систем, Project Online может поддерживать и отслеживать сведения о проекте на протяжении всего его жизненного цикла. 
    
- Project Server — служба, размещаемая на корпоративных серверах. С ее помощью предприятие управляет сведениями о проекте, программе и портфеле, содержащимися на сервере, а также обеспечивает их защиту. В Project Server реализована внутренняя защита сервера и доступны функции с широкими возможностями настройки, ориентированные на проекты, программы и портфели Project Online с внешним размещением.
    
Project Online обладает тремя онлайн-наборами API: клиентской объектной моделью (CSOM), объектной моделью JavaScript (JSOM) и службой передачи репрезентативного состояния (REST). 
  
- Реализация .NET CSOM — это предпочтительный интерфейс при разработке приложений Windows, которые взаимодействуют с клиентами Project Online. Типичные среды, ориентированные на пользователей приложений, включают настольные компьютеры с Windows и устройства Microsoft Surface. Внутренние приложения Project Online, написанные с помощью .NET CSOM, могут подключаться к внешним серверам с бизнес-логикой и источниками данных. В запросах на получение данных из Project Online применяется система запросов по типу LINQ, которая обладает расширенным возможностями в сравнении со стандартными функциями получения.
    
- Интерфейс объектной модели JavaScript (JSOM) обеспечивает поддержку разных браузеров для надстроек Project Online. Надстройка — это веб-приложение, которое хранится в клиенте Project Online. Когда пользователю нужно запустить надстройку, код надстройки скачивается и запускается в браузере на компьютере пользователя. 
    
- Модель REST/Odata обеспечивает связь по протоколу HTTP. Мы рекомендуем применять этот интерфейс для приложений в средах, отличных от Windows. Конечные точки связи — объекты на сайте веб-приложения Project (PWA). В качестве результатов выступают обычные коды состояния HTTP.
    
В этой статье рассматриваются приложения, использующие интерфейс .NET CSOM.
  
## <a name="prerequisites"></a>Предварительные условия

Запустите базовую систему под управлением Windows 10 и добавьте следующие элементы:
  
- .NET Framework 4.0 или более поздний полный выпуск. Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- Visual Studio 2013 или более поздний выпуск. Допустимо использовать любой выпуск. Для разработки примера приложения использовалась среда Visual Studio 2015 Community Edition. Выпуск Community Edition доступен по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- Пакет SDK клиентских компонентов SharePoint. Project Online и Project Server возглавляют список компонентов SharePoint и сборок SharePoint. Клиентские компоненты SharePoint включены в выпуски Visual Studio Professional Edition и Visual Studio Enterprise Edition. Если вы используете выпуск Visual Studio Community Edition, последняя версия пакета SDK для инструментов разработчика Office доступна по адресу https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Учетная запись Project Online. Учетные данные необходимы для доступа к сайту размещения. Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Проекты с данными на сайте размещения.
    
> [!NOTE]
> Рекомендуется использовать стандартную среду .NET Framework (4.0 или более поздний выпуск). Не используйте клиентский профиль .NET Framework 4. 
  
## <a name="develop-the-application"></a>Разработка приложения

При разработке классического приложения для SharePoint предпочтительным интерфейсом выступает клиентская объектная модель (CSOM). 
  
Вы можете скачать [примеры CSOM для Project](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) из коллекции ресурсов для разработчиков Project в Центре разработчиков Office.
  
В первых двух разделах рассказывается об основных проблемах — создании проекта Visual Studio с соответствующим пространством имен и сборками и получении доступа к серверу размещения. В оставшихся разделах рассматривается получение данных с помощью CSOM из одного или нескольких объектов. 
  
Извлечение данных из клиентских приложений выполняется с узла в два этапа. Первый этап: приложение составляет и отправляет серверу один или несколько запросов на получение данных. Второй этап: приложение направляет серверу уведомление на выполнение отправленных запросов. Сервер отвечает на запрос, отправляя результаты клиенту.
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, компоновки соответствующих сборок и объявления требуемых пространств имен. Visual Studio поддерживает нескольких типов проектов разработки. 
  
#### <a name="select-a-visual-studio-project"></a>Выберите проект Visual Studio

1. Запустите Visual Studio и выберите **Создать проект** на начальной странице. 
    
   В диалоговом окне нового проекта перечисляются доступные шаблоны приложений и поля данных для любого выбранного шаблона. 
    
2. Для этого приложения укажите приведенные ниже элементы. На экране появятся ключевые слова с атрибутом Bold.
    
   1. Из установленных шаблонов на левой панели выберите **C#** => **Windows** => **Классическое приложение**. 
    
   2. В верхней части центральной панели выберите **.NET Framework 4**. 
    
   3. В центральной области укажите следующий тип приложения: **Консольное приложение**. 
    
   4. В нижней части укажите имя и расположение проекта, а также имя решения. 
    
   5. Кроме того, в нижней части установите флажок **Создать каталог для решения**. 
    
3. Нажмите кнопку **ОК**, чтобы создать начальный проект. 
    
#### <a name="add-assemblies"></a>Добавление сборок

Для решения VS необходимы следующие сборки: ProjectServerClient из пакета SDK Project 2103, несколько сборок из пакета SDK SharePoint и .NET Framework System.Security.
  
1. В обозревателе решений VS щелкните правой кнопкой мыши по записи "Ссылки" и выберите **Добавить ссылку...** из контекстного меню. 
    
2. Отметьте **Microsoft.ProjectServer.Client.dll**. 
    
   При необходимости нажмите кнопку **Обзор...** в нижней части диалогового окна и перейдите в каталог установки пакета SDK Project 2013, чтобы найти сборку. 
    
3. Нажмите кнопку **ОК**. 
    
4. Добавьте пространство имен PrjoctServer Client в CS-файл.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Добавьте сборку пакета SDK SharePoint 2013 с помощью консоли диспетчера пакетов NuGet. 
  
1. В меню VS "Сервис" выберите следующее: **Сервис =\> Диспетчер пакетов NuGet =\> Консоль диспетчера пакетов**. 
    
2. В консоли диспетчера пакетов введите следующую команду и нажмите клавишу \<ВВОД\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   **Консоль диспетчера пакетов** предоставит описание результатов команды. Номер сборки SharePoint показывается в обозревателе решений VS в ссылках проекта. 
    
3. Добавьте пространство имен в CS-файл:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

Сборка System.Security входит в состав среды .NET Framework и устанавливается вместе с ней. Для примера приложения требуется дополнительное пространство имен, используемое для проверки подлинности при шифровании строк в размещающей системе. После проверки подлинности приложение получает доступ к проектам размещающей системы. Добавьте пространство имен System.Security в CS-файл следующим образом:
  
1. В обозревателе решений VS щелкните правой кнопкой мыши по записи "Ссылки" и выберите **Добавить ссылку...** из контекстного меню. 
    
2. Выберите **Сборки =\> Платформа** в левой части диалогового окна "Диспетчер ссылок", затем установите флажок **System.Security**. 
    
3. Нажмите кнопку **ОК**. 
    
4. Добавьте пространство имен System.Security в CS-файл.
    
   ```cs
    using System.Security;
   ```

Начало CS-файла должно содержать следующие пространства имен:
  
- System;
    
- System.Collections.Generic;
    
- System.Linq;
    
- System.Test;
    
- Microsoft.ProjectServer.Client;
    
- Microsoft.SharePoint.Client;
    
- System.Security.
    
### <a name="connect-to-the-host-system"></a>Подключение к размещающей системе

Project Online — приложение SharePoint, поэтому разумно воспользоваться проверкой подлинности в SharePoint. С помощью указанного ниже фрагмента кода можно подготовить доступ к размещенной среде.
  
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

Действия по подготовке доступа к размещенной среде включают следующие шаги:
  
1. Создайте контекст объекта для проектов. Код для данного действия содержится в предыдущем фрагменте кода. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   Контекст наследуется другими компонентами, позволяя системе управлять контекстом объектной модели проектов.
    
2. Определите сайт размещения. Данное действие выполняется приведенным ниже кодом из предыдущего фрагмента кода.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   При создании экземпляра контекста проектов необходимо предоставить доступ к корню приложения для семейства веб-сайтов проектов. Приложение использует подстроку URL-адреса корня проектов. Снимок этого расположения выделен красным прямоугольником на приведенном ниже рисунке. Для проверки подлинности нужна строка от начала до подстроки "pwa". В листинге кода приложение использует строку "https://XXXXXXXX.sharepoint.com/sites/pwa".
        
   ![Снимок экрана: URL-адрес для семейства веб-сайтов проектов в красной рамке.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Снимок экрана: URL-адрес для семейства веб-сайтов проектов в красной рамке.")
  
3. Поместите пароль в защищенную строку. Данное действие выполняется приведенным ниже кодом из предыдущего фрагмента кода.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   Учетная запись пользователя и пароль — учетные данные для доступа к сайту размещения. 
    
4. Добавьте учетную запись пользователя и пароль к учетным данным контекста объекта. Данное действие выполняется приведенным ниже кодом из предыдущего фрагмента кода.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

Созданный экземпляр контекста проекта готов к использованию.
  
### <a name="list-all-published-projects"></a>Перечисление всех опубликованных проектов

Project Online и ProjectServer используют прокси-серверы для операций создания, отчетности, обновления и удаления (CRUD). Узел/сервер эффективно обрабатывает запросы, а клиент выполняет следующие действия при взаимодействии с сервером:
  
1. Определят контекст для взаимодействия. 
    
   Контекст используется коллекцией проектов, а также другими объектами и коллекциями через наследование, включая коллекции задач, семейства назначений, промежуточные объекты и настраиваемые поля. 
    
2. Используйте объектную модель для получения объекта, коллекции или данных.
    
   На этом шаге используется система LINQ в качестве запроса или метода. Спецификация контролирует получаемые результаты. Часто этот шаг внедряется как основа метода загрузки (шаг 3). 
    
3. Загрузите спецификацию получения из предыдущего шага с помощью метода Load() или LoadQuery().
    
   Для загрузки коллекций и объектов используйте Load(). Для запросов с условиями по типу "where" и "group" используйте LoadQuery(). 
    
4. Выполните запрос, применив метод ExecuteQuery().
    
   Метод ExecuteQuery() уведомляет узел о готовности выполнения запроса или запросов. После получения уведомления узел выполнит запросы и отправит результаты клиенту. 
    
Приложение сможет использовать сведения клиента. Приведенный ниже фрагмент кода выполняет перебор опубликованных проектов и выводит на печать идентификатор и имя каждого опубликованного проекта на узле.
  
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

Вывод:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Создание запроса

Используя действия из предыдущего фрагмента кода, приложение извлечет список проектов указанной учетной записи на сайте размещения. 
  
1. ProjectContext указывается для проектов списка. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Укажите элемент для получения. 
    
   ```cs
    projContext.Load(projects);
   ```

   Если указать только коллекцию, сервер извлечет коллекцию проектов, заполняя каждый проект значениями согласно установленным по умолчанию свойствам. Попытка доступа к свойствам, входящим в набор свойств по умолчанию, приведет к успешным результатам. При попытке доступа к свойствам, которые не входят в набор свойств по умолчанию, отобразится исключение "Не инициализировано".
    
3. Загрузите запрос (projContext.Load).
    
   Загрузка описывается в предыдущем шаге.
    
4. Выполните запрос (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Извлечение сведений верхнего уровня о проекте

Свойства не по умолчанию необходимо указать в запросе к серверу. Приведенный ниже фрагмент кода загружает контекст коллекции проектов, как в предыдущем примере. Затем спецификация запрашивает дополнительные свойства не по умолчанию, чтобы включить их в результат. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

Оператор Load определяет контекст коллекции проектов и добавляет к результатам запроса StartDate, Phase и Stage. Допустимые дополнительные свойства: скаляры, объекты или коллекции. К скалярным элементам можно обращаться напрямую. Для объектов и коллекций нужна дополнительная обработка, как показано в приведенном ниже фрагменте кода.
  
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

Результат выполнения первых трех проектов:
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>Получение всех задач проекта

Каждый проект содержит множество задач. Получение задач одного проекта включает указанные ниже этапы.
  
1. Определите контекст коллекции проектов.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Получите сведения о проекте, включая свойства задач.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Примечание. Приложение обращается к опубликованным проектам. Контекст для текущих опубликованных проектов — pubProj. 
    
3. Определите контекст для коллекции задач.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   Свойство `pubProj.Tasks` ссылается на задачи текущего опубликованного проекта. 
    
4. Загрузите спецификацию для извлечения коллекции задач, включая соответствующие свойства не по умолчанию.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Выполните запрос, чтобы получить коллекцию задач с соответствующими свойствами.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Теперь данные сведения доступны локально. Приведенный ниже фрагмент кода обрабатывает коллекцию опубликованных задач с помощью ввода команд в консоли.
  
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

Результат выполнения задач для одного проекта:
  
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

### <a name="access-information-at-multiple-levels"></a>Доступ к сведениям на нескольких уровнях

Каждая задача может относиться к одному или нескольким людям (другое название — ресурс), способствующим выполнению задачи. Коллекции назначений и ресурсов содержат эти сведения для каждой задачи. 
  
Процесс состоит из следующих этапов:
  
1. Получение контекста для задачи проекта.
    
2. Создание запроса и загрузка запроса для назначений, привязанных к задаче. 
    
3. Выполнение запроса для назначений.
    
4. Создание запроса и загрузка запроса для ресурса, связанного с индивидуальным назначением. 
    
5. Выполнение запроса для ресурса.
    
> [!NOTE] 
> - Коллекция назначений явно указывается при запросе сведений с сервера, так как не относится к свойству по умолчанию для коллекции задач. Последующий запрос выполняется для извлечения коллекции с сервера. 
> - Ресурс — это объект. Запрос назначения содержит имя ресурса, связанного с назначением.
    
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

Результат выполнения для задач 52, 75 и 76 проекта:
  
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

### <a name="access-custom-enterprise-level-fields"></a>Доступ к настраиваемым полям уровня предприятия

Настраиваемые поля доступны в Project Online. Далее приводятся поля уровня предприятия, которые можно связать с отдельным проектом. В этом разделе описано, как получить доступ к этим полям. 
  
Настраиваемые поля не включаются в набор свойств по умолчанию, связанный с проектом. Поэтому их необходимо явно указать в спецификации получения. Высокоуровневое представление процесса состоит из следующих элементов:
  
1. Туннель к настраиваемому полю по его общему имени.
    
2. Получение внутреннего имени настраиваемого поля.
    
3. Возврат к глобальному контексту и опрос системы с помощью внутреннего имени настраиваемого поля.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Туннель к настраиваемому полю возвращает его внутреннее имя, которое используется при опросе системы.

Эта задача определяет получение, при котором используется свойство не по умолчанию, с одной добавленной деталью.
  
1. Начните с использования контекста проекта, как описано в начале этой статьи.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Дополнительно добавьте два элемента к запросу получения коллекций проектов для получения любых свойств не по умолчанию:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   Условие `p => p.IncludeCustomFields` определяет необходимость использования объекта проекта, который поддерживает настраиваемые поля. 
    
   Условие `p => p.IncludeCustomFields.CustomFields` запрашивает включение данных настраиваемого поля в результаты запроса. Эти сведения используются после получения внутреннего имени настраиваемого поля. 
    
3. Загрузите запрос.
    
   Загрузка описана в предыдущем шаге.
    
4. Выполните запрос.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Используйте эти сведения на стороне клиента, чтобы создать запрос для получения настраиваемых полей, связанных с текущим проектом.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Найдите соответствующее настраиваемое поле и получите внутреннее имя поля. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Внутреннее имя настраиваемого поля получено. Высокоуровневые элементы 1 и 2 готовы.
    
7. Вернитесь к контексту проекта и получите значение элемента настраиваемого поля.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > При получении значения настраиваемого поля его внутреннее имя используется в качестве индекса. 
  
Результат выполнения трех проектов содержит идентификатор проекта, имя проекта, имя настраиваемого поля, внутреннее имя настраиваемого поля и значение настраиваемого поля.
  
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

Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/project) в Центре разработчиков Office.
    

