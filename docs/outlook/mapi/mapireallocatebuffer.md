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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перераспределяет буфер памяти. Он используется с функцией [мапиаллокатебуффер](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |омапикс. h  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Параметры

 _лпв_
  
> Указатель на память, которую необходимо перераспределить.
    
 _улсизе_
  
> Размер выделяемого буфера (в байтах).
    
 _лппв_
  
> Указатель на возвращенный выделенный буфер.
    
## <a name="remarks"></a>Примечания

 **Мапиреаллокатебуффер** выделяет новый блок памяти запрошенного размера и копирует содержимое буфера, переданного в новый блок памяти. Если блок памяти, который передается, содержит внутренние указатели, указатели не меняются для согласования с новым расположением. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)

