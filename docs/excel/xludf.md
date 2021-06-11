---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- функция xludf [Excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430646"
---
# <a name="xludf"></a>xlUDF

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызывает функцию, определяемую пользователем (UDF). Эта функция позволяет DLL вызывать определенные пользователем функции Visual Basic для приложений(VBA), функции макроса XLM и зарегистрированные функции, содержащиеся в других надстройках.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameters

_pxFnRef_ **(xltypeRef,** **xltypeSRef,** **xltypeStr** или **xltypeNum)**
  
Ссылка на функцию, которая вам нужно вызвать. Это может быть ссылка ячейки макроса, зарегистрированное имя функции в качестве строки или регистрация ID функции. Для функций надстройки XLL, зарегистрированных с помощью **xlfRegister** или **REGISTER** с предоставленным аргументом  _pxFunctionText,_ ID можно получить с помощью **xlfEvaluate,** чтобы найти имя. 
  
_pxArg1, ..._
  
Ноль или более аргументов в пользу функции, определяемой пользователем. При вызове этой функции в версиях до Excel 2007 года максимальное количество дополнительных аргументов, которые можно передать, составляет 29, то есть 30, включая _pxFnRef_. Начиная с Excel 2007 г. это ограничение повышается до 254, что составляет 255, включая _pxFnRef_.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает любое значение возвращенной функции, определенной пользователем.
  
## <a name="example"></a>Пример

В следующем примере **выполняется TestMacro** на листе Macro1 в BOOK1.XLS. Убедитесь, что макрос находится на листе с именем Macro1. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

