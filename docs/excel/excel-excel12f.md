---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- функция Excel [Excel 2007], функция Excel12f [Excel 2007]
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
# <a name="excelexcel12f"></a><span data-ttu-id="87909-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="87909-104">Excel/Excel12f</span></span>

 <span data-ttu-id="87909-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="87909-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="87909-106">Функции библиотеки Framework.</span><span class="sxs-lookup"><span data-stu-id="87909-106">Framework library functions.</span></span> <span data-ttu-id="87909-107">**Excel** — это оболочка для функции [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="87909-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="87909-108">**Excel12f** — это оболочка для функции [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="87909-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="87909-109">Каждый из них проверяет, не имеет ли ни одного из аргументов нулевого значения, что свидетельствует о том, что не удалось создать временную **XLOPER** или **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="87909-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="87909-110">При возникновении ошибки каждая печатает сообщение отладки.</span><span class="sxs-lookup"><span data-stu-id="87909-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="87909-111">По завершении каждая освобождает всю временную память, которая могла быть создана **для временных и** **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="87909-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="87909-112">**Excel12f** можно вызывать только из библиотеки DLL, начиная с библиотеки Excel 2007 C API C.</span><span class="sxs-lookup"><span data-stu-id="87909-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="87909-113">Кроме того, она работает только при запуске с Excel 2007 и завершается с помощью **кслретфаилед** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="87909-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="87909-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="87909-114">Parameters</span></span>

 <span data-ttu-id="87909-115">_ифунктион_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="87909-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="87909-116">Число, обозначающее команду или функцию, которую необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="87909-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="87909-117">Дополнительные сведения см. в статье [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="87909-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="87909-118">_пксрес_</span><span class="sxs-lookup"><span data-stu-id="87909-118">_pxRes_</span></span>
  
<span data-ttu-id="87909-119">Указатель на результат вычисления функции.</span><span class="sxs-lookup"><span data-stu-id="87909-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="87909-120">Все модули памяти, на которые указывает результат, будут выделены приложением Excel и должны быть освобождены в вызове [кслфри](xlfree.md) , когда он больше не нужен, или путем установки **кслбиткслфри** при его возврате в Excel.</span><span class="sxs-lookup"><span data-stu-id="87909-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="87909-121">_икаунт_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="87909-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="87909-122">Число аргументов, которые будут переданы в функцию.</span><span class="sxs-lookup"><span data-stu-id="87909-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="87909-123">Начиная с Excel 2007, предельное число аргументов равно 255.</span><span class="sxs-lookup"><span data-stu-id="87909-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="87909-124">В более ранних версиях лимит равен 30.</span><span class="sxs-lookup"><span data-stu-id="87909-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="87909-125">_argument1, ..._</span><span class="sxs-lookup"><span data-stu-id="87909-125">_argument1, ..._</span></span>
  
<span data-ttu-id="87909-126">Необязательные аргументы функции.</span><span class="sxs-lookup"><span data-stu-id="87909-126">The optional arguments to the function.</span></span> <span data-ttu-id="87909-127">Все аргументы должны быть указателями в **XLOPER**s в случае **Excel**или **XLOPER12**s в случае **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="87909-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="87909-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87909-128">Return value</span></span>

<span data-ttu-id="87909-129">Обе функции возвращают одни и те же коды ошибок и успешности, что и в **Excel4**, **Excel4v**, **Excel12**и **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="87909-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="87909-130">Полное описание этих кодов приведено в статье [Excel4/Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="87909-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="87909-131">Кроме того, эти функции платформы возвращают **кслретфаилед** без вызова API C, если обнаружен указатель NULL на параметр.</span><span class="sxs-lookup"><span data-stu-id="87909-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="87909-132">Пример</span><span class="sxs-lookup"><span data-stu-id="87909-132">Example</span></span>

<span data-ttu-id="87909-133">В этом примере в функцию **Excel12f** передается неверный аргумент, который отправляет сообщение отладчику.</span><span class="sxs-lookup"><span data-stu-id="87909-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="87909-134">См. также</span><span class="sxs-lookup"><span data-stu-id="87909-134">See also</span></span>



[<span data-ttu-id="87909-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="87909-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="87909-136">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="87909-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

