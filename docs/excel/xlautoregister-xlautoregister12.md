---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- функция xlautoregister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421167"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="e08de-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="e08de-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="e08de-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e08de-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e08de-106">Excel вызывает функцию [xlAutoRegister](xlautoregister-xlautoregister12.md) всякий раз, когда вызов был сделан в регистр функции XLM **или** функцию XPI, эквивалентную [XlfRegister](xlfregister-form-1.md)C, при этом отсутствуют типы возвращаемой и аргументированной функции.</span><span class="sxs-lookup"><span data-stu-id="e08de-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="e08de-107">Она позволяет XLL искать внутренние списки экспортных функций и команд для регистрации функции с указанными типами аргументов и возврата.</span><span class="sxs-lookup"><span data-stu-id="e08de-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="e08de-108">Начиная с Excel 2007 г., Excel вызывает функцию **xlAutoRegister12** в предпочтение функции **xlAutoRegister,** если она экспортируется XLL.</span><span class="sxs-lookup"><span data-stu-id="e08de-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="e08de-109">Excel XLL не требуется для реализации и экспорта этих функций.</span><span class="sxs-lookup"><span data-stu-id="e08de-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e08de-110">Если **xlAutoRegister** /  **xlAutoRegister12** пытается зарегистрировать функцию, не поставляя типы аргументов и возврата, возникает цикл повторного вызова, который в конечном итоге переполниет стек вызовов и сбои Excel.</span><span class="sxs-lookup"><span data-stu-id="e08de-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="e08de-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="e08de-111">Parameters</span></span>

 <span data-ttu-id="e08de-112">_pxName_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="e08de-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="e08de-113">Имя зарегистрированной функции XLL.</span><span class="sxs-lookup"><span data-stu-id="e08de-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e08de-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e08de-114">Property value/Return value</span></span>

<span data-ttu-id="e08de-115">Функция должна возвращать результат попытки зарегистрировать _pxName_ функции XLL с помощью **функции xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="e08de-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="e08de-116">Если указанная функция не является экспортом XLL, она должна вернуть **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="e08de-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="e08de-117">ошибка, **или NULL,** Excel будет интерпретироваться **в #VALUE!.**</span><span class="sxs-lookup"><span data-stu-id="e08de-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e08de-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e08de-118">Remarks</span></span>

<span data-ttu-id="e08de-119">Реализация **xlAutoRegister** должна выполнять нечувствительный поиск через внутренние списки функций и команд XLL, экспортированных в поисках совпадения с переданным именем.</span><span class="sxs-lookup"><span data-stu-id="e08de-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="e08de-120">Если функция или команда найдена, **xlAutoRegister** должен попытаться зарегистрировать ее с помощью функции **xlfRegister,** чтобы предоставить строку, которая Excel типам возврата и аргументов функции, а также любые другие необходимые сведения о функции.</span><span class="sxs-lookup"><span data-stu-id="e08de-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="e08de-121">Затем он должен вернуться в Excel все **вызовы xlfRegister** возвращены.</span><span class="sxs-lookup"><span data-stu-id="e08de-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="e08de-122">Если функция была успешно зарегистрирована, **xlfRegister** возвращает **значение xltypeNum,** содержащее ID регистра функции.</span><span class="sxs-lookup"><span data-stu-id="e08de-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="e08de-123">Пример</span><span class="sxs-lookup"><span data-stu-id="e08de-123">Example</span></span>

<span data-ttu-id="e08de-124">Пример реализации этой  `SAMPLES\EXAMPLE\EXAMPLE.C` функции см. в файле.</span><span class="sxs-lookup"><span data-stu-id="e08de-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e08de-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e08de-125">See also</span></span>



[<span data-ttu-id="e08de-126">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="e08de-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="e08de-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="e08de-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

