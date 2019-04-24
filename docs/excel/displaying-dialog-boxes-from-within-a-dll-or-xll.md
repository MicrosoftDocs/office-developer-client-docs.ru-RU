---
title: Отображение диалоговых окон в библиотеке DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [Excel 2007], отображение диалоговых окон из диалоговых окон [Excel 2007], отображение из DLL или XLL, библиотеки DLL [Excel 2007], отображение диалоговых окон из
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310939"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Отображение диалоговых окон в библиотеке DLL или XLL

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы отобразить диалоговое окно Win32 с помощью, например, функции **DialogBox**для Windows SDK, необходимо сначала получить все дескрипторы 32 и главного окна для Excel. Для получения дополнительных сведений см [экземпляр Access и дескрипторы основных окон](how-to-access-excel-instance-and-main-window-handles.md) 
  
Предполагается, что проект содержит ресурс диалогового окна, поэтому необходимо выполнить несколько действий, чтобы настроить подпрограмму обработки сообщений для нового отображаемого диалогового окна и восстановить процедуру обработки сообщений Excel при закрытии диалогового окна. В примере команды [фшовдиалог](fshowdialog.md) в универсальном проекте показано, как использовать функции Windows для правильного выполнения этой задачи. 
  
Вы также можете отображать диалоговые окна с помощью API C без использования функций Windows SDK. Однако возможности диалоговых окон в API C очень ограничены по сравнению с элементами Windows, Visual Basic для приложений (VBA) или Microsoft Foundation Classes (MFC). Например, диалоговые окна API C всегда являются модальными.
  
## <a name="see-also"></a>См. также



[Создание XLL-файлов](creating-xlls.md)
  
[Разработка библиотек DLL](developing-dlls.md)
  
[Доступ к дескрипторам основного окна и экземпляра Excel](how-to-access-excel-instance-and-main-window-handles.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

