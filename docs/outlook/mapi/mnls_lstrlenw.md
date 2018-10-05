---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392090"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет, длина указанной строки Юникод, за исключением конечный символ null.
  
> [!TIP]
> Рекомендуется использовать [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Символом null строка Юникод для проверки.
    
## <a name="return-value"></a>Возвращаемое значение

Функция возвращает целое число в длину строки. Это число знаков в строке, за исключением конечный символ null. Если _lpsz_ имеет значение NULL, функция возвращает ноль. 
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **lstrlen** . Для получения дополнительных сведений см [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

