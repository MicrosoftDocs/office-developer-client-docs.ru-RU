---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406649"
---
# <a name="xlautoopen"></a><span data-ttu-id="ad387-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="ad387-104">xlAutoOpen</span></span>

 <span data-ttu-id="ad387-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad387-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ad387-106">Функция обратного вызова, которая должна быть реализована и экспортирована каждым действительным XLL.</span><span class="sxs-lookup"><span data-stu-id="ad387-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="ad387-107">Функция **xlAutoOpen** рекомендуется использовать для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и т. д.</span><span class="sxs-lookup"><span data-stu-id="ad387-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="ad387-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad387-108">Parameters</span></span>

<span data-ttu-id="ad387-109">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="ad387-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ad387-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad387-110">Property value/Return value</span></span>

<span data-ttu-id="ad387-111">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="ad387-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad387-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad387-112">Remarks</span></span>

<span data-ttu-id="ad387-113">Microsoft Excel вызывает **xlAutoOpen** всякий раз при активации XLL.</span><span class="sxs-lookup"><span data-stu-id="ad387-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="ad387-114">XLL-модуль активируется в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="ad387-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="ad387-115">В начале сеанса Excel, если он был активен в последнем сеансе Excel, который нормально завершил работу.</span><span class="sxs-lookup"><span data-stu-id="ad387-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="ad387-116">При загрузке во время сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="ad387-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="ad387-117">XLL можно загрузить несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="ad387-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="ad387-118">Выбрав команду **Открыть** в меню **файл** (где версия Excel поддерживает этот метод загрузки XLL-модулей).</span><span class="sxs-lookup"><span data-stu-id="ad387-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="ad387-119">С помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="ad387-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="ad387-120">Из другого XLL, который вызывает [xlfRegister](xlfregister-form-1.md) с именем этой библиотеки DLL в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="ad387-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="ad387-121">На листе макросов XLM, который вызывает [Register](xlfregister-form-1.md) с именем этой библиотеки DLL в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="ad387-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="ad387-122">Если надстройка отключена и повторно активирована во время сеанса Excel, эта функция вызывается при повторной активации.</span><span class="sxs-lookup"><span data-stu-id="ad387-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="ad387-123">Пример</span><span class="sxs-lookup"><span data-stu-id="ad387-123">Example</span></span>

<span data-ttu-id="ad387-124">Просмотрите файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C`, в частности, примеры реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="ad387-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad387-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ad387-125">See also</span></span>



[<span data-ttu-id="ad387-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="ad387-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="ad387-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="ad387-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="ad387-128">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="ad387-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

