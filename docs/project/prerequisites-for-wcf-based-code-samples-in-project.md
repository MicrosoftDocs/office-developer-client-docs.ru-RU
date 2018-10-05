---
title: Необходимые условия для примеров кода на основе WCF в Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе WCF, включенные в разделы справочника по интерфейса Project Server (PSI).
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383382"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Необходимые условия для примеров кода на основе WCF в Project

Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе WCF, включенные в разделы справочника по интерфейса Project Server (PSI).
   
Многие из примеров кода на основе WCF, включенных в [библиотеки и веб-службы Project Server 2013 класс ссылаться](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) изначально были созданы для разработчиков документации по Project 2010 и использовать стандартный формат для веб-служб WCF. Примеры по-прежнему работают в Project Server 2013 и предназначены для копируются в консольного приложения и запуска в качестве завершения блока. Имеются следующие исключения в образце. 
  
Примеры кода в документации по Project 2013 для разработчиков, которые не отличаются от примеры, разработанных для Office Project Server 2007 использовать веб-службы ASMX. Примеры на основе ASMX также можно адаптировать для использования службы WCF. В этой статье показано, как использовать образцы со службами WCF. Сведения о том, как использовать образцы с веб-службы ASMX видеть [Необходимые условия для образцов кода на основе ASMX в проекте](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Если клиентской объектной модели (CSOM) содержит методы, которые требуются приложению, необходимо разработать новые приложения с помощью CSOM. CSOM позволяет приложениям для работы с Project Online и локальной установки Project Server 2013. В противном случае — если приложение использует PSI, следует использовать интерфейс WCF, который является технологии, рекомендуется использовать сетевые подключения. Приложения, использующие интерфейс ASMX или WCF интерфейс может работать только для локальных установок Project Server 2013. 
>
> Дополнительные сведения о CSOM можно [Архитектура Project Server 2013](project-server-2013-architecture.md) и [объектной модели со стороны клиента (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Перед запуском примеров кода необходимо настроить среду разработки, настроить приложение, добавить файл конфигурации службы (или настроить службы WCF программными средствами), а также изменить значения универсальных констант, чтобы они соответствовали вашей среде.
  
## <a name="setting-up-the-development-environment"></a>Настройка среды разработки
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Настройка тестовой системы Project Server.**
    
    Во время разработки или тестирования всегда используйте тестовую систему Project Server. Даже если ваш код работает идеально, зависимости между проектами, ведение отчетов или другие зависящие от среды факторы могут привести к непредусмотренным последствиям. 
    
    > [!NOTE]
    > Убедитесь, что действительный пользователь на сервере и проверьте наличие достаточных разрешений для вызовов PSI, используемые приложением. Раздел документации разработчика для каждого метода PSI включает в себя таблице разрешения Project Server. Например метод [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) требуется глобальное разрешение **NewProject** и разрешение **SaveProjectTemplate** . 
  
    В некоторых случаях может потребоваться удаленной отладки на сервере. Кроме того, необходимо настроить обработчик событий, установка сборки обработчика событий на каждом компьютере Project Server в ферме SharePoint, а затем настройки обработчика событий для экземпляра Project Web App с помощью страницы параметров Project Server в целом Параметры приложений центра администрирования SharePoint.
    
2. **Настройте компьютер разработчика.**
    
    Обычно вы осуществляете доступ к PSI по сети. Примеры кода предназначены для выполнения на клиенте, который, кроме особо оговоренных случаев, находится отдельно от сервера.
    
    1. **Установите правильную версию Visual Studio.** За исключением того, если не указано иное, примеры кода написаны в Visual C#. Они могут использоваться с Visual Studio 2010 или Visual Studio 2012. Убедитесь, что самым последним пакетом установки. 
    
    2. **Скопируйте DLL-библиотеки Project Server на компьютере разработчика.** Скопируйте следующие сборки из `[Program Files]\Microsoft Office Servers\15.0\Bin` на сервере Project Server на компьютере разработчика: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Сведения о порядке компиляции и использования сборки прокси ProjectServerServices.dll для служб WCF в PSI см. в разделе [Использование сборки прокси PSI и описаний IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Установите файлы IntelliSense.**
    
    Использование описания IntelliSense для классов и членов в Project Server сборки, копия обновленные IntelliSense XML-файлы из пакета SDK Project 2013 Загрузите в ту же папку, где расположены сборки Project Server. Например скопируйте файл Microsoft.Office.Project.Server.Library.xml в каталог, где приложение будет задать ссылку на сборку Microsoft.Office.Project.Server.Library.dll.
    
    Описания IntelliSense для службы PSI требуют создания сборкой PSI прокси-сервера с помощью сценария CompileWCFProxyAssembly.cmd в `Documentation\IntelliSense\WCF` подкаталог в пакет SDK для Project 2013 для загрузки. Сценарий создает сборки на основе WCF ProjectServerServices.dll прокси-сервера. Дополнительные сведения содержатся в файле .mht [ReadMe_IntelliSense] в пакет SDK для загрузки. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Создание приложения и добавление ссылки на службу
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Создание консольного приложения.**
    
    Когда вы создаете консольное приложение, выберите в раскрывающемся списке диалогового окна **Новый проект** значение **.NET Framework 4**. Вы можете скопировать пример кода PSI в это новое приложение.
    
2. **Добавьте ссылки, необходимые для WCF.**
    
    В обозревателе решений добавьте ссылку на **System.ServiceModel** (см). Веб-приложение будет использовать **System.ServiceModel.Web**.
    
    Также добавьте ссылку на **System.Runtime.Serialization**.
    
    **Рис. 1. Добавление ссылок в Visual Studio для приложения WCF**

    ![Добавление ссылок для WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Добавление ссылок для WCF")
  
3. **Скопируйте код**.
    
    Скопируйте полный пример кода в файл Program.cs консольного приложения.
    
4. **Задайте пространство имен для примера приложения.**
    
    Вы можете либо изменить пространство имен, указанное в верхней части примера, на используемое по умолчанию пространство имен приложения, либо изменить используемое по умолчанию пространство имен приложения в соответствии с данным примером. Для изменения используемого по умолчанию пространства имен приложения вы можете изменить свойства приложения. 
    
    Например образец кода для [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) имеет пространство имен **Microsoft.SDK.Project.Samples.CreateResourceTest**. Если имя проекта Visual Studio **ResourceTest**, копирование файла Program.cs пространства имен, а затем откройте панель **свойств** проекта (в меню **проект** выберите пункт **Свойства ResourceTest**). На вкладке **приложение** скопируйте пространства имен в текстовом поле **пространство имен по умолчанию** . 
    
5. **Установите ссылки на службы.**
    
    Во многих примерах требуются ссылки на одну или несколько служб PSI. Они перечисляются в самом примере или в комментариях перед примером. Чтобы получить правильное пространство имен ссылок на службы, убедитесь, что предварительно было установлено пространство имен по умолчанию для приложения.
    
    Существует три способа добавления ссылки на службу WCF.
    
    - Постройте сборку прокси PSI с именем ProjectServerServices.dll, а затем установите ссылку на эту сборку. См. раздел [Использование сборки прокси PSI и описаний IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Добавьте файл прокси из выходных данных svcutil.exe в решение Visual Studio. См. раздел [Добавление файла прокси PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Добавьте ссылку на службу с помощью Visual Studio. См. раздел [Добавление ссылки на службу](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Использование сборки прокси-сервера PSI и описаний IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Сборки прокси-сервера можно использовать для всех общедоступных служб WCF в PSI. Компиляция сборки ProjectServerServices.dll прокси-сервера с помощью `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` использовать при написании скриптов в пакет SDK для Project 2013 для загрузки, а затем скопируйте сборку прокси-сервера на компьютере разработчика. Скопируйте файл ProjectServerServices.xml для IntelliSense в ту же папку. В Visual Studio задания ссылки на сборку ProjectServerServices.dll прокси-сервера. 
  
Пакетов обновления Project Server и обновления можно обновить файлы прокси-сервера и создание новой сборки прокси-сервера с помощью сценария GenWCFProxyAssembly.cmd в той же папке файл для загрузки пакета SDK. Для ссылки на страницу загрузки пакета SDK документации [Project 2013 для разработчиков](project-2013-developer-documentation.md). Для получения дополнительных сведений обратитесь к разделу [Добавление ссылки на службу](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> При извлечении исходных файлов прокси-сервера из файл Source.zip файл, файлы в `Documentation\IntelliSense\WCF\Source` папки текущей даты публикации из загружаемого пакета Project 2013 SDK. Для создания обновлено PSI прокси-сервер исходные файлы, запустите сценарий GenASMXProxyAssembly.cmd на сервере Project Server. Дополнительные сведения содержатся в разделе [Добавление ссылки на службу](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Скрипты в `Documentation\IntelliSense\ASMX` папки не работают для приложений на основе WCF. Сценарий GenASMXProxyAssembly.cmd вызывает Wsdl.exe, который создает исходные файлы кода для службы ASMX. Файлы прокси-сервер ASMX включают разных классов и свойств. Например веб-службы на основе ASMX ресурсов включает в себя класс **ресурсов** , тогда как службу ресурсов на основе WCF включает интерфейс **ресурсов** , интерфейс **ResourceChannel** и класс **ResourceClient** . 
  
Произвольные пространства имен, созданные как для веб-службы ASMX, так и для службы WCF, одинаковые, поэтому файл ProjectServerServices.xml для IntelliSense работает с любой сборкой. Например, пространство имен службы Resource в сборке прокси на основе WCF и в сборке прокси на основе ASMX — **SvcResource**. Конечно, имена пространств имен можно изменить, но необходимо убедиться, что имена в сборке прокси и в файле IntelliSense ProjectServerServices.xml совпадают.
  
Если в примере кода для пространства имен службы PSI используется другое имя, например **ProjectWebSvc**, то для обеспечения работы IntelliSense необходимо изменить его на **SvcProject**, чтобы это пространство имен соответствовало сборке прокси. 
  
Можно указать следующие преимущества использования сборки прокси на основе WCF.
  
- Можно разрабатывать большинство решений со сборкой прокси на компьютере, отличном от компьютера Project Server. Для настройки отдельной ссылки на службу требуется разработка на компьютере Project Server.
    
- Сборка прокси включает все пространства имен служб PSI, поэтому не придется добавлять несколько файлов прокси.
    
- При добавлении в файл ProjectServerServices.xml в тот же каталог, где нужно задать ссылку на сборку ProjectServerServices.dll прокси-сервера, вы можете получить описания IntelliSense для PSI классы и члены. Для получения дополнительных сведений см [ReadMe_IntelliSense] `Documentation\IntelliSense` папки загружаемого пакета Project 2013 SDK. 
    
**Рис. 2. Использование IntelliSense для метода в службе Resource**

![Использование Intellisense для метода ReadResource] (media/pj15_PrerequisitesWCF_Intellisense.gif "Использование Intellisense для метода ReadResource")
  
Недостаток использования сборки прокси состоит в том, что решение имеет больший размер, и необходимо распространять и устанавливать сборку прокси с решением. Кроме того, необходимо либо использовать одни и те же пространства имен в сборке прокси и в файлах IntelliSense, либо изменить скрипт для построения сборки прокси и изменения файла IntelliSense ProjectServerServices.xml, чтобы он использовал другие пространства имен.
  
### <a name="adding-a-psi-proxy-file"></a>Добавление файла прокси PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Загрузить пакет SDK Project 2013 включает в себя исходные файлы, созданные с помощью команды SvcUtil.exe для сборки прокси-сервера. Исходные файлы находятся в файле файл Source.zip в `Documentation\IntelliSense\WCF` подкаталог. Вместо установки ссылки на сборку прокси-сервера, можно добавить одну или несколько исходных файлов решение Visual Studio. Например чтобы использовать службы проектов и ресурсов, добавьте wcf. Project.cs и wcf. Файлы Resource.cs в решение. 
  
В WCF основной класс в каждой службе PSI определяется интерфейсом и реализуется в классе клиента для доступа к членам. Например, интерфейс **SvcProject.Resource** реализуется в классе **SvcProject.ResourceClient**. Чтобы задать объект **ResourceClient** как переменную класса с именем **resourceClient**, можно использовать следующий код. В этом примере метод **SetClientEndpoints** создает объект **resourceClient**, который использует конечную точку **basicHttp_Project**, заданную в файле app.config. Дополнительные сведения о файле app.config см. в разделе [Добавление файла конфигурации службы](#pj15_PrerequisitesWCF_AddConfig). 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> Независимо от того, используется ли сборка прокси PSI или добавляется файл прокси для ссылки на службу Project с именем **SvcResource**, необходимо применять этот же код для создания и размещения объекта **resourceClient**. 
  
### <a name="adding-a-service-reference"></a>Добавление ссылки службы
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Если не использовать прокси-сервер на основе WCF сборки или добавить файл прокси-сервера для службы PSI, можно задать один или несколько ссылок на отдельные службы непосредственно в Visual Studio. Можно также использовать первого шага следующую процедуру для создания файлов обновленные прокси-сервер, для подготовки к `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` использовать при написании скриптов, включенных в пакет SDK для Project 2013 для загрузки. 
  
> [!NOTE]
> Устанавливать ссылку на службу необходимо в Visual Studio на компьютере Project Server. Вместо непосредственного добавления ссылок на службы в Visual Studio рекомендуется использовать сборку прокси ProjectServerServices.dll или добавлять исходные файлы прокси. 
  
Далее показано, как задать ссылку на службу с помощью Visual Studio 2012 на компьютере под управлением пробную установку Project Server:
  
1. Для доступа к внутренним службам WCF запустите Visual Studio на компьютере Project Server.
    
2. В **обозревателе решений** щелкните правой кнопкой мыши папку **References** (Ссылки), а затем выберите команду **Add Service Reference** (Добавить ссылку на службу). 
    
3. В диалоговом окне **Добавить ссылку на службу** в поле **адрес** введите https://localhost:32843/ _GUID_/psi/ _ServiceName_SVC и затем нажмите клавишу **Ввод**. Замените _идентификатор GUID_ приложения-службы Project Server, например 534c37eb00d74ccfadcecf9827e95239 имя виртуального каталога. Замените _имя_службы_ имя службы, такие как ресурсов (см). 
    
   Имя виртуального каталога службы Project Server можно получить одним из следующих способов.
    
   - Откройте Центр администрирования SharePoint 2013 приложение в браузере. Выберите **Управление приложениями-службами**, а затем выберите необходимое приложение службы PSI Project Server. Например выберите **ProjectServerService**. URL-адрес страницы Управление сайтами Project Web App содержит имя виртуального каталога. Например, в `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, — это имя виртуального каталога `534c37eb00d74ccfadcecf9827e95239` (имя каталога содержит без штрихов). 
    
   - Откройте диалоговое окно **диспетчера служб IIS** на компьютере Project Server. Разверните узел **Веб-службы SharePoint** в области **Подключения**, а затем разворачивайте виртуальные каталоги службы, пока не найдете каталог, включающий папку PSI. Выберите этот каталог, затем в области **Действия** выберите пункт **Дополнительные параметры** и скопируйте имя каталога в поле **Виртуальный путь**. 
    
      > [!NOTE]
      > Может быть более одного виртуального каталога службы Project Server. Вы можете виртуального каталога, содержащую экземпляр Project Web App, которое требуется проверьте. 
  
   - Командлет **get-SPServiceApplication** в Windows PowerShell, который устанавливается вместе с SharePoint 2013. В меню **Пуск** панели задач выберите пункт **Все программы**, выберите **Продукты Microsoft SharePoint 2013**и выберите пункт **Командная консоль SharePoint 2013**. Вот команда и результаты в окне **Командная консоль 2013get - SharePoint** для приложений-служб определенный (вашей GUID будет отличаться). Скопируйте идентификатор GUID для приложения-службы Project Server. 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Если известно полное имя приложения-службы Project Server, с его помощью можно получить значение GUID, например:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Удалите дефисы в GUID, чтобы получить имя виртуального каталога. 
  
   URL-адреса, такие как `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` являются стандартными для службы Project Server. 
    
4. После разрешает ссылку на службу, введите имя ссылки в текстовом поле **пространство имен** . Примеры кода в документации для разработчиков по Project 2013 используйте произвольных пространства имен **Svc _имя_службы_**. Например службу ресурсов в примерах кода называется **SvcResource**.
    
    **Рис. 3. Добавление ссылки на службу Resource на основе WCF**

    ![Добавление ссылки на службу ресурсов на основе WCF] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Добавление ссылки на службу ресурсов на основе WCF")
  
5. Замените файл web.config временные в каталоге службы Project исходной (переименовывается в файл web.config), а затем перезапустите `iisreset`.
    
## <a name="setting-other-references"></a>Настройка других ссылок
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Приложения Project Server часто используют другие службы, такие как веб-служб SharePoint 2013. Если требуются другие службы или справочные материалы, они указаны в примере кода.
  
Локальные ссылки на примеры кода, перечислены в операторы **using** в верхней части примера. 
  
1. В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку**.
    
2. Нажмите кнопку **Обзор**, а затем найдите расположение, в котором сохранены ранее скопированные библиотеки DLL Project Server. Выберите нужные библиотеки DLL и нажмите кнопку **ОК**.
    
> [!NOTE]
> Убедитесь, что версии сборок на компьютере разработки точно соответствуют версиям на целевом компьютере Project Server. 
  
## <a name="adding-a-service-configuration-file"></a>Добавление файла конфигурации службы
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Если приложение настраивает службы WCF программными средствами, то оно не использует файл конфигурации службы. В противном случае приложение Windows или консольное приложение использует элемент **system.serviceModel** в файле app.config; веб-приложение включает **system.serviceModel** в web.config. Дополнительные сведения об использовании файла app.config и о настройке служб WCF программными средствами см. в пошаговом руководстве [Разработка приложений PSI с использованием WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
При создании исходный файл службы прокси-сервера, команда SvcUtil.exe также создает файл output.config, который является основой для элемента **system.serviceModel** по умолчанию в файле app.config или файла web.config. Загрузить пакет SDK Project 2013 загружается пример файла output.config в `Documentation\IntelliSense\WCF\Source.zip`. Например файл output.config по умолчанию, который создает SvcUtil.exe для службы ресурсов включает в себя две привязки, с именем **BasicHttpBinding_Resource** и **BasicHttpBinding_Resource1**. Элемент **клиента** включает в себя две конечные точки по умолчанию. — Это одна конечная точка для безопасного доступа к адрес HTTP через порт 32843, а другое — для обычного доступа через порт 32843, как показано ниже: 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

В конфигурации службы PSI не используются привязки и конечные точки по умолчанию. В Project Server требуется, чтобы приложения получали доступ к службам PSI через внутренний файл ProjectServer.svc, который действует как маршрутизатор для вызовов внутренних служб. Чтобы создать файл app.config, выполните следующие действия.
  
1. Если задать ссылку на сборку ProjectServerServices.dll прокси-сервера или добавить исходный файл прокси-сервера для службы, приложения не содержит файл app.config. Добавление нового элемента в проект Visual Studio. В диалоговом окне **Добавление нового элемента** выберите шаблон **Файл конфигурации приложения** , присвойте ему имя app.config и нажмите кнопку **Добавить**.
    
2. Удалите весь текст в файле app.config и затем скопируйте следующий код в файл. Можно использовать же привязки, например `basicHttpConf`, для каждой конечной точки службы. Если вы хотите использовать более одного привязки, например для привязки протоколов HTTP и HTTPS, необходимо создать привязку для каждого протокола.
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Замените `ServerName/ProjectServerName` в поле адрес конечной точки клиента с именем сервера и экземпляр Project Web App. 
    
4. Замените `ServiceName` с именем службы PSI, такие как ресурсов. Убедитесь, заменить все три вхождения имя службы, например:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Чтобы использовать несколько служб PSI, создайте по одному элементу **endpoint** для каждой службы и для каждого элемента **binding**, используемого этой службой. Например, следующие конечные точки настраивают клиент таким образом, чтобы базовая привязка HTTP использовалась для службы Project и службы QueueSystem. 
    
    > [!NOTE]
    > Если вы запустили приложение и получили сообщение об ошибке, говорящее, что сервер перегружен, или что запрос HTTP не разрешен, проверьте правильность адресов конечных точек в файле app.config. 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Файл app.config можно изменить с помощью **Редактора конфигураций служб WCF** в Visual Studio (в меню " **Сервис** "). На рисунке 4 показано, как задать элемент **контракт** в диалоговом окне **Редактор конфигурации службы Microsoft** . Если решение использует сборки PSI прокси-сервер, откройте ProjectServerServices.dll в `bin\debug` каталог решения Visual Studio. Диалоговое окно **Типов контрактов** показывает все контракты службы WCF (см). 
  
**Рис. 4. Использование редактора конфигураций службы WCF**

![С помощью редактора конфигураций служб WCF] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "С помощью редактора конфигураций служб WCF")
  
Если решение использует файл прокси-сервер службы, такие как wcfResource.cs, выполните компиляцию приложения, а затем откройте исполняемого файла в `bin\debug` каталога. Дополнительные сведения об изменении файла app.config можно [Пошаговое руководство: разработка PSI приложений с помощью WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Рис. 5. Использование браузера типов контрактов в редакторе конфигураций службы WCF**

![Использование браузера типов контрактов] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Использование браузера типов контрактов")
  
## <a name="using-multiple-authentication"></a>Использование нескольких методов проверки подлинности
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Проверка подлинности пользователей локального сервера Project Server, проверка подлинности Windows или проверки подлинности форм по осуществляется с помощью утверждений обработки в SharePoint. Несколько проверка подлинности означает, что веб-приложения, где был подготовлен Project Web App поддерживает проверку подлинности Windows и проверка подлинности на основе форм. Если это так, любой вызов к службе WCF, использующего проверку подлинности Windows завершится с ошибкой из-за ошибки, так как процесс утверждения не может определить, какой тип пользователя для проверки подлинности:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Для устранения этой проблемы в WCF все вызовы методов PSI должны быть в области **OperationContextScope**, которая задается для каждой службы PSI. Не следует вкладывать области для нескольких служб; например, при использовании вызовов служб Resource и Project каждый ряд вызовов должен быть в своей собственной области. 
  
В следующем примере метод **DisableFormsAuth** может вызываться из каждого раздела **OperationContextScope** в приложении. Метод удаляет любое значение заголовка, ранее отключенного проверки подлинности форм, так что проверка подлинности форм можно производить, если параметр _isWindowsAuth_ имеет **значение false**. Если _isWindowsAuth_ имеет **значение true**, метод **DisableFormsAuth** отключается проверка подлинности через формы. 
  
В методе **WcfSample** объект **projectClient** является экземпляром класса **SvcProject.ProjectClient** PSI. 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> Выполнение вызовов PSI в области **OperationContextScope** необходимо только для приложений, которые выполняются в среде с использованием нескольких методов проверки подлинности. Если Project Server использует только проверку подлинности Windows, то не требуется устанавливать область и добавлять заголовок веб-запроса, который отключает проверку подлинности на основе форм. 
> 
> Исправление для приложения на основе ASMX на другой. Для получения дополнительных сведений обратитесь к разделу *проверки подлинности с помощью нескольких* в [Необходимые условия для образцов кода на основе ASMX в проекте](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Изменение значений универсальных констант
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Большинство образцов имеет один или несколько переменных, которые необходимо обновить образец работал надлежащим образом в вашей среде. В следующем примере Если протокол SSL, используйте протокол HTTPS вместо протокола HTTP. Замените _имя сервера_ имя сервера, на котором вы используете. Замените _ProjectServerName_ имя виртуального каталога сайта project server, например веб-клиента Project. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Все прочие переменные, которые необходимо изменить, указываются вверху примера кода.
  
## <a name="verifying-the-results"></a>Проверка результатов
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Получение и интерпретации результатов из примера кода не всегда просто. Например при создании проекта, необходимо опубликовать проект, чтобы оно может отображаться на странице центра проектов в Project Web App.
  
Вы можете проверить результаты примера кода несколькими различными способами, например:
  
- Просмотр элементов, которые будут использовать клиента Project Professional 2013 для откройте проект на сервере Project Server
    
- Просмотр опубликованных проектов на странице центра проектов Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).
    
- Просмотр журнала очереди в Project Web App. Открыть страницу "Параметры сервера" (в верхнем правом углу щелкните значок **Параметры** ), а затем выберите **Мои задания в очереди** в разделе **Личные параметры** ( `https://ServerName/ProjectServerName/MyJobs.aspx`). В раскрывающемся списке **представление** можно сортировать по состояние задания. Состояние по умолчанию — **в ходе выполнения и произошел сбой задания за прошлую неделю**. 
    
- Используйте страницу параметров сервера в Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) для управления заданиями в очереди и удаления или принудительный возврат корпоративных объектов. Необходимо иметь разрешения администратора для доступа к этих ссылок на странице "Параметры сервера".
    
- Используйте **Microsoft SQL Server Management Studio** для выполнения запроса в таблице базы данных Project Server. Например, с помощью следующего запроса можно получить верхние 200 строк таблицы MSP_WORKFLOW_STAGE_PDPS, чтобы просмотреть информацию о страницах сведений о проекте (PDP) на этапах рабочего процесса. 
    
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
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

После тестирования некоторые примеры кода существует корпоративных объектов и параметров, которые следует удалить или сбросить. На странице "Параметры сервера" в Project Web App можно использовать для управления корпоративными данными ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Ссылки на странице "Параметры сервера" позволяет удалять старые элементы, принудительный возврат проектов, управлять очередь заданий для всех пользователей и выполнять другие задачи администрирования.
  
Далее перечисляются некоторые ссылки на странице параметров сервера, которые можно использовать для выполнения обычных действий по очистке после выполнения примеров кода.
  
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

- [Предварительные требования для основанных на ASMX примеров кода в Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Пошаговое руководство. Разработка приложений PSI с использованием WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Использование олицетворения с WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Справочный обзор PSI Project](project-psi-reference-overview.md) 
- [Центр по разработке для SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

