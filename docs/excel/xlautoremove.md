---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- функция xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807351"
---
# <a name="xlautoremove"></a><span data-ttu-id="43f64-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="43f64-104">xlAutoRemove</span></span>

 <span data-ttu-id="43f64-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43f64-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43f64-106">Вызывается с Microsoft Excel, если пользователь деактивирует XLL во время сеанса обмена Excel с помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="43f64-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="43f64-107">Эта функция не вызывается при сеанс Excel закрывается, обычно или аварийно, с установленной надстройкой.</span><span class="sxs-lookup"><span data-stu-id="43f64-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="43f64-108">Эта функция используется для отображения настраиваемого диалогового окна о том, что надстройка отключен, чтение или запись в реестр, например.</span><span class="sxs-lookup"><span data-stu-id="43f64-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="43f64-109">Excel не требуется XLL внедрение и экспорт этой функции.</span><span class="sxs-lookup"><span data-stu-id="43f64-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="43f64-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43f64-110">Parameters</span></span>

<span data-ttu-id="43f64-111">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="43f64-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="43f64-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43f64-112">Property value/Return value</span></span>

<span data-ttu-id="43f64-113">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="43f64-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43f64-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="43f64-114">Remarks</span></span>

<span data-ttu-id="43f64-115">Эта функция вашей XLL должны быть выполнены все задачи при удалении с диспетчер надстроек.</span><span class="sxs-lookup"><span data-stu-id="43f64-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="43f64-116">Пример</span><span class="sxs-lookup"><span data-stu-id="43f64-116">Example</span></span>

<span data-ttu-id="43f64-117">В файлах `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции.</span><span class="sxs-lookup"><span data-stu-id="43f64-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="43f64-118">Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="43f64-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="43f64-119">См. также</span><span class="sxs-lookup"><span data-stu-id="43f64-119">See also</span></span>



[<span data-ttu-id="43f64-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="43f64-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="43f64-121">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="43f64-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

