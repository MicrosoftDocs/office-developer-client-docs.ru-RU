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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579601"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выделяет буфер памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Параметры

 _cbSize_
  
> [in] Размер, в байтах, выделения буфера. 
    
 _lppBuffer_
  
> [out] Указатель на возвращаемый выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и вернул буфер запрошенные памяти.
    
## <a name="remarks"></a>Замечания

Во время **MAPIAllocateBuffer** вызовите обработки, вызывающий реализации Получает блок памяти от операционной системы. Буфер памяти, выделенный на адрес четных байтов. На платформах, где доступа "длинное целое" — это более эффективный операционная система выделяет буфера на адрес, размер которых в байтах делится на четыре. 
  
Вызов выпусков функция [MAPIFreeBuffer](mapifreebuffer.md) буфер памяти, выделенный с **MAPIAllocateBuffer**путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и буферов по ссылке, когда объем памяти больше не требуется. 
  
## <a name="see-also"></a>См. также



[MAPIReallocateBuffer](mapireallocatebuffer.md)

