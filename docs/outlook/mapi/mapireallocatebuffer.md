---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809899"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Относится к**: Outlook 
  
Перешла к буфер памяти. Он используется с функцией [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |omapix.h  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Параметры

 _lpv_
  
> Указатель на память перераспределить.
    
 _ulSize_
  
> Размер в байтах, выделения буфера.
    
 _lppv_
  
> Указатель на возвращаемый выделенный буфер.
    
## <a name="remarks"></a>Замечания

 **MAPIReallocateBuffer** выделяет новый блок памяти запрошенный размер и копирует содержимое буфера, которое передается в этот новый блок памяти. Если блок памяти, который передается содержит внутренних указателей, указатели не изменяйте в соответствии с в новом месте. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)

