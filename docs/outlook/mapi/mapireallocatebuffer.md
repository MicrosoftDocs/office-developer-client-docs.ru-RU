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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435287"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Перераспределение буфера памяти. Он используется с функцией [MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |omapix.h  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parameters

 _lpv_
  
> Указатель на память, которая должна быть перенадвижена.
    
 _ulSize_
  
> Размер выделенного буфера в bytes.
    
 _lppv_
  
> Указатель на возвращенный выделенный буфер.
    
## <a name="remarks"></a>Примечания

 **MAPIReallocateBuffer** выделяет новый блок памяти запрашиваемого размера и копирует содержимое буфера, который передается в этот новый блок памяти. Если пройденный блок памяти содержит внутренние указатели, указатели не изменяются, чтобы соответствовать новому расположению. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)

