---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- функция xlfregisterid [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420061"
---
# <a name="xlfregisterid"></a><span data-ttu-id="19c78-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="19c78-104">xlfRegisterId</span></span>

<span data-ttu-id="19c78-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19c78-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19c78-106">Может быть вызвано из DLL, которое само по себе было вызвано Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="19c78-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="19c78-107">Если функция уже зарегистрирована, она возвращает существующий ID реестра для этой функции без ее перерегистрации.</span><span class="sxs-lookup"><span data-stu-id="19c78-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="19c78-108">Если функция еще не зарегистрирована, она регистрирует ее и возвращает итоговую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="19c78-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="19c78-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="19c78-109">Parameters</span></span>

<span data-ttu-id="19c78-110">_pxModuleText_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="19c78-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="19c78-111">Имя DLL, содержащего функцию.</span><span class="sxs-lookup"><span data-stu-id="19c78-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="19c78-112">_pxProcedure_ **(xltypeStr** или **xltypeNum)**</span><span class="sxs-lookup"><span data-stu-id="19c78-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="19c78-113">Если строка, имя вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="19c78-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="19c78-114">Если номер, ordinal export number of the function to call.</span><span class="sxs-lookup"><span data-stu-id="19c78-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="19c78-115">Для ясности и надежности всегда используйте строковую форму.</span><span class="sxs-lookup"><span data-stu-id="19c78-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="19c78-116">_pxTypeText_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="19c78-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="19c78-117">Необязательная строка, указывая типы всех аргументов для функции и тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="19c78-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="19c78-118">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="19c78-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="19c78-119">Этот аргумент может быть опущен для отдельной DLL (XLL), определяющей **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="19c78-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="19c78-120">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19c78-120">Property value/Return value</span></span>

<span data-ttu-id="19c78-121">Возвращает зарегистрированный ID функции **(xltypeNum),** который можно использовать в последующих вызовах **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="19c78-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19c78-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="19c78-122">Remarks</span></span>

<span data-ttu-id="19c78-123">Эта функция полезна, если вы не хотите беспокоиться о сохранении регистрации, но вам потребуется один позже для незарегистрации.</span><span class="sxs-lookup"><span data-stu-id="19c78-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="19c78-124">Это также полезно для назначения меню, инструментов и кнопок, когда функции, которые вы хотите назначить, находится в DLL.</span><span class="sxs-lookup"><span data-stu-id="19c78-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="19c78-125">Если функция DLL или XLL была зарегистрирована с допустимым аргументом  _pxFunctionText,_ предоставленным **xlfRegister,** его удостоверение регистра также можно получить, передав  _pxFunctionText_ функции **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="19c78-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19c78-126">См. также</span><span class="sxs-lookup"><span data-stu-id="19c78-126">See also</span></span>

- [<span data-ttu-id="19c78-127">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="19c78-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="19c78-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="19c78-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="19c78-129">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="19c78-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

