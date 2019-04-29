---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- Функция диалогмсгпрок [Excel 2007]
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
  
Эта процедура связана с встроенным диалоговым окном Windows, которое отображается в [фшовдиалог](fshowdialog.md) . Он предоставляет процедуры службы, вызываемые Windows для событий (сообщений), происходящих, когда пользователь работает с одной из кнопок диалогового окна, полей ввода или элементов управления. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Параметры

 _хвнддлг_ (**HWND**)
  
Содержит дескриптор окна HWND диалогового окна.
  
 _Message (сообщение_ ) (**Uint**)
  
Сообщение, на которое необходимо ответить.
  
 _wParam_ (**WParam**)
  
 _lParam_ (**LParam**)
  
Аргументы, переданные Windows.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **Значение true** , если сообщение обработано, в противном случае — **false** . 
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

