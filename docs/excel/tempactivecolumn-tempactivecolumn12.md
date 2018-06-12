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
- функция tempactivecolumn12 [excel 2007], функция TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807324"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка на целый столбец на активном листе. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameters

 _столбец_ (**БАЙТ**)
  
Ссылка на столбец. Это с отсчетом от нуля, поэтому этот столбец A передается как 0. В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число. Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1. Столбец — это 32-разрядное целое число со знаком в XLCALL. З.
  
## <a name="return-value"></a>������������ ��������

Возвращает **xltypeRef** внешняя ссылка на столбец, переданные в. 
  
## <a name="example"></a>Пример

В следующем примере используется **TempActiveColumn12** для выбора целый столбец б. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

