---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [Excel 2007]
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
  
Возвращает ручку окна верхнего Microsoft Excel окна.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Содержит ручку окна **(xltypeInt)** в **поле val.w.** 
  
## <a name="remarks"></a>Примечания

Эта функция полезна для написания кода Windows API.
  
При вызове этой функции с [помощью Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER является подписанной 16-битной короткой int. Это может содержать только 16-битную 32-Windows. Чтобы найти высокую часть, код должен итерировать через все открытые окна в поисках совпадения с низкой частью. Начиная с Excel 2007 г. целая переменная **XLOPER12** — это подписанный 32-битный int и, следовательно, содержит всю ручку, удаляя необходимость итерации всех открытых окон. 
  
### <a name="example"></a>Пример

См. код функции [fShowDialog](fshowdialog.md)  `SAMPLES\GENERIC\GENERIC.C` в .
  
## <a name="see-also"></a>См. также

- [xlGetInst](xlgetinst.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

