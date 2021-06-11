---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- функция excel12v [Excel 2007], функция Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414993"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="b855b-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="b855b-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="b855b-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b855b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b855b-106">Вызывает внутреннюю Microsoft Excel лист, функцию или команду макроса или специальную функцию или команду только для XLL из ресурса DLL, XLL или кода.</span><span class="sxs-lookup"><span data-stu-id="b855b-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="b855b-107">Все последние версии Excel поддерживают **Excel4v.**</span><span class="sxs-lookup"><span data-stu-id="b855b-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="b855b-108">Начиная с Excel 2007 года **поддерживается Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="b855b-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="b855b-109">Эти функции могут быть вызваны только Excel, когда управление передано DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="b855b-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="b855b-110">Их также можно вызвать, Excel, которые косвенно передали управление с помощью вызова Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="b855b-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="b855b-111">Они не могут быть вызваны в любое другое время.</span><span class="sxs-lookup"><span data-stu-id="b855b-111">They cannot be called at any other time.</span></span> <span data-ttu-id="b855b-112">Например, они не могут быть вызваны во время вызовов на функцию DllMain или в другое время, когда операционная система вызывает DLL, или из потока, созданного DLL.</span><span class="sxs-lookup"><span data-stu-id="b855b-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="b855b-113">Функции Excel4 и [Excel12](excel4-excel12.md) принимают их аргументы в качестве списка переменной длины в стеке, в то время как функции **Excel4v** и **Excel12v** принимают их аргументы в качестве массива.</span><span class="sxs-lookup"><span data-stu-id="b855b-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="b855b-114">Во всех остальных отношениях **Excel4** ведет себя так же, как **и Excel4v,** **а Excel12** ведет себя так же, как **и Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="b855b-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="b855b-115">Parameters</span><span class="sxs-lookup"><span data-stu-id="b855b-115">Parameters</span></span>

 <span data-ttu-id="b855b-116">_iFunction_ **(int)**</span><span class="sxs-lookup"><span data-stu-id="b855b-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="b855b-117">Номер, который указывает команду, функцию или специальную функцию, которую необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="b855b-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="b855b-118">Список допустимого  _значения iFunction_ см. в следующем разделе Примечание.</span><span class="sxs-lookup"><span data-stu-id="b855b-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="b855b-119">_pxRes_ **(LPXLOPER** или **LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="b855b-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="b855b-120">Указатель на **XLOPER** (в случае **Excel4v)** или **XLOPER12** (в случае **Excel12v),** которые будут удерживать результат оцениваемой функции.</span><span class="sxs-lookup"><span data-stu-id="b855b-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="b855b-121">_iCount_ **(int)**</span><span class="sxs-lookup"><span data-stu-id="b855b-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="b855b-122">Количество последующих аргументов, которые будут переданы функции.</span><span class="sxs-lookup"><span data-stu-id="b855b-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="b855b-123">В версиях Excel до 2003 года это может быть любое число от 0 до 30.</span><span class="sxs-lookup"><span data-stu-id="b855b-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="b855b-124">Начиная с Excel 2007 г. это может быть любое число от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="b855b-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="b855b-125">_rgx_ **(LPXLOPER []** или **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="b855b-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="b855b-126">Массив, содержащий аргументы для функции.</span><span class="sxs-lookup"><span data-stu-id="b855b-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="b855b-127">Все аргументы в массиве должны быть указателями на **значения XLOPER** или **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="b855b-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="b855b-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b855b-128">Return value</span></span>

<span data-ttu-id="b855b-129">Эти функции возвращают те же значения, что **и Excel4** и **Excel12.**</span><span class="sxs-lookup"><span data-stu-id="b855b-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b855b-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="b855b-130">Remarks</span></span>

<span data-ttu-id="b855b-131">Эти функции полезны, если количество аргументов, переданных оператору, переменно.</span><span class="sxs-lookup"><span data-stu-id="b855b-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="b855b-132">Например, **Excel4v** и **Excel12v** полезны при регистрации функций с помощью [xlfRegister,](xlfregister-form-1.md) где количество аргументов зависит от количества аргументов, принятых зарегистрированной функцией.</span><span class="sxs-lookup"><span data-stu-id="b855b-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="b855b-133">**Excel4v** и **Excel12v** также полезны при записи функции оболочки **для Excel4** или **Excel12.**</span><span class="sxs-lookup"><span data-stu-id="b855b-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="b855b-134">В этих случаях необходимо преобразовать список переменных аргументов, как это обычно предоставляется **в Excel4** или **Excel12,** в один аргумент массива переменного размера, чтобы вызвать обратно в Excel с помощью **Excel4v** или **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="b855b-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="b855b-135">Пример</span><span class="sxs-lookup"><span data-stu-id="b855b-135">Example</span></span>

<span data-ttu-id="b855b-136">В примерах кода см. код для **функций Excel** **и Excel12f** в Excel XLL SDK 2010 г., в следующем расположении, где установлен SDK:</span><span class="sxs-lookup"><span data-stu-id="b855b-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="b855b-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="b855b-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b855b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b855b-138">See also</span></span>



[<span data-ttu-id="b855b-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="b855b-139">Excel4/Excel12</span></span>](excel4-excel12.md)

