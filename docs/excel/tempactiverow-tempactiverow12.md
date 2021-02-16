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
- функция tempactiverow [excel 2007],Функция TempActiveRow12 [Excel 2007]
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
  
Функции библиотеки framework, которые создают временную **XLOPER12** /  **XLOPER12,** содержащую внешнюю ссылку на всю строку на активном листе. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Параметры

 _row_
  
Строка, на которая будет ссылаться. Аргументы строки основаны на нуле, поэтому строка 1 передается в качестве 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, в котором книга работает в режиме совместимости, максимальное значение составляет 65 535 = 2^16-1 и является максимальным значением, которое может приниматься в качестве значения, которое может приниматься в word integer. Начиная с Excel 2007, где запущена книга, максимальное значение составляет 1 048 575 = 2^20 - 1. RW определяется как 32-битное подписанное в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **внешнюю ссылку xltypeRef** на переданные ячейки строк. 
  
## <a name="example"></a>Пример

В этом примере функция **TempActiveRow12 используется** для выбора строки 113. 
  
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

