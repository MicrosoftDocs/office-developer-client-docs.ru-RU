---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Универсальный dll [excel 2007], функции, функции [Excel 2007], универсальный DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807275"
---
# <a name="functions-in-the-generic-dll"></a>Функции из универсальной библиотеки DLL

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Папка `\EXAMPLES\GENERIC\` содержит файлы проекта Microsoft Visual Studio и файлы исходного кода, которые требуются для компиляции примера DLL GENERIC.xll. Можно использовать этот проект как шаблон для создания собственных XLL-модулей для Microsoft Excel. Исходный код в этот проект демонстрирует многие функции интерфейса API для C Excel. 
  
При загрузке GENERIC.xll, он создает новые **универсальные** меню с четырьмя командами: 
  
- **Диалоговое окно** - отображает диалоговое окно Microsoft Excel. 
    
- **Танец** - перемещается выделение только после нажатия клавиши **ESC** . 
    
- **Собственная диалогового окна** — отображает диалоговое окно Windows. 
    
- **Выход** - GENERIC.xll выгрузки и удаляет **универсальный** меню. 
    
GENERIC.xll также предоставляет три функции листа, Func1, FuncSum и FuncFib, которую можно использовать при загрузке GENERIC.xll. GENERIC.xll можно загрузить с помощью диспетчера надстроек, или она загружается, если она была активна в конце обычной последнего сеанса Excel.
  
Этот проект использует библиотеку framework (FRMWRK32.lib).
  
## <a name="in-this-section"></a>В этой статье

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

