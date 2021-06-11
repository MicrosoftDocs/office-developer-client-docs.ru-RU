---
title: Отображение диалогов из DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [Excel 2007], отображающие диалоги из диалогов [Excel 2007], отображающие из DLL или XLL,DLLs [Excel 2007], отображая диалоги из
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
  
Чтобы отобразить диалоговое окно Win32 с помощью, например, функции Windows SDK **DialogBox,** сначала необходимо получить полный 32-битный экземпляр и основные ручки окна для Excel. Дополнительные сведения см. в [Excel Экземпляр и Основные ручки окна.](how-to-access-excel-instance-and-main-window-handles.md) 
  
Предполагая, что в проекте содержится ресурс диалоговых полей, необходимо предпринять несколько действий, чтобы настроить режим обработки сообщений в недавно отображенном диалоговом окне и восстановить режим обработки Excel при закрытии диалогового окна. Пример команды [fShowDialog](fshowdialog.md) в проекте Generic демонстрирует использование функций Windows, чтобы сделать это правильно. 
  
Вы также можете отображать диалоги с помощью API C без использования Windows функций SDK. Однако возможности диалоговых полей API C очень ограничены по сравнению с возможностями Windows, Visual Basic для приложений (VBA) или классов Microsoft Foundation (MFC). (Например, диалоги C API всегда являются модальными).
  
## <a name="see-also"></a>См. также



[Создание XLL-файлов](creating-xlls.md)
  
[Разработка библиотек DLL](developing-dlls.md)
  
[Доступ к дескрипторам основного окна и экземпляра Excel](how-to-access-excel-instance-and-main-window-handles.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

