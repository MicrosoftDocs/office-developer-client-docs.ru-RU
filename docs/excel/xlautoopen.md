---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlautoopen [Excel 2007]
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
# <a name="xlautoopen"></a><span data-ttu-id="b89b0-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="b89b0-104">xlAutoOpen</span></span>

 <span data-ttu-id="b89b0-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b89b0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b89b0-106">Функция вызова, которая должна быть реализована и экспортироваться каждым допустимым XLL.</span><span class="sxs-lookup"><span data-stu-id="b89b0-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="b89b0-107">Функция **xlAutoOpen** — это рекомендуемое место для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и так далее.</span><span class="sxs-lookup"><span data-stu-id="b89b0-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="b89b0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89b0-108">Parameters</span></span>

<span data-ttu-id="b89b0-109">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="b89b0-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b89b0-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b89b0-110">Property value/Return value</span></span>

<span data-ttu-id="b89b0-111">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="b89b0-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b89b0-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b89b0-112">Remarks</span></span>

<span data-ttu-id="b89b0-113">Microsoft Excel **xlAutoOpen при** активации XLL.</span><span class="sxs-lookup"><span data-stu-id="b89b0-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="b89b0-114">XLL активируется в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="b89b0-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="b89b0-115">В начале сеанса Excel, если он был активен в последнем сеансе Excel, завершившейся нормально.</span><span class="sxs-lookup"><span data-stu-id="b89b0-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="b89b0-116">При загрузке во время Excel сеанса.</span><span class="sxs-lookup"><span data-stu-id="b89b0-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="b89b0-117">XLL можно загрузить несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="b89b0-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="b89b0-118">Выбрав Open **в** меню **File** (где версия Excel поддерживает этот метод загрузки XLLs).</span><span class="sxs-lookup"><span data-stu-id="b89b0-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="b89b0-119">С помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="b89b0-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="b89b0-120">Из другого XLL, который [вызывает xlfRegister](xlfregister-form-1.md) с именем этого DLL в качестве единственным аргументом.</span><span class="sxs-lookup"><span data-stu-id="b89b0-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="b89b0-121">С макрос листа XLM, который вызывает [REGISTER](xlfregister-form-1.md) с именем этого DLL в качестве единственным аргументом.</span><span class="sxs-lookup"><span data-stu-id="b89b0-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="b89b0-122">Если надстройка отключена и активирована во время сеанса Excel, эта функция будет активирована.</span><span class="sxs-lookup"><span data-stu-id="b89b0-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="b89b0-123">Пример</span><span class="sxs-lookup"><span data-stu-id="b89b0-123">Example</span></span>

<span data-ttu-id="b89b0-124">Просмотр файлов  `SAMPLES\EXAMPLE\EXAMPLE.C`  `SAMPLES\GENERIC\GENERIC.C` и, например, реализаций этой функции.</span><span class="sxs-lookup"><span data-stu-id="b89b0-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b89b0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b89b0-125">See also</span></span>



[<span data-ttu-id="b89b0-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="b89b0-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="b89b0-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="b89b0-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="b89b0-128">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="b89b0-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

