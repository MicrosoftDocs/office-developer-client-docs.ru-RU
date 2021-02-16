---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Функция excel [excel 2007],Excel12f function [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431675"
---
# <a name="excelexcel12f"></a><span data-ttu-id="4ad4f-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="4ad4f-104">Excel/Excel12f</span></span>

 <span data-ttu-id="4ad4f-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ad4f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4ad4f-106">Функции библиотеки framework.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-106">Framework library functions.</span></span> <span data-ttu-id="4ad4f-107">**Excel** является оболочкой для [функции Excel4.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="4ad4f-108">**Excel12f** — это оболочка для [функции Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="4ad4f-109">Каждый из них проверяет, что ни один из аргументов не имеет нулевого уровня, что указывает на сбой создания временного **XLOPER** или **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="4ad4f-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="4ad4f-110">В случае возникновения ошибки каждая из них печатает сообщение отлаки.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="4ad4f-111">После завершения каждый из них освободит все временные объемы памяти, которые могли быть созданы для временных **XLOPER** и **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="4ad4f-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER** s and **XLOPER12** s.</span></span>
  
 <span data-ttu-id="4ad4f-112">**Excel12f** можно запускать только из библиотеки DLL, начиная с библиотеки API C Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="4ad4f-113">Кроме того, он работает только при запуске, начиная с Excel 2007, и не работает с **xlretFailed** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="4ad4f-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad4f-114">Parameters</span></span>

 <span data-ttu-id="4ad4f-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="4ad4f-116">Номер, указывающий команду или функцию, которые вы хотите вызвать.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="4ad4f-117">Дополнительные сведения см. в [excel4/Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="4ad4f-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="4ad4f-118">_pxRes_</span></span>
  
<span data-ttu-id="4ad4f-119">Указатель на результат оцениваемой функции.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="4ad4f-120">Любая память, на которая указывается в результате, будет выделена Excel и должна быть освобождена в вызове [xlFree](xlfree.md) после того, как она больше не требуется, или путем настройки **xlbitXLFree,** если она возвращается в Excel.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="4ad4f-121">_iCount_ (**int)**</span><span class="sxs-lookup"><span data-stu-id="4ad4f-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="4ad4f-122">Количество аргументов, которые будут переданы функции.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="4ad4f-123">Начиная с Excel 2007, ограничение составляет 255 аргументов.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="4ad4f-124">В предыдущих версиях ограничение составляет 30.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="4ad4f-125">_argument1, ..._</span><span class="sxs-lookup"><span data-stu-id="4ad4f-125">_argument1, ..._</span></span>
  
<span data-ttu-id="4ad4f-126">Необязательные аргументы функции.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-126">The optional arguments to the function.</span></span> <span data-ttu-id="4ad4f-127">Все аргументы должны быть указателями на **XLOPER** в случае **Excel** или **XLOPER12** в случае **Excel12f.**</span><span class="sxs-lookup"><span data-stu-id="4ad4f-127">All arguments must be pointers to **XLOPER** s in the case of **Excel**, or **XLOPER12** s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4ad4f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad4f-128">Return value</span></span>

<span data-ttu-id="4ad4f-129">Обе функции возвращают те же коды ошибок и успешности, что **и Excel4,** **Excel4v,** **Excel12** и **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="4ad4f-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="4ad4f-130">Полное описание этих кодов см. в excel4 и [Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="4ad4f-131">Кроме того, эти функции Framework возвращают **xlretFailed** без вызова API C, если обнаружен указатель NULL на параметр.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4ad4f-132">Пример</span><span class="sxs-lookup"><span data-stu-id="4ad4f-132">Example</span></span>

<span data-ttu-id="4ad4f-133">В этом примере в функцию **Excel12f** передается плохой аргумент, который отправляет сообщение отладилю.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4ad4f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4ad4f-134">See also</span></span>



[<span data-ttu-id="4ad4f-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="4ad4f-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="4ad4f-136">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="4ad4f-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

