---
title: Клиентская объектная модель (CSOM) для Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Клиентская объектная модель (CSOM) Project Server 2013 реализует распространенные функции сервера. CSOM Project Server включает в себя CSOM Microsoft .NET, CSOM Microsoft Silverlight, CSOM Windows Phone 8 и объектную модель JavaScript (JSOM). Кроме того, CSOM включает службу OData, которая включает интерфейс REST. Интерфейс REST предназначен главным образом для разработки приложений на отличных от Windows платформах (например, iOS и Android).
localization_priority: Priority
ms.openlocfilehash: b722e316f5cb2054eb6522297c5c5ef3e75f9fa4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723112"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Клиентская объектная модель (CSOM) для Project 2013

Клиентская объектная модель (CSOM) Project Server 2013 реализует распространенные функции сервера. CSOM Project Server включает в себя CSOM Microsoft .NET, CSOM Microsoft Silverlight, CSOM Windows Phone 8 и объектную модель JavaScript (JSOM). Кроме того, CSOM включает службу OData, которая включает интерфейс REST. Интерфейс REST предназначен главным образом для разработки приложений на отличных от Windows платформах (например, iOS и Android).
  
> [!NOTE]
> Решения для Project Online должны использовать CSOM. Однако локальные приложения могут использовать CSOM или интерфейс Project Server (PSI). Если CSOM включает функции, которые вы планируете использовать, рекомендуем использовать CSOM для новых приложений. 
  
В расширениях CSOM объект **ProjectContext** обеспечивает точку входа для содержимого и функций сервера. CSOM .NET, CSOM Silverlight и CSOM Windows Phone используют объект [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx), а JSOM использует объект **PS.ProjectContext**. Свойства **ProjectContext** предоставляют прямой доступ к базовым объектам Project Server в текущем семействе веб-сайтов Project Web App. Дополнительные сведения о расположении сборок CSOM и файла JavaScript см. в статье [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
 **Приложения и модель безопасности** должны использовать CSOM для операций CRUD (создание, чтение, обновление, удаление) в Project Server 2013 и Project Online. Приложения Project не используют модель проверки подлинности только для приложений в SharePoint 2013. Приложение Project Server требует особой области запросов на получение разрешений, которая определяет, от чьего имени выполняются команды. 
  
 **Запросы REST.** Вы можете создавать запросы REST службы CSOM OData без использования метаданных. Некоторые сторонние средства позволяют использовать сборки .NET для CSOM, чтобы разрабатывать приложения для других устройств. Например, выполните поиск в Интернете по такой фразе: "средства для кроссплатформенной разработки на .NET для iOS или Android". 
  
> [!NOTE]
> Хотя параметр `$metadata` для службы отчетов **ProjectData** допустим (`https://ServerName/pwaName/_api/ProjectData/$metadata`), параметр `$metadata` для службы **ProjectServer** CSOM удален в выпущенной версии Project Server 2013. Сведения о том, как найти объекты и элементы CSOM, доступные как конечные точки REST, см. в статье [Библиотека JavaScript и справочные материалы по REST для Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Чтобы просмотреть объекты, доступные в CSOM через интерфейс REST, вы можете использовать запрос `https://ServerName/pwaName/_api/ProjectServer`. Для запросов REST объект **ProjectServer** отражает свойства объекта [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) в управляемой сборке Microsoft.ProjectServer.Client.dll и объекта [PS.ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) в JSOM. Например, можно использовать браузер для получения данных из CSOM о проектах в Project Web App, назначениях в указанном проекте и названий задач, касающихся определенного назначения для указанного ресурса, с помощью указанных ниже запросов (в каждом запросе используется один и тот же URL-префикс `https://ServerName/pwaName/_api`). GUID — это пример значения для **Project.Id**, **EnterpriseResource.Id** и **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

В отличие от интерфейса OData для службы **ProjectData**, доступного только для чтения отчетов, вы можете выполнять операции CRUD, используя запросы REST с помощью службы **ProjectServer**. Запросы REST для CSOM Project Server рассчитаны главным образом на платформы, отличные от классической версии Windows (например, на Windows RT, iOS и Android). Для классических и серверных платформ Windows (например, Windows 7, Windows 8 и Windows Server 2008 R2) можно использовать управляемые сборки CSOM. Для веб-приложений можно использовать PS.js для JavaScript. Информацию о выполнении операций CRUD с помощью запросов REST см. в статье [Использование операций запроса OData в запросах REST в SharePoint](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) (SDK для SharePoint 2013). Информацию об использовании службы **ProjectData** см. в статье [Запрашивание каналов OData для данных отчетов](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
В таблице 1 перечислены свойства **ProjectContext**, представляющие объекты Project Server. Вы можете использовать эти объекты для получения других объектов Project Server 2013 (например, назначений и задач). 
  
**Таблица 1. Свойства ProjectContext, предоставляющие доступ к объектам Project Server в CSOM и JSOM**

|**CSOM (.NET, Silverlight и Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Events](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Stages](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>В этом разделе

В статье [Начало работы с CSOM Project Server и .NET](getting-started-with-the-project-server-csom-and-net.md) есть общая информация о CSOM Project Server и .NET, инструкции по созданию простого расширения CSOM .NET в Visual Studio 2012 и примеры кода. 
  
В статье [Начало работы с объектной моделью JavaScript Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) есть общая информация о JSOM Project Server, инструкции по созданию простого расширения JSOM в Visual Studio 2012 и примеры кода. 
  
Узнать, как использовать CSOM, можно также в приведенных ниже статьях:
  
- [Пакетное обновление настраиваемых полей и создание сайтов проектов из рабочего процесса в Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Работа с проектами при помощи объектной модели JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Кроме того, вы можете использовать Visual Studio 2010 для .NET Framework 4 для разработки с помощью CSOM. 
  
## <a name="reference"></a>Справочные материалы

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Дополнительные ресурсы



[Архитектура Project Server 2013](project-server-2013-architecture.md)


[Выбор правильного набора API в SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

