---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341729"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует строку в буфер.
  
> [!CAUTION]
> Не следует использовать. Вместо этого [рассмотрите возможность использования StringCchCopy.](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Параметры

lpString1
  
> [out] Буфер для получения содержимого строки, на которое указывает параметр lpString2.
    
lpString2
  
> [in] Строка, орвав нуль, которая должна быть скопирована.
    
## <a name="return-value"></a>Возвращаемое значение

Если функция успешно работает, возвращаемая величина является указателем на буфер.
  
Если функция завершается сбой, возвращается значение NULL, а lpString1 может не быть завершена на null.
  
## <a name="remarks"></a>Примечания

Эта функция обтекает **функцию lstrcpy.** Дополнительные сведения см. [в lstrcpy.](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)
  
## <a name="see-also"></a>См. также



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

