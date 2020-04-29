---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- Функция ексцелкурсорпрок [Excel 2007]
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
  
Когда модальное диалоговое окно отображается над окном Microsoft Excel, курсор является занятым курсором на окне Excel. Эти ловушки **WndProc** WM_SETCURSOR вводить сообщения Windows и отменяют курсор на обычную стрелку. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Параметры

 _хвнддлг_ (**HWND**)
  
Содержит дескриптор окна HWND диалогового окна.
  
 _Message_ (**uint**)
  
Сообщение, на которое необходимо ответить.
  
 _wParam_ (**wParam**)
  
 _lParam_ (**lParam**)
  
Аргументы, переданные Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

LRESULT: 0, если сообщение было обработано, в противном случае результат возвращается методом **WndProc**по умолчанию.
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

