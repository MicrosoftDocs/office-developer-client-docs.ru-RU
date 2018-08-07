---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- функция hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807268"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="c6e32-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="c6e32-104">HookExcelWindow</span></span>

 <span data-ttu-id="c6e32-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6e32-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c6e32-106">Устанавливает **ExcelCursorProc** , чтобы вызывается до Microsoft Excel главного **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="c6e32-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="c6e32-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6e32-107">Parameters</span></span>

 <span data-ttu-id="c6e32-108">_hWndExcel_ (**ОБРАБАТЫВАТЬ**)</span><span class="sxs-lookup"><span data-stu-id="c6e32-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="c6e32-109">Обработка форма главных окон Excel.</span><span class="sxs-lookup"><span data-stu-id="c6e32-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c6e32-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6e32-110">Property value/Return value</span></span>

<span data-ttu-id="c6e32-111">Функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c6e32-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6e32-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6e32-112">Remarks</span></span>

<span data-ttu-id="c6e32-113">Функция получает адреса Excel **WndProc** посредством использования **GetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="c6e32-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="c6e32-114">Это значение сохраняется в глобальный, который можно использовать для звонков по умолчанию **WndProc** и восстановить его.</span><span class="sxs-lookup"><span data-stu-id="c6e32-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="c6e32-115">И, наконец он заменяет этот адрес адресом **ExcelCursorProc** с помощью **SetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="c6e32-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="c6e32-116">Пример</span><span class="sxs-lookup"><span data-stu-id="c6e32-116">Example</span></span>

<span data-ttu-id="c6e32-117">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="c6e32-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6e32-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c6e32-118">See also</span></span>



[<span data-ttu-id="c6e32-119">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="c6e32-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

