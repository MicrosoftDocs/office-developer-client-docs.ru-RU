---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411556"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Кодирует идентификатор входа в строку ASCII. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parameters

 _cb_
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _pentry._ 
    
 _pentry_
  
> [in] Указатель на [структуру ENTRYID,](entryid.md) которая содержит кодируемый идентификатор входа. 
    
 _psz_
  
> [вышел] Указатель на возвращенную строку ASCII.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Функции [HrEntryIDFromSz](hrentryidfromsz.md) и **HrSzFromEntryID** обеспечивают преобразование между строками и двоичными форматами идентификаторов записи. С MAPI необходимо использовать структуры с двоичными данными. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrSzFromEntryID** выделяет память для строки ASCII с помощью [функции MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  

