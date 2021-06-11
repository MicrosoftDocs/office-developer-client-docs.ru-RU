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
- функция tempstr12 [Excel 2007], функция TempStrConst [Excel 2007]
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
  
Функция библиотеки Framework, которая создает временную **строку XLOPER/XLOPER12,** содержаную строку **xltypeStr,** принимая в качестве входной строки исходные строки с нетленным разрешением. Функция выделяет новый буфер памяти и копирует в нее переданную строку. Строка ввода не изменяется и поэтому объявляется **как const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на строку источника с null-terminated. В случае **XLOPER** s TempStrConst усечены строки длиной более 255 bytes. В случае **XLOPER12** s TempStr12Const усечены строки, которые длиннее 32 767 символов Юникод.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку xltypeStr,** содержащую копию переданного буфера строки. 
  
## <a name="remarks"></a>Примечания

Обратите внимание, что функция **XLOPER** string Framework **TempStr** ведет себя по-разному и пытается переписать первый символ поставленной строки с последующей длиной строки. Это не всегда безопасно: Microsoft Excel может произойти сбой при сдав строке только для чтения. Этот способ создания временных строк теперь отстает в пользу того, как работают **TempStrConst** и **TempStr12.** Поэтому первый символ строки ввода рассматривается как начало строки, то есть не как символ длины или как пространство для символа длины. Не следует передавать строки с закодированной в начале длиной, так как последствия могут быть непредсказуемыми. 
  
## <a name="example"></a>Пример

В этом примере используется **функция TempStr12** для создания строки для окна сообщений. 
  
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

