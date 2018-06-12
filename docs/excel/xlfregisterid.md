---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- функция xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807363"
---
# <a name="xlfregisterid"></a><span data-ttu-id="361bb-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="361bb-104">xlfRegisterId</span></span>

<span data-ttu-id="361bb-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="361bb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="361bb-106">Может быть вызван из библиотеки DLL, которая был вызван с Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="361bb-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="361bb-107">Если функция уже зарегистрирован, она возвращает идентификатор регистрации для этой функции без повторная регистрация его.</span><span class="sxs-lookup"><span data-stu-id="361bb-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="361bb-108">Если функция не зарегистрирован, он регистрирует его и возвращает итоговый код регистра.</span><span class="sxs-lookup"><span data-stu-id="361bb-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="361bb-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="361bb-109">Parameters</span></span>

<span data-ttu-id="361bb-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="361bb-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="361bb-111">Имя DLL, содержащей функцию.</span><span class="sxs-lookup"><span data-stu-id="361bb-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="361bb-112">_pxProcedure_ (**xltypeStr** или **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="361bb-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="361bb-113">Если строка, имя вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="361bb-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="361bb-114">Если номер, порядковый номер экспорта число вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="361bb-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="361bb-115">Для ясности и надежности всегда используйте форму строки.</span><span class="sxs-lookup"><span data-stu-id="361bb-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="361bb-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="361bb-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="361bb-117">Необязательный атрибут типа string, указав типов всех аргументов в функцию и типа возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="361bb-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="361bb-118">Дополнительные сведения см в разделе «Примечания».</span><span class="sxs-lookup"><span data-stu-id="361bb-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="361bb-119">Этот аргумент можно опустить, для изолированной DLL (XLL) определение **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="361bb-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="361bb-120">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="361bb-120">Property value/Return value</span></span>

<span data-ttu-id="361bb-121">Возвращает идентификатор регистрации функции (**xltypeNum**), который можно использовать в последующих вызовов **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="361bb-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="361bb-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="361bb-122">Remarks</span></span>

<span data-ttu-id="361bb-123">Эта функция полезна, когда требуется заниматься обслуживание кодом реестра, но необходимо одно более поздней версии для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="361bb-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="361bb-124">Также полезно для назначения для меню, средств и кнопки при функцию, которую необходимо назначить в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="361bb-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="361bb-125">Где зарегистрировала функции DLL или XLL с аргументом допустимый _pxFunctionText_ указан в **xlfRegister**Идентификатору register также можно получить, передав _pxFunctionText_ функция **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="361bb-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="361bb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="361bb-126">See also</span></span>

- [<span data-ttu-id="361bb-127">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="361bb-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="361bb-128">ОТМЕНА РЕГИСТРАЦИИ</span><span class="sxs-lookup"><span data-stu-id="361bb-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="361bb-129">Функции API XLM важные и полезные C</span><span class="sxs-lookup"><span data-stu-id="361bb-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

