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
- Функция темпактивереф [Excel 2007], функция TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301570"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** , содержащую внешнюю ссылку на прямоугольный блок ячеек на активном листе. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Параметры

 _Рвфирст_
  
Начальная строка ссылки.
  
 _Рвласт_
  
Конечная строка ссылки.
  
Аргументы строки отсчитываются от нуля, поэтому строка 1 передается как 0. В Microsoft Office Excel 2003 и более ранних версиях, начиная с Excel 2007 Запуск книги в режиме совместимости, максимальное значение равно 65 535 = 2 ^ 16-1 и является максимальным значением, которое может принимать слово Integer. Начиная с Excel 2007 Запуск книги, максимальное значение равно 1 048 575 = 2 ^ 20-1. RW определяется как 32-разрядное целое число со знаком в XLCALL. Высоты.
  
 _Колфирст_
  
Начальный номер столбца ссылки.
  
 _Колласт_
  
Номер конечного столбца ссылки.
  
Аргументы столбца отсчитываются от нуля, поэтому столбец A передается как 0. В Excel 2003 и более ранних версиях, начиная с Excel 2007 выполнение книги в режиме совместимости, максимальное значение равно 255 = 2 ^ 8-1 и является максимальным значением, которое может быть получено с помощью БАЙТового целого числа. Начиная с Excel 2007 Запуск книги, максимальное значение равно 16 383 = 2 ^ 14-1. COL определен как 32-разрядное целое число со знаком в XLCALL. Высоты.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает внешнюю ссылку **кслтипереф** на прямоугольный блок передаваемых ячеек. 
  
## <a name="example"></a>Пример

В этом примере функция **TempActiveRef12** используется для выбора ячеек A105: C110. 
  
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

