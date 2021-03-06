---
title: Предварительные требования для основанных на ASMX примеров кода в Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- примеры кода, сервер проекта, Project Server, программирование, PSI, компиляцию образцов кода, PSI, программирование
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Сведения о создании проектов в Visual Studio с помощью образцов кода на основе ASMX, включенных в справочные разделы Project интерфейса сервера (PSI).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357091"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Предварительные требования для основанных на ASMX примеров кода в Project

Сведения о создании проектов в Visual Studio с помощью образцов кода на основе ASMX, включенных в справочные разделы Project интерфейса сервера (PSI).
  
Многие примеры кода, включенные в библиотеку классов [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) и ссылки на веб-службы, изначально были созданы для SDK Office Project 2007 г. и используются в стандартном формате для веб-служб ASMX. Образцы по-прежнему работают в Project Server 2013 и предназначены для копирования в консольное приложение и выполнения в качестве полного подразделения. Исключения из этого правила отмечаются в примере. 
  
Новые образцы PSI в Project 2013 г. соответствуют формату, использующему Windows связи (WCF). Основанные на ASMX примеры также можно адаптировать для использования служб WCF. В данной статье рассказывается, как использовать данные примеры с веб-службами ASMX. Сведения об использовании образцов с помощью служб WCF см. в примере [Prerequisites for WCF-based code samples in Project.](prerequisites-for-wcf-based-code-samples-in-project.md)
  
> [!NOTE]
> Интерфейс веб-службы ASMX PSI признан нерекомендуемым в Project Server 2013, однако все еще поддерживается. Если клиентская объектная модель (CSOM) включает методы, необходимые для вашего приложения, то новые приложения следует разрабатывать с использованием этой CSOM. CSOM позволяет приложениям работать с Project Online или локальной установкой Project Server 2013. В противном случае, если ваше приложение использует интерфейс PSI, то оно должно использовать интерфейс WCF, что является рекомендуемой технологией для сетевого взаимодействия. Приложения, которые используют интерфейс ASMX или интерфейс WCF, могут работать только для локальной установки Project Server 2013. Дополнительные сведения о CSOM см. в [Project Server 2013 и](project-server-2013-architecture.md) клиентской объектной модели [(CSOM) за Project 2013](client-side-object-model-csom-for-project-2013.md)г. 
  
Перед выполнением примеров кода вам следует настроить среду разработки и само приложение, а также изменить значения общих констант в соответствии с вашей средой.
  
## <a name="setting-up-the-development-environment"></a>Настройка среды разработки
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Настройте тестовую систему Project Server**.
    
   Во время разработки или тестирования всегда используйте тестовую систему Project Server. Даже если ваш код работает идеально, зависимости между проектами, ведение отчетов или другие зависящие от среды факторы могут привести к непредусмотренным последствиям. 
    
   > [!NOTE]
   > Убедитесь, что на сервере вы являетесь допустимым пользователем и имеете достаточно прав на вызовы PSI, используемые вашим приложением. Справочный раздел по каждому методу PSI включает в себя таблицу разрешений Project Server. Например, [Project. Метод QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) требует глобального **разрешения NewProject** и **разрешения SaveProjectTemplate.** 
  
   В некоторых ситуациях может требоваться выполнение удаленной отладки на сервере. Возможно, вам также придется настроить обработщик событий, установив сборку обработщика событий на каждом компьютере Project Server в ферме SharePoint, а затем настроить обработщик событий для экземпляра Project Web App с помощью страницы Project Server Параметры в общем приложении Параметры центрального администрирования SharePoint.
    
