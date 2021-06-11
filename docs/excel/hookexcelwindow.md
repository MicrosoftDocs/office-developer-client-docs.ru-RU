---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- функция hookexcelwindow [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413509"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Устанавливает **ExcelCursorProc** так, чтобы он назывался перед Microsoft Excel **WndProc.**
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ **(HANDLE)**
  
Основная Excel Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Примечания

Функция получает адрес Excel **WndProc** с помощью **GetWindowLong()**. Это значение хранится в глобальном значении, которое можно использовать для вызова **WndProc по** умолчанию, а также для его восстановления. Наконец, он заменяет этот адрес на адрес **ExcelCursorProc** с помощью **SetWindowLong()**.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

