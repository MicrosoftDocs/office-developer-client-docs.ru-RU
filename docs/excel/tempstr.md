---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Функция tempstr [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418045"
---
# <a name="tempstr"></a>TempStr

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string. В качестве ввода требуется строка источника с ненулевом прекращением. Он пытается переписать первый символ поставленной строки с последующей длиной строки. Это не всегда безопасно: Microsoft Excel может произойти сбой при сдав строке только для чтения. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на строку источника с null-terminated. **TempStr** усечены строки, которые длиннее 255 bytes. 
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку xltypeStr,** содержащую указатель в переданный буфер строки. 
  
## <a name="remarks"></a>Примечания

Этот способ создания временных строк теперь отстает в пользу того, как работают [TempStrConst и TempStr12.](tempstrconst-tempstr12.md) Эти функции выделяют новый буфер памяти и копируют в него переданную строку. Строки ввода **для TempStrConst** и **TempStr12** не изменяются и поэтому объявляются **как const**. В отличие от этого, строка ввода **в TempStr** изменяется и поэтому не может быть объявлена **как const**. Первый символ строки ввода рассматривается как пространство для символа длины и перезаписывается этой функцией.
  
## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

