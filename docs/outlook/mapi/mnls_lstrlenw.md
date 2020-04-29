---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338467"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет длину указанной строки Юникода, за исключением завершающего знака null.
  
> [!TIP]
> Вместо этого рекомендуется использовать [стрингкчленгс](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Параметры

 _лпсз_
  
> возврата Строка Юникода с завершающим нулем для проверки.
    
## <a name="return-value"></a>Возвращаемое значение

Функция возвращает целое число с длиной строки. Это количество символов в строке, за исключением завершающего знака null. Если _лпсз_ имеет значение null, функция возвращает ноль. 
  
## <a name="remarks"></a>Примечания

Эта функция заключает в оболочку функцию **лстрлен** . Дополнительные сведения см. в разделе [лстрлен](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[лстрлен](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[стрингкчленгс](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

