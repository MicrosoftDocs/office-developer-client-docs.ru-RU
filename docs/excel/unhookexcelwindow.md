---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- Функция unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409449"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="94ef9-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="94ef9-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="94ef9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94ef9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94ef9-106">Удаляет **ExcelCursorProc,** ранее установленный **HookExcelWindow.**</span><span class="sxs-lookup"><span data-stu-id="94ef9-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="94ef9-107">Это было бы сделано для того, чтобы **ExcelCursorProc был вызван** до основного **WndProc** Microsoft Excel .</span><span class="sxs-lookup"><span data-stu-id="94ef9-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="94ef9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94ef9-108">Parameters</span></span>

 <span data-ttu-id="94ef9-109">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="94ef9-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="94ef9-110">Основной работник Windows Excel.</span><span class="sxs-lookup"><span data-stu-id="94ef9-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="94ef9-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94ef9-111">Property value/Return value</span></span>

<span data-ttu-id="94ef9-112">Функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="94ef9-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94ef9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="94ef9-113">Remarks</span></span>

<span data-ttu-id="94ef9-114">Эта функция восстанавливает Excel по умолчанию **WndProc** с помощью **SetWindowLong()** для восстановления адреса, сохраненного с помощью **HookExcelWindow()**.</span><span class="sxs-lookup"><span data-stu-id="94ef9-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="94ef9-115">Пример</span><span class="sxs-lookup"><span data-stu-id="94ef9-115">Example</span></span>

<span data-ttu-id="94ef9-116">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="94ef9-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94ef9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="94ef9-117">See also</span></span>



[<span data-ttu-id="94ef9-118">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="94ef9-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

