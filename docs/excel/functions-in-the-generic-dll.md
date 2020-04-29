---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- универсальная библиотека DLL [Excel 2007], функции, функции [Excel 2007], Общая библиотека DLL
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
  
В этой `\EXAMPLES\GENERIC\` папке содержатся файлы проекта Microsoft Visual Studio и файлы исходного кода, необходимые для компиляции примера GENERIC DLL Generic. XLL. Вы можете использовать этот проект в качестве шаблона для создания собственных XLL Microsoft Excel. Исходный код в этом проекте демонстрирует многие функции API C для Excel. 
  
При загрузке GENERIC. XLL создается новое **универсальное** меню с четырьмя командами: 
  
- **Диалоговое окно** — отображает диалоговое окно Microsoft Excel. 
    
- **Данце** — выделяет выделенный фрагмент, пока вы не нажмете клавишу **ESC** . 
    
- **Собственное диалоговое окно** — отображает диалоговое окно Windows. 
    
- **Exit** — выгружает Generic. XLL и удаляет **Общее** меню. 
    
GENERIC. XLL также предоставляет три функции листа, func1, Функсум и Функфиб, которые можно использовать каждый раз, когда загружается GENERIC. XLL. GENERIC. XLL можно загрузить с помощью диспетчера надстроек или загрузить, если она была активна в обычном конце последнего сеанса Excel.
  
В этом проекте используется библиотека Framework (FRMWRK32. lib).
  
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

