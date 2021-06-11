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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _cbSize_
  
> [in] Размер выделенного буфера в bytes. 
    
 _lppBuffer_
  
> [вышел] Указатель на возвращенный выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает запрашиваемую буферную память.
    
## <a name="remarks"></a>Примечания

Во **время обработки вызовов MAPIAllocateBuffer** реализация вызовов получает блок памяти из операционной системы. Буфер памяти выделяется на 10-номерный byte-адрес. На платформах, где более эффективным является длительный доступ к сети, операционная система выделяет буфер на адрес, размер которого в bytes — несколько из четырех. 
  
Вызов функции [MAPIFreeBuffer](mapifreebuffer.md) освобождает буфер памяти, выделенный **MAPIAllocateBuffer,** путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и любых буферов, связанных с ней, когда память больше не требуется. 
  
## <a name="see-also"></a>См. также



[MAPIReallocateBuffer](mapireallocatebuffer.md)

