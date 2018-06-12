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
- функция tempactiveref [excel 2007], функция TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807321"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка прямоугольный блок ячеек на активном листе. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameters

 _rwFirst_
  
Начальный строка ссылки.
  
 _rwLast_
  
Конечная строка ссылки.
  
Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1. RW определяется как 32-разрядное целое число со знаком в XLCALL. З.
  
 _colFirst_
  
Начальный номер столбца ссылки.
  
 _colLast_
  
Последний номер столбца ссылки.
  
Столбец аргументы являются с отсчетом от нуля, поэтому этот столбец A передается как 0. В Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1. Столбец — это 32-разрядное целое число со знаком в XLCALL. З.
  
## <a name="return-value"></a>������������ ��������

Возвращает **xltypeRef** внешняя ссылка прямоугольный блок ячеек, переданные в. 
  
## <a name="example"></a>Пример

В этом примере функция **TempActiveRef12** используется для выбора A105:C110 ячеек. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

