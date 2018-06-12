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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810051"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Применимо к**: Outlook 
  
Определяет, длина указанной строки Юникод, за исключением конечный символ null.
  
> [!TIP]
> Рекомендуется использовать [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Символом null строка Юникод для проверки.
    
## <a name="return-value"></a>������������ ��������

Функция возвращает целое число в длину строки. Это число знаков в строке, за исключением конечный символ null. Если _lpsz_ имеет значение NULL, функция возвращает ноль. 
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **lstrlen** . Для получения дополнительных сведений см [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

