---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc function [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406516"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Эта процедура связана с диалоговом окне Windows, [отображаемом fShowDialog.](fshowdialog.md) Он предоставляет процедуры обслуживания, которые Windows вызвал для событий (сообщений), которые происходят, когда пользователь работает с одной из кнопок диалоговых окон, полей ввода или элементов управления. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Параметры

 _hWndDlg_ (**HWND)**
  
Содержит HWND-окне Windows диалоговых окон.
  
 _message_ **(UINT)**
  
Сообщение, на которое необходимо ответить.
  
 _wParam_ **(WPARAM)**
  
 _lParam_ (**LPARAM)**
  
Аргументы, переданные Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **TRUE,** если сообщение обработано, **false,** если нет. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

