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
ms.openlocfilehash: a524a7eb40c33d6de2f64cd5373c9a39a8a1e3df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565300"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Повторно создает запись идентификатора из кодировки ASCII. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
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

 _sz_
  
> [in] Указатель на строку ASCII из которого требуется создать запись идентификатора. 
    
 _печатной_
  
> [out] Указатель на размер, в байтах, идентификатор записи, на который указывает параметр _ppentry_ . 
    
 _ppentry_
  
> [out] Указатель на указатель на структуру возвращенные [ENTRYID](entryid.md) , который содержит новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Повторное создание прошла успешно.
    
MAPI_E_INVALID_ENTRYID
  
> Недопустимый идентификатор записи.
    
## <a name="remarks"></a>Примечания

Функции **HrEntryIDFromSz** и [HrSzFromEntryID](hrszfromentryid.md) преобразование между строки и двоичного формата идентификаторы записей. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrEntryIDFromSz** выделение памяти для строки ASCII, с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

