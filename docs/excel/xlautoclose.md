---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- функция xlautoclose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807354"
---
# <a name="xlautoclose"></a><span data-ttu-id="a4a68-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="a4a68-104">xlAutoClose</span></span>

 <span data-ttu-id="a4a68-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a4a68-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a4a68-106">Вызывается приложением Microsoft Excel при каждом отключении XLL.</span><span class="sxs-lookup"><span data-stu-id="a4a68-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="a4a68-107">Надстройка отключается после нормального завершения сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a68-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="a4a68-108">Надстройку может отключить пользователь во время сеанса Excel, что также потянет за собой вызов этой функции.</span><span class="sxs-lookup"><span data-stu-id="a4a68-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="a4a68-109">Для внедрения и экспорта этой функции в приложении Excel надстройка XLL не обязательна, но рекомендована: с помощью XLL можно отключать функции и команды, освобождать ресурсы, отменять настройки и т. д.</span><span class="sxs-lookup"><span data-stu-id="a4a68-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="a4a68-110">Если надстройка XLL не отключает функции и команды явным образом, это делает Excel после вызова функции **xlAutoClose**.</span><span class="sxs-lookup"><span data-stu-id="a4a68-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="a4a68-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4a68-111">Parameters</span></span>

<span data-ttu-id="a4a68-112">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="a4a68-112">This function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a4a68-113">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4a68-113">Property value/Return value</span></span>

<span data-ttu-id="a4a68-114">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="a4a68-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4a68-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4a68-115">Remarks</span></span>

<span data-ttu-id="a4a68-116">Excel вызывает функцию **xlAutoClose** каждый раз, когда надстройка XLL отключается (то есть выгружается из памяти).</span><span class="sxs-lookup"><span data-stu-id="a4a68-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="a4a68-117">Надстройка XLL отключается в перечисленных ниже ситуациях:</span><span class="sxs-lookup"><span data-stu-id="a4a68-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="a4a68-118">При нормальном завершении сеанса Excel, во время которого она была активна.</span><span class="sxs-lookup"><span data-stu-id="a4a68-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="a4a68-119">Если она была явным образом выгружена из памяти во время сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a68-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="a4a68-120">XLL может выгружаться несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="a4a68-120">An XLOPER/XLOPER12 can be created in several ways:</span></span>
    
- <span data-ttu-id="a4a68-121">С помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="a4a68-121">Using the Add-In Manager</span></span>
    
- <span data-ttu-id="a4a68-122">Из другой надстройки XLL, которая вызывает [xlfUnregister](xlfunregister-form-1.md), указывая имя этой библиотеки DLL в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="a4a68-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="a4a68-123">Из макроса XLM, который вызывает [UNREGISTER](xlfunregister-form-1.md), указывая имя этой библиотеки DLL в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="a4a68-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="a4a68-124">Эта функция должна выполнять следующее:</span><span class="sxs-lookup"><span data-stu-id="a4a68-124">This function should do the following:</span></span>
  
- <span data-ttu-id="a4a68-125">Удалять меню или элементы меню, которые были добавлены надстройкой XLL.</span><span class="sxs-lookup"><span data-stu-id="a4a68-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="a4a68-126">В случае надобности выполнять любую глобальную очистку.</span><span class="sxs-lookup"><span data-stu-id="a4a68-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="a4a68-127">Удалять какие-либо созданные имена, в частности имена экспортированных функций.</span><span class="sxs-lookup"><span data-stu-id="a4a68-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="a4a68-128">Помните, что регистрация функций может привести к созданию некоторых имен, если присутствует четвертый аргумент для **РЕГИСТРАЦИИ**.</span><span class="sxs-lookup"><span data-stu-id="a4a68-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="a4a68-129">Пример</span><span class="sxs-lookup"><span data-stu-id="a4a68-129">Example</span></span>

<span data-ttu-id="a4a68-130">В файлах `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции.</span><span class="sxs-lookup"><span data-stu-id="a4a68-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="a4a68-131">Следующий код — из файла `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="a4a68-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a4a68-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a4a68-132">See also</span></span>



[<span data-ttu-id="a4a68-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="a4a68-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="a4a68-134">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="a4a68-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

