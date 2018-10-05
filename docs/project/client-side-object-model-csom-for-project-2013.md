---
title: Клиентская объектная модель (CSOM) для Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Project Server 2013 клиентской объектной модели (CSOM) реализует общие функциональные возможности сервера. Project Server CSOM включает в себя Microsoft .NET CSOM, CSOM Microsoft Silverlight, CSOM 8 Windows Phone и объектная модель JavaScript (JSOM). Кроме того CSOM включает в себя службе OData, который позволяет интерфейса REST. Интерфейс REST предназначены в основном для разработки приложений на платформах отличных от Windows, например, iOS и Android.
ms.openlocfilehash: 8be603fbee35f228dea0fa6b6be087b8e09c30e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394449"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Клиентская объектная модель (CSOM) для Project 2013

Project Server 2013 клиентской объектной модели (CSOM) реализует общие функциональные возможности сервера. Project Server CSOM включает в себя Microsoft .NET CSOM, CSOM Microsoft Silverlight, CSOM 8 Windows Phone и объектная модель JavaScript (JSOM). Кроме того CSOM включает в себя службе OData, который позволяет интерфейса REST. Интерфейс REST предназначены в основном для разработки приложений на платформах отличных от Windows, например, iOS и Android.
  
> [!NOTE]
> Решения для Project Online необходимо использовать CSOM. Тем не менее локальные приложения могут использовать CSOM или интерфейса Project Server (PSI). Если CSOM предоставляет функциональные возможности, которые планируется использовать, рекомендуется использовать CSOM для новых приложений. 
  
В расширениях CSOM объект **ProjectContext** предоставляет точку входа для сервера контента и функций. .NET CSOM, Silverlight CSOM и CSOM Windows Phone используйте объект [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) и JSOM использует **PS. ProjectContext** объекта. Свойства **ProjectContext** предоставить прямой доступ к объектам Project Server core в текущем семействе сайтов Project Web App. Сведения о расположении файл JavaScript и сборки CSOM [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) см. 
  
 **Приложения и модель безопасности** Приложения должны использовать CSOM для CRUD (Создание, чтение, обновление, удаление) операции с Project Server 2013 и Project Online. Приложения Project не используйте модели проверки подлинности только для приложений в SharePoint 2013. Приложению Project Server требуется область запроса определенные разрешения, указывающее, от имени которого выполняются команды. 
  
 **Запросы REST** Для создания запросов REST службы CSOM OData без использования метаданных. Некоторые средства сторонних производителей включить использование сборки .NET для CSOM для разработки приложений для других устройств. Например поиск в Интернете «кроссплатформенный .NET средства разработки для операций ввода-вывода или Android.» 
  
> [!NOTE]
> Хотя `$metadata` вариант для **ProjectData** отчетов службы является допустимым ( `https://ServerName/pwaName/_api/ProjectData/$metadata`), `$metadata` параметр для службе **ProjectServer** CSOM удаляется в выпущенной версии Project Server 2013. Чтобы найти CSOM объекты и члены, доступные в качестве конечных точек REST, можно найти [библиотеку JavaScript и справочник по REST для Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Чтобы просмотреть сущности, доступные в CSOM через интерфейс REST, можно использовать `https://ServerName/pwaName/_api/ProjectServer` запроса. Для запросов REST сущности **ProjectServer** напоминает свойства объекта [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) в сборке Microsoft.ProjectServer.Client.dll управляемых и [PS. ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) объекта в JSOM. К примеру, можно использовать браузер для получения сведений из CSOM о проектов в Project Web App назначений в указанный проект и имя задачи указанному назначению для заданного ресурса с помощью следующих запросов (использует каждого запроса же `https://ServerName/pwaName/_api` префикса URL-адрес). Идентификаторы GUID — это пример значения для **Project.Id**, **EnterpriseResource.Id**и **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

В отличие от интерфейса OData для службы **ProjectData** , которое доступно только для чтения для отчетов, это можно сделать с помощью запросов REST в службе **ProjectServer** операций CRUD. Запросы REST для Project Server CSOM предназначенных для платформ не на рабочем столе Windows, такие как Windows RT, iOS и Android. Для настольных и серверных платформ Windows, такие как Windows 7, Windows 8 и Windows Server 2008 R2 можно использовать CSOM управляемые сборки. Для веб-приложения можно использовать PS.js для JavaScript. Сведения о выполнении операций CRUD, с помощью запросов REST приведены в разделе [операции запросов OData используется в запросах SharePoint REST](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) в пакет SDK для SharePoint 2013. Сведения об использовании службы **ProjectData** [запросов OData каналов данных отчетов Project](https://msdn.microsoft.com/library/office/jj163048.aspx)см.
  
В таблице 1 перечислены свойства **ProjectContext** , которые представляют объекты сервера Project Server. Эти объекты можно использовать для получения других сущности Project Server 2013, такие как назначений и задач. 
  
**Таблица 1. Свойства ProjectContext, предоставляющие доступ к объектам Project Server в CSOM и JSOM**

|**CSOM (.NET, Silverlight и Windows Phone)**|**JSOM**|
|:-----|:-----|
|[Настраиваемых полей](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |настраиваемых полей  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[События](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |таблиц подстановки  <br/> |
|[Этапы](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Проекты](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Этапы](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>В этой статье

[Приступая к работе с Project Server CSOM и .NET](getting-started-with-the-project-server-csom-and-net.md) предоставляет общие сведения о Project Server CSOM и .NET, инструкции о том, как создать простое расширение .NET CSOM в Visual Studio 2012 и примеры кода, поддерживающей. 
  
[Приступая к работе с объектной моделью Project Server 2013 JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md) предоставляет общие сведения о JSOM Project Server, инструкции о том, как создать простое расширение JSOM в Visual Studio 2012 и примеры кода, поддерживающей. 
  
Узнать, как использовать CSOM, можно также в приведенных ниже статьях.
  
- [Пакетное обновление настраиваемых полей и создание сайтов проектов из рабочего процесса в Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Работа с проектами с помощью объектной модели JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Можно также использовать Visual Studio 2010 для платформы .NET Framework 4 разработка с помощью CSOM. 
  
## <a name="reference"></a>Справочные материалы

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>См. также



[Project Server 2013 architecture](project-server-2013-architecture.md)


[Выбор правильного набора API в SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

