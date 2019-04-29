---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- Функция хукексцелвиндов [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413509"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="e121a-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="e121a-104">HookExcelWindow</span></span>

 <span data-ttu-id="e121a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e121a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e121a-106">Устанавливает **ексцелкурсорпрок** таким образом, чтобы он вызывался до основного **WndProc**Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e121a-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="e121a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e121a-107">Parameters</span></span>

 <span data-ttu-id="e121a-108">_хвндексцел_ (**Handle**)</span><span class="sxs-lookup"><span data-stu-id="e121a-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="e121a-109">Основной дескриптор Windows Excel.</span><span class="sxs-lookup"><span data-stu-id="e121a-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e121a-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e121a-110">Property value/Return value</span></span>

<span data-ttu-id="e121a-111">Функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e121a-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e121a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e121a-112">Remarks</span></span>

<span data-ttu-id="e121a-113">Функция получает адрес объекта Excel **WndProc** с помощью **жетвиндовлонг ()**.</span><span class="sxs-lookup"><span data-stu-id="e121a-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="e121a-114">Он сохраняет это значение в глобальном наборе, который можно использовать для вызова **WndProc** по умолчанию, а также для его восстановления.</span><span class="sxs-lookup"><span data-stu-id="e121a-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="e121a-115">Наконец, он заменяет этот адрес адресом **ексцелкурсорпрок** с помощью **сетвиндовлонг ()**.</span><span class="sxs-lookup"><span data-stu-id="e121a-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="e121a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="e121a-116">Example</span></span>

<span data-ttu-id="e121a-117">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="e121a-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e121a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e121a-118">See also</span></span>



[<span data-ttu-id="e121a-119">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="e121a-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

