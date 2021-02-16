---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- Функция xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429981"
---
# <a name="xlstack"></a>xlStack

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Проверяет объем пространства, оставленного в стеке.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает количество оставшихся в стеке **(xltypeInt) bytes( xltypeInt).**
  
## <a name="remarks"></a>Примечания

Объем доступного пространства стека последних версий переполнен 16-битным подписанным integer **XLOPER.** Это означает, что **xlStack** может возвращать значение между -32767 и 32768 при использовании **XLOPER** s и **Excel4** или **Excel4v**. Чтобы получить правильное значение в этом случае, необходимо вернуть возвращенное значение к короткой без подписи.
  
Начиная с Excel 2007, эту функцию следует вызывать с помощью **XLOPER12** и **Excel12** или **Excel12v.** В этом случае возвращаемой величиной является объем доступного пространства стека или 64 КБ, в зависимости от того, чем меньше.
  
Excel имеет ограниченный объем пространства в стеке, и не следует перегнастить это пространство. Никогда не помещай в стек очень большие структуры данных и делайте как можно больше локальных переменных статическими. Избегайте рекурсивного вызова функций, так как это быстро заполнит стек.
  
Если вы подозреваете, что вы перезагруте стек, часто вызываем эту функцию, чтобы узнать, сколько места на стеке осталось.
  
## <a name="example"></a>Пример

В первом примере отображается оповещение, содержащее количество оставленного места в стеке и содержащееся в  `\SAMPLES\EXAMPLE\EXAMPLE.C` нем. Второй пример делает то же самое, работая с **XLOPER** и не содержится в примере кода SDK.
  
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

