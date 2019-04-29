---
title: Архитектура и возможности программирования Project Server 2013
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
- проект 2013, архитектура и программируемость, программирование, программирование, Project Server, проект 2013, преимущества для EPM, архитектура и Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Статьи в этом разделе описывают общую архитектуру решения по управлению корпоративными проектами (EPM), которое сочетает Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413789"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Архитектура и возможности программирования Project Server 2013

Статьи в этом разделе описывают общую архитектуру решения по управлению корпоративными проектами (EPM), которое сочетает Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Project Server 2013 создан с помощью .NET Framework 4 и является третьим основным выпуском Project Server для реализации многоуровневой многоуровневой архитектуры. Для облачного доступа Project Server 2013 реализует клиентскую объектную модель (CSOM) и службу OData для создания отчетов, которые можно использовать в веб-приложениях, мобильных приложениях и приложениях Silverlight. Для локальных приложений клиенты могут использовать либо службы CSOM, либо службы интерфейса Project Server (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Общие сведения об архитектуре Project Server

В подразделах этого раздела описывается общая архитектура решения для управления корпоративными проектами (EPM), которая сочетает в себе Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Для программного доступа к Project Server следует использовать CSOM или службы PSI с интерфейсом Windows Communication Foundation (WCF). Интерфейс веб-службы ASMX PSI является устаревшим в Project Server 2013, но по-прежнему работает. PSI обеспечивает эффективный доступ с помощью наборов данных, и вы можете создавать обработчики для событий на стороне сервера. CSOM сам использует PSI для доступа к уровню бизнес-объектов Project Server. Вместо четырех баз данных Project Server 2013 в Project Server используется одна база данных на уровне доступа к данным.
  
Project Server 2013 тесно интегрируется с SharePoint Server 2013. Служба приложения Project может быть связана с другими семействами веб-сайтов SharePoint в ферме. Project Server может работать с списками задач SharePoint в семействе веб-сайтов и сообщать о них, а также получать полный доступ, когда Project Server импортирует и управляет списками задач в качестве корпоративных проектов. Project Server также использует версию 4 для Windows Workflow Foundation (WF4) и добавляет действия рабочего процесса для решений управления запросами.
  
Сведения о многочисленных новых возможностях, предоставляемых Project 2013 для разработчиков, а также об устаревших функциях можно узнать [в статье Updates for Developers in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>В этом разделе:

[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, в том числе клиенты и серверы. 
  
[Программирование Project Server](project-server-programmability.md) обсуждает основные функции расширения project Server 2013, настройка Project Web App и обновление приложений, созданных для предыдущих версий Project Server. 
  
[Что делает PSI и не выполняет](what-the-psi-does-and-does-not-do.md) описание сценариев, в которых можно использовать PSI, и список действий, которые не могут выполняться в PSI. 
  
[Действия, выполняемЫЕ CSOM,](what-the-csom-does-and-does-not-do.md) не описывают сценарии, в которых можно использовать CSOM, и перечислены действия, которые не могут делать CSOM. 
  
### <a name="topics-not-covered"></a>Неохваченные темы

В статьях раздела *архитектура и программирование* не задокументированы компоненты клиентских настольНых компьютеров Project (project стандартный 2013 и project профессиональный 2013) или Project Web App. 
  
Справка по Visual Basic для приложений (VBA) доступна в редакторе Visual Basic в Project Standard и Project профессиональный.
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Обновления для разработчиков в Project 2013](updates-for-developers-in-project-2013.md)
    
- [Начало разработки рабочих процессов Project Server](getting-started-developing-project-server-workflows.md)
    

