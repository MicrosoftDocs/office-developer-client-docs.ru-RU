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
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588890"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет, длина указанной строки Юникод, за исключением конечный символ null.
  
> [!TIP]
> Рекомендуется использовать [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Символом null строка Юникод для проверки.
    
## <a name="return-value"></a>������������ ��������

Функция возвращает целое число в длину строки. Это число знаков в строке, за исключением конечный символ null. Если _lpsz_ имеет значение NULL, функция возвращает ноль. 
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **lstrlen** . Для получения дополнительных сведений см [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

