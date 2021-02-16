---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- Функция unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409449"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Удаляет **ExcelCursorProc,** ранее установленный **HookExcelWindow.** Это было бы сделано для того, чтобы **ExcelCursorProc был вызван** до основного **WndProc** Microsoft Excel .
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Параметры

 _hWndExcel_ (**HANDLE**)
  
Основной работник Windows Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Примечания

Эта функция восстанавливает Excel по умолчанию **WndProc** с помощью **SetWindowLong()** для восстановления адреса, сохраненного с помощью **HookExcelWindow()**.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

