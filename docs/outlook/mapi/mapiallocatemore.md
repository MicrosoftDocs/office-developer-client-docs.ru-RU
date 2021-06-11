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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выделяет буфер памяти, связанный с другим буфером, ранее выделенным с функцией [MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
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

## <a name="parameters"></a>Parameters

 _cbSize_
  
> [in] Размер, в bytes, нового буфера, который будет выделен. 
    
 _lpObject_
  
> [in] Указатель на существующий буфер MAPI, выделенный с помощью **MAPIAllocateBuffer.**
    
 _lppBuffer_
  
> [вышел] Указатель на возвращенный, недавно выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и вернул указатель в запрашиваемую память.
    
## <a name="remarks"></a>Примечания

Во **время обработки вызовов MAPIAllocateMore** реализация вызовов получает блок памяти из операционной системы. Буфер памяти выделяется на 10-номерный byte-адрес. На платформах, где более эффективным является длительный доступ к сети, операционная система выделяет буфер на адрес, размер которого в bytes — несколько из четырех. 
  
Единственный способ освободить буфер, выделенный **с помощью MAPIAllocateMore,** — передать указатель буфера, указанный в параметре _lpObject,_ функции [MAPIFreeBuffer.](mapifreebuffer.md) Связь между буферами памяти, выделенными [MAPIAllocateBuffer](mapiallocatebuffer.md) и **MAPIAllocateMore,** позволяет **MAPIFreeBuffer** освободить оба буфера одним вызовом. 
  

