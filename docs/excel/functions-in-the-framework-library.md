---
title: Функции в библиотеке Framework
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- функции библиотеки Framework [excel 2007], функции [Excel 2007] библиотеки Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807270"
---
# <a name="functions-in-the-framework-library"></a>Функции в библиотеке Framework

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы обеспечить создание XLL-модулей для упрощения был создан библиотеки Framework. Включает простой функции для управления **XLOPER**/ **XLOPER12** памяти, создание временной **XLOPER**/ **XLOPER12**, надежно вызов функции обратного вызова Microsoft Excel (**Excel4**, **Excel4v** ** Excel12 **, ** Excel12v **) и отладки строк на подключенного терминала печати.
  
Функции, включенные в этой библиотеке облегчить фрагмент кода, выглядит следующим образом.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Упрощенная код выглядит как следующий пример.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

В библиотеке Framework включены следующие функции:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Функции, используемые с XLOPERs**|**Функции, используемые с XLOPER12s**|
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
   
Использование этих функций сокращает время, необходимое для записи DLL или XLL. Начало разработки в моем приложении УНИВЕРСАЛЬНЫЙ также сокращает время разработки. Использование УНИВЕРСАЛЬНЫХ. C как шаблон для настройки framework XLL-модуль и затем замените существующий код на свой.
  
Временные **XLOPER**/ **XLOPER12** функции создать **XLOPER**/ **XLOPER12** значения с помощью памяти из локального кучи управляется библиотеки Framework. **XLOPER**/ **XLOPER12** значения остаются действительными до вызова функции **FreeAllTempMemory** или любой из функции **Excel** или **Excel12f** . (Функции **Excel** и **Excel12f** освободить память все временные перед возвращением.) 
  
Чтобы использовать функции библиотеки Framework, необходимо включить FRAMEWRK. H в коде C и добавьте FRAMEWRK. C или FRMWRK32. Файлы LIB в проект кода.
  
## <a name="see-also"></a>См. также

- [���������� �� ������� Excel 2013 XLL SDK API](excel-xll-sdk-api-function-reference.md)

