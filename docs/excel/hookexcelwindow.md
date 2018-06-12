---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- функция hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807268"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Устанавливает **ExcelCursorProc** , чтобы вызывается до Microsoft Excel главного **WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ (**ОБРАБАТЫВАТЬ**)
  
Обработка форма главных окон Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Замечания

Функция получает адреса Excel **WndProc** посредством использования **GetWindowLong()**. Это значение сохраняется в глобальный, который можно использовать для звонков по умолчанию **WndProc** и восстановить его. И, наконец он заменяет этот адрес адресом **ExcelCursorProc** с помощью **SetWindowLong()**.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

