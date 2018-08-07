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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810034"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Относится к**: Outlook 
  
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

