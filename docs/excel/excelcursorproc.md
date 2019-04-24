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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304097"
---
# <a name="excelcursorproc"></a><span data-ttu-id="fffcd-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="fffcd-104">ExcelCursorProc</span></span>

 <span data-ttu-id="fffcd-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fffcd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fffcd-106">Когда модальное диалоговое окно отображается над окном Microsoft Excel, курсор является занятым курсором на окне Excel.</span><span class="sxs-lookup"><span data-stu-id="fffcd-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="fffcd-107">Это **WndProc** ВЫПОЛНЯЕТ треппинг вм_сеткурсор типов сообщений Windows и изменяет курсор на обычную стрелку.</span><span class="sxs-lookup"><span data-stu-id="fffcd-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="fffcd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fffcd-108">Parameters</span></span>

 <span data-ttu-id="fffcd-109">_хвнддлг_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="fffcd-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="fffcd-110">Содержит дескриптор окна HWND диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="fffcd-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="fffcd-111">_Message (сообщение_ ) (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="fffcd-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="fffcd-112">Сообщение, на которое необходимо ответить.</span><span class="sxs-lookup"><span data-stu-id="fffcd-112">The message to respond to.</span></span>
  
 <span data-ttu-id="fffcd-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="fffcd-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="fffcd-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="fffcd-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="fffcd-115">Аргументы, переданные Windows.</span><span class="sxs-lookup"><span data-stu-id="fffcd-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fffcd-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fffcd-116">Property value/Return value</span></span>

<span data-ttu-id="fffcd-117">LRESULT: 0, если сообщение было обработано, в противном случае результат возвращается методом **WndProc**по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fffcd-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="fffcd-118">Пример</span><span class="sxs-lookup"><span data-stu-id="fffcd-118">Example</span></span>

<span data-ttu-id="fffcd-119">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="fffcd-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fffcd-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fffcd-120">See also</span></span>



[<span data-ttu-id="fffcd-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="fffcd-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

