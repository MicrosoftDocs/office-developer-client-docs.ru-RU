---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- Функция xlautoopen [excel 2007]
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
# <a name="xlautoopen"></a><span data-ttu-id="598d9-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="598d9-104">xlAutoOpen</span></span>

 <span data-ttu-id="598d9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="598d9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="598d9-106">Функция callback, которую необходимо реализовать и экспортировать с помощью каждой допустимой XLL.</span><span class="sxs-lookup"><span data-stu-id="598d9-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="598d9-107">Функция **xlAutoOpen** — это рекомендуемое место для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и других функций.</span><span class="sxs-lookup"><span data-stu-id="598d9-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="598d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="598d9-108">Parameters</span></span>

<span data-ttu-id="598d9-109">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="598d9-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="598d9-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="598d9-110">Property value/Return value</span></span>

<span data-ttu-id="598d9-111">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="598d9-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="598d9-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="598d9-112">Remarks</span></span>

<span data-ttu-id="598d9-113">Microsoft Excel вызывает **xlAutoOpen** при активации XLL.</span><span class="sxs-lookup"><span data-stu-id="598d9-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="598d9-114">XLL активируется в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="598d9-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="598d9-115">В начале сеанса Excel, если он был активен в последнем сеансе Excel, который завершился нормально.</span><span class="sxs-lookup"><span data-stu-id="598d9-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="598d9-116">При загрузке во время сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="598d9-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="598d9-117">XLL можно загрузить несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="598d9-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="598d9-118">Выбрав пункт **"Открыть** в **меню "Файл"** (где версия Excel поддерживает этот метод загрузки XLL).</span><span class="sxs-lookup"><span data-stu-id="598d9-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="598d9-119">С помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="598d9-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="598d9-120">Из другой XLL, которая вызывает [xlfRegister](xlfregister-form-1.md) с именем этой DLL в качестве единственным аргументом.</span><span class="sxs-lookup"><span data-stu-id="598d9-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="598d9-121">Из листа макроса XLM, который вызывает [REGISTER](xlfregister-form-1.md) с именем этой DLL в качестве единственным аргументом.</span><span class="sxs-lookup"><span data-stu-id="598d9-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="598d9-122">Если надстройка деактивирована и активирована повторно во время сеанса Excel, эта функция будет вызвана при повторной активности.</span><span class="sxs-lookup"><span data-stu-id="598d9-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="598d9-123">Пример</span><span class="sxs-lookup"><span data-stu-id="598d9-123">Example</span></span>

<span data-ttu-id="598d9-124">См. файлы  `SAMPLES\EXAMPLE\EXAMPLE.C`  `SAMPLES\GENERIC\GENERIC.C` и примеры реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="598d9-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="598d9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="598d9-125">See also</span></span>



[<span data-ttu-id="598d9-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="598d9-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="598d9-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="598d9-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="598d9-128">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="598d9-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

