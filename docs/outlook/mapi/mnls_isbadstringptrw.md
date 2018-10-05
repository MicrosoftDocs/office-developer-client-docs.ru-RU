---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Последнее изменение: 20 февраля 2012 г.'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398740"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет, что указатель на строку широкий действительна.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку расширенных символов.
    
 _ucchMax_
  
> [in] Максимальная длина строки в символы, включая конца строки.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение true, если строка неисправно.
  
## <a name="remarks"></a>Замечания

Эта функция является [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Для получения дополнительных сведений см [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

