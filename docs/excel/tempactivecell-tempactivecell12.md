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
- функция tempactivecell12 [excel 2007], функция TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807318"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка на ячейку на активном листе. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Параметры

 _row_
  
Ссылаться на строку. Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1. RW определяется как 32-разрядное целое число со знаком в XLCALL. З.
  
 _столбец_
  
Ссылка на столбец. Это с отсчетом от нуля, поэтому этот столбец A передается как 0. В Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1. Столбец — это 32-разрядное целое число со знаком в XLCALL. З.
  
## <a name="return-value"></a>������������ ��������

Возвращает **xltypeRef** внешняя ссылка ячейки, переданные в. 
  
## <a name="example"></a>Пример

В следующем примере используется **TempActiveCell12** для отображения содержимого B94 на активном листе. 
  
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

