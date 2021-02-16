---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- Функция tempactivecell12 [excel 2007],Функция TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413194"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки framework, которые создают временную **XLOPER12** /  **XLOPER12,** содержащую внешнюю ссылку на ячейку на активном листе. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Параметры

 _row_
  
Строка, на которая будет ссылаться. Аргументы строки основаны на нуле, поэтому строка 1 передается в качестве 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, в котором книга работает в режиме совместимости, максимальное значение составляет 65 535 = 2^16-1 и является максимальным значением, которое может приниматься в качестве значения, которое может приниматься в word integer. Начиная с Excel 2007, где запущена книга, максимальное значение составляет 1 048 575 = 2^20 - 1. RW определяется как 32-битное подписанное в XLCALL.H.
  
 _col_
  
Столбец, на который следует ссылаться. Это значение основано на нуле, поэтому столбец A передается как 0. В Excel 2003 и более ранних версиях, а начиная с Excel 2007, где книга запущена в режиме совместимости, максимальное значение — 255 = 2^8- 1 и максимальное значение, которое может приниматься с помощью byTE-inte. Начиная с Excel 2007, где запущена книга, максимальное значение — 16 383 = 2^14 - 1. COL определяется как 32-битное подписанное в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **внешнюю ссылку xltypeRef** на переданную ячейку. 
  
## <a name="example"></a>Пример

В следующем примере **tempActiveCell12** используется для отображения содержимого B94 на активном листе. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

