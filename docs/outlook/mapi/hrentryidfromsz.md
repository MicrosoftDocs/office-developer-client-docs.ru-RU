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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437730"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Воссоздает идентификатор записи из коди-кодии ASCII. 
  
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

## <a name="parameters"></a>Parameters

 _sz_
  
> [in] Указатель на строку ASCII, из которой создается идентификатор записи. 
    
 _pcb_
  
> [вышел] Указатель на размер в bytes идентификатора записи, указываемого параметром _ppentry._ 
    
 _ppentry_
  
> [вышел] Указатель на указатель на возвращаемую [структуру ENTRYID,](entryid.md) содержаную новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Отдых был успешным.
    
MAPI_E_INVALID_ENTRYID
  
> ID записи был недействительным.
    
## <a name="remarks"></a>Примечания

Функции **HrEntryIDFromSz** и [HrSzFromEntryID](hrszfromentryid.md) обеспечивают преобразование между строками и двоичными форматами идентификаторов записи. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrEntryIDFromSz** выделяет память для строки ASCII с помощью [функции MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  

