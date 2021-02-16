---
title: Отображение диалогов из DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], отображение диалогов из диалогов [Excel 2007], отображение из DLL или XLL,DLL [Excel 2007], отображение диалогов из
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417870"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Отображение диалогов из DLL или XLL

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы отобразить диалоговое окно Win32 с помощью, например, функции Windows SDK **DialogBox,** необходимо сначала получить полный 32-битный экземпляр и окне окне Excel. Дополнительные сведения [см. в примере Access Excel и окне Main Window Handles.](how-to-access-excel-instance-and-main-window-handles.md) 
  
Предположим, что проект содержит ресурс диалоговых окно, необходимо предпринять несколько действий, чтобы настроить процедуру обработки сообщений для нового отображаемого диалоговых окна и восстановить процедуру обработки сообщений Excel, когда диалоговое окно закрыто. Пример команды [fShowDialog в](fshowdialog.md) универсальном проекте демонстрирует правильное использование функций Windows. 
  
Диалоги также можно отображать с помощью API C без использования функций Windows SDK. Однако возможности API C в диалоговом окне очень ограничены по сравнению с возможностями Windows, Visual Basic для приложений (VBA) или классов Microsoft Foundation (MFC). (Например, диалоги API C всегда модальные).
  
## <a name="see-also"></a>См. также



[Создание XLL-файлов](creating-xlls.md)
  
[Разработка библиотек DLL](developing-dlls.md)
  
[Доступ к дескрипторам основного окна и экземпляра Excel](how-to-access-excel-instance-and-main-window-handles.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

