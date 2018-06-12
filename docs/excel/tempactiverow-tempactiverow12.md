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
- функция tempactiverow [excel 2007], функция TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807319"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка всю строку на активном листе. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parameters

 _Строка_
  
Ссылаться на строку. Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1. RW определяется как 32-разрядное целое число со знаком в XLCALL. З.
  
## <a name="return-value"></a>������������ ��������

Возвращает **xltypeRef** внешняя ссылка переданную ячейки строки. 
  
## <a name="example"></a>Пример

В этом примере функция **TempActiveRow12** используется для выбора строки 113. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

