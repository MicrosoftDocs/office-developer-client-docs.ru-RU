---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- функция xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807372"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает дескриптор окна верхнего уровня Microsoft Excel.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Параметры

Эта функция не содержит аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Содержит дескриптор окна (**xltypeInt**) в поле **val.w** . 
  
## <a name="remarks"></a>Замечания

Эта функция полезна для написания кода Windows API.
  
При вызове этой функции, с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)переменной целое число возвращаемых XLOPER является подписанных короткий внутреннего 16-разрядный Это только может содержать низкой 16 бит дескриптор 32-разрядная версия Windows. Чтобы найти высокой часть, код должен выполните итерацию по совпадение с низкой части всех открытых окон. Начиная с версии Excel 2007, переменной integer **XLOPER12** является подписью int 32-разрядная версия и поэтому содержит весь дескриптор, нужно будет выполнять итерацию всех открытых окон. 
  
### <a name="example"></a>Пример

Просмотр кода для [функции fShowDialog](fshowdialog.md) в `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>См. также

- [xlGetInst](xlgetinst.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

