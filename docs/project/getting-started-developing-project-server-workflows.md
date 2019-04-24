---
title: Начало разработки рабочих процессов Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Процессы управления запросами в Project Server 2013 включают рабочие процессы, помогающие управлять предложениями по проекту и анализом портфелей. В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344473"
---
# <a name="getting-started-developing-project-server-workflows"></a>Начало разработки рабочих процессов Project Server

Процессы управления запросами в Project Server 2013 включают рабочие процессы, помогающие управлять предложениями по проекту и анализом портфелей. В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.
  
Рабочие процессы Project Server 2013 используют платформу рабочих процессов SharePoint Server 2013, созданную на базе версии 4 Windows Workflow Foundation (WF4). Рабочие процессы на основе WF4 являются декларативными, что означает, что средство создания рабочего процесса сохраняет стадии, действия, условия и другие элементы рабочего процесса в код XAML, который интерпретируется во время выполнения. Для создания декларативных рабочих процессов можно использовать SharePoint Designer 2013 или Visual Studio 2012. Для рабочего процесса необходим исполняемый модуль диспетчера рабочих процессов 1,0, который может находиться на локальном сервере для локальных решений или на удаленном сервере для решений Project Online.
  
Вы можете использовать SharePoint Designer 2013 для создания сравнительно простых декларативных рабочих процессов. Для сложных рабочих процессов и шаблонов рабочих процессов, которые можно использовать повторно, можно использовать Visual Studio 2012 для разработки и отладки рабочих процессов Project Web App. Дополнительные сведения см. [в статье Создание рабочих процессов Project с помощью Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Рекомендуется разрабатывать и тестировать рабочие процессы не в рабочей, а в тестовой установке Project Server. Рабочие процессы, разработанные для предварительных версий Project Server 2013, должны быть проверены на наличие версии выпуска и могут быть созданы повторно и повторно развернуты. 
  
## <a name="in-this-section"></a>Содержание

[Создание рабочего процесса Project Server для управления запросами](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>См. также



[Массовое обновление настраиваемых полей и создание сайтов проектов из рабочего процесса Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Разработка рабочих процессов в SharePoint Designer 2013 и Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Что нового в рабочих процессах для SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Разработка рабочих процессов в SharePoint 2013 с помощью Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Создание рабочих процессов проекта с помощью Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Введение для разработчиков Windows Workflow Foundation (WF) в .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Путеводитель по управлению запросами (технический документ)](https://msdn.microsoft.com/library/ff973112.aspx)

