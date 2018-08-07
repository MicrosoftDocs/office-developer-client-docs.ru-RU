---
title: xlfUnregister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807373"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="0f8bf-104">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="0f8bf-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0f8bf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0f8bf-106">Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="0f8bf-107">Это эквивалентно вызову **Отменить РЕГИСТРАЦИЮ** из таблицы Excel XLM макрос.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="0f8bf-108">**xlfUnregister** может быть вызван в двух вариантах:</span><span class="sxs-lookup"><span data-stu-id="0f8bf-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="0f8bf-109">Форма 1: Отменяет отдельные команды или функции.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="0f8bf-110">Форма 2: Выгрузка и деактивирует надстройке XLL.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="0f8bf-111">Принудительно вызывает в виде 2, эта функция DLL или кода ресурса, выгрузки полностью.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="0f8bf-112">Она отменяет все функции в DLL, даже в том случае, если они находятся в настоящее время используется другой макрос, независимо от того, какие счетчика.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="0f8bf-113">Эта функция вызывает **xlAutoClose**и затем отменяет регистрацию всех функций в DLL-Библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="0f8bf-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f8bf-114">Parameters</span></span>

<span data-ttu-id="0f8bf-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="0f8bf-116">Имя библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0f8bf-117">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f8bf-117">Property value/Return value</span></span>

<span data-ttu-id="0f8bf-118">В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="0f8bf-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="0f8bf-119">В случае неудачи возвращает **значение FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f8bf-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f8bf-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="0f8bf-121">Не вызывайте эту форму функции от внедрения [xlAutoClose](xlautoclose.md) при попытке отменить регистрацию всех ресурсов DLL-Библиотеку с одной простой функции вызова.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="0f8bf-122">Это приводит к рекурсивный вызов **xlAutoClose** и переполнение стека.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="0f8bf-123">Не забудьте удалить имена</span><span class="sxs-lookup"><span data-stu-id="0f8bf-123">Remember to delete names</span></span>

<span data-ttu-id="0f8bf-124">Если аргумент _pxFunctionText_ **xlfRegister**указан при регистрации функции DLL-Библиотеку и команды, необходимо явно удалить имена путем вызова **xlfSetName** для каждого из них, пропуск второй аргумент, чтобы функция больше не отображается в Мастер функций.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="0f8bf-125">Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="0f8bf-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0f8bf-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0f8bf-126">See also</span></span>

- [<span data-ttu-id="0f8bf-127">xlfRegister (����� 1)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="0f8bf-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="0f8bf-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="0f8bf-129">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="0f8bf-130">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="0f8bf-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

