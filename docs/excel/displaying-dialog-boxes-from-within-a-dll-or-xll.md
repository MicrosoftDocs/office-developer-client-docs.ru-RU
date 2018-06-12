---
title: Отображение диалоговых окон из DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL-модулей [excel 2007], отображение диалоговых окон из диалоговых окон [Excel 2007], отображение данных из DLL или XLL, отображение диалоговых окон из библиотек DLL [Excel 2007]
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807159"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Отображение диалоговых окон из DLL или XLL

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы открыть диалоговое окно Win32, с помощью, например, функции Windows SDK **следующейтаблице**необходимо получить полного экземпляра 32-разрядная версия и значками главного окна для Excel. Дополнительные сведения см в [экземпляре Excel клиента и обрабатывает главного окна](how-to-access-excel-instance-and-main-window-handles.md). 
  
Предположим, что проект содержит ресурс диалогового окна, необходимо выполнить несколько шагов присвоено, вновь отображаемых диалогового окна сообщения обработки ошибок и восстановление процедуру обработки при закрытии диалоговое окно сообщения Excel. Пример командной [fShowDialog](fshowdialog.md) в проекте универсальный демонстрируется использование функций Windows для этого правильно. 
  
Также можно отобразить диалоговых окон с помощью интерфейса API для C без использования функций Windows SDK. Тем не менее диалоговое окно поле возможности интерфейса API для C очень ограничены по сравнению с учетными записями Windows, Visual Basic для приложений (VBA) или Microsoft Foundation Classes (MFC). (Например, диалоговые окна интерфейса API для C всегда являются модальными).
  
## <a name="see-also"></a>См. также



[Создание XLL-модулей](creating-xlls.md)
  
[Разработка библиотеки DLL](developing-dlls.md)
  
[Доступ к экземпляру Excel и значками главное окно](how-to-access-excel-instance-and-main-window-handles.md)
  
[Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

