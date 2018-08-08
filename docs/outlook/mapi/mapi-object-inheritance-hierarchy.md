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
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809775"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Иерархия наследования MAPI объекта

**Относится к**: Outlook 
  
Все интерфейсы, реализованные объектов MAPI в конечном счете наследовать от [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), интерфейс OLE, которая позволяет объекты для связи. Большинство интерфейсов напрямую наследовать от **IUnknown**, но некоторые наследование от одного из двух базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) или [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). На следующем рисунке показана иерархия наследования завершения в MAPI.
  
**Иерархия наследования MAPI**
  
![Иерархия наследования MAPI] (media/amapi_06.gif "Иерархия наследования MAPI")
  
## <a name="see-also"></a>См. также

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Обзор интерфейса и объект MAPI](mapi-object-and-interface-overview.md)

