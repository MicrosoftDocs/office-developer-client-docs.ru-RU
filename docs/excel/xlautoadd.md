---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413761"
---
# <a name="xlautoadd"></a><span data-ttu-id="4affa-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="4affa-104">xlAutoAdd</span></span>

 <span data-ttu-id="4affa-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4affa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4affa-106">Добавлено Microsoft Excel, когда пользователь активирует XLL во время сеанса Excel с помощью Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="4affa-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="4affa-107">Эта функция не называется, Excel запускается и загружает предварительно установленную надстройку.</span><span class="sxs-lookup"><span data-stu-id="4affa-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="4affa-108">Эта функция может использоваться для отображения настраиваемого диалогового окна, которое сообщает пользователю о том, что надстройка активирована, или для чтения или записи в реестр или проверки сведений о лицензировании, например.</span><span class="sxs-lookup"><span data-stu-id="4affa-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="4affa-109">Excel XLL не требуется для реализации и экспорта этой функции.</span><span class="sxs-lookup"><span data-stu-id="4affa-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="4affa-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4affa-110">Parameters</span></span>

<span data-ttu-id="4affa-111">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="4affa-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4affa-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4affa-112">Property value/Return value</span></span>

<span data-ttu-id="4affa-113">Реализация этой функции должна возвращать 1.</span><span class="sxs-lookup"><span data-stu-id="4affa-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="4affa-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="4affa-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4affa-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="4affa-115">Remarks</span></span>

<span data-ttu-id="4affa-116">Используйте эту функцию, если XLL должен что-либо сделать, если он добавлен Add-In Manager.</span><span class="sxs-lookup"><span data-stu-id="4affa-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="4affa-117">Пример</span><span class="sxs-lookup"><span data-stu-id="4affa-117">Example</span></span>

<span data-ttu-id="4affa-118">См.  `\SAMPLES\EXAMPLE\EXAMPLE.C`  `\SAMPLES\GENERIC\GENERIC.C` и, например, реализацию этой функции.</span><span class="sxs-lookup"><span data-stu-id="4affa-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="4affa-119">Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="4affa-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4affa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4affa-120">See also</span></span>



[<span data-ttu-id="4affa-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="4affa-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="4affa-122">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="4affa-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

