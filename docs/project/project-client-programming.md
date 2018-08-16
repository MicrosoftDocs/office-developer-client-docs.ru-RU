---
title: Программирование клиента Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, project объектной модели Project, программирования, программирования, проекта VBA, Visual Basic для приложений, объектной модели VBA, объектной модели проектов, VBA, Visual Basic для приложений
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Приложения рабочего стола клиента Project 2013 — Project Стандартный 2013 и Project Professional 2013 — могут быть настроены и расширенных с помощью VBA для записи макросов. Настройка пользовательского интерфейса ленты и создание сложных надстройками новое расширение модели для областей задач в проекте, основанные на общей платформе Office 2013 включает надстроек Office можно использовать Visual Studio 2012. Project Стандартный 2013 и Project Professional 2013 можно выполнять общие надстроек Office и использовать задач области надстройки, разработанными специально для проекта для интеграции с SharePoint, других веб-сайтов и веб-приложений и внешних данных.
ms.openlocfilehash: e8604b4d479d0c64f8d45ad2363d7391d57408ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813056"
---
# <a name="project-client-programming"></a>Программирование клиента Project

Приложения рабочего стола клиента Project 2013 — Project Стандартный 2013 и Project Professional 2013 — могут быть настроены и расширенных с помощью VBA для записи макросов. Настройка пользовательского интерфейса ленты и создание сложных надстройками новое расширение модели для областей задач в проекте, основанные на общей платформе Office 2013 включает надстроек Office можно использовать Visual Studio 2012. Project Стандартный 2013 и Project Professional 2013 можно выполнять общие надстроек Office и использовать задач области надстройки, разработанными специально для проекта для интеграции с SharePoint, других веб-сайтов и веб-приложений и внешних данных.
  
 **Перемещение в Visual Studio** VBA можно использовать для записи макросов и разработку решений относительно простой автоматизации. Разработка надстроек для области задач, надстройки и несколько сложнее, надежные, масштабируемые и легко развернутых решений мы рекомендуем использовать Visual Studio 2012. Microsoft .NET Framework 4.0 и основной сборки взаимодействия Project 2013 предоставляют многочисленные преимущества для разработки и развертывания решений, автоматизировать и интеграции клиентов Project 2013. 
  
> [!NOTE]
> С помощью Visual Studio 2010 для разработки надстройки Project. Тем не менее Visual Studio 2012 включает в себя шаблоны и расширения, которые предназначены для создания надстроек Office клиентов. 
  
Объектной модели **MSProject** для VBA в Project 2013 практически не совпадает с **Microsoft.Office.Interop.MSProject** объектной модели для решения с управляемым кодом со средствами для разработчиков Office для Visual Studio 2013 (также известной как VSTO). Visual Studio 2012 включает в себя шаблоны для разработки уровня приложения надстройки для Project 2010 и Project 2013 (версии Project Standard или Project Professional). VSTO и инструменты разработчика Office для Visual Studio 2012 упростить разработку, тестирование и развертывание расширенной интеграции решений, которые можно использовать клиент рабочего стола Project и других приложений Office 2013 и интегрировать с сайтами SharePoint, списки, и рабочие процессы. 
  
Надстройки для области задач и другие надстройки для Office и SharePoint может продаваться в магазине Office (просмотреть [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) для использования с Project Online и локальной установки. Надстройки VSTO и макросов VBA не распространяется в магазине Office; они предназначены для локального использования с Project Стандартный и Project Professional. Можно распределить макросов VBA в рамках проекта. MPP-файла, установить их в нескольких проектах файл на своем компьютере или распространять их в глобальный корпоративный шаблон в Project Server 2013. Надстройки VSTO могут распространяться на более безопасной развертывания [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx) , которая позволяет легко обновлений. 
  
## <a name="reference"></a>Справочные материалы

[Справочник разработчика по Project VBA](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx) Содержит вводную и статьи по справке VBA. 
  
## <a name="related-sections"></a>Связанные разделы

[Архитектура Project Server 2013](project-server-2013-architecture.md) Показывает, как клиенты Project для взаимодействия с Project Server. 
  
## <a name="see-also"></a>См. также



[Project для разработчиков (en)](http://msdn.microsoft.com/en-us/office/aa905469)
  
[Центр для разработчиков Office](https://dev.office.com)
  
[Центр разработчиков Visual Studio](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
  
[Развертывание и безопасность технологии ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)
  
[Справочник по доступным полям](http://office.microsoft.com/en-us/project-help/available-fields-reference-HA102749299.aspx?CTT=1)
