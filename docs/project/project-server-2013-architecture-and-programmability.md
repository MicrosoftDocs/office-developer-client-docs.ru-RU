---
title: Архитектура Project Server 2013 и Программируемость
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
- преимущества архитектуры и программирования, программирования, Project Server, Project 2013 для EPM, архитектуры и Project Server, Project 2013
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: В статьях этого раздела описывается общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813062"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Архитектура Project Server 2013 и Программируемость

В статьях этого раздела описывается общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Project Server 2013, созданных с помощью .NET Framework 4 и — это третий основной версии Project Server для обеспечения true многоуровневой архитектуре. Для доступа к облачных Project Server 2013 реализует клиентской объектной модели (CSOM) и службе OData для создания отчетов, который может использоваться веб-приложений, мобильных приложений и приложений Silverlight. Для приложений в локальной клиенты могут использовать CSOM или службы интерфейса Project Server (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Общие сведения об архитектуре Project Server

В этом разделе описываются общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
  
Для программного доступа к серверу Project Server с помощью интерфейса Windows Communication Foundation (WCF) следует использовать службы PSI или CSOM. Интерфейс веб-службы ASMX из PSI рекомендуется использовать в Project Server 2013, но по-прежнему работает. PSI включает эффективного доступа с помощью наборов данных и можно создать обработчики для событий на сервере. CSOM самого использует PSI для доступа к бизнес-объектов Project Server уровне. Вместо четырех баз данных Project Server Project Server 2013 использует одну базу данных в уровень доступа к данным.
  
Project Server 2013 глубоко интегрированы с SharePoint Server 2013. Служба приложения Project может быть связан с другим семействам сайтов SharePoint в ферме. Project Server можно работать с и создание отчетов по SharePoint, списки задач в семейства веб-сайтов и может также получить полный доступ, где Project Server импортирует и управляет списки задач как корпоративных проектов. Project Server также использует версии 4 Windows Workflow Foundation (WF4) и добавляет действий рабочего процесса для решений по управлению запросами.
  
Описание множество новых функций, предоставляемых Project 2013 для разработчиков и компонентов, которые поддерживаются посетите страницу [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>В этой статье

[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, включая клиенты и серверы. 
  
[Возможность программирования Project Server](project-server-programmability.md) рассматриваются возможности основных расширяемости Project Server 2013 Настройка Project Web App и обновление приложения, созданные для предыдущих версий Project Server. 
  
[Что PSI делает и не имеет](what-the-psi-does-and-does-not-do.md) описаны сценарии использования PSI и перечислены возможности, которые не PSI. 
  
[CSOM что делает и не поддерживает](what-the-csom-does-and-does-not-do.md) описаны сценарии, где можно использовать CSOM и перечислены возможности, которые не CSOM. 
  
### <a name="topics-not-covered"></a>Темы не охватывают

Статьи в разделе *архитектуры и программирования* свойства проекта настольных клиентов (стандартный 2013 Project и Project Professional 2013) или Project Web App не документов. 
  
Visual Basic для приложений (VBA) Справка доступна в редакторе Visual Basic в Project Стандартный и Project Professional.
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Обновления для разработчиков в Project 2013](updates-for-developers-in-project-2013.md)
    
- [Начало разработки рабочих процессов Project Server](getting-started-developing-project-server-workflows.md)
    

