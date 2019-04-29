---
title: Иконтабадминремовесторе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435420"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет адресную книгу контакта (CAB-файл), указанную указанным ИДЕНТИФИКАТОРом записи, из иерархии адресной книги.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _Кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _Лпентрид_
  
> возврата Указатель на идентификатор записи объекта, который требуется открыть.
    

