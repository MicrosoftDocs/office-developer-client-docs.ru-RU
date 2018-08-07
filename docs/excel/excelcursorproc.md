---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- функция excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807249"
---
# <a name="excelcursorproc"></a><span data-ttu-id="437c1-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="437c1-104">ExcelCursorProc</span></span>

 <span data-ttu-id="437c1-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="437c1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="437c1-106">При отображении модального диалогового окна на Microsoft Excel окно курсор является «занят» через окно Excel.</span><span class="sxs-lookup"><span data-stu-id="437c1-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="437c1-107">В этом **WndProc** извещения WM_SETCURSOR введите сообщения Windows и изменения курсор назад к обычным стрелку.</span><span class="sxs-lookup"><span data-stu-id="437c1-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="437c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="437c1-108">Parameters</span></span>

 <span data-ttu-id="437c1-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="437c1-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="437c1-110">Содержит маркер HWND Windows диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="437c1-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="437c1-111">_сообщение_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="437c1-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="437c1-112">Ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="437c1-112">The message to respond to.</span></span>
  
 <span data-ttu-id="437c1-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="437c1-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="437c1-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="437c1-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="437c1-115">Аргументов, передаваемых операционной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="437c1-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="437c1-116">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="437c1-116">Property value/Return value</span></span>

<span data-ttu-id="437c1-117">LRESULT: 0, если сообщение было обработано, в противном случае возвращается результат по умолчанию **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="437c1-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="437c1-118">Пример</span><span class="sxs-lookup"><span data-stu-id="437c1-118">Example</span></span>

<span data-ttu-id="437c1-119">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="437c1-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="437c1-120">См. также</span><span class="sxs-lookup"><span data-stu-id="437c1-120">See also</span></span>



[<span data-ttu-id="437c1-121">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="437c1-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

