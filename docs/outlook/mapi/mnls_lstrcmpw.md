---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Последнее изменение: 18 июня 2012 г.'
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810021"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Применимо к**: Outlook 
  
Сравнение двух строк Юникод.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameters

 _lpString1_
  
> [in] Указатель для первой строки Юникод для сравнения.
    
 _lpString2_
  
> [in] Указатель на втором строку в кодировке Юникод для сравнения.
    
## <a name="return-value"></a>������������ ��������

Возвращает значения, описанного при вызове эквивалентный **MNLS_CompareStringW** за исключением CSTR_EQUAL. 
  
## <a name="remarks"></a>Замечания

 _MNLS_lstrcmpW_ выполняет сравнение путем вызова [MNLS_CompareStringW](mnls_comparestringw.md) с локальным GetUserDefaultLCID 0 для флаги и значение -1 для cch1 и cch2. 
  
## <a name="see-also"></a>См. также



[GetUserDefaultLCID](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

