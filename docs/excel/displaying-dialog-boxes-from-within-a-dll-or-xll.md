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
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="9b018-104">Отображение диалогов из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="9b018-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="9b018-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9b018-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9b018-106">Чтобы отобразить диалоговое окно Win32 с помощью, например, функции Windows SDK **DialogBox,** необходимо сначала получить полный 32-битный экземпляр и окне окне Excel.</span><span class="sxs-lookup"><span data-stu-id="9b018-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="9b018-107">Дополнительные сведения [см. в примере Access Excel и окне Main Window Handles.](how-to-access-excel-instance-and-main-window-handles.md)</span><span class="sxs-lookup"><span data-stu-id="9b018-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="9b018-108">Предположим, что проект содержит ресурс диалоговых окно, необходимо предпринять несколько действий, чтобы настроить процедуру обработки сообщений для нового отображаемого диалоговых окна и восстановить процедуру обработки сообщений Excel, когда диалоговое окно закрыто.</span><span class="sxs-lookup"><span data-stu-id="9b018-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="9b018-109">Пример команды [fShowDialog в](fshowdialog.md) универсальном проекте демонстрирует правильное использование функций Windows.</span><span class="sxs-lookup"><span data-stu-id="9b018-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="9b018-110">Диалоги также можно отображать с помощью API C без использования функций Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9b018-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="9b018-111">Однако возможности API C в диалоговом окне очень ограничены по сравнению с возможностями Windows, Visual Basic для приложений (VBA) или классов Microsoft Foundation (MFC).</span><span class="sxs-lookup"><span data-stu-id="9b018-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="9b018-112">(Например, диалоги API C всегда модальные).</span><span class="sxs-lookup"><span data-stu-id="9b018-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b018-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9b018-113">See also</span></span>



[<span data-ttu-id="9b018-114">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="9b018-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="9b018-115">Разработка библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="9b018-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="9b018-116">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="9b018-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="9b018-117">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="9b018-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

