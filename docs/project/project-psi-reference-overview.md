---
title: Справочный обзор PSI Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- веб-службы, календарь, проверка подлинности для веб-службы, ResourcePlan, Web, StatusReports, веб-службы, PSI, пространства имен, обработчиков событий, Project Server, веб-служба уведомлений, QueueSystem, веб-службы, Project 2013 платформы LoginWindows, веб службы, веб-службы, отчеты о состоянии, веб-служба, ресурсов, WinProj, веб-службы, WssInterop, веб-службы, веб-службы, Winproj, события обработчики, LookupTable, Web, веб-клиента Project, веб-службы, веб-службы, безопасности, уведомления веб-службы, веб-службы Расписания, веб-службы, QueueSystem, PSI, веб-службы, веб-службы, событий, PSI, программирования, веб-службы, LookupTable, версию, веб-служба, настраиваемых полей, веб-службы, веб-службы, веб-клиента Project, PSI, ресурсов, веб-службы, веб-службы, ResourcePlan, расписания, Web службы, веб-службы, правила, PSI, управляемого кода ссылку, безопасности, веб-службы, веб-службы, настраиваемых полей, URL-адрес для PSI (en), веб-службы, WssInterop, Web, Admin, Web ссылку PSI, веб-служба, cubeadmin задание таймера, представления, веб-службы, календарь, веб-служба Web Служба, представления, администратора, веб-службы, LoginForms, веб-службы, веб-служба, LoginForms, PSI, URL-адреса, ObjectLinkProvider, веб-службы, архив, Web службы, cubeadmin задание таймера, Web, правил, веб-служба, веб-службы, проверка подлинности для веб-служб, PSI, Project Server , события, события, веб-службы, веб-служба Project, отчеты о состоянии, веб-службы, веб-служба, ObjectLinkProvider, интерфейс Project Server, веб-методы PSI, Web, StatusReports, веб-службы, архив, Project, веб-службы, веб-службы, LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: Интерфейс Project Server (PSI) — это API для разработки приложений, которые интегрируются с Project Server 2013 в локальной.
ms.openlocfilehash: 58235e16afd208d0d4415e28ad200cc7ff62ac8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390123"
---
# <a name="project-psi-reference-overview"></a>Справочный обзор PSI Project

Интерфейс Project Server (PSI) — это API для разработки приложений, которые интегрируются с Project Server 2013 в локальной.
  
В этой статье представлен обзор документированных сборки, пространства имен и службы в PSI. [Справочник по библиотеке и веб-службы Project Server 2013 класс](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) в пакете SDK содержит все управляемого кода в документации по PSI и пространства имен [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) в Project Server 2013. Для разработки приложений для Project Online, необходимо использовать пространство имен **Microsoft.ProjectServer.Client** вместо PSI. 

