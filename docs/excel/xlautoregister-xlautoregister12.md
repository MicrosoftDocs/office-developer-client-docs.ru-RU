---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Функция xlAutoRegister [Excel 2007]
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
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="e34c9-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="e34c9-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="e34c9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e34c9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e34c9-106">Excel вызывает [функцию xlAutoRegister](xlautoregister-xlautoregister12.md) при каждом вызове в **регистре**функции XLM или в эквивалентной функции C API [xlfRegister](xlfregister-form-1.md)с типами возвращаемых значения и аргументов функции, которую вы зарегистрировали.</span><span class="sxs-lookup"><span data-stu-id="e34c9-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="e34c9-107">Он позволяет XLL выполнить поиск по внутренним спискам экспортированных функций и команд, чтобы зарегистрировать функцию с указанными аргументами и возвращаемыми типами.</span><span class="sxs-lookup"><span data-stu-id="e34c9-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="e34c9-108">Начиная с Excel 2007, Excel вызывает функцию **xlAutoRegister12** в предпочтение функции **xlAutoRegister** , если она экспортируется XLL.</span><span class="sxs-lookup"><span data-stu-id="e34c9-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="e34c9-109">В Excel не требуется XLL для реализации и экспорта любой из этих функций.</span><span class="sxs-lookup"><span data-stu-id="e34c9-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e34c9-110">Если **xlAutoRegister**/ **xlAutoRegister12** пытается зарегистрировать функцию, не предоставляя аргументы и типы возвращаемых данных, вызывается рекурсивный цикл вызова, который в конечном итоге переполняет стек вызовов и завершает работу Excel.</span><span class="sxs-lookup"><span data-stu-id="e34c9-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="e34c9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e34c9-111">Parameters</span></span>

 <span data-ttu-id="e34c9-112">_пкснаме_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="e34c9-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="e34c9-113">Имя регистрируемой функции XLL.</span><span class="sxs-lookup"><span data-stu-id="e34c9-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e34c9-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e34c9-114">Property value/Return value</span></span>

<span data-ttu-id="e34c9-115">Функция должна возвращать результат попытки зарегистрировать функцию XLL _пкснаме_ с помощью функции **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="e34c9-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="e34c9-116">Если указанная функция не является одним из экспортируемых компонентов XLL, она должна возвращать **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="e34c9-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="e34c9-117">ошибка или **значение NULL** , которое будет интерпретировано в приложении Excel на **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="e34c9-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e34c9-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e34c9-118">Remarks</span></span>

<span data-ttu-id="e34c9-119">Ваша реализация **xlAutoRegister** должна выполнять поиск с учетом регистра, используя внутренние списки функций и команд, которые она экспортирует, в поисках сравнения с переданным именем.</span><span class="sxs-lookup"><span data-stu-id="e34c9-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="e34c9-120">Если функция или команда найдена, **xlAutoRegister** должна попытаться зарегистрировать ее, используя функцию **xlfRegister** , убедившись, что вы задаете строку, сообщающую Excel о типах возвращаемых данных и аргументах функции, а также о любой другой обязательной информации о функции.</span><span class="sxs-lookup"><span data-stu-id="e34c9-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="e34c9-121">Затем он должен вернуться в Excel, что бы возвращался вызов **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="e34c9-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="e34c9-122">Если функция была зарегистрирована успешно, **xlfRegister** возвращает значение **КСЛТИПЕНУМ** , содержащее идентификатор регистра функции.</span><span class="sxs-lookup"><span data-stu-id="e34c9-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="e34c9-123">Пример</span><span class="sxs-lookup"><span data-stu-id="e34c9-123">Example</span></span>

<span data-ttu-id="e34c9-124">В этом файле `SAMPLES\EXAMPLE\EXAMPLE.C` представлен пример реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="e34c9-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e34c9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e34c9-125">See also</span></span>



[<span data-ttu-id="e34c9-126">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="e34c9-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="e34c9-127">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="e34c9-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

