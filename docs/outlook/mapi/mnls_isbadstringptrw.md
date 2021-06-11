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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356856"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет, допустима ли указатель на широкую строку.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Указатель на широкую строку символов.
    
 _ucchMax_
  
> [in] Максимальная длина строки в символах, включая терминатор.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает boolean, который является верным, если строка плоха.
  
## <a name="remarks"></a>Примечания

Эта функция [обертывания IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Дополнительные сведения см. [в полосе IsBadStringPtr.](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)
  

