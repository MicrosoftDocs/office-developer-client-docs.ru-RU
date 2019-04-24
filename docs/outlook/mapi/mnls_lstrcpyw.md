---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Дата последнего изменения: 18 июня 2012 г.'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341729"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует строку в буфер.
  
> [!CAUTION]
> Не следует использовать. Вместо этого рекомендуется использовать [стрингкчкопи](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Параметры

lpString1
  
> вышли Буфер для получения содержимого строки, на которую указывает параметр lpString2.
    
lpString2
  
> возврата Копируемая строка, заканчивающаяся нулем.
    
## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на буфер.
  
Если функция завершается с ошибкой, возвращается значение NULL, а lpString1 не может оканчиваться нулем.
  
## <a name="remarks"></a>Комментарии

Эта функция заключает в оболочку функцию **лстркпи** . Дополнительные сведения см. в разделе [лстркпи](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[лстркпи](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

