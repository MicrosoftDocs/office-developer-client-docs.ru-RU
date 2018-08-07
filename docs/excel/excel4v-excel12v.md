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
- функция Excel12v [excel 2007], функция Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807259"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="a8d3e-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="a8d3e-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="a8d3e-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8d3e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8d3e-106">Вызывает внутренней функции Microsoft Excel, функцию листа макросов или команды, или только для XLL специальные функции или команды, из в DLL-Библиотеку, XLL или ресурс кода.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="a8d3e-107">Все последние версии Excel поддерживают **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="a8d3e-108">Начиная с версии Excel 2007, **Excel12v** поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="a8d3e-109">Эти функции могут вызываться только в том случае, когда Excel истекло управления DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="a8d3e-110">Они также могут вызываться, когда Excel истекло управления косвенно через вызов Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="a8d3e-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="a8d3e-111">Они не могут вызывать в любое время.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-111">They cannot be called at any other time.</span></span> <span data-ttu-id="a8d3e-112">Например они не может вызываться при выполнении вызова функции DllMain или в других случаях, когда операционная система называется библиотеки DLL или из потока, созданные в библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="a8d3e-113">Функции [Excel4 и Excel12](excel4-excel12.md) примите их аргументах как список переменной длины в стеке, тогда как функции **Excel4v** и **Excel12v** примите их аргументах как массив.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="a8d3e-114">Во всех других отношениях **Excel4** происходит так же, как **Excel4v**и **Excel12** происходит так же, как **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="a8d3e-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8d3e-115">Parameters</span></span>

 <span data-ttu-id="a8d3e-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a8d3e-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="a8d3e-117">Число, указывающее команды, функции или специальные функции, которому нужно позвонить.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="a8d3e-118">Список значений допустимый _iFunction_ в следующем разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="a8d3e-119">_pxRes_ (**LPXLOPER** или **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a8d3e-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="a8d3e-120">Указатель на **XLOPER** (в случае **Excel4v**) или **XLOPER12** (в случае **Excel12v**), который будет содержать результат вычисления функции.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="a8d3e-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a8d3e-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="a8d3e-122">Число последующих аргументов, передаваемых в функцию.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="a8d3e-123">В версиях Excel 2003 до это может быть любое число от 0 до 30.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="a8d3e-124">Начиная с версии Excel 2007, это может быть любое число от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="a8d3e-125">_rgx_ (**LPXLOPER []** или **[LPXLOPER12]**)</span><span class="sxs-lookup"><span data-stu-id="a8d3e-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="a8d3e-126">Массив, содержащий аргументы для функции.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="a8d3e-127">Все аргументы в массиве должны быть указатели на **XLOPER** или **XLOPER12** значения.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="a8d3e-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="a8d3e-129">Эти функции возвращают те же значения, как **Excel4** и **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8d3e-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8d3e-130">Remarks</span></span>

<span data-ttu-id="a8d3e-131">Эти функции полезны, где число аргументов, передаваемых в оператор — это переменная.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="a8d3e-132">Например **Excel4v** и **Excel12v** полезны при регистрации функции с помощью [xlfRegister](xlfregister-form-1.md) , где число аргументов, общее зависит от числа аргументов, занимаемых функцию регистрации.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="a8d3e-133">**Excel4v** и **Excel12v** также используются при записи функции программы-оболочки для **Excel4** или **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="a8d3e-134">В таких случаях необходимо преобразовать список аргументов переменных, как бы обычно **Excel4** или **Excel12**, чтобы указать аргумент один массив переменного размера для обратного вызова Excel с помощью **Excel4v** или **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="a8d3e-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="a8d3e-135">Пример</span><span class="sxs-lookup"><span data-stu-id="a8d3e-135">Example</span></span>

<span data-ttu-id="a8d3e-136">Примеры кода просмотрите код для функции **Excel** и **Excel12f** в Excel 2010 XLL SDK, в следующем расположении, где установлен пакет SDK:</span><span class="sxs-lookup"><span data-stu-id="a8d3e-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="a8d3e-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="a8d3e-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8d3e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a8d3e-138">See also</span></span>



[<span data-ttu-id="a8d3e-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="a8d3e-139">Excel4/Excel12</span></span>](excel4-excel12.md)

