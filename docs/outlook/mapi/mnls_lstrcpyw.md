---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Последнее изменение: 18 июня 2012 г.'
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575464"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Копирует строки в буфер.
  
> [!CAUTION]
> Не используйте. Рекомендуется использовать [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Параметры

lpString1
  
> [out] Буфер для получения содержимого строки, на который указывает параметр lpString2.
    
lpString2
  
> [in] Строка для копирования символом null.
    
## <a name="return-value"></a>������������ ��������

Если функция успешно выполнена, возвращается указатель на буфер.
  
В случае сбоя функция возвращает значение NULL, и lpString1 могут быть символом null.
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **lstrcpy** . Для получения дополнительных сведений см [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

