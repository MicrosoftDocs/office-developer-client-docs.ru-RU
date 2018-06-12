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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807249"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
При отображении модального диалогового окна на Microsoft Excel окно курсор является «занят» через окно Excel. В этом **WndProc** извещения WM_SETCURSOR введите сообщения Windows и изменения курсор назад к обычным стрелку. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameters

 _hWndDlg_ (**HWND**)
  
Содержит маркер HWND Windows диалогового окна.
  
 _сообщение_ (**UINT**)
  
Ответ на сообщение.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Аргументов, передаваемых операционной системой Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

LRESULT: 0, если сообщение было обработано, в противном случае возвращается результат по умолчанию **WndProc**.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

