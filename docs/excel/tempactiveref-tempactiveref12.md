---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- функция tempactiveref [Excel 2007], функция TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415546"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную **XLOPER XLOPER12,** содержащую внешнюю ссылку на прямоугольный блок ячеек на /   активном листе. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameters

 _rwFirst_
  
Начальная строка ссылки.
  
 _rwLast_
  
Конечная строка ссылки.
  
Аргументы строки основаны на нулевой основе, поэтому строка 1 передается в качестве 0. В Microsoft Office Excel 2003 г. и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 65 535 = 2^16 — 1 и является максимальным значением, которое может приниматься в integer WORD. Начиная с Excel 2007 г. при запуске книги максимальное значение — 1 048 575 = 2^20 — 1. RW определяется как 32-битный подписанный в XLCALL.H.
  
 _colFirst_
  
Начальный номер столбца ссылки.
  
 _colLast_
  
Конечное число столбца ссылки.
  
Аргументы столбцов основаны на нулевой основе, поэтому столбец A передается в качестве 0. В Excel 2003 и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 255 = 2^8 — 1 и является максимальным значением, которое может приниматься в integer BYTE. Начиная с Excel 2007 года при запуске книги максимальное значение — 16 383 = 2^14 — 1. COL определяется как 32-битный подписанный в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает внешнюю **ссылку xltypeRef** на прямоугольный блок переданных клеток. 
  
## <a name="example"></a>Пример

В этом примере используется **функция TempActiveRef12** для выбора ячеек A105:C110. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

