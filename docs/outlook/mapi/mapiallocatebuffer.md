---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425696"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выделяет буфер памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Параметры

 _cbSize_
  
> [in] Размер выделяемого буфера (в bytes). 
    
 _lppBuffer_
  
> [out] Указатель на возвращенный выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвращен запрашиваемой памяти.
    
## <a name="remarks"></a>Примечания

Во время обработки вызовов **MAPIAllocateBuffer** реализация вызова получает блок памяти из операционной системы. Буфер памяти выделяется для even-numbered byte address. На платформах, где длинный полный доступ более эффективен, операционная система выделяет буфер на адресе, размер которого в кратном размере кратно четырем. 
  
Вызов функции [MAPIFreeBuffer](mapifreebuffer.md) освобождает буфер памяти, выделенный **MAPIAllocateBuffer,** путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и всех связанных с ней буферов, когда память больше не требуется. 
  
## <a name="see-also"></a>См. также



[MAPIReallocateBuffer](mapireallocatebuffer.md)

