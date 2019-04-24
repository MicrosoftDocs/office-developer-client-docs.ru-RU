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
- Функция темпактиверов [Excel 2007], функция TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310418"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, которые создают временную структуру **XLOPER**/ **** , содержащую внешнюю ссылку на всю строку на активном листе. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Параметры

 _Строка_
  
Строка, на которую необходимо сослаться. Аргументы строки отсчитываются от нуля, поэтому строка 1 передается как 0. В Microsoft Office Excel 2003 и более ранних версиях, начиная с Excel 2007 Запуск книги в режиме совместимости, максимальное значение равно 65 535 = 2 ^ 16-1 и является максимальным значением, которое может принимать слово Integer. Начиная с Excel 2007 Запуск книги, максимальное значение равно 1 048 575 = 2 ^ 20-1. RW определяется как 32-разрядное целое число со знаком в XLCALL. Высоты.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает внешнюю ссылку **кслтипереф** на переданные ячейки строк. 
  
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



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

