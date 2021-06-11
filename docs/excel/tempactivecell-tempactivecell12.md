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
- функция tempactivecell12 [Excel 2007], функция TempActiveCell [Excel 2007]
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
  
Функции библиотеки Framework, создав временную **XLOPER XLOPER12,** содержащую внешнюю ссылку на ячейку /   на активном листе. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parameters

 _строка_
  
Строка, на который следует ссылаться. Аргументы строки основаны на нулевой основе, поэтому строка 1 передается в качестве 0. В Microsoft Office Excel 2003 г. и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 65 535 = 2^16 — 1 и является максимальным значением, которое может приниматься в integer WORD. Начиная с Excel 2007 г. при запуске книги максимальное значение — 1 048 575 = 2^20 — 1. RW определяется как 32-битный подписанный в XLCALL.H.
  
 _col_
  
Столбец, на который следует ссылаться. Это нулевое значение, поэтому столбец A передается в качестве 0. В Excel 2003 и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 255 = 2^8 — 1 и является максимальным значением, которое может приниматься в integer BYTE. Начиная с Excel 2007 года при запуске книги максимальное значение — 16 383 = 2^14 — 1. COL определяется как 32-битный подписанный в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **внешнюю ссылку xltypeRef** на переданную ячейку. 
  
## <a name="example"></a>Пример

В следующем примере **TempActiveCell12** отображает содержимое B94 на активном листе. 
  
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

