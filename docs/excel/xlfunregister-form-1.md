---
title: xlfUnregister (форма 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Функция xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410086"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="001d6-104">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="001d6-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="001d6-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="001d6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="001d6-106">Может вызываться из команды DLL или XLL, которая вызывается Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="001d6-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="001d6-107">Это эквивалентно вызову **Unregister** из листа макросов Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="001d6-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="001d6-108">**xlfUnregister** можно вызывать в двух формах:</span><span class="sxs-lookup"><span data-stu-id="001d6-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="001d6-109">Форма 1: Отмена регистрации отдельной команды или функции.</span><span class="sxs-lookup"><span data-stu-id="001d6-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="001d6-110">Форма 2: выгрузка и деактивация XLL.</span><span class="sxs-lookup"><span data-stu-id="001d6-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="001d6-111">Эта функция уменьшает количество использований функции или команды DLL, которые были зарегистрированы с помощью **xlfRegister** или **Register**, в форме 1.</span><span class="sxs-lookup"><span data-stu-id="001d6-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="001d6-112">Если число использований уже равно нулю, эта функция не оказывает никакого действия.</span><span class="sxs-lookup"><span data-stu-id="001d6-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="001d6-113">Если счетчик использования всех функций в библиотеке DLL достигает нуля, Библиотека DLL выгружается из памяти.</span><span class="sxs-lookup"><span data-stu-id="001d6-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="001d6-114">**xlfRegister** (Форма 1) также определяет скрытое имя, которое представляет собой аргумент text функции, _пксфунктионтекст_, и который определяет идентификатор регистрации функции или команды.</span><span class="sxs-lookup"><span data-stu-id="001d6-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="001d6-115">При отмене регистрации функции это имя должно быть удалено с помощью **xlfSetName** , чтобы имя функции больше не переЧислено мастером функций.</span><span class="sxs-lookup"><span data-stu-id="001d6-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="001d6-116">Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="001d6-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="001d6-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="001d6-117">Parameters</span></span>

<span data-ttu-id="001d6-118">_пксрегистерид_ (**кслтипенум**)</span><span class="sxs-lookup"><span data-stu-id="001d6-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="001d6-119">ИДЕНТИФИКАТОР регистрации функции, которая будет отменена.</span><span class="sxs-lookup"><span data-stu-id="001d6-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="001d6-120">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="001d6-120">Property value/Return value</span></span>

<span data-ttu-id="001d6-121">В случае успеха возвращает **значение true** (**кслтипебул**), в противном случае возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="001d6-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="001d6-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="001d6-122">Remarks</span></span>

<span data-ttu-id="001d6-123">ИДЕНТИФИКАТОР регистрации функции возвращается **xlfRegister** при первой регистрации функции.</span><span class="sxs-lookup"><span data-stu-id="001d6-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="001d6-124">Его также можно получить, вызвав [функцию кслфрегистерид](xlfregisterid.md) или [функцию xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="001d6-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="001d6-125">Обратите внимание, что Кслфрегистерид пытается зарегистрировать функцию, если она еще не зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="001d6-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="001d6-126">По этой причине, если вы пытаетесь получить идентификатор только для того, чтобы можно было отменить регистрацию функции, ее лучше получить, передав зарегистрированное имя в **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="001d6-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="001d6-127">Если функция не была зарегистрирована, **xlfEvaluate** завершается с ошибкой #NAME? ошибкой.</span><span class="sxs-lookup"><span data-stu-id="001d6-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="001d6-128">Пример</span><span class="sxs-lookup"><span data-stu-id="001d6-128">Example</span></span>

<span data-ttu-id="001d6-129">Обратитесь к коду функции **фексит** в `\SAMPLES\GENERIC\GENERIC.C`файле.</span><span class="sxs-lookup"><span data-stu-id="001d6-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="001d6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="001d6-130">See also</span></span>

- [<span data-ttu-id="001d6-131">xlfRegister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="001d6-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="001d6-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="001d6-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="001d6-133">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="001d6-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="001d6-134">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="001d6-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

