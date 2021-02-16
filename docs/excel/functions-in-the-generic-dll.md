---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
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
  
Папка содержит файлы проектов Microsoft Visual Studio и файлы исходных кодов, необходимые для компиляции примера  `\EXAMPLES\GENERIC\` DLL GENERIC.xll. Этот проект можно использовать в качестве шаблона для написания собственных XLL Microsoft Excel. Исходный код в этом проекте демонстрирует многие функции API C для Excel. 
  
При загрузке GENERIC.xll создается новое **универсальное** меню с четырьмя командами: 
  
- **Диалоговое окно** — отображает диалоговое окно Microsoft Excel. 
    
- **1** — перемещает выделение, пока не нажать клавишу **ESC.** 
    
- **Диалоговое окно Native** — отображает диалоговое окно Windows. 
    
- **Exit** — выгружает GENERIC.xll и удаляет **универсальное** меню. 
    
GENERIC.xll также предоставляет три функции таблицы, Func1, FuncSum и FuncFib, которые можно использовать при загрузке GENERIC.xll. GENERIC.xll можно загрузить с помощью диспетчера надстройки или загрузить, если он был активен в обычном конце последнего сеанса Excel.
  
Этот проект использует библиотеку структуры (FRMWRK32.lib).
  
## <a name="in-this-section"></a>В этом разделе:

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

