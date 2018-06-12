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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807336"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Удаляет **ExcelCursorProc** , которая ранее была установлена **HookExcelWindow**. Это может быть сделано, чтобы **ExcelCursorProc** вызван перед основной Microsoft Excel **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ (**ОБРАБАТЫВАТЬ**)
  
Обработка форма главных окон Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Замечания

Эта функция восстанавливает Excel по умолчанию **WndProc** использование **SetWindowLong()** для восстановления адрес, который был сохранен с **HookExcelWindow()**.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

