---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- функция xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807367"
---
# <a name="xlstack"></a>xlStack

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Проверка свободного места в стеке.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает число байт (**xltypeInt**), оставшихся в стеке.
  
## <a name="remarks"></a>Замечания

Объем доступных стек последних версий выходящее за 16-разрядного целого числа со знаком из **XLOPER**. Это означает, что этот **xlStack** может возвращать значение между-32767 и 32768 при вызове с помощью **XLOPER**s и **Excel4** или **Excel4v**. Чтобы получить правильное значение в этом случае, необходимо привести возвращаемое значение для неподписанных short.
  
Начиная с версии Excel 2007, необходимо вызвать эту функцию, с помощью **XLOPER12**s и **Excel12** или **Excel12v**, является случай возвращаемое значение, свободное место стека или 64 КБ, какое из значений является меньшим.
  
Excel имеет ограниченный объем пространства в стеке, после чего следует позаботиться не к переполнению этого пространства. Никогда не создавать очень больших структур данных в стеке и сделать статические столько локальных переменных по мере возможности. Избегайте функции рекурсивный вызов, так как, который будет быстро заполняется стека.
  
Если предполагается, что переполнение стека, эта функция часто, чтобы увидеть, сколько места стека.
  
## <a name="example"></a>Пример

В первом примере отображаются сообщения с оповещением, содержащий объем места для стека и содержащихся в `\SAMPLES\EXAMPLE\EXAMPLE.C`. Во втором примере выполняются те же действия, работа с **XLOPER**s и не находится в примере кода пакета SDK.
  
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

- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