2. **Настройте компьютер разработки.**
    
   Обычно доступ к интерфейсу PSI осуществляется по сети. Примеры кода разработаны для запуска на клиенте, находящемся отдельно от сервера, если не указано иное.
    
   1. **Установите правильную версию Visual Studio.** Если не указано иное, то примеры кода написаны на Visual C#. Они могут использоваться с Visual Studio 2010 или Visual Studio 2012. Убедитесь, что установлен самый последний пакет обновления. 
        
   2. **Скопируйте библиотеки DDL Project Server на компьютер разработки.** Скопируйте следующие сборки с компьютера Project Server на `[Program Files]\Microsoft Office Servers\15.0\Bin` компьютер разработки: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll;
      - Microsoft.Office.Project.Server.Library.dll;
        
   3. Дополнительные сведения о том, как компилировать и использовать сборку прокси-сервера ProjectServerServices.dll для веб-служб ASMX в PSI, см. в статье [Использование сборки прокси-сервера PSI и описаний IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Установите файлы IntelliSense.**
    
    Чтобы использовать IntelliSense для классов и участников сборки Project Server, скопируйте обновленные IntelliSense XML-файлы из загрузки SDK Project 2013 г. в тот же каталог, где расположены сборки Project Server. Например, скопируйте файл Microsoft.Office.Project.Server.Library.xml в каталог, где ваше приложение будет устанавливать ссылку на сборку Microsoft.Office.Project.Server.Library.dll.
    
    IntelliSense для веб-служб PSI необходимо создать прокси-сборку PSI с помощью скрипта CompileASMXProxyAssembly.cmd в подпрограмме в загрузке `Documentation\IntelliSense\WSDL` SDK Project 2013 г. Этот скрипт создает основанную на ASMX сборку прокси-сервера ProjectServerServices.dll. Дополнительные сведения см. в файле [ReadMe_IntelliSense] в загружаемом пакете SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Создание приложения и добавление ссылки на веб-службу
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Создайте консольное приложение**.
    
   Когда вы создаете консольное приложение, выберите в раскрывающемся списке диалогового окна **Новый проект** значение **.NET Framework 4**. Вы можете скопировать пример кода PSI в это новое приложение.
    
2. **Добавьте необходимую для ASMX ссылку.**
    
   В обозревателе решений добавьте ссылку на **System.Web.Services** (см. рисунок 1). 
    
   **Рис. 1. Добавление ссылки в Visual Studio**

   ![Добавление ссылки в Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "добавление ссылки в Visual Studio")
  
3. **Скопируйте код**.
    
   Скопируйте полный пример кода в файл Program.cs консольного приложения.
    
4. **Задайте пространство имен для примера приложения**.
    
   Вы можете либо изменить пространство имен, указанное в верхней части примера, на используемое по умолчанию пространство имен приложения, либо изменить используемое по умолчанию пространство имен приложения в соответствии с данным примером. Для изменения используемого по умолчанию пространства имен приложения вы можете изменить свойства приложения.
    
   Например, пример кода [queueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) имеет пространство имен **Microsoft.SDK.Project. Samples.RenameProject**. Если имя проекта Visual Studio имеет значение **RenameProject**, скопируйте пространство имен из файла Program.cs, а затем откройте область **Свойства** проекта (в меню **Проект** выберите **Свойства RenameProject**). На вкладке **Приложение** скопируйте пространство имен в текстовое поле **Пространство имен по умолчанию**. 
    
5. **Задайте веб-ссылки**.
    
   Для большинства примеров требуется ссылка на одну или несколько веб-служб PSI. Они указаны в самом примере или в комментариях перед ним. Чтобы получить правильное пространство имен для веб-ссылок, сначала следует задать пространство имен приложения по умолчанию.
    
   Существует три способа добавить ссылку на веб-службу ASMX для PSI:
    
   - Создайте сборку проксиProjectServerServices.dll PSI, а затем установите ссылку на сборку. Чтобы IntelliSense, рекомендуется добавить ссылку на PSI. См. описание сборки [прокси-IntelliSense PSI.](#pj15_PrerequisitesASMX_BuildingProxy)
    
   - Добавьте файл прокси из выходных данных wsdl.exe в решение Visual Studio. См. статью [Добавление файла прокси PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Добавьте ссылку на веб-службу с помощью Visual Studio. См. статью [Добавление ссылки на веб-службу](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Использование сборки прокси PSI и описаний IntelliSense.

Сборку проксиProjectServerServices.dll для всех веб-служб на основе ASMX в PSI можно создать и использовать с помощью скрипта CompileASMXProxyAssembly.cmd в папке загрузки `Documentation\IntelliSense\WSDL` SDK Project 2013 г. Ссылку на скачивание см. в Project [документации разработчика 2013 г.](project-2013-developer-documentation.md)
  
> [!NOTE]
> При извлечении файлов источника прокси из Source.zip файла файлы в папке актуальны с даты публикации загрузки `Documentation\IntelliSense\WSDL\Source` SDK Project 2013 г. Чтобы создать обновленные исходные файлы прокси PSI, запустите скрипт GenASMXProxyAssembly.cmd на компьютере Project Server. Скрипты в  `Documentation\IntelliSense\WCF` папке не работают для приложений на основе ASMX. Скрипт GenWCFProxyAssembly.cmd вызывает SvcUtil.exe, который создает файлы исходного кода для служб WCF. Файлы прокси WCF включают в себя различные атрибуты, интерфейс канала и класс клиента для каждой службы PSI. Например, основанная на WCF служба Resource включает в себя интерфейс **ResourceChannel**, интерфейс **Resource** и класс **ResourceClient**. Основанная на ASMX веб-служба Resource включает в себя класс **Resource** с немного другими свойствами. 
  
Ниже приведен скрипт GenASMXProxyAssembly.cmd, который создает выходные WSDL-файлы для веб-служб PSI, а затем компилирует сборку.
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

Этот скрипт использует файл ClassList_asmx.txt, который содержит список веб-служб, доступных для сторонних разработчиков.
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

Скрипты создают сборку с именем ProjectServerServices.dll. Не путайте ее с ProjectServerServices.dll для основанной на WCF сборки. Имена сборок не отличаются, чтобы любую из сборок можно было использовать с файлом IntelliSense ProjectServerServices.xml.
  
Скрипты создают одинаковое произвольное пространство имен как для веб-служб ASMX, так и для служб WCF, поэтому файл IntelliSense ProjectServerServices.xml работает с любой из сборок. Например, пространством имен службы Resource в основанной на WCF сборке прокси-сервера и в основанной на ASMX сборке прокси-сервера является **SvcResource**. Вы, конечно же, можете изменять имена пространств имен, однако при этом нужно следить за тем, чтобы они совпадали в сборке прокси-сервера и в файле IntelliSense ProjectServerServices.xml.
  
Если пример кода использует для пространства имен веб-службы PSI другое имя, например **ProjectWebSvc**, для работы IntelliSense вам следует изменить данный пример таким образом, чтобы он использовал **SvcProject** и в результате пространство имен соответствовало сборке прокси-сервера. 
  
Преимущество использования основанной на ASMX сборке прокси-сервера состоит в том, что она включает в себя все пространства имен веб-служб PSI; поэтому вам не нужно создавать несколько веб-ссылок. Другое преимущество заключается в том, что при добавлении файла ProjectServerServices.xml в тот же каталог, где вы задали ссылку на сборку прокси-сервера ProjectServerServices.dll, вы можете получить описания IntelliSense для классов и членов PSI. На рисунке 2 показан текст IntelliSense для метода **Project.QueueCreateProject**. Дополнительные сведения см. в файле [ReadMe_IntelliSense] в папке IntelliSense загрузки SDK Project 2013 г. 
  
**Рис. 2. Использование IntelliSense для метода в веб-службе Project**

![Использование Intellisense для метода в службе PSI]с помощью Intellisense для метода(media/pj15_PrerequisitesASMX_Intellisense.gif "в службе PSI")
  
Недостатки использования этой сборки прокси-сервера заключаются в том, что такое решение больше по размеру, кроме того, вам требуется распространять и устанавливать вместе с ним сборку прокси-сервера. Вам также приходится использовать те же пространства имен, которые указаны в сборке прокси-сервера и файлах IntelliSense, если только вы не измените скрипт и файл IntelliSense ProjectServerServices.xml для использования других пространств имен.
  
### <a name="adding-a-psi-proxy-file"></a>Добавление файла прокси PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Загрузка Project SDK 2013 включает исходные файлы, созданные командой Wsdl.exe для сборки прокси. Исходные файлы находятся Source.zip в  `Documentation\IntelliSense\ASMX` подтекстом. Вместо задания ссылки на сборку прокси-сервера вы можете добавить один или несколько этих исходный файлов в решение Visual Studio. Например, после выполнения скрипта GenASMXProxyAssembly.cmd добавьте файл wsdl.Project.cs в решение. Вместо запуска скрипта вы можете выполнить следующие команды для создания одного исходного файла, например: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Чтобы определить объект **Project** как переменную класса с именем **project**, используйте следующий код. Метод **AddContextInfo** добавляет сведения о контексте в объект **project** для проверки подлинности Windows и проверки подлинности на основе форм. 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> Используете ли вы сборку прокси-сервера PSI или добавляете файл прокси для ссылки на службу Project с именем **SvcProject**, для создания объекта **project** вы воспользуетесь одним и тем же кодом. 
  
### <a name="adding-a-web-service-reference"></a>Добавление ссылки на веб-службу
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Если вы не используете основанную на ASMX сборку прокси-сервера и не добавляете выходной WSDL-файл, вы можете задать одну или несколько индивидуальных веб-ссылок. В следующих действиях покажите, как установить веб-ссылку с помощью Visual Studio 2012.
  
1. В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку на службу**. 
    
2. В диалоговом окне **Добавить ссылку на службу** выберите **Дополнительно**.
    
3. В диалоговом окне **Настройки ссылок на службы** выберите **Добавить веб-ссылку**.
    
4. В **текстовом** поле URL-адреса введите и нажмите `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` **кнопку Введите** или выберите **значок Go.** Если установлен протокол SSL, вам следует использовать вместо протокола HTTP протокол HTTPS. 

   Например, используйте следующий URL-адрес для Project на сайте для `https://MyServer/pwa` Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Или откройте веб-браузер и перейдите к `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` . Сохраните файл в локальном каталоге, например `C:\Project\WebServices\ServiceName.wsdl` . В поле **URL-адрес** диалогового окна **Добавить веб-ссылку** введите протокол файла и путь к этому файлу. Например, введите `file://C:\Project\WebServices\Project.wsdl` . 
    
5. После устранения ссылки введите имя ссылки в текстовом окне **веб-ссылки.** В примерах кода в документации Project 2013 года используется произвольное стандартное имя **Svc _ServiceName._** Например, веб-Project называется **SvcProject** (см. рис. 3). 
    
   **Рис. 3. Добавление ссылки на веб-службу ASMX**

   ![Добавление ссылки веб-службы ASMX](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Добавление ссылки веб-службы ASMX")
  
Для компонентов приложения, которые должны выполняться на компьютере с Project Server, используйте олицетворение или установите более высокий уровень разрешений, используйте ссылку на службу WCF вместо веб-ссылки ASMX. Дополнительные сведения см. в примере кода на [основе WCF](prerequisites-for-wcf-based-code-samples-in-project.md)в Project.
  
## <a name="setting-other-references"></a>Настройка других ссылок
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Серверные приложения часто используют другие службы, например веб SharePoint Server 2013. Если требуются другие службы, это указано в примере.
  
Локальные ссылки для примера кода указаны в операторах **using** в верхней части примера: 
  
1. В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку**.
    
2. Нажмите кнопку **Обзор** и перейдите в расположение, где вы сохранили скопированные ранее библиотеки DLL Project Server. Выберите требуемые библиотеки DLL и нажмите кнопку **ОК**.
    
> [!NOTE]
> Убедитесь, что версии сборки на компьютере разработки точно соответствуют версиям сборки на конечном компьютере Project Server. 
  
## <a name="using-multiple-authentication"></a>Использование нескольких методов проверки подлинности
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Проверка подлинности пользователей локального Project Server, независимо от Windows проверки подлинности или проверки подлинности Форм, происходит с помощью обработки утверждений в SharePoint Server 2013. Многократная проверка подлинности означает, что веб-приложение Project Web App на котором Project Web App, поддерживает проверку подлинности Windows и проверку подлинности на основе форм. Если имеет место указанная ситуация, вызов в веб-службу ASMX, которая использует проверку подлинности Windows, завершится со следующей ошибкой, так как процесс утверждений не может определить, для какого типа пользователей выполнять проверку подлинности:
  
`The server was unable to process the request due to an internal error. . . .`

Чтобы устранить эту проблему с ASMX, все вызовы в методы PSI должны направляться в производный класс, который определен для каждой веб-службы PSI. Этот производный класс также должен использовать класс **SvcLoginWindows.LoginWindows**, чтобы получить файл cookie для производного класса служб PSI. В следующем примере класс **ProjectDerived** является производным от класса **SvcProject.Project**. Этот производный класс добавляет свойство **EnforceWindowsAuth** и переопределяет заголовок веб-запроса для каждого вызова в метод в классе **Project**. Если свойство **EnforceWindowsAuth** имеет значение **true**, метод **GetWebRequest** добавляет заголовок, отключающий проверку подлинности на основе форм. Если **EnforceWindowsAuth** имеет значение **false**, выполнение проверки подлинности на основе форм разрешается.
  
Чтобы использовать следующий пример **ASMXLogon_MultiAuth**, создайте консольное приложение, выполните действия из раздела [Создание приложения и добавление ссылки на веб-службу](#pj15_PrerequisitesASMX_Configure), а затем добавьте файл прокси wsdl.LoginWindows.cs и файл прокси wsdl.Project.cs. Метод **Main** создает экземпляр **project** класса **ProjectDerived**. Этот пример должен использовать производный класс **LoginWindowsDerived** для получения объекта **CookieContainer** для свойства **project.CookieContainer**, которое позволяет отличить проверку подлинности на основе форм от проверки подлинности Windows. После этого объект **project** можно использовать для выполнения вызовов в любой метод в классе **SvcProject.Project**. 
  
> [!NOTE]
> Служба **LoginWindows** необходима только для приложений ASMX в среде с несколькими методами проверки подлинности. В примере **ASMXLogon_MultiAuth** метод **GetLogonCookie** получает файл cookie для объекта **loginWindows**. Для свойства **project.CookieContainer** устанавливается значение **loginWindows.CookieContainer**. 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

Использование производного класса **LoginWindows** и выполнение вызовов PSI с заголовком веб-запроса, отключающим проверку подлинности на основе форм необходимы для приложений, которые выполняются в среде с несколькими методами проверки подлинности. Если Project Server использует только проверку подлинности на основе утверждений, производный класс, добавляющий заголовок веб-запроса, не требуется. Предыдущий пример подходит для использования в обеих средах. 
  
Для приложений, основанных на WCF, используется другое решение. Дополнительные сведения см. в разделе *Использование* нескольких разделов проверки подлинности в разделе Необходимые условия для образцов кода на основе [WCF](prerequisites-for-wcf-based-code-samples-in-project.md)в Project.
  
## <a name="changing-the-values-of-generic-constants"></a>Изменение значений общих констант
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

В большинстве примеров используется одна или несколько переменных, которые необходимо обновить, чтобы пример работал в текущей среде соответствующим образом. В следующем примере при наличии SSL используйте протокол HTTPS вместо протокола HTTP. Замените  _ServerName_ именем используемого сервера. Замените _ProjectServerName_ виртуальным именем каталога сайта Project Server, например PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Все остальные переменные, которые вам следует изменить, или иные предварительные требования указаны в верхней части примера кода.
  
## <a name="verifying-the-results"></a>Проверка результатов
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Получение и интерпретация результатов примера кода не всегда бывает простой задачей. Например, при создании проекта необходимо опубликовать проект, прежде чем он появится на Project центре в Project Web App.
  
Результаты примера кода можно проверить несколькими способами; некоторые из них приведены ниже.
  
- Используйте клиент Project профессиональный 2013 года, чтобы открыть проект с компьютера Project Server и просмотреть нужные элементы.
    
- Просмотр опубликованных проектов на Project центральной странице Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Просмотр журнала Очереди в Project Web App. Откройте страницу Параметры сервера (выберите значок **Параметры** в правом верхнем углу),  а затем выберите мои задания в очереди в разделе **Personal Параметры** ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). В раскрывающемся списке **View** (Просмотр) можно выполнить сортировку по состоянию заданий. Состояние по умолчанию — **Задания в ходе выполнения и с ошибками за прошлую неделю**. 
    
- Используйте страницу Сервер Параметры в Project Web App ( ) для управления всеми заданиями очереди и удаления или принудительной проверки `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` корпоративных объектов. Для доступа к этим ссылкам на странице параметров сервера вы должны обладать правами администратора.
    
- Используйте **Microsoft SQL Server Management Studio**, чтобы выполнить запрос для таблицы в базе данных Project. Например, используйте следующий запрос, чтобы выбрать 200 верхних строк таблицы pub.MSP_WORKFLOW_STAGE_PDPS для отображения информации о страницах сведений о проектах (PDP) в этапах рабочего проекта. 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a>Очистка
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

После тестирования некоторых примеров кода остаются корпоративные объекты и параметры, которые следует удалить или сбросить. Вы можете использовать страницу server Параметры в Project Web App для управления корпоративными данными ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Ссылки на страницу параметров сервера позволяют вам удалить старые элементы, принудительно возвращать проекты, управлять очередью заданий для всех пользователей и выполнять другие административные задачи.
  
Ниже приведено несколько ссылок на страницу параметров сервера, которые вы можете использовать для выполнения стандартных операций очистки после запуска примеров кода:
  
- **Корпоративные настраиваемые поля и таблицы подстановки**
    
- **Управление заданиями в очереди**
    
- **Удаление корпоративных объектов**
    
- **Принудительный возврат корпоративных объектов**
    
- **Типы корпоративных проектов**
    
- **Этапы рабочего процесса**
    
- **Стадии рабочего процесса**
    
- **Страницы сведений о проекте**
    
- **Отчетные периоды**
    
- **Параметры и значения по умолчанию для расписания**
    
- **Классификации строк**
    
Дополнительные параметры управляются SharePoint Server 2013 для каждого экземпляра Project Web App, а не определенной страницей Project Web App Server Параметры. В приложении SharePoint центра администрирования выберите общие приложения  **Параметры,** выберите Управление под **Project Server Параметры,** а затем выберите экземпляр Project Web App в выпадаемом списке на странице Сервер Параметры. Например, выберите **обработчики** событий на стороне сервера, чтобы добавить или удалить обработчики событий для выбранного Project Web App экземпляра. 
  
## <a name="see-also"></a>См. также
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Предварительные требования для примеров кода на основе WCF в Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Использование обезличения с помощью WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Обзор справочника по Project PSI](project-psi-reference-overview.md)
- [Центр по разработке для SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

