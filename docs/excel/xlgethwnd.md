---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- Функция xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425458"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает окне окне верхнего уровня Microsoft Excel.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Параметры

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Содержит окне **(xltypeInt)** в **поле val.w.** 
  
## <a name="remarks"></a>Примечания

Эта функция полезна для написания кода API Windows.
  
При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER является подписанной 16-битной короткой переменной. Это может содержать только 16-битные 32-битные 32-битные точки Windows. Чтобы найти высокую часть, код должен проходить по всем открытым окнам в поисках совпадения с низкой частью. Начиная с Excel 2007, целомерная переменная **XLOPER12** — это 32-битное целое значение, которое содержит весь лад, удаляя необходимость в итерации всех открытых окон. 
  
### <a name="example"></a>Пример

См. код функции [fShowDialog](fshowdialog.md) в  `SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>См. также

- [xlGetInst](xlgetinst.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

