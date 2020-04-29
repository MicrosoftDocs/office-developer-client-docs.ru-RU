---
title: иенумфбблоккклоне
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413404"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Параметры

_ппклоне_
  
> вышли Указатель на копию интерфейса [иенумфбблокк](ienumfbblock.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_OUTOFMEMORY  <br/> |Недостаточно памяти для создания копии.  <br/> |
   
## <a name="see-also"></a>См. также

- [Константы (API сведений о доступности)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

