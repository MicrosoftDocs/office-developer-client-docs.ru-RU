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
- vba, объектная модель проекта,Project, programmability,Programmability, Project VBA,Visual Basic для приложений, объектная модель Project,VBA, объектная модель, VBA,Visual Basic для приложений
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Клиентские клиентские приложения Project 2013 для настольных ПК ( Project Стандартный 2013 и Project профессиональный 2013) можно настраивать и расширять с помощью VBA для записи макроса. Вы можете использовать Visual Studio 2012 для настройки пользовательского интерфейса ленты и создания сложных надстройок. Надстройки Office позволяют использовать новую модель возможностей для области задач в Project, построенную на общей платформе Office 2013. Project стандартный 2013 и Project профессиональный 2013 могут запускать общие надстройки Office и использовать надстройки области задач, разработанные специально для Project, для интеграции с SharePoint, другими веб-сайтами и веб-приложениями, а также внешними данными.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301514"
---
# <a name="project-client-programming"></a>Программирование клиента Project

Клиентские приложения Project 2013 для настольных ПК Project Стандартный 2013 и Project профессиональный 2013 можно настраивать и расширять с помощью VBA для записи макроса. Вы можете использовать Visual Studio 2012 для настройки пользовательского интерфейса ленты и создания сложных надстройок. Надстройки Office позволяют использовать новую модель возможностей для области задач в Project, построенную на общей платформе Office 2013. Project стандартный 2013 и Project профессиональный 2013 могут запускать общие надстройки Office и использовать надстройки области задач, разработанные специально для Project, для интеграции с SharePoint, другими веб-сайтами и веб-приложениями, а также внешними данными.
  
 **Переход к Visual Studio** VBA полезен для записи макроса и разработки относительно простых решений автоматизации. Чтобы разрабатывать надстройки области задач, надстройки и более сложные, безопасные, масштабируемые и легко развертываемые решения, рекомендуется использовать Visual Studio 2012. Microsoft .NET Framework 4.0 и основная сборка междомения Project 2013 предоставляют множество преимуществ для разработки и развертывания решений, автоматизируемых и интегрируемых классических клиентов Project 2013. 
  
> [!NOTE]
> Вы можете использовать Visual Studio 2010 для разработки надстройки Project. Однако Visual Studio 2012 включает шаблоны и расширения, предназначенные для создания клиентов надстройки Office. 
  
Объектная модель **MSProject** для VBA в Project 2013 практически такая же, как объектная модель **Microsoft.Office.Interop.MSProject** для решений с управляемым кодом с помощью средств разработчика Office для Visual Studio 2013 (также известной как VSTO). Visual Studio 2012 включает шаблоны для разработки надстройки на уровне приложений для Project 2010 и Project 2013 (версии Project Стандартный или Project профессиональный). VSTO и инструменты разработчика Office для Visual Studio 2012 упрощают разработку, тестирование и развертывание расширенных решений интеграции, которые могут использовать настольный клиент Project и другие приложения Office 2013, а также интегрируются с сайтами, списками и рабочими процессами SharePoint. 
  
Надстройки области задач и другие надстройки для Office и SharePoint можно продавать в Магазине Office (см. ) для использования как с Project Online, так и с локальной [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) установкой. Макрос VBA и надстройки VSTO нельзя распространять в Магазине Office; Они предназначены для локального использования с Project Standard и Project профессиональный. Макрос VBA можно распространять в проекте. MPP-файл, установите их в файле Global.MPT на компьютере или раздайте в глобальном корпоративном шаблоне в Project Server 2013. Надстройки VSTO можно распространять более [](https://msdn.microsoft.com/library/t71a733d.aspx) безопасно с помощью ClickOnce развертывания, что позволяет легко обновлять их. 
  
## <a name="reference"></a>Справка

[Справочник разработчика Project VBA](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Содержит вводные статьи и статьи справки по VBA. 
  
## <a name="related-sections"></a>Связанные разделы

[Архитектура Project Server 2013](project-server-2013-architecture.md) Показывает, как клиенты Project взаимодействуют с Project Server. 
  
## <a name="see-also"></a>См. также

- [Project для разработчиков](https://msdn.microsoft.com/office/aa905469)
- [Центр разработчиков Office](https://dev.office.com)
- [Visual Studio центра разработчиков](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce безопасности и развертывания](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Справочник по доступным полям](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

