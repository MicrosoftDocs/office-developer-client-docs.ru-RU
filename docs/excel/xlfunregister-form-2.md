---
title: xlfUnregister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419907"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="812bd-104">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="812bd-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="812bd-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="812bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="812bd-106">Может быть вызвано из команды DLL или XLL, которая сама была вызвана Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="812bd-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="812bd-107">Это эквивалентно вызову **UNREGISTER** из макрос Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="812bd-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="812bd-108">**xlfUnregister** можно назвать в двух формах:</span><span class="sxs-lookup"><span data-stu-id="812bd-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="812bd-109">Форма 1. Незарегистрированные отдельные команды или функции.</span><span class="sxs-lookup"><span data-stu-id="812bd-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="812bd-110">Форма 2. Выгрузка и отключение XLL.</span><span class="sxs-lookup"><span data-stu-id="812bd-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="812bd-111">Вызванная в форме 2, эта функция заставляет полностью выгружать ресурс DLL или кода.</span><span class="sxs-lookup"><span data-stu-id="812bd-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="812bd-112">Он выполняет регистрацию всех функций в DLL, даже если они в настоящее время используются другим макросом, независимо от того, сколько используется.</span><span class="sxs-lookup"><span data-stu-id="812bd-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="812bd-113">Эта функция **вызывает xlAutoClose,** а затем отстранять все функции в DLL.</span><span class="sxs-lookup"><span data-stu-id="812bd-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="812bd-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="812bd-114">Parameters</span></span>

<span data-ttu-id="812bd-115">_pxModuleText_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="812bd-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="812bd-116">Имя DLL.</span><span class="sxs-lookup"><span data-stu-id="812bd-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="812bd-117">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="812bd-117">Property value/Return value</span></span>

<span data-ttu-id="812bd-118">В случае успешной работы **возвращает TRUE** **(xltypeBool).**</span><span class="sxs-lookup"><span data-stu-id="812bd-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="812bd-119">В случае неудачи возвращает **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="812bd-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="812bd-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="812bd-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="812bd-121">Не вызывайте эту форму функции из реализации [xlAutoClose](xlautoclose.md) в попытке отозвать все ресурсы DLL одним простым вызовом функции.</span><span class="sxs-lookup"><span data-stu-id="812bd-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="812bd-122">Это приводит к повторному вызову **xlAutoClose** и переполнению стека.</span><span class="sxs-lookup"><span data-stu-id="812bd-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="812bd-123">Не забудьте удалить имена</span><span class="sxs-lookup"><span data-stu-id="812bd-123">Remember to delete names</span></span>

<span data-ttu-id="812bd-124">Если вы указали аргумент  _pxFunctionText_ **на xlfRegister,** при регистрации функций и команд DLL необходимо явно удалить имена, позвонив **xlfSetName** для каждого из них, исключив второй аргумент, чтобы функция больше не появилась в мастере функции.</span><span class="sxs-lookup"><span data-stu-id="812bd-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="812bd-125">Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="812bd-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="812bd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="812bd-126">See also</span></span>

- [<span data-ttu-id="812bd-127">xlfRegister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="812bd-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="812bd-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="812bd-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="812bd-129">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="812bd-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="812bd-130">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="812bd-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

