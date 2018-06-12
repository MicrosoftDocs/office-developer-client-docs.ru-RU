---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- функция unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807336"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="afae6-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="afae6-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="afae6-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="afae6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="afae6-106">Удаляет **ExcelCursorProc** , которая ранее была установлена **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="afae6-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="afae6-107">Это может быть сделано, чтобы **ExcelCursorProc** вызван перед основной Microsoft Excel **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="afae6-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="afae6-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="afae6-108">Parameters</span></span>

 <span data-ttu-id="afae6-109">_hWndExcel_ (**ОБРАБАТЫВАТЬ**)</span><span class="sxs-lookup"><span data-stu-id="afae6-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="afae6-110">Обработка форма главных окон Excel.</span><span class="sxs-lookup"><span data-stu-id="afae6-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="afae6-111">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afae6-111">Property value/Return value</span></span>

<span data-ttu-id="afae6-112">Функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="afae6-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afae6-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="afae6-113">Remarks</span></span>

<span data-ttu-id="afae6-114">Эта функция восстанавливает Excel по умолчанию **WndProc** использование **SetWindowLong()** для восстановления адрес, который был сохранен с **HookExcelWindow()**.</span><span class="sxs-lookup"><span data-stu-id="afae6-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="afae6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="afae6-115">Example</span></span>

<span data-ttu-id="afae6-116">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="afae6-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="afae6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="afae6-117">See also</span></span>



[<span data-ttu-id="afae6-118">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="afae6-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

