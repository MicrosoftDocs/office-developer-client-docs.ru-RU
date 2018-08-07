---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- функция xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19807338"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="c190d-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="c190d-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="c190d-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c190d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c190d-106">Excel вызывает [функцию xlAutoRegister](xlautoregister-xlautoregister12.md) при вызова функции XLM, **Регистрация**или эквивалентный интерфейса API для C [xlfRegister функции](xlfregister-form-1.md), с помощью типов возврата и аргумент функции регистрации отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c190d-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="c190d-107">Это позволяет XLL-Модулей для поиска его внутренней списки экспортированных функций и команды, чтобы зарегистрировать функцию в аргументе и возвращаемые типы указан.</span><span class="sxs-lookup"><span data-stu-id="c190d-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="c190d-108">Начиная с версии Excel 2007, Excel вызывает функцию **xlAutoRegister12** вместо функции **xlAutoRegister** при экспорте с XLL.</span><span class="sxs-lookup"><span data-stu-id="c190d-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="c190d-109">Excel не требуется XLL внедрение и экспортировать любой из этих функций.</span><span class="sxs-lookup"><span data-stu-id="c190d-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c190d-110">Если **xlAutoRegister**/ **xlAutoRegister12** пытается зарегистрировать функцию без указания аргументов и возвращаемых типов, вызывающий рекурсивный цикл возникает которого со временем переполнение стека вызовов и завершает работу Excel.</span><span class="sxs-lookup"><span data-stu-id="c190d-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="c190d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c190d-111">Parameters</span></span>

 <span data-ttu-id="c190d-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="c190d-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="c190d-113">Имя функции XLL, который требуется зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="c190d-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c190d-114">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c190d-114">Property value/Return value</span></span>

<span data-ttu-id="c190d-115">Функция должна вернуть результат попытки для регистрации функции XLL _pxName_ , с помощью функции **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="c190d-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="c190d-116">Если указанная функция не является одним из экспортируемые, он должен возвращать **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="c190d-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="c190d-117">сообщение об ошибке, или **значение NULL,** что Excel будет интерпретировать в **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="c190d-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c190d-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="c190d-118">Remarks</span></span>

<span data-ttu-id="c190d-119">Реализация **xlAutoRegister** следует выполнять поиск без учета регистра через вашей XLL внутренних списков функций и команд, экспортируется совпадение с именем переданное.</span><span class="sxs-lookup"><span data-stu-id="c190d-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="c190d-120">При обнаружении функции или команды, **xlAutoRegister** производится попытка регистрации с помощью функции **xlfRegister** , сохраняя для предоставления строка, которая указывает типы возврата и аргумент функции, а также любые другие необходимые Excel сведения о функции.</span><span class="sxs-lookup"><span data-stu-id="c190d-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="c190d-121">Он должен возвращать в Excel независимо от существующих в **xlfRegister** , возвращенного.</span><span class="sxs-lookup"><span data-stu-id="c190d-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="c190d-122">Если функция успешно зарегистрирована, **xlfRegister** возвращает значение **xltypeNum** , содержащее идентификатор регистрации функции.</span><span class="sxs-lookup"><span data-stu-id="c190d-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c190d-123">Пример</span><span class="sxs-lookup"><span data-stu-id="c190d-123">Example</span></span>

<span data-ttu-id="c190d-124">Просмотрите файл `SAMPLES\EXAMPLE\EXAMPLE.C` пример внедрения этой функции.</span><span class="sxs-lookup"><span data-stu-id="c190d-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c190d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c190d-125">See also</span></span>



[<span data-ttu-id="c190d-126">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="c190d-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="c190d-127">ОТМЕНА РЕГИСТРАЦИИ</span><span class="sxs-lookup"><span data-stu-id="c190d-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

