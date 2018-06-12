---
title: xlfUnregister (формы 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- функция xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807358"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="df7db-104">xlfUnregister (формы 1)</span><span class="sxs-lookup"><span data-stu-id="df7db-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="df7db-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="df7db-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="df7db-106">Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="df7db-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="df7db-107">Это эквивалентно вызову **Отменить РЕГИСТРАЦИЮ** из таблицы Excel XLM макрос.</span><span class="sxs-lookup"><span data-stu-id="df7db-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="df7db-108">**xlfUnregister** может быть вызван в двух вариантах:</span><span class="sxs-lookup"><span data-stu-id="df7db-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="df7db-109">Форма 1: Отменяет отдельные команды или функции.</span><span class="sxs-lookup"><span data-stu-id="df7db-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="df7db-110">Форма 2: Выгрузка и деактивирует надстройке XLL.</span><span class="sxs-lookup"><span data-stu-id="df7db-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="df7db-111">Вызывает в виде 1, эта функция уменьшает число использования функции DLL или команды, которое ранее было зарегистрировано с помощью **xlfRegister** или **регистрации**.</span><span class="sxs-lookup"><span data-stu-id="df7db-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="df7db-112">Если счетчик использования уже равно нулю, эта функция не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="df7db-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="df7db-113">По достижении нулевой счетчик использования всех функций в библиотеке DLL библиотеки DLL выгрузки из памяти.</span><span class="sxs-lookup"><span data-stu-id="df7db-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="df7db-114">**xlfRegister** (Форма 1) также определяет скрытые имя которого является аргумента функции текст, _pxFunctionText_и которая вычисляет функцию или идентификатор команды регистрации.</span><span class="sxs-lookup"><span data-stu-id="df7db-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="df7db-115">После отмены регистрации функцию, это имя следует удалить с помощью **xlfSetName** , чтобы с помощью мастера функций, больше не отображается имя функции.</span><span class="sxs-lookup"><span data-stu-id="df7db-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="df7db-116">Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="df7db-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="df7db-117">Parameters</span><span class="sxs-lookup"><span data-stu-id="df7db-117">Parameters</span></span>

<span data-ttu-id="df7db-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="df7db-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="df7db-119">КОД регистрации функции для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="df7db-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="df7db-120">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df7db-120">Property value/Return value</span></span>

<span data-ttu-id="df7db-121">В случае успеха возвращает **значение TRUE** (**xltypeBool**), в противном случае возвращается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="df7db-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df7db-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="df7db-122">Remarks</span></span>

<span data-ttu-id="df7db-123">Зарегистрированные регистрации, код функции, возвращаемый **xlfRegister** при первом выполнении функции.</span><span class="sxs-lookup"><span data-stu-id="df7db-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="df7db-124">Он также можно получить путем вызова [функции xlfRegisterId](xlfregisterid.md) или [xlfEvaluate функции](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="df7db-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="df7db-125">Обратите внимание, что этот xlfRegisterId пытается зарегистрировать функцию, если он еще не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="df7db-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="df7db-126">По этой причине если только вы пытаетесь получить идентификатор, поэтому можно отменить регистрацию функцию, лучше его можно получить, передав зарегистрированное имя **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="df7db-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="df7db-127">Если функция не зарегистрирована, **xlfEvaluate** происходит сбой с #NAME? Ошибка.</span><span class="sxs-lookup"><span data-stu-id="df7db-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="df7db-128">Пример</span><span class="sxs-lookup"><span data-stu-id="df7db-128">Example</span></span>

<span data-ttu-id="df7db-129">Просмотр кода для функции **fExit** в `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="df7db-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="df7db-130">См. также</span><span class="sxs-lookup"><span data-stu-id="df7db-130">See also</span></span>

- [<span data-ttu-id="df7db-131">xlfRegister (����� 1)</span><span class="sxs-lookup"><span data-stu-id="df7db-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="df7db-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="df7db-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="df7db-133">xlfUnregister (формы 2)</span><span class="sxs-lookup"><span data-stu-id="df7db-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="df7db-134">Функции API XLM важные и полезные C</span><span class="sxs-lookup"><span data-stu-id="df7db-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

