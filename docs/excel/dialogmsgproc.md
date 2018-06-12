---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- функция dialogmsgproc [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807150"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Эта процедура связан с помощью собственного диалоговое окно Windows, [fShowDialog](fshowdialog.md) отображает. Она предоставляет службы подпрограммы, вызываемой Windows для событий (сообщений), которые происходят, когда пользователь работает одну из кнопок диалоговое окно "", поля ввода или элементов управления. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 **Значение TRUE,** Если сообщение обработано, **значение FALSE,** Если это не так. 
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

