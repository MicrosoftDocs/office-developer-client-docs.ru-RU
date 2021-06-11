---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- функция tempactiverow [Excel 2007], функция TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413110"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, создав временную **XLOPER XLOPER12,** содержащую внешнюю ссылку на всю строку /   на активном листе. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parameters

 _строка_
  
Строка, на который следует ссылаться. Аргументы строки основаны на нулевой основе, поэтому строка 1 передается в качестве 0. В Microsoft Office Excel 2003 г. и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 65 535 = 2^16 — 1 и является максимальным значением, которое может приниматься в integer WORD. Начиная с Excel 2007 г. при запуске книги максимальное значение — 1 048 575 = 2^20 — 1. RW определяется как 32-битный подписанный в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает внешнюю **ссылку xltypeRef** на переданные ячейки строки. 
  
## <a name="example"></a>Пример

В этом примере используется **функция TempActiveRow12** для выбора строки 113. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

