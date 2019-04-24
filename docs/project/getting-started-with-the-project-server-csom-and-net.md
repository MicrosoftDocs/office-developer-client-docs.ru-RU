---
title: Начало работы с Project Server CSOM и .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Клиентскую объектную модель (CSOM) Project Server 2013 можно использовать для разработки решений Project Online и локальных решений с помощью .NET Framework 4. В этой статье описано создание консольного приложения, использующего CSOM для создания и публикации проектов. После публикации проекта приложение ожидает, пока служба очередей Project Server завершит публикацию, а затем выводит список опубликованных проектов.
localization_priority: Priority
ms.openlocfilehash: b53587ca1959faefdc1b40f08c4adfda4ee11d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360579"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Начало работы с CSOM Project Server и .NET

Клиентскую объектную модель (CSOM) Project Server 2013 можно использовать для разработки решений Project Online и локальных решений с помощью .NET Framework 4. В этой статье описано создание консольного приложения, использующего CSOM для создания и публикации проектов. После публикации проекта приложение ожидает, пока служба очередей Project Server не завершит публикацию, а затем выводит список опубликованных проектов.
  
Общие сведения о CSOM Project Server см. в статье [Обновления для разработчиков решений в Project 2013](updates-for-developers-in-project-2013.md). Справочные материалы по пространству имен CSOM см. в статье [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Создание проекта CSOM в Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Разрабатывать решения, использующие CSOM Project Server, можно в Visual Studio 2010 или Visual Studio 2012. CSOM Project Server включает в себя три сборки для разработки клиентских приложений, приложений Microsoft Silverlight и приложений для Windows Phone 8 с помощью .NET Framework 4. CSOM также включает файл JavaScript для разработки веб-приложений, как описано в статье [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
Вы можете скопировать необходимую сборку CSOM с компьютера с Project Server или из скачанного пакета SDK для Project 2013 на удаленный компьютер разработчика. Консольное приложение **QueueCreateProject**, описанное в этой статье, не является приложением Silverlight или приложением для Windows Phone 8, поэтому вам понадобится сборка Microsoft.ProjectServer.Client.dll. Так как CSOM не зависит от интерфейса Project Server (PSI) на основе WCF или ASMX, добавлять ссылки на службы для PSI или использовать пространство имен **Microsoft.Office.Project.Server.Library** необязательно. 
  
В приложении **QueueCreateProject** в качестве имени создаваемого проекта и максимального времени ожидания очереди используются аргументы командной строки. В процедуре 1 создается базовое консольное приложение, добавляется подпрограмма анализа командной строки, а также сообщение об использовании, если в командной строке есть ошибки. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Процедура 1. Создание проекта CSOM в Visual Studio

1. Скопируйте сборку Microsoft.ProjectServer.Client.dll из папки `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` на компьютер разработчика. Скопируйте сборку в папку с удобным расположением для других сборок Project Server и SharePoint, на которые вы собираетесь ссылаться (например, `C:\Project\Assemblies`).
    
2. Скопируйте сборки Microsoft.SharePoint.Client.dll и Microsoft.SharePoint.Client.Runtime.dll из той же исходной папки на компьютер разработчика. Сборка Microsoft.ProjectServer.Client.dll зависит от связанных сборок SharePoint.
    
3. В Visual Studio создайте консольное приложение Windows и задайте требуемую версию .NET Framework 4. Например, присвойте приложению имя QueueCreateProject.
    
   > [!NOTE]
   > Если вы забыли задать требуемую версию, после создания проекта в Visual Studio откройте окно **Свойства QueueCreateProject** в меню **Проект**. На вкладке **Приложение** в раскрывающемся списке **Требуемая версия .NET Framework** выберите **.NET Framework 4**. Не используйте вариант **Клиентский профиль .NET Framework 4**. 
  
4. В обозревателе решений добавьте ссылки на указанные ниже сборки.
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. В файле Program.cs измените операторы `using`, как показано ниже. 
    
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

При разработке CSOM требуется инициализировать объект **ProjectContext** с помощью URL-адреса Project Web App. В коде в процедуре 2 используется константа **pwaPath**. Если вы планируете использовать приложение для нескольких экземпляров Project Web App, можете сделать **pwaPath** переменной и добавить еще один аргумент командной строки. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Процедура 2. Получение контекста проекта

1. Добавьте константы и переменные класса **Program**, которые будет использовать приложение **QueueCreateProject**. Кроме URL-адреса Project Web App, приложение использует имя типа корпоративного проекта (EPT) по умолчанию, имя создаваемого проекта и максимальное время ожидания очереди в секундах. В этом случае переменная **timeoutSeconds** позволяет проверить влияние различных значений времени ожидания на приложение. Объект **ProjectContext** является основным для доступа к CSOM. 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Замените комментарий `/* Add calls to methods here to get the project context and create a project. */` приведенным ниже кодом. Объект **Microsoft.ProjectServer.Client.ProjectContext** инициализируется с использованием URL-адреса Project Web App. Методы **CreateTestProject** и **ListPublishedProjects** показаны в процедуре 4 и процедуре 5. 
    
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
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Процедура 3. Получение GUID EPT для нового проекта

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

Указанная ниже подпрограмма использует запрос LINQ и лямбда-выражение для выбора объекта EPT, но все равно скачивает все объекты **EnterpriseProjectType**. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Задание сведений о создании и публикация проекта
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

Метод **CreateTestProject** создает объект **ProjectCreationInformation** и указывает сведения, необходимые для создания проекта. Требуется указать GUID и имя проекта. Дату начала, описание проекта и GUID EPT указывать необязательно. 
  
После того как свойства нового проекта заданы, метод **Projects.Add** добавляет его в коллекцию **Projects**. Чтобы сохранить и опубликовать проект, необходимо вызвать метод **Projects.Update**, чтобы отправить сообщение в очередь Project Server и создать проект. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Процедура 4. Задание свойств нового проекта, его создание и публикация

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

2. Замените комментарий `/* Add code here to wait for the queue. */` приведенным ниже кодом, чтобы дождаться завершения задания в очереди. Подпрограмма ожидает завершения в течение указанного времени в секундах (**timeoutSeconds**) или продолжает работу, если задание в очереди завершается раньше. Возможные состояния заданий в очереди см. в статье [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx). 
    
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

Метод **ListPublishedProjects** получает коллекцию всех проектов, опубликованных в Project Web App. Новый проект не включается в коллекцию **Projects**, если задание в очереди, которое создает проект в процедуре 4, не удается выполнить или время его ожидания истекает. 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Процедура 5. Перечисление опубликованных проектов

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

2. Задайте правильное значение для URL-адреса Project Web App, скомпилируйте приложение **QueueCreateProject**, а затем протестируйте его, как описано в процедуре 6. 
    
## <a name="testing-the-queuecreateproject-application"></a>Тестирование приложения QueueCreateProject
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Для первого запуска приложения **QueueCreateProject** в тестовом экземпляре Project Web App, особенно если Project Server установлен на виртуальной машине, приложению может потребоваться больше десяти секунд (время ожидания очереди по умолчанию). 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Процедура 6. Тестирование приложения QueueCreateProject

1. Откройте окно **Свойства QueueCreateProject**, перейдите на вкладку **Отладка**, а затем добавьте следующие аргументы командной строки в раздел **Параметры запуска**: `-n "Test proj 1" -t 20`.
    
   Запустите приложение (например, нажмите клавишу **F5**). Если времени ожидания достаточно, в приложении отобразятся следующие данные (если в экземпляре Project Web App есть другие опубликованные проекты, они также будут показаны):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Чтобы использовать время ожидания очереди по умолчанию (10 с), выполните еще одну проверку со следующими аргументами командной строки: `-n "Test proj 1"`.
    
   Так как проект Test proj 1 уже существует, в приложении отобразятся указанные ниже данные.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Чтобы использовать время ожидания очереди по умолчанию (10 с), выполните еще одну проверку со следующими аргументами командной строки: `-n "Test proj 2"`.
    
   Приложение **QueueCreateProject** создаст и опубликует проект Test proj 2. 
    
4. Задав время ожидания, недостаточное для завершения задания в очереди, выполните еще одну проверку со следующими аргументами командной строки: `-n "Test proj 3" -t 1`.
    
   Так как времени ожидания очереди недостаточно, проект не будет создан. В приложении отобразятся приведенные ниже данные.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Измените код, чтобы приложение не дожидалось завершения задания в очереди. Например, закомментируйте код ожидания очереди (кроме строки `projCreated = true`), как показано ниже. 
    
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

6. Повторно скомпилируйте приложение и выполните еще одну проверку со следующими аргументами командной строки: `-n "Test proj 4"`.
    
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

Обновите страницу центра проектов в Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`), чтобы отобразить опубликованные проекты. На приведенном ниже рисунке видно, что тестовые проекты опубликованы.

**Проверка опубликованных проектов в Project Web App**

![Проверка опубликованных проектов в Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Проверка опубликованных проектов в Project Web App")
  
На примере приложения **QueueCreateProject** мы показали, как создать проект с помощью CSOM, используя класс **ProjectCreationInformation**, добавить проект в опубликованную коллекцию, дождаться завершения задания в очереди с помощью метода **WaitForQueue** и перечислить коллекцию опубликованных проектов. 
  
## <a name="complete-code-example"></a>Полный пример кода
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Ниже приведен полный код приложения **QueueCreateProject**. Ссылка на класс [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) также содержит код в этой статье. 
  
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
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
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

- [Обновления для разработчиков решений в Project 2013](updates-for-developers-in-project-2013.md) 
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
    

