---
title: Начало работы с Project Server CSOM и .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Project Server 2013 клиентской объектной модели (CSOM) можно использовать для разработки Project Online и локальных решений с помощью .NET Framework 4. В этой статье описывается создание консольного приложения, использующего CSOM для создания и публикации проектов. После публикации проекта, приложение ожидает службы очередей Project Server завершить действие опубликовать и выводит список опубликованных проектов.
ms.openlocfilehash: 1815122ce824fcd2f9b8c9119346ca02c720ae89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812950"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Начало работы с Project Server CSOM и .NET

Project Server 2013 клиентской объектной модели (CSOM) можно использовать для разработки Project Online и локальных решений с помощью .NET Framework 4. В этой статье описывается создание консольного приложения, использующего CSOM для создания и публикации проектов. После публикации проекта, приложение ожидает службы очередей Project Server завершить действие опубликовать и выводит список опубликованных проектов.
  
Общие сведения о Project Server CSOM посетите страницу [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md). Ссылки на разделы в пространстве имен CSOM в разделе [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Создание проекта CSOM в Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Можно использовать Visual Studio 2010 или Visual Studio 2012 для разработки решений, использующих Project Server CSOM. Project Server CSOM включает в себя три сборки для разработки клиентских приложений, приложений Microsoft Silverlight и Windows Phone 8 приложений с помощью .NET Framework 4. CSOM также включает в себя файл JavaScript для разработки веб-приложений, как описано в [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Можно скопировать CSOM сборки, в которой необходимо на компьютере с Project Server или из загружаемого пакета Project 2013 SDK для удаленной разработки компьютера. Консольное приложение **QueueCreateProject** , описанного в данном разделе не приложение Silverlight или приложении Windows Phone 8, вам потребуется Microsoft.ProjectServer.Client.dll сборки. Так как CSOM не зависит от на основе WCF или на основе ASMX Project Server интерфейса (PSI), не нужно задать ссылку на службу для PSI или использовать пространство имен **Microsoft.Office.Project.Server.Library** . 
  
В приложении **QueueCreateProject** в качестве имени создаваемого проекта и максимального времени ожидания очереди используются аргументы командной строки. В процедуре 1 создается базовое консольное приложение, добавляется подпрограмма анализа командной строки, а также сообщение об использовании, если в командной строке есть ошибки. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Процедура 1. Создание проекта CSOM в Visual Studio

1. Скопируйте сборку Microsoft.ProjectServer.Client.dll из `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` папку на компьютере разработчика. Скопируйте сборку в папку удобным для других Project Server и SharePoint ссылочные сборки, которые будут использовать, такие как `C:\Project\Assemblies`.
    
2. Скопируйте сборки Microsoft.SharePoint.Client.dll и Microsoft.SharePoint.Client.Runtime.dll из той же исходной папки на компьютер разработчика. Сборка Microsoft.ProjectServer.Client.dll зависит от связанных сборок SharePoint.
    
3. В Visual Studio создайте консольное приложение Windows и требуемая версия .NET Framework 4. Например имя приложения QueueCreateProject.
    
   > [!NOTE]
   > Если вы забыли задать требуемую версию, после создания проекта в Visual Studio откройте окно **Свойства QueueCreateProject** в меню **Проект**. На вкладке **Приложение** в раскрывающемся списке **Требуемая версия .NET Framework** выберите **.NET Framework 4**. Не используйте вариант **Клиентский профиль .NET Framework 4**. 
  
4. В обозревателе решений добавьте ссылки на указанные ниже сборки.
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. В файле Program.cs изменение `using` операторы, как показано ниже. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. Добавьте методы анализа аргументов командной строки для имени проекта и укажите время ожидания очереди, отображения сведений об использовании и выхода из приложения (в секундах). Замените основной код в файле Program.cs указанным ниже кодом.
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a>Получение контекста проекта
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

Разработка CSOM требуется **ProjectContext** объект инициализирован с URL-адрес Project Web App. Код в процедуре 2 использует константу **pwaPath** . Если вы планируете использовать в приложении для нескольких экземпляров Project Web App, можно сделать **pwaPath** переменную и добавьте другой аргумент командной строки. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Процедура 2. Получение контекста проекта

1. Добавьте **программы** класс константы и переменные, которые будут использоваться приложением **QueueCreateProject** . В дополнение к Project Web App URL-адрес приложение использует имя типа корпоративного проекта по умолчанию (типа корпоративного проекта), имя проекта, чтобы создать и очереди Максимальное время ожидания в секундах. В этом случае переменная **timeoutSeconds** позволяет проверить, как различные значения времени ожидания влияют на приложение. Объект **ProjectContext** — это основной объект для доступа к CSOM. 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Замените `/* Add calls to methods here to get the project context and create a project. */` комментарий следующим кодом. Инициализируется объект **Microsoft.ProjectServer.Client.ProjectContext** , с помощью URL-адрес Project Web App. Метод **CreateTestProject** и метод **ListPublishedProjects** показаны в процедуру 4 и 5 процедуры. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Получение типа корпоративного проекта
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

В примере приложения **QueueCreateProject** показан выбор типа корпоративного проекта Enterprise Project. Если в сведениях о создании проекта не указан GUID EPT, приложение будет использовать EPT по умолчанию. Метод **GetEptUid** используется методом **CreateTestProject**, описанным в процедуре 4. 
  
Метод **GetEptUid** запрашивает в объекте **ProjectContext** коллекцию объектов **EnterpriseProjectTypes** с указанным именем EPT. После выполнения запроса для переменной **eptUid** задается GUID первого объекта **EnterpriseProjectType** в коллекции **eptList**. Так как имена EPT уникальны, имеется только один объект **EnterpriseProjectType** с указанным именем. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Процедура 3. Получение GUID EPT для нового проекта

- Добавьте метод **GetEptUid** в класс **Program**. 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

Найти GUID EPT можно несколькими способами. Показанный в методе **GetEptUid** запрос эффективен, так как он скачивает только один объект **EnterpriseProjectType**, который соответствует имени EPT. Приведенная ниже альтернативная подпрограмма менее эффективна, так как она скачивает полный список EPT в клиентское приложение и выполняет итерацию по списку. 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

Указанная ниже подпрограмма используются запрос LINQ и лямбда-выражение для выбора объекта EPT, но все равно скачивает все объекты **EnterpriseProjectType**. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Задание сведений о создании и публикация проекта
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

Метод **CreateTestProject** создает объект **ProjectCreationInformation** и указывает сведения, необходимые для создания проекта. Требуется указать GUID и имя проекта. Дату начала, описание проекта и GUID EPT указывать необязательно. 
  
После того как свойства нового проекта заданы, метод **Projects.Add** добавляет его в коллекцию **Projects**. Чтобы сохранить и опубликовать проект, необходимо вызвать метод **Projects.Update**, чтобы отправить сообщение в очередь Project Server и создать проект. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Процедура 4. Задание свойств нового проекта, его создание и публикация

1. Добавьте метод **CreateTestProject** в класс **Program**. Приведенный ниже код создает и публикует проект, но не дожидается завершения задания в очереди. 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. Замените `/* Add code here to wait for the queue. */` комментарий ожидания задания очереди следующим кодом. Процедура ожидает не более указанного **timeoutSeconds** количество секунд или переходит при завершении задания очереди до истечения времени ожидания. Состояния заданий в очереди в разделе [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) . 
    
   Вызывать методы **Load** и **ExecuteQuery** для объекта **QueueJob** необязательно. Если объект **QueueJob** не инициализируется при вызове метода **WaitForQueue**, его инициализирует Project Server. 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a>Перечисление опубликованных проектов
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

Метод **ListPublishedProjects** возвращает коллекцию всех проектов, опубликованных в Project Web App. Если задания очереди, который создает проект в 4 процедуры не завершается успешно, или времени ожидания, новый проект не включены в коллекцию **проектов** . 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Процедура 5. Перечисление опубликованных проектов

1. Добавьте метод **ListPublishedProjects** в класс **Program**. 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. Установите правильное значение для URL-адреса Project Web App, выполните компиляцию приложения **QueueCreateProject** и проверить приложение, как показано 6 процедуры. 
    
## <a name="testing-the-queuecreateproject-application"></a>Тестирование приложения QueueCreateProject
<a name="pj15_GettingStartedCSOM_Testing"> </a>

При первом запуске приложения **QueueCreateProject** тестирования экземпляра Project Web App, особенно если Project Server устанавливается на виртуальной машине, приложение может потребоваться больше времени на выполнение, чем время ожидания очереди по умолчанию из 10 секунд. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Процедура 6. Тестирование приложения QueueCreateProject

1. Откройте окно **Свойств QueueCreateProject** , перейдите на вкладку **отладки** и добавьте следующие аргументы командной строки в разделе **Параметры запуска** :`-n "Test proj 1" -t 20`
    
   Запуск приложения (например, нажмите клавишу **F5**). Если значение времени ожидания будет достаточно длинной, приложение отображает следующие выходные данные (Если других опубликованных проектов в экземпляр Project Web App, они также отображается):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Выполнение другой теста с помощью следующей командной строки, использовать время ожидания очереди 10 секунд по умолчанию.`-n "Test proj 1"`
    
   Так как проект Test proj 1 уже существует, в приложении отобразятся указанные ниже данные.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Выполнение другой теста с помощью следующей командной строки, использовать время ожидания очереди 10 секунд по умолчанию.`-n "Test proj 2"`
    
   Приложение **QueueCreateProject** создаст и опубликует проект Test proj 2. 
    
4. Запустите другого теста с помощью следующей командной строки и задать время ожидания быть для задания очереди для завершения:`-n "Test proj 3" -t 1`
    
   Так как времени ожидания очереди недостаточно, проект не будет создан. В приложении отобразятся приведенные ниже данные.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Измените код, чтобы приложения без ожидания задания очереди. Например, закомментировать код, который ожидает выполнения задания в очереди, за исключением `projCreated = true` строки, как показано ниже. 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. Выполните повторную компиляцию приложения и выполните другого теста с помощью следующей командной строки:`-n "Test proj 4"`
    
   Так как подпрограмма **WaitForQueue** закомментирована, приложение не использует значение времени ожидания по умолчанию. Несмотря на то, что приложение не ждет очереди, в нем может отобразиться проект Test proj 4, если публикация на Project Server будет выполнена достаточно быстро. 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

Обновите страницу центра проектов в Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), чтобы показать опубликованных проектов. На следующем рисунке показана публикацию проектов тестирования.

**Проверка опубликованных проектов в Project Web App**

![Проверка опубликованных проектов в Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Проверка опубликованных проектов в Project Web App")
  
Пример приложения **QueueCreateProject** показано как создать объект project с помощью CSOM с помощью класса **ProjectCreationInformation** , как добавить в проект в коллекцию опубликованные как следует ожидать выполнения задания очереди с с помощью метода **WaitForQueue** , а также для перечисления коллекции опубликованных проектов. 
  
## <a name="complete-code-example"></a>Полный пример кода
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Ниже приведен полный код для примера приложения **QueueCreateProject** . Ссылка на класс [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) также включает код в этом разделе. 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Обновления для разработчиков в Project 2013](updates-for-developers-in-project-2013.md) 
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
    

