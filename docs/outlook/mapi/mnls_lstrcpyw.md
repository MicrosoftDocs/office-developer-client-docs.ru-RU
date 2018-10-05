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
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382710"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует строки в буфер.
  
> [!CAUTION]
> Не используйте. Рекомендуется использовать [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
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
    
## <a name="return-value"></a>Возвращаемое значение

Если функция успешно выполнена, возвращается указатель на буфер.
  
В случае сбоя функция возвращает значение NULL, и lpString1 могут быть символом null.
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **lstrcpy** . Для получения дополнительных сведений см [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

