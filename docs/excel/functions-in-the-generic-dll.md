---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- общие dll [Excel 2007], функции,функции [Excel 2007], Общий DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420600"
---
# <a name="functions-in-the-generic-dll"></a>Функции из универсальной библиотеки DLL

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Папка содержит Microsoft Visual Studio и исходные файлы кода, необходимые для компиляции примера `\EXAMPLES\GENERIC\` DLL GENERIC.xll. Этот проект можно использовать в качестве шаблона для написания собственных Microsoft Excel XLLs. Исходный код этого проекта демонстрирует многие функции API Excel C. 
  
При загрузке GENERIC.xll создается новое **общее** меню с четырьмя командами: 
  
- **Диалоговое** окно . Отображает Microsoft Excel диалоговое окно. 
    
- **Dance** — перемещает выбор до нажатия **клавиши ESC.** 
    
- **Диалоговое окно** Native — отображает Windows диалоговое окно. 
    
- **Exit** — разгружает GENERIC.xll и удаляет **общее** меню. 
    
GENERIC.xll также предоставляет три функции таблицы: Func1, FuncSum и FuncFib, которые можно использовать при загрузке GENERIC.xll. GENERIC.xll можно загрузить с помощью диспетчера надстройки или загрузить, если она была активна в обычном конце последнего сеанса Excel.
  
В этом проекте используется библиотека фреймворков (FRMWRK32.lib).
  
## <a name="in-this-section"></a>В этом разделе

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

