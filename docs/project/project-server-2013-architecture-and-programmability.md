---
title: Project Архитектура и программируемость Server 2013
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
- project 2013, архитектура и программируемость, программируемость, Project Server, Project 2013, преимущества для EPM, Architecture и Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: В статьях в этом разделе описывается общая архитектура решения Enterprise Project Управления (EPM), которое объединяет Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413789"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Архитектура и программируемость Server 2013

В статьях в этом разделе описывается общая архитектура решения Enterprise Project Управления (EPM), которое объединяет Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Project Сервер 2013 построен с платформа .NET Framework 4 и является третьим крупным выпуском Project Server, чтобы обеспечить настоящую многоуровневую архитектуру. Для облачного доступа Project Server 2013 реализует клиентскую объектную модель (CSOM) и службу OData для отчетов, которые можно использовать в веб-приложениях, мобильных приложениях и приложениях Silverlight. Для локального приложения клиенты могут использовать службы CSOM или Project интерфейса (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Введение в архитектуру Project Server

В этом разделе описана общая архитектура решения Enterprise Project Управления (EPM), которое объединяет Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Для программного доступа Project Server следует использовать CSOM или службы PSI с интерфейсом Windows Communication Foundation (WCF). Интерфейс веб-службы ASMX PSI обесценяется в Project Server 2013, но по-прежнему работает. PSI обеспечивает эффективный доступ с помощью наборов данных, и вы можете создавать обработчики для событий на стороне сервера. Сам CSOM использует PSI для доступа к Project серверу бизнес-объекта. Вместо четырех Project серверов Project Server 2013 используется одна база данных в уровне доступа к данным.
  
Project Сервер 2013 глубоко интегрируется с SharePoint Server 2013. Служба Project приложений может быть связана с другими SharePoint веб-сайтов в ферме. Project Сервер может работать с SharePoint списками задач в коллекции сайтов, а также получать полный контроль, Project Server импортирует и управляет списками задач в качестве корпоративных проектов. Project Сервер также использует версию 4 Windows workflow Foundation (WF4) и добавляет действия рабочего процесса для решений по управлению спросом.
  
Для обсуждения многих новых функций, которые Project 2013 предоставляет для разработчиков, а также функции, которые являются амортизации, см. в [статьях Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>В этом разделе

[Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013 года, включая клиенты и серверы. 
  
[Project Программируемость](project-server-programmability.md) Сервера обсуждает основные функции Project Server 2013, настройку Project Web App и обновление приложений, которые были построены для предыдущих версий Project Server. 
  
[То, что PSI делает](what-the-psi-does-and-does-not-do.md) и не описывает сценарии, в которых можно использовать PSI, и перечисляет то, что не может сделать PSI. 
  
[То, что CSOM делает](what-the-csom-does-and-does-not-do.md) и не делает, описывает сценарии, в которых CSOM можно использовать, и перечисляет то, что CSOM не может сделать. 
  
### <a name="topics-not-covered"></a>Темы, не охваченные

Статьи в разделе  Архитектура и программируемость не документировать функции Project настольных клиентов (Project стандартный 2013 и Project профессиональный 2013 г.) или Project Web App. 
  
Visual Basic для приложений (VBA) справка доступна в редакторе Visual Basic в Project стандартный и Project профессиональный.
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Обновления для разработчиков в Project 2013](updates-for-developers-in-project-2013.md)
    
- [Начало разработки рабочих процессов Project Server](getting-started-developing-project-server-workflows.md)
    

