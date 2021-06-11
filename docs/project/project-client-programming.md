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
- vba, объектная модель проекта, Project, программируемость, программируемость, Project VBA, Visual Basic для приложений, Project объектная модель, VBA, объектная модель, VBA,Visual Basic для приложений
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Клиентские Project 2013 г. — Project стандартный 2013 г. и Project профессиональный 2013 г. — могут быть настроены и расширены с помощью VBA для записи макрос. Вы можете использовать Visual Studio 2012 для настройки пользовательского интерфейса ленты и создания сложных надстройок. Office Надстройки позволяют использовать новую модель размягчивости для области задач в Project, которые построены на общей платформе Office 2013 г. Project стандартный 2013 и Project профессиональный 2013 г. можно запускать общие надстройки Office и использовать надстройки области задач, разработанные специально для Project для интеграции с SharePoint, другими веб-сайтами и веб-приложениями и внешними данными.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301514"
---
# <a name="project-client-programming"></a>Программирование клиента Project

Клиентские Project 2013 г. — Project стандартный 2013 г. и Project профессиональный 2013 г. — могут быть настроены и расширены с помощью VBA для записи макрос. Вы можете использовать Visual Studio 2012 для настройки пользовательского интерфейса ленты и создания сложных надстройок. Office Надстройки позволяют использовать новую модель размягчивости для области задач в Project, которые построены на общей платформе Office 2013 г. Project стандартный 2013 и Project профессиональный 2013 г. можно запускать общие надстройки Office и использовать надстройки области задач, разработанные специально для Project для интеграции с SharePoint, другими веб-сайтами и веб-приложениями и внешними данными.
  
 **Перемещение в Visual Studio** VBA полезен для записи макрос и разработки относительно простых решений автоматизации. Для разработки надстройок, надстройок и более сложных, безопасных, масштабируемых и легко развертываемых решений рекомендуется использовать Visual Studio 2012 г. Основная сборка платформа .NET Framework 4.0 и Project 2013 г. предоставляют множество преимуществ для разработки и развертывания решений, которые автоматизируют и интегрируют Project настольных клиентов 2013 г. 
  
> [!NOTE]
> Вы можете использовать Visual Studio 2010 для разработки Project надстройки. Однако Visual Studio 2012 г. включает шаблоны и расширения, предназначенные для создания Office надстройки. 
  
Объектная модель **MSProject** для VBA Project 2013 г., по сути, такая же, как **и Microsoft.Office. Объектная модель Interop.MSProject** для решений с управляемым кодом с Office средствами разработчика для Visual Studio 2013 (также известный как VSTO). Visual Studio 2012 г. включает шаблоны для разработки надстройок на уровне приложений за Project 2010 г. и Project 2013 г. (либо Project стандартный, либо Project профессиональный версии). VSTO и Office средства разработки для Visual Studio 2012 г. упрощают разработку, тестирование и развертывание расширенных интеграционных решений, которые могут использовать настольные клиенты Project и другие приложения Office 2013 г., а также интегрироваться с SharePoint сайтов, списков и рабочих процессов. 
  
Надстройки области задач и другие надстройки для Office и SharePoint можно продавать в магазине Office (см.) для использования как с Project Online, так и с локальной [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) установкой. Макрос и VSTO VBA нельзя распространять в Office Магазине; они предназначены для локального использования с Project стандартный и Project профессиональный. Макрос VBA можно распространять в рамках проекта. MPP-файл, установите их в файл Global.MPT на компьютере или раздайте в корпоративном глобальном шаблоне Project Server 2013. VSTO надстройки можно более безопасно распространять через [ClickOnce,](https://msdn.microsoft.com/library/t71a733d.aspx) что позволяет легко обновлять. 
  
## <a name="reference"></a>Справочные материалы

[Project ссылки на разработчика VBA](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Содержит вводные статьи и статьи справки по VBA. 
  
## <a name="related-sections"></a>Связанные разделы

[Project Server 2013](project-server-2013-architecture.md) Показывает, как Project клиенты взаимодействуют с Project Server. 
  
## <a name="see-also"></a>См. также

- [Project для разработчиков](https://msdn.microsoft.com/office/aa905469)
- [Office центра разработки](https://dev.office.com)
- [Visual Studio центра разработки](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce Безопасность и развертывание](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Справочник по доступным полям](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

