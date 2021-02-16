---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- функция tempactivecolumn12 [excel 2007],Функция TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417877"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки framework, которые создают временную **XLOPER12** /  **XLOPER12,** содержащую внешнюю ссылку на весь столбец активного листа. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Параметры

 _col_ (**BYTE)**
  
Столбец, на который следует ссылаться. Это значение основано на нуле, поэтому столбец A передается как 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, в котором книга работает в режиме совместимости, максимальное значение — 255 = 2^8 - 1 и это максимальное значение, которое может приниматься с помощью byTE-inte. Начиная с Excel 2007, где запущена книга, максимальное значение — 16 383 = 2^14 - 1. COL определяется как 32-битное подписанное в XLCALL.H.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **внешнюю ссылку xltypeRef** на переданный столбец. 
  
## <a name="example"></a>Пример

В следующем примере **tempActiveColumn12** используется для выбора всего столбца B. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

