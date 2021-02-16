---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- функция tempmissing [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435959"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную  /  **XLOPER XLOPER12** типа **xltypeMissing.**
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких параметров.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на **XLtypeMissing** **XLOPER** /  **XLOPER12.**
  
## <a name="example"></a>Пример

В этом примере **tempMissing12** используется для предоставления **xlcWorkspace** трех отсутствующих аргументов, за которыми следует **boolean** **FALSE** для подавления отображения полос прокрутки на рабочем экране. Первые три аргумента соответствуют другим незатроченным настройкам рабочей области. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

