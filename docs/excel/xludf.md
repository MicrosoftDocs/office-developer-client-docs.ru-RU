---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- Функция xludf [excel 2007]
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
  
Вызов пользовательской функции (UDF). Эта функция позволяет DLL вызывать пользовательские функции Visual Basic для приложений VBA, функции языка макроса XLM и зарегистрированные функции, содержащиеся в других надстройки.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Параметры

_pxFnRef_ (**xltypeRef,** **xltypeSRef,** **xltypeStr** или **xltypeNum)**
  
Ссылка на функцию, которая вы хотите вызвать. Это может быть ссылка на ячейку листа макроса, зарегистрированное имя функции в качестве строки или зарегистрированный ИД функции. Для функций надстройки XLL, зарегистрированных с помощью **xlfRegister** или **REGISTER** с предоставленным аргументом  _pxFunctionText,_ можно получить ИД с помощью **xlfEvaluate** для искомого имени. 
  
_pxArg1, ..._
  
Ноль или больше аргументов для пользовательской функции. При вызове этой функции в версиях, более ранних, чем Excel 2007, максимальное число дополнительных аргументов, которые можно передать, составляет 29, что составляет 30, включая  _pxFnRef_. Начиная с Excel 2007 это ограничение повышается до 254, что составляет 255, включая _pxFnRef._
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает любое значение, возвращенное пользовательской функцией.
  
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

