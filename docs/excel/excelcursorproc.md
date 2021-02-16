---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- функция excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432494"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Когда модальные диалоговые окна отображаются в окне Microsoft Excel, курсор является курсором занятости в окне Excel. Этот **WndProc** WM_SETCURSOR тип сообщений Windows и изменяет курсор на обычную стрелку. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Параметры

 _hWndDlg_ (**HWND)**
  
Содержит HWND-окне Windows диалоговых окон.
  
 _message_ **(UINT)**
  
Сообщение, на которое необходимо ответить.
  
 _wParam_ (**WPARAM)**
  
 _lParam_ (**LPARAM)**
  
Аргументы, переданные Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

LRESULT: 0, если сообщение было обработано, в противном случае результат возвращается **WndProc по умолчанию**.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

