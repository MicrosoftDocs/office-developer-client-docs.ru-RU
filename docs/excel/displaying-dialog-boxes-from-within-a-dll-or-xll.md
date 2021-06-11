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
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="5f976-104">Отображение диалогов из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="5f976-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="5f976-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5f976-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5f976-106">Чтобы отобразить диалоговое окно Win32 с помощью, например, функции Windows SDK **DialogBox,** сначала необходимо получить полный 32-битный экземпляр и основные ручки окна для Excel.</span><span class="sxs-lookup"><span data-stu-id="5f976-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="5f976-107">Дополнительные сведения см. в [Excel Экземпляр и Основные ручки окна.](how-to-access-excel-instance-and-main-window-handles.md)</span><span class="sxs-lookup"><span data-stu-id="5f976-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="5f976-108">Предполагая, что в проекте содержится ресурс диалоговых полей, необходимо предпринять несколько действий, чтобы настроить режим обработки сообщений в недавно отображенном диалоговом окне и восстановить режим обработки Excel при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5f976-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="5f976-109">Пример команды [fShowDialog](fshowdialog.md) в проекте Generic демонстрирует использование функций Windows, чтобы сделать это правильно.</span><span class="sxs-lookup"><span data-stu-id="5f976-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="5f976-110">Вы также можете отображать диалоги с помощью API C без использования Windows функций SDK.</span><span class="sxs-lookup"><span data-stu-id="5f976-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="5f976-111">Однако возможности диалоговых полей API C очень ограничены по сравнению с возможностями Windows, Visual Basic для приложений (VBA) или классов Microsoft Foundation (MFC).</span><span class="sxs-lookup"><span data-stu-id="5f976-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="5f976-112">(Например, диалоги C API всегда являются модальными).</span><span class="sxs-lookup"><span data-stu-id="5f976-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f976-113">См. также</span><span class="sxs-lookup"><span data-stu-id="5f976-113">See also</span></span>



[<span data-ttu-id="5f976-114">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="5f976-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="5f976-115">Разработка библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="5f976-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="5f976-116">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="5f976-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="5f976-117">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="5f976-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

