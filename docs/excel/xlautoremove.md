---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- функция xlautoremove [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425479"
---
# <a name="xlautoremove"></a><span data-ttu-id="43e09-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="43e09-104">xlAutoRemove</span></span>

 <span data-ttu-id="43e09-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43e09-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43e09-106">Вызвано Microsoft Excel, когда пользователь отключает XLL во время сеанса Excel с помощью Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="43e09-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="43e09-107">Вызов этой функции не выполняется, если сеанс Excel закрывается (правильно или ненормально) при установленной надстройке.</span><span class="sxs-lookup"><span data-stu-id="43e09-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="43e09-108">Эта функция может использоваться для отображения настраиваемого диалоговое окно, в которое пользователь сообщает, что надстройка отключена, или, например, для чтения или записи в реестр.</span><span class="sxs-lookup"><span data-stu-id="43e09-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="43e09-109">Excel XLL не требуется для реализации и экспорта этой функции.</span><span class="sxs-lookup"><span data-stu-id="43e09-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="43e09-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43e09-110">Parameters</span></span>

<span data-ttu-id="43e09-111">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="43e09-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="43e09-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43e09-112">Property value/Return value</span></span>

<span data-ttu-id="43e09-113">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="43e09-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43e09-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="43e09-114">Remarks</span></span>

<span data-ttu-id="43e09-115">Используйте эту функцию, если XLL необходимо выполнить любую задачу, если она удалена Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="43e09-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="43e09-116">Пример</span><span class="sxs-lookup"><span data-stu-id="43e09-116">Example</span></span>

<span data-ttu-id="43e09-117">В файлах `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции.</span><span class="sxs-lookup"><span data-stu-id="43e09-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="43e09-118">Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="43e09-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="43e09-119">См. также</span><span class="sxs-lookup"><span data-stu-id="43e09-119">See also</span></span>



[<span data-ttu-id="43e09-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="43e09-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="43e09-121">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="43e09-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

