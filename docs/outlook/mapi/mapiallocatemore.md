---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809874"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Относится к**: Outlook 
  
Выделяет буфер памяти, который связан с другой буфера, выделенного ранее с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Параметры

 _cbSize_
  
> [in] Размер, в байтах, выделения нового буфера. 
    
 _lpObject_
  
> [in] Указатель на существующий MAPI буфер, выделенный с помощью **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [out] Указатель на возвращенное вновь выделенный буфер.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и вернул указатель на запрошенный память.
    
## <a name="remarks"></a>Замечания

Во время **MAPIAllocateMore** вызовите обработки, вызывающий реализации Получает блок памяти от операционной системы. Буфер памяти, выделенный на адрес четных байтов. На платформах, где доступа "длинное целое" — это более эффективный операционная система выделяет буфера на адрес, размер которых в байтах делится на четыре. 
  
— Это единственный способ освободить буфер, выделенный с **MAPIAllocateMore** указателя буфера, указанный в параметре _lpObject_ функции [MAPIFreeBuffer](mapifreebuffer.md) . Связь между буферов памяти, выделенный с [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore** позволяет **MAPIFreeBuffer** для освобождения обоих буферов с помощью одного вызова. 
  

