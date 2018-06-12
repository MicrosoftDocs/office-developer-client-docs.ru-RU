---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- функция xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807354"
---
# <a name="xlautoclose"></a><span data-ttu-id="e0d80-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="e0d80-104">xlAutoClose</span></span>

 <span data-ttu-id="e0d80-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0d80-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e0d80-106">При отключении XLL вызывается Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e0d80-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="e0d80-107">Надстройка отключается при завершении сеанса Excel обычно.</span><span class="sxs-lookup"><span data-stu-id="e0d80-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="e0d80-108">Надстройка может быть отключена пользователем во время сеанса обмена Excel, и эта функция будет вызываться в этом случае.</span><span class="sxs-lookup"><span data-stu-id="e0d80-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="e0d80-109">Excel не требуется XLL внедрение и экспорт этой функции, хотя рекомендуется, чтобы вашей XLL можно отменить регистрацию функций и команд, освобождения ресурсов, отменить настроек и т.д.</span><span class="sxs-lookup"><span data-stu-id="e0d80-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="e0d80-110">Если функции и команды не отменена явным образом, XLL, Excel выполняется после вызова функции **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="e0d80-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="e0d80-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0d80-111">Parameters</span></span>

<span data-ttu-id="e0d80-112">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="e0d80-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e0d80-113">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0d80-113">Property value/Return value</span></span>

<span data-ttu-id="e0d80-114">Реализация этой функции необходимо вернуть 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="e0d80-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0d80-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e0d80-115">Remarks</span></span>

<span data-ttu-id="e0d80-116">Excel вызывает функцию **xlAutoClose** при XLL отключена, то есть, выгружать из памяти.</span><span class="sxs-lookup"><span data-stu-id="e0d80-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="e0d80-117">XLL деактивирован в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="e0d80-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="e0d80-118">В конце обычный сеанс Excel при активной во время этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e0d80-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="e0d80-119">Если явно выгружен во время сеанса обмена Excel.</span><span class="sxs-lookup"><span data-stu-id="e0d80-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="e0d80-120">XLL-модуль можно выгрузить несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="e0d80-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="e0d80-121">Использование диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="e0d80-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="e0d80-122">Из другой XLL, который вызывает [xlfUnregister](xlfunregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="e0d80-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="e0d80-123">Из таблицы макросов XLM, который вызывает [Отменить РЕГИСТРАЦИЮ](xlfunregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="e0d80-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="e0d80-124">Эта функция должна выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="e0d80-124">This function should do the following:</span></span>
  
- <span data-ttu-id="e0d80-125">Удалите все меню и пунктов меню, которые были добавлены, XLL.</span><span class="sxs-lookup"><span data-stu-id="e0d80-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="e0d80-126">Выполните необходимую очистку глобальные.</span><span class="sxs-lookup"><span data-stu-id="e0d80-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="e0d80-127">Удалите имена, которые были созданы, особенно имена экспортированных функций.</span><span class="sxs-lookup"><span data-stu-id="e0d80-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="e0d80-128">Имейте в виду, что регистрация функций может стать причиной некоторые имена, чтобы создать, если присутствует аргумент четвертая для **регистрации** .</span><span class="sxs-lookup"><span data-stu-id="e0d80-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="e0d80-129">Пример</span><span class="sxs-lookup"><span data-stu-id="e0d80-129">Example</span></span>

<span data-ttu-id="e0d80-130">Файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C` для примера реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="e0d80-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="e0d80-131">Следующий код является из `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="e0d80-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="e0d80-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e0d80-132">See also</span></span>



[<span data-ttu-id="e0d80-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="e0d80-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="e0d80-134">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="e0d80-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

