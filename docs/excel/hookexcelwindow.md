---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- Функция хукексцелвиндов [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310831"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Устанавливает **ексцелкурсорпрок** таким образом, чтобы он вызывался до основного **WndProc**Microsoft Excel.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Параметры

 _хвндексцел_ (**Handle**)
  
Основной дескриптор Windows Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция не возвращает значение.
  
## <a name="remarks"></a>Замечания

Функция получает адрес объекта Excel **WndProc** с помощью **жетвиндовлонг ()**. Он сохраняет это значение в глобальном наборе, который можно использовать для вызова **WndProc** по умолчанию, а также для его восстановления. Наконец, он заменяет этот адрес адресом **ексцелкурсорпрок** с помощью **сетвиндовлонг ()**.
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

