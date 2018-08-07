---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- функции Excel [excel 2007], функция Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807186"
---
# <a name="excelexcel12f"></a><span data-ttu-id="f928f-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="f928f-104">Excel/Excel12f</span></span>

 <span data-ttu-id="f928f-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f928f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f928f-106">Функции библиотеки Framework.</span><span class="sxs-lookup"><span data-stu-id="f928f-106">Framework library functions.</span></span> <span data-ttu-id="f928f-107">**Excel** является оболочкой для функции [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="f928f-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="f928f-108">**Excel12f** является оболочкой для функции [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="f928f-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="f928f-109">Каждый проверяется, что ни один из аргументов равно нулю, что указывает, что не удалось создать временные **XLOPER** или **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="f928f-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="f928f-110">Если возникает ошибка, каждый печатает сообщение отладки.</span><span class="sxs-lookup"><span data-stu-id="f928f-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="f928f-111">По завершении каждого освобождает все временные памяти, который мог быть создан для временного s **XLOPER**и **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="f928f-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="f928f-112">**Excel12f** могут вызываться только из DLL, начиная с Excel 2007 C API библиотеки.</span><span class="sxs-lookup"><span data-stu-id="f928f-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="f928f-113">Кроме того его только работы при запуске, начиная с помощью Excel 2007 и в противном случае — ошибка в **xlretFailed** .</span><span class="sxs-lookup"><span data-stu-id="f928f-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="f928f-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="f928f-114">Parameters</span></span>

 <span data-ttu-id="f928f-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="f928f-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="f928f-116">Число, указывающее команда или функция, которому нужно позвонить.</span><span class="sxs-lookup"><span data-stu-id="f928f-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="f928f-117">Для получения дополнительных сведений см [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="f928f-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="f928f-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="f928f-118">_pxRes_</span></span>
  
<span data-ttu-id="f928f-119">Указатель на результат вычисления функции.</span><span class="sxs-lookup"><span data-stu-id="f928f-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="f928f-120">Память, на который указывает в результате будет выделено, Excel и нужно освободить в вызове [xlFree](xlfree.md) после больше не требуется, или задав **xlbitXLFree** Если возвращаясь в Excel.</span><span class="sxs-lookup"><span data-stu-id="f928f-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="f928f-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="f928f-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="f928f-122">Число аргументов, передаваемых в функцию.</span><span class="sxs-lookup"><span data-stu-id="f928f-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="f928f-123">Начиная с версии Excel 2007, ограничение составляет 255 аргументов.</span><span class="sxs-lookup"><span data-stu-id="f928f-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="f928f-124">В более ранних версиях ограничение: 30.</span><span class="sxs-lookup"><span data-stu-id="f928f-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="f928f-125">_аргумент1..._</span><span class="sxs-lookup"><span data-stu-id="f928f-125">_argument1, ..._</span></span>
  
<span data-ttu-id="f928f-126">Необязательные аргументы для функции.</span><span class="sxs-lookup"><span data-stu-id="f928f-126">The optional arguments to the function.</span></span> <span data-ttu-id="f928f-127">Все аргументы должны быть указатели на **XLOPER**в случае **Excel**, или **XLOPER12**в случае **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="f928f-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f928f-128">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f928f-128">Return value</span></span>

<span data-ttu-id="f928f-129">Обе функции возвращают же об ошибках и коды при успешном выполнении как **Excel4**, **Excel4v**, **Excel12**и **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="f928f-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="f928f-130">В разделе [Excel4/Excel12](excel4-excel12.md) полное описание этих кодов.</span><span class="sxs-lookup"><span data-stu-id="f928f-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="f928f-131">Кроме того эти функции Framework возвращают обнаружил **xlretFailed** без вызова интерфейса API C, если указатель на параметр NULL.</span><span class="sxs-lookup"><span data-stu-id="f928f-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f928f-132">Пример</span><span class="sxs-lookup"><span data-stu-id="f928f-132">Example</span></span>

<span data-ttu-id="f928f-133">В этом примере функция **Excel12f** , которая отправляет сообщение в отладчике передает недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="f928f-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f928f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f928f-134">See also</span></span>



[<span data-ttu-id="f928f-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="f928f-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="f928f-136">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="f928f-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