PSI в Project Server 2013 имеет два интерфейса. Интерфейс ASMX для веб-службы определяется обнаружения и языка (disco и WSDL) файлов в `https://ServerName/ProjectServerName/_vti_bin/psi/` виртуальный каталог (например, Projectdisco.aspx и Projectwsdl.aspx). Интерфейс ASMX доступны только с помощью URL-адреса для локальной установки Project Web App (например, `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Чтобы отобразить веб-службы в браузере, необходимо включить `?wsdl` вариант URL-адреса. Поскольку интерфейс ASMX создан с помощью инфраструктуры Windows Communication Foundation (WCF), ASMX-файлы для веб-службы Project Server в виртуальном каталоге PSI фактически не существуют. 
  
Интерфейс служб WCF определяется SVC-файлов в серверной `https://ServerName:32843/GUID/PSI/` виртуального каталога в приложении веб-службы SharePoint. Службы URL-адрес PSI в виртуальном каталоге приложения-службы Project (например, `https://ServerName:32843/GUID/PSI/project.svc`) включает в себя SVC-файлов. Однако нельзя непосредственно использовать серверной URL-адрес для задания ссылки на службу WCF. Чтобы разработать приложение или компонент, который использует службы WCF PSI, можно использовать сборки прокси-сервера или файла прокси-сервера. Загрузить пакет SDK Project 2013 включает в себя файлы прокси-сервера для службы WCF в Project Server 2013 и построения скриптов для получения обновленных файлов прокси-сервера WCF и компиляция файлов в сборки прокси-сервера для последних Project Server.
  
Имя каталога приложения-службы Project — это значение GUID, которое совпадает с GUID экземпляра Project Web App в локальной. В окне **Диспетчер Internet Information Services (IIS)** разверните узел **Веб-служб SharePoint** , выберите имя каталога GUID и нажмите кнопку **Дополнительные параметры** , чтобы скопировать значение **Виртуального пути** . 
  
> [!IMPORTANT]
> Интерфейс веб-службы ASMX из PSI рекомендуется использовать в Project Server 2013, но по-прежнему поддерживается. Новые приложения должны использовать WCF интерфейса PSI или CSOM. Дополнительные сведения об устаревших функциях в статье [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md)
> 
> Новые приложения и компоненты промежуточного программного обеспечения, на которых выполняется только на локальной установки Project Server, следует использовать интерфейс WCF, который является технологии, рекомендуется использовать сетевые подключения. Устаревшие приложения, использующие интерфейс ASMX необходимо использовать URL-адреса через Project Web App проверяет разрешения Project Server. 
> 
> Дополнительные сведения об интерфейсе ASMX и порядок использования интерфейса WCF можно [Необходимые условия для образцов кода на основе ASMX в проекте](prerequisites-for-asmx-based-code-samples-in-project.md) и [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Для разработки приложений, использующих интерфейс WCF, можно использовать Visual Studio 2010 или Visual Studio 2012. Для создания декларативных рабочих процессов Project Server, можно использовать SharePoint Designer 2013. Рабочих процессов Project Server, которым требуется доступ к PSI или CSOM может быть разработан с помощью Visual Studio 2012.
  
### <a name="using-the-psi-reference"></a>Использование справки PSI
<a name="pj15_PSIRefOverview_Using"> </a>

Объектная модель PSI больших и многие классы и члены являются только для внутреннего использования. В результате может быть некоторая путаница найти разделы, которые будут в [Project Server 2013 класс библиотеки и веб-ссылки на службу](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx). Большинство ссылки на разделы, которые будут использовать для разработки, в следующих групп:
  
- **Методы основного класса:** Каждой службы PSI содержит основной класс с именем для имени службы. Например служба **ресурсов** содержит класс [ресурсов](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) , который находится в пространстве имен [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx) . Чтобы просмотреть список методов, которые доступны в классе **ресурсов** , разверните узел класс в области содержимого и выберите в разделе **Ресурсов, методов** . 
    
- **Свойства DataRow:** Многие из методов основной класс использовать или возврата **набора данных**. Каждый объект **DataTable** в **набор данных** содержит данные в один или несколько объектов **DataRow** . В большинстве случаев необходимо просмотреть только свойства строки, не всех других членов классов **DataSet**, **DataTable**или **DataRow** . Например класс **ResourceAssignmentDataSet** включает в себя подклассов для **ResourceAssignmentDataTable** и [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx) класса. Для просмотра списка свойств, которые находятся в классе **ResourceAssignmentRow** , разверните узел класс в области содержимого и выберите в разделе **Свойства ResourceAssignmentDataSet.ResourceAssignmentRow** . 
    
Помимо пространства имен служб [библиотеки и веб-службы Project Server 2013 класс ссылаться](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) раздел содержит ссылки на три Project Server сборки, используемые в разработке решений сторонних производителей для локальных установок. Мы предоставляют только минимальной документации для этих сборок. PSI справочных материалах задокументировано основных классов и членов в 23 общедоступных служб. Службы PSI шесть не только для внутреннего использования, а не рассматриваются. 
  
> [!NOTE]
> Классы в клиентской объектной модели (CSOM) можно использовать независимо от других сборок Project Server и служб. Можно использовать пространство имен **Microsoft.ProjectServer.Client** в среде удаленного развертывания на компьютере с Project Server и разработка приложений, которые интегрируются с Project Online или с локальной установкой Project Server. Однако CSOM содержит подмножество функциональных возможностей завершения PSI. CSOM позволяет разработки наиболее распространенные сценарии для интеграции с Project Server. Для получения дополнительных сведений см [CSOM что делает и не имеет](what-the-csom-does-and-does-not-do.md) и [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Для разработки большинство приложений, использующих PSI нет необходимости разрабатывать на компьютере сервера Project Server или задать ссылки на Project Server сборки в глобальном кэше сборок. Необходимые сборки Project Server можно скопировать на компьютере разработчика. Project Server 2013 устанавливает следующие сборки в _[Program Files]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Пространства имен для службы PSI имеют произвольных имена, созданные для сборки PSI прокси-сервера, ProjectServerServices.dll, который создается в качестве документации. В ссылке PSI каждого пространства имен службы имеет имя заполнителя (например, _[проекта веб-службы]_) и веб-ссылки (например, `https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Сборки и пространства имен Project Server
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Многие сборки устанавливаются при установке Project Server; описаны только четыре сборки Project Server. Сторонние разработчики обычно используйте только несколько классов и членов в этих сборках. Недокументированного сборки Project Server включают пространства имен и классы, которые использует Project Server, во внутренней сети, таких как классы для Project Web App бизнес-сущностей и доступа к данным уровнем (DAL). Если установка в Visual Studio ссылки на одну из документированным сборок Project Server, могут видеть все пространства имен, классы и элементы в обозреватель объектов Visual Studio.
  
> [!NOTE]
> Многие элементы задокументированных пространств имен Project Server используются только внутренним образом и имеют минимальный объем документации. 
  
При разработке для Project Online для доступа к возможностям Project Server можно использовать только CSOM. Нет доступа к службы PSI или другие сборки, Project Server.
  
[Справочник по библиотеке и веб-службы Project Server 2013 класс](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) для PSI содержит пространства имен из следующие сборки: 
  
- **Microsoft.Office.Project.Server.Library.dll** эта сборка содержит один документированным пространства имен и три недокументированного пространства имен, следующим образом: 
    
  - Пространство имен [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) включает множество перечислений и класс поля и свойства, которые часто используются в локальных приложений для Project Server. Например разработчики обычно используется перечисления, такие как **CustomField.Type**и соответствующие им классы **PSClientError**, **PSErrorInfo**и **фильтра** . 
    
    В пространстве имен **Microsoft.Office.Project.Server.Library** также содержатся следующие семь классов свойств, включающих свыше 3200 подклассов: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    Свойство классы используются во внутренней сети и не рассматриваются. Свойство классы используются для сериализации между Project Professional 2013 и Project Server. При работе с использованием пространства имен **Microsoft.Office.Project.Server.Library** в Visual Studio, обозревателя объектов отображаются все классы свойства, которые усложняет поиск классов, которые могут помочь в разработке сторонних производителей. Так как сторонние разработчики нет необходимости использовать свойство классы, их не документа в пакет SDK. 
    
  - **Microsoft.Office.Project.Server.DataServices** классы и элементы этого пространства имен используются во внутреннем службы **OData** в Project Online для доступа к отчетности таблиц в базе данных Project. Классы **DataServices** не документированы. 
    
  - **Microsoft.Office.Project.Server.Administration** класс и его элементы этого пространства имен во внутренней сети используются для сбора данных диагностики и не рассматриваются. 
    
  - **Microsoft.Office.Project.Server.Base** классы и элементы этого пространства имен во внутренней сети используются в качестве базовых классов, а не рассматриваются. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** этого пространства имен во внутренней сети используются для создания схемы фильтра, а не задокументирован. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** эта сборка используется для устаревших рабочих процессов Project Server 2010, которые можно по-прежнему работают в Project Server 2013. Для создания новых рабочих процессов, следует использовать SharePoint Designer 2013 или можно также использовать Visual Studio 2012 с классом [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) . Сборка Microsoft.Office.Project.Server.Workflow.dll включает в себя следующие три пространства имен: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) это пространство имен содержит классы, используемые для действий рабочего процесса Project Server. Действия включают чтение, сравнение и обновление свойств проекта. Другие классы управления рабочими процессами и включать ответных звонков рабочий процесс при изменении проектов. 
    
  - **Microsoft.Office.Project.PWA** это пространство имен содержит внутренний прокси-сервера для PSI (en), для использования с Project Web App и настраиваемые действия рабочего процесса; не задокументирован. 
    
    Действий настраиваемого рабочего процесса требуется ссылка на **Microsoft.Office.Project.PWA** для доступа ко всем классы в службы PSI. Например класс **Microsoft.Office.Project.PWA.PSI** включает в себя свойство **ProjectWebService** , которое возвращает прокси-сервер для пространства имен [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx) . 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** это пространство имен включает в себя внутренней прокси-классы для основного класса в каждой службы PSI. С помощью повышенным уровнем разрешений пользователя, рабочий процесс, рабочий процесс можно вызвать методы PSI через прокси-классы. Прокси-классы не документированы. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) является единственным пространства имен в этой сборке. Содержит приемник событий и классов аргументов событий для службы PSI и другие внутренние классы. 
    
  Разработчики пишут обработчики событий, производные от классов приемника события. Большинство основных классов в службах PSI имеет соответствующий класс приемника события. Например, класс **ProjectEventReceiver** содержит методы приемника события до операции и события после операции, которые соответствуют методам в классе **Project** в PSI. Методы **OnCreating** и **OnCreated** являются методами приемника события до операции и события после операции для метода **QueueCreateProject**. 
    
  Разработчики обычно используют следующие классы приемника события:
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  Класс **RulesEventReceiver** и класс **StatusReportsEventReceiver** во внутренней сети используются в Project Web App. 
    
- **Microsoft.ProjectServer.Client.dll** эта сборка содержит CSOM для разработки с помощью .NET Framework 4. Сборка располагается в `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Разработка приложений с использованием пространства имен **Microsoft.ProjectServer.Client** не зависит от интерфейсы API в локальной Project Server и служб, несмотря на то, что приложений может работать с либо локальный или online установленного сервера Project Server. Связанные CSOM сборки, которые можно использовать для Windows Phone 8, Microsoft Silverlight или JavaScript с веб-приложений в разделе [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
    
- **Microsoft.Office.Project.Server.Schema.dll** пакет SDK для Project 2013 документировать пространства имен **Microsoft.Office.Project.Server.Schema** , который находится в `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll` сборки. Пространство имен содержит определения всех **наборов данных**, **DataTable**и **DataRow** классы, используемые в PSI (en), а также много похожие классы, которые использует Project Server во внутренней сети. Открытые классы в каждой службы PSI описаны в ссылке на отдельных служб. Например класс **DriverDataSet.DriverRow** описана в пространстве имен [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx) . 
    
  > [!NOTE]
  > Приложения, используйте CSOM, использование обработчиков событий удаленного или получить доступ к Project Online не используют пространство имен **Microsoft.Office.Project.Server.Schema** . 
  
  В некоторых приложениях, использующих обработчики событий с полным доверием, когда обработчики событий устанавливаются на компьютере Project Server, необходимо установить ссылку на сборку Microsoft.Office.Project.Schema.dll. Далее приводятся два примера.
    
  - В обработчике события после операции **OnCreated** с полным доверием для настраиваемых полей можно использовать аргумент события **e.CustomFieldInformation** со ссылкой на пространство имен **Microsoft.Office.Project.Server.Schema** для определений **CustomFieldDataSet** и **CustomFieldsRow**. 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - Настраиваемому действию рабочего процесса может требоваться ссылка на **Microsoft.Office.Project.Server.Schema** для определений **DataSet**. 
    
## <a name="psi-services"></a>Службы PSI
<a name="pj15_PSIRefOverview_PSI"> </a>

PSI представляют собой набор служб WCF и идентичные ASMX для веб-служб Project Server 2013. Чтобы использовать службу в проект Visual Studio, сначала задать ссылку на URL-адрес `.svc` файл или `.asmx?wsdl` service с помощью случайное имя для nameservice. Служебная программа wsdl.exe или служебной программы svcutil.exe создает исходный код прокси-сервера для этого пространства имен и компилятор создает сборки службы прокси-сервера для включения в приложении. 
  
> [!NOTE]
> Справочник PSI содержит имена nameservice заполнитель для службы PSI, такие как _[веб-службы администрирования]_, _[драйвер веб-службы]_ и _[проекта веб-службы]_. Каждый nameservice PSI включает в себя основной класс, который содержит веб-методы для этой службы. К примеру если задания ссылки на службы **администрирования** и присвойте ему имя **WebSvcAdmin**, затем в приложении **WebSvcAdmin** nameservice включает в себя основного класса **Admin** , имеющей веб-методы **GetServerCurrency** **ListInstalledLanguages**, **ReadServerVersion**и т. д. Чтобы получить список не рекомендуемые для использования службы PSI в статье [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md) . 
  
30 общее служб PSI **проверки подлинности**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **веб-клиента Project**, **представления**и **WinProj** предназначены для внутреннего использования с Project Web App и Project Профессиональный и являются не задокументирован. Несмотря на то, что можно создать файлы прокси-сервера или сборки прокси-сервера, который включает в себя внутренней службы PSI, внутренней службы не для использования сторонних производителей; Справочник по PSI документировать этих служб. На следующем рисунке показано расположение серверным службам PSI в диспетчере служб IIS. 
  
**Поиск служб PSI в IIS**

![Службы PSI в диспетчере служб IIS] (media/pj15_PSIReference_IIS.gif "Службы PSI в диспетчере служб IIS")
  
Далее приводятся классы, которые содержат веб-методы, в службах PSI.
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Содержит методы, используемые на страницах **Администрирования Project Server** в Project Web App. Определяет финансовый год, управляет параметрами отчеты о состоянии и денежных единиц, отчетов периодов, журнала аудита и параметров для Active Directory. 
    
2. [Архив](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Включает в себя методы для управления резервного копирования и восстановления проектов, категории безопасности, настраиваемые поля, ресурсы, параметры системы, представления и глобального корпоративного проекта. Считывает и обновляет расписание архива. Архивы; все проекты или удаляет указанный архивных проектов. Сохраняет резервного копирования объектов таблицы архива базы данных и восстановление, резервное копирование объектов с таблицами базы данных опубликованных проектов. 
    
3. **Проверка подлинности** Содержит методы для внутреннего использования только с Project профессиональный и Project Web App. 
    
4. [Календарь](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Управляет исключения корпоративных календарей. Извлекает и проверка в календарей ресурсов. Создает, удаляет список всех, обновляет или возвращает исключения календарей. 
    
5. [Cubeadmin задание таймера](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Управляет параметрами куба OLAP. Получает сервера анализа данных, состояние базы данных и список кубов. Помещает запрос службы построения куба в очередь. Считывает и обновляет определения вычисляемых элементов и параметры поля для измерений и мер в кубе. 
    
6. [Настраиваемых полей](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Управляет корпоративных настраиваемых полей. Включает в себя извлечение и возврат методы и создания, чтения, обновления и методы удаления (CRUD) для корпоративных настраиваемых полей. 
    
7. [Драйвер](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Управление драйверами анализа портфеля и определения приоритетов факторов для создания проекта и управления запросами. Включает в себя методы CRUD для рамки начала проекта. 
    
8. [События](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Управляет связей обработчика событий Project Server. Включает в себя методы CRUD для связи обработчика событий Project Server для определенных событий или для всех сопоставлений обработчика событий. 
    
9. **ExchangeSync** Это внутренняя служба Project Server, который обрабатывает события Exchange Server. Project Web App для синхронизации назначений между Project Server и Exchange Server, вместо синхронизации непосредственно с клиентом Outlook, как и в Office Project Server 2007 используется **ExchangeSync** . 
    
    Доступ к службе **ExchangeSync** возможен только с помощью URL-адреса **ProjectServiceApplication**. Классы и элементы **ExchangeSync** для сторонней разработки не поддерживаются. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Предоставляет методы **для входа** и **выхода из системы** с проверкой подлинности на основе форм. Доступ к службе **LoginForms** доступен только на клиентский сайт Project Web App. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Предоставляет методы **для входа** и **выхода из системы** , для которых будет использоваться проверка подлинности Windows на основе ASMX с приложениями с целью проверки подлинности на нескольких (утверждений и на основе форм) установок Project Server 2013. Доступ к службе **LoginWindows** доступен только на клиентский сайт Project Web App. 
    
    > [!CAUTION]
    > Служба **LoginWindows** не используется в приложениях на основе WCF и для приложений, работающих в установках Project Server, применяющих только проверку подлинности на основе утверждений или **OAuth**; в этих случаях метод **Login** всегда возвращает **false**. Проверка подлинности на основе утверждений обрабатывает интегрированную проверку подлинности Windows. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Управляет таблицы подстановки, многоязычных таблиц подстановки и их соответствующих маски кода. Извлекает, проверка в, считывает, создает, удаляет и обновления. 
    
13. [Уведомления](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Управление оповещениями и напоминаниями. Содержит методы, получение, установка, регистрации и отмены регистрации результатов оповещения. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Управление веб-объекты и ссылки для документов и элементов списка на сайтах SharePoint. Создает, удаляет или считывает проекта, связанный с проектом, задаче или связанных задач веб-объекты. 
    
    > [!NOTE]
    > Служба **ObjectLinkProvider** поддерживается в Project Server 2013. Для получения дополнительных сведений обратитесь к разделу *устарел функции* в [обновляется в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md). 
  
15. **OData** Предоставляет внутренний интерфейс **OData** для работы с отчетами таблицы и представления. Доступ к службе **OData** доступен только в серверной **ProjectServiceApplication** URL-адрес. Закрытый службы **OData** в PSI предоставляет один метод **ODataClient.ProcessOdataMessage**, который Project Server использует для обработки запросов для работы с отчетами данных. HTTP-запросы, выполните в интерфейсной службе **ProjectData** . 
    
    Сведения о службе **ProjectData** и протокола OData для чтения данных отчетов можно [ProjectData — Справочник по службе Project OData](https://msdn.microsoft.com/library/office/jj163015.aspx).
    
16. **P12Upgrade** Внутренний методы для установки Project Server 2013 обновление установки Office Project Server 2007. Доступ к службе **P12Upgrade** доступен только с помощью **ProjectServiceApplication** URL-адрес. Методы **P12Upgrade** не поддерживается для разработки приложений сторонних производителей. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Содержит методы CRUD для зависимости проекта, а также для оптимизатора, планировщик работы и анализа решений. 
    
18. [Проекта](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Управление проектами. Извлекает, проверка в, создает, удаление, считывает или обновления проектов в таблицах базы данных черновиков Project или опубликованных таблиц. Помещение сообщения в очереди для публикации. 
    
    Создание или удаление сущности в рамках проектов (задачи, ресурсы, назначения и т. д.). Получает сведения о или обновляет рабочей группы или адрес сайта проекта. Получает состояние проекта, список проектов в таблицах черновиков, все суммарные задачи, задачи, доступные для назначения для указанного ресурса или все проекты которых имеет назначения ресурса.
    
    Создает обязательства и управляет ими, создает проектные инициативы и проекты из списков задач SharePoint, а также обнаруживает отношения "проект-главный проект".
    
19. **psiserviceapp** Используется системой Project Online. **Psiserviceapp** классы и члены для разработки сторонних производителей не поддерживаются. 
    
20. **Веб-клиента Project** Содержит множество методов, оптимизированных для Project Web App, включая методы для правила утверждения обновления задач и управление отчетами о состоянии. Методы **веб-клиента Project** часто специализированные и несколько избыточных по сравнению с эквивалентный методы в другие службы PSI. Методы **веб-клиента Project** использовать или возврата многие из одной наборов данных, как и другие методы PSI. 
    
    Доступ к службе **PWA** возможен только с помощью URL-адреса **ProjectServiceApplication**. Классы и элементы **PWA** для сторонней разработки не поддерживаются. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Управляет очередей Project Server. Возвращает число заданий, задания и время ожидания задания группы, состояние заданий, указанного задания, владельцем задания или заданий для указанных проектов. Управляет корреляции заданий и настраивает очереди. 
    
22. [Ресурс](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Управляет корпоративных ресурсов. Извлекает, проверка в, обновляет или создает ресурсы и пользователи Project Server и их параметров проверки подлинности; Поиск ресурсов по имени или GUID; Считывает ресурсов или пользовательских данных и структуры декомпозиции ресурсов (СДРЕС) и сведения о безопасности; Получает все назначения ресурса; и сброс паролей пользователей. Класс **ресурсов** включает в себя методы CRUD для делегирования пользователей. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Управляет планов ресурсов. Извлекает проверок в, публикацию и включает в себя методы CRUD для планов ресурсов. 
    
24. [Безопасность](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Включает в себя методы CRUD для шаблонов безопасности, категории безопасности, организации и глобальных разрешений и разрешений группы. Класс **безопасности** включает в себя методы для категорий проекта. 
    
25. [Отчеты о состоянии](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Управление обновлениями состояния и назначений. Применяет обновления состояния и утверждения, отправляет данные состояния обновляется, сводные данные для добавленных обновлений, удаляет обновления утвержденных состояния или истории утверждения для указанного пользователя или удаляет все сведения о состоянии для набора проектов. Создает и получает делегирует назначения; Задает продолжительность работы назначения. Получает нового назначения для текущего пользователя; Получает История транзакций для назначения или задачи, повременные фактические данные или иерархии суммарных задач. 
    
    Выполняет предварительный просмотр или импорт данных расписания или читает рабочее и нерабочее время пользователя. Находит ожидающие обновления состояния, сведения для отправленных обновлений или запись транзакции изменений в отправленном обновлении. Читает состояние группы.
    
26. [Табеля учета рабочего времени](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Управление расписаниями. Содержит методы CRUD для расписания и отправляет данные или отзыва расписаний. Находит расписания, которые позднее или ожидает утверждения; Находит расписаний, даты или периода времени. Получает список утверждающих табеля учета рабочего времени. Предварительно загружает фактические данные расписаний и проверяет строки расписания. **Класс** включает в себя метод **ReadProjectTimesheetLines** и метод **SubmitTimesheetLines** для чтения и отправка расписаний для другого ресурса без необходимости установки олицетворения. 
    
27. **Просмотр** Служба **представления** предназначена только для использования в Project Web App. Методы в классе **представления** Управление представлениями и просмотр отчетов и прочитайте полей в представлениях. 
    
    Доступ к службе **View** возможен только с помощью URL-адреса **ProjectServiceApplication**. Методы **View** не поддерживаются для сторонней разработки. 
    
28. **WinProj** Служба **WinProj** предназначена для использования только с Project профессиональный. Сторонние разработчики не следует использовать методы **WinProj** по программированию с помощью Project Server. 
    
    Некоторые методы **WinProj** используют наборы данных, например **ProjectRelationsDataSet** и **ResourceDataSet**, которые также используются службами **Project** и **Resource**, но в Project Professional для них требуются особые свойства и функции. 
    
    Доступ к службе **WinProj** возможен только с помощью URL-адреса **ProjectServiceApplication**. Методы **WinProj** для сторонней разработки не поддерживаются. 
    
29. [Рабочий процесс](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Включает в себя методы CRUD типы корпоративных проектов и управление этапы рабочего процесса и этапов. Запускает рабочие процессы, задает сведения о состоянии и управляет этапов страницы (PDP) сведений о project в рабочих процессах управления запросами. Для разработки рабочих процессов Project Server, можно использовать SharePoint Designer 2013 для декларативных рабочих процессов или использовать инструменты разработчика Office для Visual Studio 2012 для разработки с помощью .NET Framework 4 и [для разработчиков (en) Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) класса в CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Управление сайтами проектов. Создает и удалению сайтов проектов. Получает сведения о и обновляет параметры SharePoint и сайты администрирования. Синхронизирует и обновляет членство на сайте проекта и групп. 
    
Каждое пространство имен службы включает все **набора данных** схемы и класс обработчика событий, которые использует службу. Например `Calendar.svc` (или `Calendar.asmx?wsdl` для ASMX веб-службы) описание службы **календаря** . Если имя ссылки **WebSvcCalendar**пространство имен прокси-сервера содержит основной класс с методами **CheckInCalendars** **календаря** , **CheckOutCalendars**и т. д. Пространство имен прокси-сервера **WebSvcCalendar** также включает класс **CalendarDataSet** и всех его подклассов. 
  
Некоторые из служб PSI содержат дублирующиеся классы **DataSet**. Например, обе службы **Project** и **Statusing** содержат класс **ProjectDataSet**. Это объясняется тем, что методы в обеих службах **Project** и **Statusing** включают ссылки на **ProjectDataSet**, и сборки прокси, созданные при установке ссылок и компиляции приложения, включают соответствующие наборы данных. Службам **Project** и **Statusing** могут требоваться значения для разных полей в классе **ProjectDataSet.ProjectRow**. 
  
При переходе по пространствам имен и классам в справке PSI, например, для просмотра веб-методов для службы **Project**, разверните пространство имен **[Веб-служба Project]** в списке **Содержимое**, а затем разверните класс **Project**. 
  
## <a name="see-also"></a>См. также

- [Project Server 2013 architecture](project-server-2013-architecture.md)
- [Возможности программирования для Project Server](project-server-programmability.md)   
- [Какие задачи PSI выполняет, а какие — нет](what-the-psi-does-and-does-not-do.md)   
- [Предварительные требования для основанных на ASMX примеров кода в Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Необходимые условия для примеров кода на основе WCF в Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [Веб-сайт центра разработчиков .NET Framework](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

