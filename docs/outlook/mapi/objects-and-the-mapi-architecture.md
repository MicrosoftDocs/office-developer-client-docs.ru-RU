---
title: Объекты и архитектура MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279792"
---
# <a name="objects-and-the-mapi-architecture"></a>Объекты и архитектура MAPI

**Область применения**: Outlook 2013 | Outlook 2016 
  
Все объекты, которые определяет MAPI, попадают в один или несколько слоев в архитектуре MAPI. Уровень клиентского интерфейса содержит все объекты, которые могут реализовать клиентские приложения, просмотра форм или сервера форм. Уровень интерфейса поставщика услуг содержит объекты, которые может реализовать поставщик услуг любого типа. Этот слой включает объекты, реализованные адресными книгами, хранилищами сообщений, поставщиками транспорта и библиотеками форм. Слой, представляючий подсистему MAPI, находится между уровнями интерфейса клиента и поставщика услуг. Слой MAPI содержит все объекты, которые MAPI реализует для клиентов или поставщиков услуг для использования. 
  
На следующем рисунке показано, где каждый из объектов MAPI вписывается в архитектуру MAPI. Объекты представлены с именами полученных интерфейсов. Например, объект раковины рекомендации отображается как [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), интерфейс, который происходит от [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) и что каждый советовать объект раковины реализует. Интерфейсы, которые мостит слои, используются или реализуются несколькими компонентами. Несмотря на то, что уровень MAPI, как представляется, разделяет уровни клиента и поставщика, подразумевая, что все коммуникации должны проходить через MAPI, это не так. Клиенты могут общаться напрямую с объектами поставщика услуг. 
  
**Уровни объектов в MAPI**
  
![Уровни объектов в слоях mapi](media/amapi_38.gif "Object в MAPI")
  
## <a name="see-also"></a>См. также

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Обзор объектов и интерфейсов MAPI](mapi-object-and-interface-overview.md)

