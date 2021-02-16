---
title: xlfUnregister (форма 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Функция xlfunregister [excel 2007]
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
# <a name="xlfunregister-form-1"></a><span data-ttu-id="6786b-104">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="6786b-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="6786b-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6786b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6786b-106">Может быть вызван из команды DLL или XLL, которая сама была вызвана Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6786b-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="6786b-107">Это эквивалентно вызову **UNREGISTER** из листа макроса XLM Excel.</span><span class="sxs-lookup"><span data-stu-id="6786b-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="6786b-108">**XlfUnregister** может быть вызван в двух формах:</span><span class="sxs-lookup"><span data-stu-id="6786b-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="6786b-109">Форма 1. Unregisters an individual command or function.</span><span class="sxs-lookup"><span data-stu-id="6786b-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="6786b-110">Форма 2. Выгружает и деактивирует XLL.</span><span class="sxs-lookup"><span data-stu-id="6786b-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="6786b-111">Эта функция, вызванная в форме 1, уменьшает количество использования функции DLL или команды, которая ранее была зарегистрирована с помощью **xlfRegister** или **REGISTER.**</span><span class="sxs-lookup"><span data-stu-id="6786b-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="6786b-112">Если количество использования уже нулевое, эта функция не действует.</span><span class="sxs-lookup"><span data-stu-id="6786b-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="6786b-113">Когда количество использования всех функций в DLL достигает нуля, DLL выгружается из памяти.</span><span class="sxs-lookup"><span data-stu-id="6786b-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="6786b-114">**XlfRegister** (форма 1) также определяет скрытое имя, которое является текстовым аргументом функции  _pxFunctionText_ и оценивается как регистрационный ИД функции или команды.</span><span class="sxs-lookup"><span data-stu-id="6786b-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="6786b-115">При отостановке регистрации функции это имя следует удалить с помощью **xlfSetName,** чтобы имя функции больше не было указано мастером функций.</span><span class="sxs-lookup"><span data-stu-id="6786b-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="6786b-116">Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="6786b-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="6786b-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="6786b-117">Parameters</span></span>

<span data-ttu-id="6786b-118">_pxRegisterId_ (**xltypeNum)**</span><span class="sxs-lookup"><span data-stu-id="6786b-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="6786b-119">ИД регистрации функции, которая должна быть отрегистрирована.</span><span class="sxs-lookup"><span data-stu-id="6786b-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6786b-120">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6786b-120">Property value/Return value</span></span>

<span data-ttu-id="6786b-121">В случае успеха **возвращается TRUE** (**xltypeBool),** в противном случае возвращается FALSE.</span><span class="sxs-lookup"><span data-stu-id="6786b-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6786b-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="6786b-122">Remarks</span></span>

<span data-ttu-id="6786b-123">ИД регистрации функции **возвращается xlfRegister** при первой регистрации функции.</span><span class="sxs-lookup"><span data-stu-id="6786b-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="6786b-124">Его также можно получить, вызывая [функцию xlfRegisterId](xlfregisterid.md) или [функцию xlfEvaluate.](xlfevaluate.md)</span><span class="sxs-lookup"><span data-stu-id="6786b-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="6786b-125">Обратите внимание, что xlfRegisterId пытается зарегистрировать функцию, если она еще не зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="6786b-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="6786b-126">По этой причине, если вы пытаетесь получить только ИД, чтобы отозарегистрировать функцию, лучше получить ее, передав зарегистрированное имя **в xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="6786b-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="6786b-127">Если функция не зарегистрирована, **xlfEvaluate** не работает с #NAME? error.</span><span class="sxs-lookup"><span data-stu-id="6786b-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6786b-128">Пример</span><span class="sxs-lookup"><span data-stu-id="6786b-128">Example</span></span>

<span data-ttu-id="6786b-129">См. код **функции fExit** в  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="6786b-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="6786b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6786b-130">See also</span></span>

- [<span data-ttu-id="6786b-131">xlfRegister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="6786b-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="6786b-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="6786b-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="6786b-133">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="6786b-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="6786b-134">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="6786b-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

