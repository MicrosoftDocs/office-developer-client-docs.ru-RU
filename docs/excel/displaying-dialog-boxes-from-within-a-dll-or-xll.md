---
title: Отображение диалоговых окон из библиотеки DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL-модулей [excel 2007], отображение диалоговых окон из диалоговых окон [Excel 2007], отображение данных из DLL или XLL, отображение диалоговых окон из библиотек DLL [Excel 2007]
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807159"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="f893d-104">Отображение диалоговых окон из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f893d-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="f893d-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f893d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f893d-106">Чтобы открыть диалоговое окно Win32, с помощью, например, функции Windows SDK **следующейтаблице**необходимо получить полного экземпляра 32-разрядная версия и значками главного окна для Excel.</span><span class="sxs-lookup"><span data-stu-id="f893d-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="f893d-107">Дополнительные сведения см в [экземпляре Excel клиента и обрабатывает главного окна](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="f893d-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="f893d-108">Предположим, что проект содержит ресурс диалогового окна, необходимо выполнить несколько шагов присвоено, вновь отображаемых диалогового окна сообщения обработки ошибок и восстановление процедуру обработки при закрытии диалоговое окно сообщения Excel.</span><span class="sxs-lookup"><span data-stu-id="f893d-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="f893d-109">Пример командной [fShowDialog](fshowdialog.md) в проекте универсальный демонстрируется использование функций Windows для этого правильно.</span><span class="sxs-lookup"><span data-stu-id="f893d-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="f893d-110">Также можно отобразить диалоговых окон с помощью интерфейса API для C без использования функций Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f893d-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="f893d-111">Тем не менее диалоговое окно поле возможности интерфейса API для C очень ограничены по сравнению с учетными записями Windows, Visual Basic для приложений (VBA) или Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="f893d-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="f893d-112">(Например, диалоговые окна интерфейса API для C всегда являются модальными).</span><span class="sxs-lookup"><span data-stu-id="f893d-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f893d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="f893d-113">See also</span></span>



[<span data-ttu-id="f893d-114">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="f893d-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="f893d-115">Разработка библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="f893d-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="f893d-116">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="f893d-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="f893d-117">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f893d-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

