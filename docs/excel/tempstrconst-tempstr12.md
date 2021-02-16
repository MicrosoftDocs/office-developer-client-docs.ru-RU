---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- Функция tempstr12 [excel 2007],TempStrConst function [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407153"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную **строку XLOPER/XLOPER12,** которая содержит **строку xltypeStr,** принимая в качестве входных данных строку источника с опечаткой null. Функция выделяет новый буфер памяти и копирует переданную строку в него. Входная строка не изменяется, поэтому объявляется как **const.**
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на нулевую строку источника. В случае **XLOPER** TempStrConst усекает строки длиной более 255байт. В случае с **XLOPER12** TempStr12Const усекает строки длиной более 32 767 символов Юникода.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку xltypeStr,** содержащую копию переданного буфера строк. 
  
## <a name="remarks"></a>Примечания

Обратите внимание, что функция **XLOPER** string Framework **TempStr** ведет себя по-разному и пытается переписать первый символ предоставленной строки с последующей длиной строки. Это не всегда безопасно: Microsoft Excel может аварийно сбой, если передать строку только для чтения. Этот способ создания временных строк теперь не поддерживается в пользу работы **TempStrConst** и **TempStr12.** Поэтому первый символ входной строки рассматривается как начало строки, то есть не как символ длины или пробел для символа длины. Не следует передавать строки, закодированные в начале символа длины, так как последствия могут быть непредсказуемыми. 
  
## <a name="example"></a>Пример

В этом примере функция **TempStr12** используется для создания строки для окна сообщения. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

