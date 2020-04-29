---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- Функция ексцелкурсорпрок [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432494"
---
# <a name="excelcursorproc"></a><span data-ttu-id="1b059-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="1b059-104">ExcelCursorProc</span></span>

 <span data-ttu-id="1b059-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b059-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1b059-106">Когда модальное диалоговое окно отображается над окном Microsoft Excel, курсор является занятым курсором на окне Excel.</span><span class="sxs-lookup"><span data-stu-id="1b059-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="1b059-107">Эти ловушки **WndProc** WM_SETCURSOR вводить сообщения Windows и отменяют курсор на обычную стрелку.</span><span class="sxs-lookup"><span data-stu-id="1b059-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="1b059-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b059-108">Parameters</span></span>

 <span data-ttu-id="1b059-109">_хвнддлг_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="1b059-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="1b059-110">Содержит дескриптор окна HWND диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1b059-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="1b059-111">_Message_ (**uint**)</span><span class="sxs-lookup"><span data-stu-id="1b059-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="1b059-112">Сообщение, на которое необходимо ответить.</span><span class="sxs-lookup"><span data-stu-id="1b059-112">The message to respond to.</span></span>
  
 <span data-ttu-id="1b059-113">_wParam_ (**wParam**)</span><span class="sxs-lookup"><span data-stu-id="1b059-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="1b059-114">_lParam_ (**lParam**)</span><span class="sxs-lookup"><span data-stu-id="1b059-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="1b059-115">Аргументы, переданные Windows.</span><span class="sxs-lookup"><span data-stu-id="1b059-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1b059-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b059-116">Property value/Return value</span></span>

<span data-ttu-id="1b059-117">LRESULT: 0, если сообщение было обработано, в противном случае результат возвращается методом **WndProc**по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b059-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="1b059-118">Пример</span><span class="sxs-lookup"><span data-stu-id="1b059-118">Example</span></span>

<span data-ttu-id="1b059-119">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="1b059-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b059-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1b059-120">See also</span></span>



[<span data-ttu-id="1b059-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="1b059-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

