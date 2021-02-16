---
title: Архитектура и программируемость Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, архитектура и программируемость, программируемость, Project Server,Project 2013, преимущества EPM, архитектура и Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: В статьях этого раздела описывается общая архитектура решения enterprise Project Management (EPM), объединяющего Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413789"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Архитектура и программируемость Project Server 2013

В статьях этого раздела описывается общая архитектура решения enterprise Project Management (EPM), объединяющего Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Project Server 2013 создан с помощью .NET Framework 4 и является третьим основным выпуском Project Server для обеспечения настоящей многоуровневой архитектуры. Для облачного доступа Project Server 2013 реализует клиентскую объектную модель (CSOM) и службу OData для отчетов, которые можно использовать в веб-приложениях, мобильных приложениях и приложениях Silverlight. Для локального приложения клиенты могут использовать службы CSOM или Project Server Interface (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Введение в архитектуру Project Server

В этом разделе описывается общая архитектура решения управления корпоративными проектами (EPM), которое объединяет Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Для программного доступа к Project Server следует использовать CSOM или службы PSI с интерфейсом Windows Communication Foundation (WCF). Интерфейс веб-службы ASMX PSI является неподготовленным в Project Server 2013, но по-прежнему работает. PSI обеспечивает эффективный доступ с помощью наборов данных, и вы можете создавать обработчики для событий на стороне сервера. Сама CSOM использует PSI для доступа к уровне бизнес-объектов Project Server. Вместо четырех баз данных Project Server в Project Server 2013 используется одна база данных на уровне доступа к данным.
  
Project Server 2013 полностью интегрируется с SharePoint Server 2013. Службу приложения Project можно связывать с другими коллекциями веб-сайтов SharePoint в ферме. Project Server может работать со списками задач SharePoint в коллекции сайтов и получать отчеты о них, а также получать полный контроль над тем, где Project Server импортирует списки задач и управляет ими как корпоративными проектами. Project Server также использует версию 4 Windows Workflow Foundation (WF4) и добавляет действия рабочего процесса для решений управления запросами.
  
О многих новых функций, которые Project 2013 предоставляет разработчикам, а также о неподготовленных функций см. в статьях "Обновления для разработчиков" в [Project 2013.](updates-for-developers-in-project-2013.md)
  
## <a name="in-this-section"></a>В этом разделе:

[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, включая клиенты и серверы. 
  
[В](project-server-programmability.md) этой теме обсуждаются основные функции реализации возможностей возможности extensibility Project Server 2013, настройки Project Web App и обновления приложений, построенных для предыдущих версий Project Server. 
  
[Что PSI делает и не](what-the-psi-does-and-does-not-do.md) описывает сценарии, в которых PSI можно использовать, и перечисляет то, что PSI не может делать. 
  
[Что CSOM делает и не](what-the-csom-does-and-does-not-do.md) описывает сценарии, в которых CSOM можно использовать, и перечисляет то, что CSOM не может делать. 
  
### <a name="topics-not-covered"></a>Темы не освещались

Статьи в разделе  "Архитектура и программируемость" не документировать функции классических клиентов Project (Project Стандартный 2013 и Project профессиональный 2013) или Project Web App. 
  
Visual Basic для приложений (VBA) доступна в редакторе Visual Basic Project Standard и Project профессиональный.
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Обновления для разработчиков в Project 2013](updates-for-developers-in-project-2013.md)
    
- [Начало разработки рабочих процессов Project Server](getting-started-developing-project-server-workflows.md)
    

