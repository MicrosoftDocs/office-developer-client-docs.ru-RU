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
- Примеры кода, project server, Project Server по программированию, PSI, компиляция примеры кода, PSI, программирование
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе ASMX, включенные в разделы справочника по интерфейса Project Server (PSI).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399328"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Предварительные требования для основанных на ASMX примеров кода в Project

Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе ASMX, включенные в разделы справочника по интерфейса Project Server (PSI).
  
Многие из примеров кода, включенных в [библиотеки и веб-службы Project Server 2013 класс ссылаться](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) изначально были созданы для пакета SDK для Office Project 2007 и использовать стандартный формат для веб-службы ASMX. Примеры по-прежнему работают в Project Server 2013 и предназначены для копируются в консольного приложения и запуска в качестве завершения блока. Имеются следующие исключения в образце. 
  
Новые образцы PSI в пакет SDK для Project 2013 соответствует формат, который использует службы Windows Communication Foundation (WCF). Примеры на основе ASMX также можно адаптировать для использования службы WCF. В этой статье показано, как использовать образцы с веб-службы ASMX. Для получения сведений об использовании примеров со службами WCF видеть [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> Интерфейс веб-службы ASMX из PSI рекомендуется использовать в Project Server 2013, но по-прежнему поддерживается. Если клиентской объектной модели (CSOM) содержит методы, которые требуются приложению, необходимо разработать новые приложения с помощью CSOM. CSOM позволяет приложениям для работы с Project Online и локальной установки Project Server 2013. В противном случае — если приложение использует PSI, следует использовать интерфейс WCF, который является технологии, рекомендуется использовать сетевые подключения. Приложения, использующие интерфейс ASMX или WCF интерфейс может работать только для локальных установок Project Server 2013. Дополнительные сведения о CSOM можно [Архитектура Project Server 2013](project-server-2013-architecture.md) и [объектной модели со стороны клиента (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Перед выполнением примеров кода вам следует настроить среду разработки и само приложение, а также изменить значения общих констант в соответствии с вашей средой.
  
## <a name="setting-up-the-development-environment"></a>Настройка среды разработки
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Настройте тестовую систему Project Server**.
    
   Во время разработки или тестирования всегда используйте тестовую систему Project Server. Даже если ваш код работает идеально, зависимости между проектами, ведение отчетов или другие зависящие от среды факторы могут привести к непредусмотренным последствиям. 
    
   > [!NOTE]
   > Убедитесь, что действительный пользователь на сервере и проверьте наличие достаточных разрешений для вызовов PSI, используемые приложением. В разделах, для каждого метода PSI включает в себя таблице разрешения Project Server. Например метод [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) требуется глобальное разрешение **NewProject** и разрешение **SaveProjectTemplate** . 
  
   В некоторых случаях может потребоваться удаленной отладки на сервере. Кроме того, необходимо настроить обработчик событий, установка сборки обработчика событий на каждом компьютере Project Server в ферме SharePoint, а затем настройки обработчика событий для экземпляра Project Web App с помощью страницы параметров Project Server в целом Параметры приложений центра администрирования SharePoint.
    
2. **Настройте компьютер разработчика.**
    
   Обычно вы осуществляете доступ к PSI по сети. Примеры кода предназначены для выполнения на клиенте, который, кроме особо оговоренных случаев, находится отдельно от сервера.
    
   1. **Установите правильную версию Visual Studio.** За исключением того, если не указано иное, примеры кода написаны в Visual C#. Они могут использоваться с Visual Studio 2010 или Visual Studio 2012. Убедитесь, что самым последним пакетом установки. 
        
   2. **Скопируйте DLL-библиотеки Project Server на компьютере разработчика.** Скопируйте следующие сборки из `[Program Files]\Microsoft Office Servers\15.0\Bin` на сервере Project Server на компьютере разработчика: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Дополнительные сведения о том, как компилировать и использовать сборку прокси-сервера ProjectServerServices.dll для веб-служб ASMX в PSI, см. в статье [Использование сборки прокси-сервера PSI и описаний IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Установите файлы IntelliSense.**
    
    Использование описания IntelliSense для классов и членов в Project Server сборки, копия обновленные IntelliSense XML-файлы из пакета SDK Project 2013 Загрузите в ту же папку, где расположены сборки Project Server. Например скопируйте файл Microsoft.Office.Project.Server.Library.xml в каталог, где приложение будет задать ссылку на сборку Microsoft.Office.Project.Server.Library.dll.
    
    Описания IntelliSense для веб-службы PSI требуют создания сборкой PSI прокси-сервера с помощью сценария CompileASMXProxyAssembly.cmd в `Documentation\IntelliSense\WSDL` подкаталог в пакет SDK для Project 2013 для загрузки. Сценарий создает сборки на основе ASMX ProjectServerServices.dll прокси-сервера. Дополнительные сведения содержатся в файле [ReadMe_IntelliSense] в пакет SDK для загрузки. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Создание приложения и добавление ссылки на веб-службу
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Создайте консольное приложение**.
    
   Когда вы создаете консольное приложение, выберите в раскрывающемся списке диалогового окна **Новый проект** значение **.NET Framework 4**. Вы можете скопировать пример кода PSI в это новое приложение.
    
2. **Добавьте необходимую для ASMX ссылку.**
    
   В обозревателе решений добавьте ссылку на **System.Web.Services** (см. рисунок 1). 
    
   **Рис. 1. Добавление ссылки в Visual Studio**

   ![Добавление ссылки в Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Добавление ссылки в Visual Studio")
  
3. **Скопируйте код**.
    
   Скопируйте полный пример кода в файл Program.cs консольного приложения.
    
4. **Задайте пространство имен для примера приложения**.
    
   Вы можете либо изменить пространство имен, указанное в верхней части примера, на используемое по умолчанию пространство имен приложения, либо изменить используемое по умолчанию пространство имен приложения в соответствии с данным примером. Для изменения используемого по умолчанию пространства имен приложения вы можете изменить свойства приложения.
    
   Например образец кода для [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) имеет пространство имен **Microsoft.SDK.Project.Samples.RenameProject**. Если имя проекта Visual Studio **RenameProject**, копирование файла Program.cs пространства имен, а затем откройте панель **свойств** проекта (в меню **проект** выберите пункт **Свойства RenameProject**). На вкладке **приложение** скопируйте пространства имен в текстовом поле **пространство имен по умолчанию** . 
    
5. **Задайте веб-ссылки**.
    
   Для большинства примеров требуется ссылка на одну или несколько веб-служб PSI. Они указаны в самом примере или в комментариях перед ним. Чтобы получить правильное пространство имен для веб-ссылок, сначала следует задать пространство имен приложения по умолчанию.
    
   Существует три способа добавить ссылку на веб-службу ASMX для PSI:
    
   - Построения PSI сборки прокси-сервера с именем ProjectServerServices.dll, а затем установите ссылку на сборку. Чтобы получить IntelliSense, это рекомендуемый способ добавить ссылку на интерфейс PSI. В разделе [использование сборки прокси-сервера PSI и описания IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Добавьте файл прокси из выходных данных wsdl.exe в решение Visual Studio. См. статью [Добавление файла прокси PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Добавьте ссылку на веб-службу с помощью Visual Studio. См. статью [Добавление ссылки на веб-службу](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Использование сборки прокси-сервера PSI и описаний IntelliSense

Можно создавать и использовать сборку ProjectServerServices.dll прокси-сервера для всех на основе ASMX веб-служб в PSI, с помощью сценария CompileASMXProxyAssembly.cmd в `Documentation\IntelliSense\WSDL` папки загружаемого пакета Project 2013 SDK. Ссылка на страницу загрузки [Документация для разработчиков Project 2013](project-2013-developer-documentation.md)см.
  
> [!NOTE]
> При извлечении исходных файлов прокси-сервера из файл Source.zip файл, файлы в `Documentation\IntelliSense\WSDL\Source` папки текущей даты публикации из загружаемого пакета Project 2013 SDK. Для создания обновлено PSI прокси-сервер исходные файлы, запустите сценарий GenASMXProxyAssembly.cmd на сервере Project Server. Скрипты в `Documentation\IntelliSense\WCF` папки не работают для приложений на основе ASMX. Сценарий GenWCFProxyAssembly.cmd вызывает SvcUtil.exe, который создает исходные файлы кода для служб WCF. Файлы прокси-сервера WCF включают различные атрибуты, интерфейс канала и класс клиента для каждой службы PSI. Например службу ресурсов на основе WCF включает в себя интерфейс **ResourceChannel** , интерфейс **ресурсов** и класс **ResourceClient** . В Интернете на основе ASMX ресурсов включает в себя класс **ресурсов** с некоторыми другими свойствами. 
  
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
  
— Это преимущество сборки прокси-сервера на основе ASMX, что она включает в себя все PSI веб-службы пространства имен; Создание нескольких веб-ссылки не нужно. Другое преимущество —, что при добавлении в файл ProjectServerServices.xml в тот же каталог, где нужно задать ссылку на сборку ProjectServerServices.dll прокси-сервера, вы можете получить описания IntelliSense для PSI классы и члены. На рисунке 2 показано текст IntelliSense для метода **Project.QueueCreateProject** . Дополнительные сведения содержатся в файле [ReadMe_IntelliSense] в папке IntelliSense загружаемого пакета Project 2013 SDK. 
  
**Рис. 2. Использование IntelliSense для метода в веб-службе Project**

![Использование Intellisense для метода в службе PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Использование Intellisense для метода в службе PSI")
  
Недостатки использования этой сборки прокси-сервера заключаются в том, что такое решение больше по размеру, кроме того, вам требуется распространять и устанавливать вместе с ним сборку прокси-сервера. Вам также приходится использовать те же пространства имен, которые указаны в сборке прокси-сервера и файлах IntelliSense, если только вы не измените скрипт и файл IntelliSense ProjectServerServices.xml для использования других пространств имен.
  
### <a name="adding-a-psi-proxy-file"></a>Добавление файла прокси PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Загрузить пакет SDK Project 2013 включает в себя исходные файлы, созданные с помощью команды Wsdl.exe для сборки прокси-сервера. Исходные файлы находятся в файл Source.zip в `Documentation\IntelliSense\ASMX` подкаталог. Вместо установки ссылки на сборку прокси-сервера, можно добавить одну или несколько исходных файлов решение Visual Studio. Например после выполнения сценария GenASMXProxyAssembly.cmd, добавьте wsdl. Файл Project.cs в решение. Вместо выполнение скрипта, можно выполните следующие команды для создания одного исходного файла, например: 
  
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

Если не использовать прокси-сервер на основе ASMX сборки или добавить WSDL-файла вывода, можно задать один или несколько отдельных веб-ссылки. Далее показано, как настроить веб-ссылку с помощью Visual Studio 2012.
  
1. В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку на службу**. 
    
2. В диалоговом окне **Добавить ссылку на службу** выберите **Дополнительно**.
    
3. В диалоговом окне **Настройки ссылок на службы** выберите **Добавить веб-ссылку**.
    
4. В текстовом поле **URL-адрес** введите `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, а затем нажмите клавишу **Ввод** или выберите значок **Переход** . Если у вас есть Secure Sockets Layer (SSL) установлен, следует использовать протокол HTTPS вместо протокола HTTP. 

   Например, используйте следующий URL-адрес для службы Project на `https://MyServer/pwa` сайт Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Или, откройте веб-браузер и перейдите к `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Сохраните файл в локальный каталог, таких как `C:\Project\WebServices\ServiceName.wsdl`. В диалоговом окне **Добавление веб-ссылки** для **URL-адреса**, введите протокол файла и путь к файлу. Например, введите `file://C:\Project\WebServices\Project.wsdl`. 
    
5. После ссылки разрешаются, введите имя ссылки в текстовом поле **имя веб-ссылки** . Примеры кода в документации для разработчиков по Project 2013 используйте имя произвольных стандартную ссылку **Svc _имя_службы_**. Например, проект веб-службы с именем **SvcProject** (см). 
    
   **Рис. 3. Добавление ссылки на веб-службу ASMX**

   ![Добавление службы веб-ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Добавление службы веб-ASMX")
  
Для компонентов приложения, которые необходимо выполнить на сервере Project Server применяющих олицетворение, или более высокого разрешения, вместо веб-ASMX использовать ссылки на службу WCF. Для получения дополнительных сведений см [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Настройка других ссылок
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Приложения Project Server часто используют другие службы, такие как веб-служб SharePoint Server 2013. Если требуются другие службы, они указаны в примере.
  
Локальные ссылки для примера кода указаны в операторах **using** в верхней части примера: 
  
1. В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку**.
    
2. Нажмите кнопку **Обзор** и перейдите в расположение, где вы сохранили скопированные ранее библиотеки DLL Project Server. Выберите требуемые библиотеки DLL и нажмите кнопку **ОК**.
    
> [!NOTE]
> Убедитесь, что версии сборки на компьютере разработки точно соответствуют версиям сборки на конечном компьютере Project Server. 
  
## <a name="using-multiple-authentication"></a>Использование нескольких методов проверки подлинности
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Проверка подлинности пользователей локального сервера Project Server, проверка подлинности Windows или проверки подлинности форм по осуществляется с помощью утверждений обработки в SharePoint Server 2013. Несколько проверка подлинности означает, что веб-приложения, где был подготовлен Project Web App поддерживает проверку подлинности Windows и проверка подлинности на основе форм. Если это так, вызов веб-службы ASMX, использующего проверку подлинности Windows завершится с ошибкой из-за ошибки, так как процесс утверждения не может определить, какой тип пользователя для проверки подлинности:
  
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
  
Исправление для приложения на основе WCF отличается. Для получения дополнительных сведений обратитесь к разделу *с использованием нескольких проверки подлинности* в [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Изменение значений общих констант
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

Большинство образцов имеет один или несколько переменных, которые необходимо обновить образец работал надлежащим образом в вашей среде. В следующем примере Если протокол SSL, используйте протокол HTTPS вместо протокола HTTP. Замените _имя сервера_ имя сервера, на котором вы используете. Замените _ProjectServerName_ имя виртуального каталога веб-узла Project Server, например веб-клиента Project. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Все остальные переменные, которые вам следует изменить, или иные предварительные требования указаны в верхней части примера кода.
  
## <a name="verifying-the-results"></a>Проверка результатов
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Получение и интерпретации результатов из примера кода не всегда просто. Например при создании проекта, необходимо опубликовать проект, чтобы оно может отображаться на странице центра проектов в Project Web App.
  
Вы можете проверить результаты примера кода несколькими различными способами, например:
  
- Просмотр элементов, которые будут использовать клиента Project Professional 2013 для откройте проект на сервере Project Server
    
- Просмотр опубликованных проектов на странице центра проектов Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).
    
- Просмотр журнала очереди в Project Web App. Открыть страницу "Параметры сервера" (в верхнем правом углу щелкните значок **Параметры** ), а затем выберите **Мои задания в очереди** в разделе **Личные параметры** ( `https://ServerName/ProjectServerName/MyJobs.aspx`). В раскрывающемся списке **представление** можно сортировать по состояние задания. Состояние по умолчанию — **в ходе выполнения и произошел сбой задания за прошлую неделю**. 
    
- Используйте страницу параметров сервера в Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) для управления заданиями в очереди и удаления или принудительный возврат корпоративных объектов. Необходимо иметь разрешения администратора для доступа к этих ссылок на странице "Параметры сервера".
    
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

После тестирования некоторые примеры кода существует корпоративных объектов и параметров, которые следует удалить или сбросить. На странице "Параметры сервера" в Project Web App можно использовать для управления корпоративными данными ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Ссылки на странице "Параметры сервера" позволяет удалять старые элементы, принудительный возврат проектов, управлять очередь заданий для всех пользователей и выполнять другие задачи администрирования.
  
Ниже приведено несколько ссылок на страницу параметров сервера, которые вы можете использовать для выполнения стандартных операций очистки после запуска примеров кода:
  
- **Корпоративные настраиваемые поля и таблицы подстановки**
    
- **Управление заданиями в очереди**
    
- **Удаление корпоративных объектов**
    
- **Принудительное возвращение корпоративных объектов**
    
- **Типы корпоративных проектов**
    
- **Этапы рабочего процесса**
    
- **Этапы рабочего процесса**
    
- **Страницы сведений о проекте**
    
- **Отчетные периоды времени**
    
- **Параметры и значения по умолчанию для расписания**
    
- **Классификация строк**
    
Дополнительные параметры управляются с SharePoint Server 2013 для каждого экземпляра Project Web App, а не с определенной странице Параметры сервера Project Web App. В приложения центра администрирования SharePoint выберите **Общие параметры приложения**, выберите **Управление** в разделе **Параметры Project Server**и затем в раскрывающемся списке на странице "Параметры сервера" нажмите кнопку экземпляр Project Web App . Например выберите **Обработчики событий на стороне сервера** , чтобы добавить или удалить обработчики событий для выбранного экземпляра Project Web App. 
  
## <a name="see-also"></a>См. также
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Необходимые условия для примеров кода на основе WCF в Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Использование олицетворения с WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Справочный обзор PSI Project](project-psi-reference-overview.md)
- [Центр по разработке для SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

