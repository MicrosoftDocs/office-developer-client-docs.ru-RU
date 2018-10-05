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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386350"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнение двух строк Юникод.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Параметры

 _lpString1_
  
> [in] Указатель для первой строки Юникод для сравнения.
    
 _lpString2_
  
> [in] Указатель на втором строку в кодировке Юникод для сравнения.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает значения, описанного при вызове эквивалентный **MNLS_CompareStringW** за исключением CSTR_EQUAL. 
  
## <a name="remarks"></a>Замечания

 _MNLS_lstrcmpW_ выполняет сравнение путем вызова [MNLS_CompareStringW](mnls_comparestringw.md) с локальным GetUserDefaultLCID 0 для флаги и значение -1 для cch1 и cch2. 
  
## <a name="see-also"></a>См. также



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

