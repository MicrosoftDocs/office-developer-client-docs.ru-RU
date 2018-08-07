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
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809861"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Относится к**: Outlook 
  
Выделяет буфер памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и вернул буфер запрошенные памяти.
    
## <a name="remarks"></a>Замечания

Во время **MAPIAllocateBuffer** вызовите обработки, вызывающий реализации Получает блок памяти от операционной системы. Буфер памяти, выделенный на адрес четных байтов. На платформах, где доступа "длинное целое" — это более эффективный операционная система выделяет буфера на адрес, размер которых в байтах делится на четыре. 
  
Вызов выпусков функция [MAPIFreeBuffer](mapifreebuffer.md) буфер памяти, выделенный с **MAPIAllocateBuffer**путем вызова функции [MAPIAllocateMore](mapiallocatemore.md) и буферов по ссылке, когда объем памяти больше не требуется. 
  
## <a name="see-also"></a>См. также



[MAPIReallocateBuffer](mapireallocatebuffer.md)

