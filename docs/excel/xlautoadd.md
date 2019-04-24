---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- Функция кслаутоадд [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303993"
---
# <a name="xlautoadd"></a><span data-ttu-id="30ee6-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="30ee6-104">xlAutoAdd</span></span>

 <span data-ttu-id="30ee6-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30ee6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="30ee6-106">Добавляется Microsoft Excel, когда пользователь активирует XLL во время сеанса Excel с помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="30ee6-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="30ee6-107">Эта функция не вызывается при запуске Excel и загрузке предварительно установленной надстройки.</span><span class="sxs-lookup"><span data-stu-id="30ee6-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="30ee6-108">Эту функцию можно использовать для отображения настраиваемого диалогового окна, которое сообщает пользователю, что надстройка активирована, а также для чтения или записи в реестр или для проверки сведений о лицензировании, например.</span><span class="sxs-lookup"><span data-stu-id="30ee6-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="30ee6-109">Для реализации и экспорта этой функции в Excel не требуется XLL.</span><span class="sxs-lookup"><span data-stu-id="30ee6-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="30ee6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="30ee6-110">Parameters</span></span>

<span data-ttu-id="30ee6-111">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="30ee6-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="30ee6-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30ee6-112">Property value/Return value</span></span>

<span data-ttu-id="30ee6-113">Ваша реализация этой функции должна вернуть 1.</span><span class="sxs-lookup"><span data-stu-id="30ee6-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="30ee6-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="30ee6-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30ee6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="30ee6-115">Remarks</span></span>

<span data-ttu-id="30ee6-116">Используйте эту функцию, если у вас есть все, что нужно сделать для XLL, когда она добавляется с помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="30ee6-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="30ee6-117">Пример</span><span class="sxs-lookup"><span data-stu-id="30ee6-117">Example</span></span>

<span data-ttu-id="30ee6-118">`\SAMPLES\GENERIC\GENERIC.C` В этой статье приведены `\SAMPLES\EXAMPLE\EXAMPLE.C` примеры реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="30ee6-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="30ee6-119">Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="30ee6-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="30ee6-120">См. также</span><span class="sxs-lookup"><span data-stu-id="30ee6-120">See also</span></span>



[<span data-ttu-id="30ee6-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="30ee6-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="30ee6-122">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="30ee6-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

