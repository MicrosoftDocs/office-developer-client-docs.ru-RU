---
title: Реализация объектов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310173"
---
# <a name="implementing-mapi-objects"></a>Реализация объектов MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Объекты MAPI можно реализовать с помощью классов C++ или C-структур данных в зависимости от языка и набора API, который использует клиент или поставщик услуг. Поставщики услуг могут быть написаны в C или C++ с интерфейсом поставщика услуг MAPI; клиентские приложения также могут использовать C или C++. По возможности клиенты и поставщики услуг, которые используют объектно-ориентированный интерфейс программирования, должны использовать C++. 
  
C++ является предпочтительным выбором, так как MAPI — это объектная технология, а C++ легче поддается объектной разработке. В результате код проще и проще, что упрощает обслуживание. Документация MAPI написана в основном для разработчиков C++; Все описания синтаксиса для методов интерфейса MAPI в этой ссылке находятся в C++.
  
Разработчики могут использовать Microsoft Visual Studio и сторонние средства разработки для разработки решений, которые называют MAPI. Обратите внимание, что разработчики должны использовать C или неуправляемую C++, но не управлять C++ для записи решений MAPI.
  
При реализации объекта MAPI клиент или поставщик услуг создает код для всех методов интерфейса, код для любых частных методов, которые специфичную для реализации, и код для поддержки частных пользователей данных для поддержания сведений о состоянии. Код для методов интерфейса должен следовать спецификациям, опубликованным MAPI этого документа ожидаемого поведения. 
  
В заглавном файле Mapidefs.h и заголовке OLE много макрос, которые клиенты и поставщики услуг на любом языке могут использовать для пользования определениями объектов MAPI. Например, существует макрос для определения методов каждого из интерфейсов MAPI. Макрос для определения методов [интерфейса IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) отображается в Mapidefs.h следующим образом: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>См. также



[Обзор объектов и интерфейсов MAPI](mapi-object-and-interface-overview.md)

