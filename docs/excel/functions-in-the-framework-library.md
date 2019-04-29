---
title: Функции в библиотеке платформы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- функции библиотеки Framework [Excel 2007], функции [Excel 2007], Библиотека Framework
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
# <a name="functions-in-the-framework-library"></a>Функции в библиотеке платформы

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Библиотека Framework была создана для упрощения создания XLL. Он включает простые функции для управления памятью **XLOPER**/ **XLOPER12** , создавая временную группу **XLOPER**/ **** и надежно вызывая функции обратного вызова Microsoft Excel (**Excel4**, **Excel4v** * * Excel12 * *, * * Excel12v * *) и печать строк отладки на присоединенном терминале.
  
Функции, включенные в эту библиотеку, помогают упростить фрагмент кода, который выглядит примерно так:
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Упрощенный код выглядит так, как показано в следующем примере.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

В библиотеку Framework включены следующие функции:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**Жеттемпмемори** <br/> |
|**Фриаллтемпмемори** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Функции, используемые с XLOPER**|**Функции, используемые с XLOPER12**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[Темпнум](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[Темпстрконст](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[Темпбул](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[Темпинт](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[Темперр](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[Темпактивереф](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[Темпактивецелл](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[Темпактиверов](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[Темпактивеколумн](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[Темпмиссинг](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
Использование этих функций сокращает количество времени, необходимого для записи DLL или XLL. Запуск разработки из примера УНИВЕРСАЛЬНого приложения также сокращает время разработки. Используйте GENERIC. C в качестве шаблона для помощи в настройке платформы XLL, а затем замените существующий код на свой собственный.
  
Функции Temporary **XLOPER**/ **XLOPER12** создают значения **XLOPER**/ **XLOPER12** , используя память из локальной кучи, управляемой библиотекой Framework. Значения параметра **XLOPER**/ **XLOPER12** действуют до тех пор, пока не будет вызвана функция **фриаллтемпмемори** или обе функции **Excel** или **Excel12f** . (В **Excel** и **Excel12f** функции освобождают всю временную память перед возвратом.) 
  
Чтобы использовать функции библиотеки Framework, необходимо включить FRAMEWRK. H в коде C и добавление FRAMEWRK. C или FRMWRK32. LIB файлы в проект кода.
  
## <a name="see-also"></a>См. также

- [Справочник по функциям API SDK XLL для Excel](excel-xll-sdk-api-function-reference.md)

