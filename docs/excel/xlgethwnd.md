---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- Функция кслжесвнд [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310068"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает дескриптор окна верхнего уровня в окне Microsoft Excel.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Параметры

У этой функции нет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Содержит дескриптор окна (**кслтипеинт**) в поле **Val. w** . 
  
## <a name="remarks"></a>Замечания

Эта функция полезна для написания кода Windows API.
  
При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращенная целочисленная переменная XLOPER имеет знак 16-bit short int. Это может быть только в том случае, если он содержит младшие 16 разрядов для дескриптора Windows 32-bit. Чтобы найти большую часть, код должен выполнить итерацию всех открытых окон, чтобы найти соответствующее значение с нижней частью. Начиная с версии Excel 2007, целочисленная переменная **XLOPER12** — это подписанное 32-разрядное целое число, поэтому он содержит весь дескриптор, устраняя необходимость в итерации всех открытых окон. 
  
### <a name="example"></a>Пример

Обратитесь к коду [функции фшовдиалог](fshowdialog.md) в `SAMPLES\GENERIC\GENERIC.C`файле.
  
## <a name="see-also"></a>См. также

- [xlGetInst](xlgetinst.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

