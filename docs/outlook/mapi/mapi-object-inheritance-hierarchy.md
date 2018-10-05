---
title: Иерархия наследования MAPI объекта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391789"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Иерархия наследования MAPI объекта

**Относится к**: Outlook 2013 | Outlook 2016 
  
Все интерфейсы, реализованные объектов MAPI в конечном счете наследовать от [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), интерфейс OLE, которая позволяет объекты для связи. Большинство интерфейсов напрямую наследовать от **IUnknown**, но некоторые наследование от одного из двух базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) или [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). На следующем рисунке показана иерархия наследования завершения в MAPI.
  
**Иерархия наследования MAPI**
  
![Иерархия наследования MAPI] (media/amapi_06.gif "Иерархия наследования MAPI")
  
## <a name="see-also"></a>См. также

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Обзор интерфейса и объект MAPI](mapi-object-and-interface-overview.md)

