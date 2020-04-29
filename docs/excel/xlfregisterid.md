---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- Функция кслфрегистерид [Excel 2007]
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
# <a name="xlfregisterid"></a><span data-ttu-id="99378-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="99378-104">xlfRegisterId</span></span>

<span data-ttu-id="99378-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="99378-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="99378-106">Может вызываться из библиотеки DLL, которая вызывается Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="99378-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="99378-107">Если функция уже зарегистрирована, она возвращает существующий идентификатор регистра для этой функции без его повторной регистрации.</span><span class="sxs-lookup"><span data-stu-id="99378-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="99378-108">Если функция еще не зарегистрирована, она регистрирует ее и возвращает результирующий идентификатор регистра.</span><span class="sxs-lookup"><span data-stu-id="99378-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="99378-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99378-109">Parameters</span></span>

<span data-ttu-id="99378-110">_пксмодулетекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="99378-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="99378-111">Имя библиотеки DLL, содержащей функцию.</span><span class="sxs-lookup"><span data-stu-id="99378-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="99378-112">_пкспроцедуре_ (**кслтипестр** или **кслтипенум**)</span><span class="sxs-lookup"><span data-stu-id="99378-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="99378-113">Если строка — имя вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="99378-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="99378-114">Если число, порядковый номер экспорта вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="99378-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="99378-115">Для ясности и надежности всегда используйте форму String.</span><span class="sxs-lookup"><span data-stu-id="99378-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="99378-116">_пкстипетекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="99378-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="99378-117">Необязательная строка, указывающая типы всех аргументов функции и тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="99378-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="99378-118">Для получения дополнительных сведений см раздел "Примечания".</span><span class="sxs-lookup"><span data-stu-id="99378-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="99378-119">Этот аргумент можно опустить для отдельной библиотеки DLL (XLL), определяющей **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="99378-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="99378-120">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99378-120">Property value/Return value</span></span>

<span data-ttu-id="99378-121">Возвращает идентификатор регистра функции (**кслтипенум**), который можно использовать в последующих вызовах **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="99378-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99378-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="99378-122">Remarks</span></span>

<span data-ttu-id="99378-123">Эта функция полезна, если вы не хотите беспокоиться об управлении ИДЕНТИФИКАТОРом регистра, но вам потребуется еще один позже для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="99378-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="99378-124">Он также полезен для назначения меню, инструментов и кнопок, когда функция, которую необходимо назначить, находится в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="99378-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="99378-125">Если функция DLL или XLL зарегистрирована с допустимым аргументом _пксфунктионтекст_ , который был предоставлен в **XLFREGISTER**, его идентификатор регистрации также можно получить, передав _пксфунктионтекст_ в функцию **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="99378-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99378-126">См. также</span><span class="sxs-lookup"><span data-stu-id="99378-126">See also</span></span>

- [<span data-ttu-id="99378-127">РЕГИСТРАЦИЯ</span><span class="sxs-lookup"><span data-stu-id="99378-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="99378-128">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="99378-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="99378-129">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="99378-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

