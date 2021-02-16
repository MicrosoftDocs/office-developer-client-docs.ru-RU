---
title: Начало разработки рабочих процессов Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Процессы управления запросами в Project Server 2013 включают в себя процессы, которые помогают управлять предложениями по проектам и анализом портфеля. В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344473"
---
# <a name="getting-started-developing-project-server-workflows"></a>Начало разработки рабочих процессов Project Server

Процессы управления запросами в Project Server 2013 включают в себя процессы, которые помогают управлять предложениями по проектам и анализом портфеля. В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.
  
В рабочего процессах Project Server 2013 используется платформа рабочего процесса SharePoint Server 2013, построенная на платформе Windows Workflow Foundation (WF4) версии 4. Рабочие процессы на основе WF4 являются декларативными, что означает, что средство создания рабочего процесса сохраняет стадии, действия, условия и другие элементы рабочего процесса в код XAML, который интерпретируется во время выполнения. Для создания декларативных рабочих процессов можно использовать SharePoint Designer 2013 Visual Studio 2012. Для рабочего процесса требуется механизм выполнения Workflow Manager Client 1.0, который может быть на локальном сервере для локальных решений или на удаленном сервере для решений Project Online.
  
SharePoint Designer 2013 можно использовать для создания относительно простых декларативных рабочих процессов. Для сложных и шаблонов рабочего процесса, которые можно использовать повторно, можно использовать Visual Studio 2012 для разработки и отлаки рабочего процесса для Project Web App. Дополнительные сведения см. в подпроекте "Создание рабочих процессов проекта [Visual Studio 2012".](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
> [!IMPORTANT]
> Рекомендуется разрабатывать и тестировать рабочие процессы не в рабочей, а в тестовой установке Project Server. Процессы, разработанные для предварительных версий Project Server 2013, должны тестироваться для версии выпуска, и их может потребоваться создать повторно и повторно. 
  
## <a name="in-this-section"></a>В этом разделе:

[Создание рабочего процесса Project Server для управления запросами](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>См. также



[Массовое обновление настраиваемой поля и создание сайтов проектов из рабочего процесса Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Разработка рабочих процессов в SharePoint Designer 2013 и Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Что нового в рабочих процессах для SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Разработка рабочих процессов в SharePoint 2013 с помощью Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Создание рабочих процессов проекта с Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Введение разработчика в Windows Workflow Foundation (WF) в .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Руководство по управлению запросами (официальный документ) от компании Вайскера](https://msdn.microsoft.com/library/ff973112.aspx)

