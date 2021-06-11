---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- функция unhookexcelwindow
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
  
Удаляет **ExcelCursorProc,** ранее установленный **HookExcelWindow.** Это было бы сделано так, чтобы **ExcelCursorProc** был вызван перед Microsoft Excel **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ **(HANDLE)**
  
Основная Excel Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Примечания

Эта функция восстанавливает Excel **WndProc** по умолчанию с помощью **SetWindowLong()** для восстановления адреса, сохраненного **hookExcelWindow()**.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

