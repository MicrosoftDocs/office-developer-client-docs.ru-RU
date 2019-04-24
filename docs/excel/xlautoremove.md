---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Функция кслауторемове [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310285"
---
# <a name="xlautoremove"></a><span data-ttu-id="9af02-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="9af02-104">xlAutoRemove</span></span>

 <span data-ttu-id="9af02-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9af02-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9af02-106">Вызывается Microsoft Excel, когда пользователь отключает XLL во время сеанса Excel с помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="9af02-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="9af02-107">Вызов этой функции не выполняется, если сеанс Excel закрывается (правильно или ненормально) при установленной надстройке.</span><span class="sxs-lookup"><span data-stu-id="9af02-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="9af02-108">Эта функция может использоваться для отображения настраиваемого диалогового окна, указывающего на то, что надстройка была отключена, а также для чтения или записи в реестре, например.</span><span class="sxs-lookup"><span data-stu-id="9af02-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="9af02-109">Для реализации и экспорта этой функции в Excel не требуется XLL.</span><span class="sxs-lookup"><span data-stu-id="9af02-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="9af02-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9af02-110">Parameters</span></span>

<span data-ttu-id="9af02-111">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="9af02-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9af02-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9af02-112">Property value/Return value</span></span>

<span data-ttu-id="9af02-113">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="9af02-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9af02-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9af02-114">Remarks</span></span>

<span data-ttu-id="9af02-115">Используйте эту функцию, если XLL-модуль должен выполнить любую задачу, когда она удалена с помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="9af02-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="9af02-116">Пример</span><span class="sxs-lookup"><span data-stu-id="9af02-116">Example</span></span>

<span data-ttu-id="9af02-117">В файлах `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции.</span><span class="sxs-lookup"><span data-stu-id="9af02-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="9af02-118">Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="9af02-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9af02-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9af02-119">See also</span></span>



[<span data-ttu-id="9af02-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="9af02-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="9af02-121">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="9af02-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

