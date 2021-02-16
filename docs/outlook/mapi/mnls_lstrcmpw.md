---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356842"
---
# <a name="mnls_lstrcmpw"></a>MNLS_lstrcmpW

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает две строки Юникода.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Параметры

 _lpString1_
  
> [in] Указатель на первую строку Юникода для сравнения.
    
 _lpString2_
  
> [in] Указатель на вторую строку Юникода для сравнения.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает значения, описанные для эквивалентного  вызова MNLS_CompareStringW за исключением CSTR_EQUAL. 
  
## <a name="remarks"></a>Примечания

 _MNLS_lstrcmpW_ сравнение выполняется путем вызова [](mnls_comparestringw.md) MNLS_CompareStringW с региональными данными для GetUserDefaultLCID, 0 для флагов и -1 для cch1 и cch2. 
  
## <a name="see-also"></a>См. также



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

