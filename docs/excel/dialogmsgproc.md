---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- Функция диалогмсгпрок [Excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310964"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="0bf56-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="0bf56-104">DIALOGMsgProc</span></span>

<span data-ttu-id="0bf56-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0bf56-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0bf56-106">Эта процедура связана с встроенным диалоговым окном Windows, которое отображается в [фшовдиалог](fshowdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf56-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="0bf56-107">Он предоставляет процедуры службы, вызываемые Windows для событий (сообщений), происходящих, когда пользователь работает с одной из кнопок диалогового окна, полей ввода или элементов управления.</span><span class="sxs-lookup"><span data-stu-id="0bf56-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="0bf56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf56-108">Parameters</span></span>

 <span data-ttu-id="0bf56-109">_хвнддлг_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="0bf56-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="0bf56-110">Содержит дескриптор окна HWND диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0bf56-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="0bf56-111">_Message (сообщение_ ) (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="0bf56-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="0bf56-112">Сообщение, на которое необходимо ответить.</span><span class="sxs-lookup"><span data-stu-id="0bf56-112">The message to respond to.</span></span>
  
 <span data-ttu-id="0bf56-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="0bf56-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="0bf56-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="0bf56-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="0bf56-115">Аргументы, переданные Windows.</span><span class="sxs-lookup"><span data-stu-id="0bf56-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0bf56-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bf56-116">Property value/Return value</span></span>

 <span data-ttu-id="0bf56-117">**Значение true** , если сообщение обработано, в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="0bf56-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="0bf56-118">Пример</span><span class="sxs-lookup"><span data-stu-id="0bf56-118">Example</span></span>

<span data-ttu-id="0bf56-119">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="0bf56-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bf56-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0bf56-120">See also</span></span>



[<span data-ttu-id="0bf56-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="0bf56-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

