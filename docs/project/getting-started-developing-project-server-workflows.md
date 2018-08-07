---
title: Начало разработки рабочих процессов Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Запросу, что процессы управления в Project Server 2013 включить рабочие процессы, которые помогут вам управлять предложений по проекту и анализа портфеля. В этом разделе представлены статьи, в которых показано, как для создания рабочих процессов для Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812917"
---
# <a name="getting-started-developing-project-server-workflows"></a>Начало разработки рабочих процессов Project Server

Запросу, что процессы управления в Project Server 2013 включить рабочие процессы, которые помогут вам управлять предложений по проекту и анализа портфеля. В этом разделе представлены статьи, в которых показано, как для создания рабочих процессов для Project Server.
  
Рабочих процессов Project Server 2013 использованию платформы рабочих процессов SharePoint Server 2013, создан на основе версии 4 Windows Workflow Foundation (WF4). Рабочих процессов на основе WF4 являются декларативные, это означает, что средства создания рабочих процессов сохраняет стадии рабочего процесса, действия, условия и другие элементы кода XAML, который обрабатывается во время выполнения. Создание декларативных рабочих процессов можно использовать SharePoint Designer 2013 или Visual Studio 2012. Рабочий процесс требует ядро выполнения 1.0 клиент диспетчера рабочих процессов, который может быть на локальном сервере для локальных решений или на удаленном сервере для Project Online решений.
  
SharePoint Designer 2013 можно использовать для создания сравнительно легко декларативных рабочих процессов. Для сложных рабочих процессов и шаблоны рабочих процессов, которые можно повторно использовать можно использовать Visual Studio 2012 для разработки и отладки рабочих процессов для Project Web App. Для получения дополнительных сведений см. [Создание рабочих процессов Project с помощью Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Используйте пробную установку Project Server, не производственной установки для разработки и тестирования рабочих процессов. Рабочие процессы, разработанных для предварительных версий Project Server 2013 должно тестироваться версии выпуска и может потребоваться создать заново и повторного развертывания. 
  
## <a name="in-this-section"></a>В этой статье

[Создание рабочего процесса Project Server для управления запросами](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>См. также



[Обновление настраиваемых полей в пакетном режиме и создание сайтов проектов из Project Online рабочего процесса](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Workflow development in SharePoint Designer 2013 and Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[Что нового в рабочих процессах для SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[Разработка рабочих процессов в SharePoint 2013 с помощью Visual Studio](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[Создание рабочих процессов Project, с помощью Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[Введение для разработчиков для Windows Workflow Foundation (WF) в .NET 4](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[Путеводитель по управлению запросами (технический документ)](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

