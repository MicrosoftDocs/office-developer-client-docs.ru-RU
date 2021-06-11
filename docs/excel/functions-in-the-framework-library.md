---
title: Функции в библиотеке Framework
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- функции библиотеки framework [Excel 2007], функции [Excel 2007], библиотека Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417548"
---
# <a name="functions-in-the-framework-library"></a>Функции в библиотеке Framework

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Библиотека Framework была создана для упростить написание XLLs. Он включает простые функции для управления памятью **XLOPER XLOPER12,** создания временного XLOPER XLOPER12, надежного вызова функций вызова Microsoft Excel /    /  **(Excel4,** **Excel4v,**** Excel12 **, ** Excel12v **) и печати строк отладки на присоединенный терминал.
  
Функции, включенные в эту библиотеку, помогают упростить часть кода, которая выглядит следующим образом.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Упрощенный код выглядит как следующий пример.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

В библиотеку Framework включены следующие функции:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Функции, используемые в XLOPERs**|**Функции, используемые в XLOPER12**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
Использование этих функций сокращает время, необходимое для записи DLL или XLL. Запуск разработки из примера приложения GENERIC также сокращает время разработки. Используйте GENERIC. C в качестве шаблона, который поможет настроить рамки XLL, а затем заменить существующий код на собственный.
  
Временные **функции XLOPER** /  **XLOPER12** создают значения **XLOPER** /  **XLOPER12** с помощью памяти из локальной кучи, управляемой библиотекой Framework. Значения **XLOPER** XLOPER12 остаются действительными до тех пор, пока вы не назовете функцию /   **FreeAllTempMemory** или функции Excel **Excel12f.**  **(Функции Excel** **и Excel12f** освободит всю временную память перед возвращением.) 
  
Чтобы использовать функции библиотеки Framework, необходимо включить FRAMEWRK. H-файл в коде C и добавьте FRAMEWRK. C или FRMWRK32. LIB-файлы для проекта кода.
  
## <a name="see-also"></a>См. также

- [Справочник по функциям API SDK XLL для Excel](excel-xll-sdk-api-function-reference.md)

