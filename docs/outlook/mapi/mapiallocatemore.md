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
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435392"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выделяет буфер памяти, связанный с другим буфером, ранее выделенным [функцией MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Параметры

 _cbSize_
  
> [in] Размер нового буфера, который необходимо выделить, в вахтах. 
    
 _lpObject_
  
> [in] Указатель на существующий буфер MAPI, выделенный с помощью **MAPIAllocateBuffer.**
    
 _lppBuffer_
  
> [out] Указатель на возвращенный недавно выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвращен указатель на запрашиваемую память.
    
## <a name="remarks"></a>Примечания

Во время обработки вызовов **MAPIAllocateMore** реализация вызова получает блок памяти из операционной системы. Буфер памяти выделяется для even-numbered byte address. На платформах, где длинный полный доступ более эффективен, операционная система выделяет буфер на адресе, размер которого в кратном размере кратно четырем. 
  
Единственный способ освободить буфер, выделенный с помощью **MAPIAllocateMore,** — передать указатель буфера, указанный в параметре _lpObject,_ функции [MAPIFreeBuffer.](mapifreebuffer.md) Связь между буферами памяти, выделенными с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore,** позволяет **MAPIFreeBuffer** освободить оба буфера одним вызовом. 
  

