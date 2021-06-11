---
title: Иерархия наследования объектов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345844"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Иерархия наследования объектов MAPI

**Область применения**: Outlook 2013 | Outlook 2016 
  
Все интерфейсы, реализованные объектами MAPI, в конечном счете наследуются [интерфейсом IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), интерфейсом OLE, который позволяет объектам общаться. Большинство интерфейсов непосредственно наследуют от **IUnknown,** но некоторые наследуют от одного из двух других базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) или [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). На следующем рисунке показана полная иерархия наследования в MAPI.
  
**Иерархия наследования MAPI**
  
![Иерархия наследования MAPI](media/amapi_06.gif "MAPI")
  
## <a name="see-also"></a>См. также

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Обзор объектов и интерфейсов MAPI](mapi-object-and-interface-overview.md)

