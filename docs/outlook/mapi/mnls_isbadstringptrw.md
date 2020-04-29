---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Дата последнего изменения: 20 февраля 2012 г.'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356856"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет, является ли указатель на широкую строку допустимым.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Параметры

 _лпсз_
  
> возврата Указатель на строку расширенных символов.
    
 _укчмакс_
  
> возврата Максимальная длина строки в символах, включая признак конца.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, равное true, если строка является недопустимой.
  
## <a name="remarks"></a>Примечания

Эта функция служит оболочкой для [исбадстрингптр](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Дополнительные сведения см. в разделе [исбадстрингптр](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

