---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- Функция кслстакк [Excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310159"
---
# <a name="xlstack"></a>xlStack

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Проверяет объем места, оставшееся на стеке.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает количество байтов (**кслтипеинт**), оставшееся в стеке.
  
## <a name="remarks"></a>Замечания

Объем доступного места в стеке последних версий превышает 16-разрядное целое число со знаком для **XLOPER**. Это означает, что **кслстакк** может возвращать значение между – 32767 и 32768 при вызове с помощью **XLOPER**s и **Excel4** или **Excel4v**. Чтобы получить правильное значение в этом случае, необходимо присвоить возвращенное значение неподписанному сокращенному типу.
  
Начиная с Excel 2007, эту функцию следует вызывать с помощью **XLOPER12**s и **Excel12** или **Excel12v**, в этом случае возвращаемое значение — это объем доступного места в стеке или 64 КБ, в зависимости от того, какое значение меньше.
  
В стеке Excel есть ограниченный объем пространства, поэтому не следует перерасходовать это пространство. Никогда не размещайте очень большие структуры данных в стеке и сделайте как можно больше локальных переменных. Избегайте рекурсивных вызовов функций, так как это быстро заполнит стек.
  
Если вы считаете, что стек занят, вызовите эту функцию часто, чтобы узнать, сколько осталось места в стеке.
  
## <a name="example"></a>Пример

В первом примере отображается оповещение, содержащее объем стека слева и содержащийся в `\SAMPLES\EXAMPLE\EXAMPLE.C`. Второй пример выполняет ту же операцию, работая с **XLOPER**s и не входит в пример кода SDK.
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>См. также

- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

