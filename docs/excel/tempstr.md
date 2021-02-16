---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Функция tempstr [excel 2007]
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
  
Неподдержаемая функция библиотеки Framework, которая создает временную **XLOPER,** содержащую строку byte **xltypeStr.** В качестве входных данных она принимает строку источника, о завершаемую нулом. Он пытается переписать первый символ предоставленной строки с последующей длиной строки. Это не всегда безопасно: Microsoft Excel может аварийно сбой, если передать строку только для чтения. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на нулевую строку источника. **TempStr** усечены строки длиной более 255байт. 
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку xltypeStr,** содержащую указатель на переданный буфер строк. 
  
## <a name="remarks"></a>Примечания

Этот способ создания временных строк теперь не поддерживается в пользу работы [TempStrConst и TempStr12.](tempstrconst-tempstr12.md) Эти функции выделяют новый буфер памяти и копируют переданную в него строку. Входные строки **для TempStrConst** и **TempStr12** не изменяются, поэтому объявляются **как const**. В отличие от этого, входная строка **tempStr** изменяется и поэтому не может быть **объявлена как const**. Первый символ входной строки рассматривается как пробел для символа длины и перезаписывается этой функцией.
  
## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

