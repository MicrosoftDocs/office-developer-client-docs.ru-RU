---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347812"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Повторно создает идентификатор записи из кодировки ASCII. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Параметры

 _СЗ_
  
> возврата Указатель на строку ASCII, из которой создается идентификатор записи. 
    
 _ПКБ_
  
> вышли Указатель на размер (в байтах) идентификатора записи, на который указывает параметр _ппентри_ . 
    
 _ппентри_
  
> вышли Указатель на указатель на возвращенную структуру [EntryID](entryid.md) , содержащую новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Отдых успешно создан.
    
МАПИ_Е_ИНВАЛИД_ЕНТРИД
  
> Недопустимый идентификатор записи.
    
## <a name="remarks"></a>Примечания

Функции **хрентридфромсз** и [хрсзфроментрид](hrszfromentryid.md) обеспечивают преобразование между строковым и двоичным форматами идентификаторов записей. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **хрентридфромсз** выделяет память для строки ASCII с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) . 
  

