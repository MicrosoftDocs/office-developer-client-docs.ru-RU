---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- функция dialogmsgproc [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807150"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="14d9b-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="14d9b-104">DIALOGMsgProc</span></span>

<span data-ttu-id="14d9b-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14d9b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="14d9b-106">Эта процедура связан с помощью собственного диалоговое окно Windows, [fShowDialog](fshowdialog.md) отображает.</span><span class="sxs-lookup"><span data-stu-id="14d9b-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="14d9b-107">Она предоставляет службы подпрограммы, вызываемой Windows для событий (сообщений), которые происходят, когда пользователь работает одну из кнопок диалоговое окно "", поля ввода или элементов управления.</span><span class="sxs-lookup"><span data-stu-id="14d9b-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="14d9b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14d9b-108">Parameters</span></span>

 <span data-ttu-id="14d9b-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="14d9b-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="14d9b-110">Содержит маркер HWND Windows диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="14d9b-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="14d9b-111">_сообщение_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="14d9b-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="14d9b-112">Ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="14d9b-112">The message to respond to.</span></span>
  
 <span data-ttu-id="14d9b-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="14d9b-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="14d9b-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="14d9b-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="14d9b-115">Аргументов, передаваемых операционной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="14d9b-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="14d9b-116">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14d9b-116">Property value/Return value</span></span>

 <span data-ttu-id="14d9b-117">**Значение TRUE,** Если сообщение обработано, **значение FALSE,** Если это не так.</span><span class="sxs-lookup"><span data-stu-id="14d9b-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="14d9b-118">Пример</span><span class="sxs-lookup"><span data-stu-id="14d9b-118">Example</span></span>

<span data-ttu-id="14d9b-119">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="14d9b-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14d9b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="14d9b-120">See also</span></span>



[<span data-ttu-id="14d9b-121">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="14d9b-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

