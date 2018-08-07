---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807334"
---
# <a name="xlautoopen"></a><span data-ttu-id="d40aa-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="d40aa-104">xlAutoOpen</span></span>

 <span data-ttu-id="d40aa-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d40aa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d40aa-106">Функция обратного вызова, который должен быть реализован и экспортировать с любой допустимый XLL-модуль.</span><span class="sxs-lookup"><span data-stu-id="d40aa-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="d40aa-107">Функция **xlAutoOpen** используется, рекомендуется откуда регистрация функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и так далее.</span><span class="sxs-lookup"><span data-stu-id="d40aa-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="d40aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d40aa-108">Parameters</span></span>

<span data-ttu-id="d40aa-109">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="d40aa-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d40aa-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d40aa-110">Property value/Return value</span></span>

<span data-ttu-id="d40aa-111">Внедрении этой функции должно возвратить значение 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="d40aa-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d40aa-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="d40aa-112">Remarks</span></span>

<span data-ttu-id="d40aa-113">Microsoft Excel вызывает **xlAutoOpen** при активации XLL.</span><span class="sxs-lookup"><span data-stu-id="d40aa-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="d40aa-114">XLL активируется в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="d40aa-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="d40aa-115">В начале сеанса обмена Excel, если она была активна последнего сеанса Excel, нормально.</span><span class="sxs-lookup"><span data-stu-id="d40aa-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="d40aa-116">Если загружена во время сеанса обмена Excel.</span><span class="sxs-lookup"><span data-stu-id="d40aa-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="d40aa-117">XLL-модуль может быть загружена несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="d40aa-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="d40aa-118">Выбрав команду **Открыть** в меню **файл** (где версии Excel поддерживает этот метод загрузки XLL-модулей).</span><span class="sxs-lookup"><span data-stu-id="d40aa-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="d40aa-119">С помощью диспетчера надстроек.</span><span class="sxs-lookup"><span data-stu-id="d40aa-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="d40aa-120">Из другой XLL [xlfRegister](xlfregister-form-1.md) с именем Эта DLL-Библиотека, которая вызывает только в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="d40aa-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="d40aa-121">Из таблицы макросов XLM, который вызывает [регистрации](xlfregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="d40aa-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="d40aa-122">Если надстройка отключена и повторно во время сеанса обмена Excel, эта функция вызывается для повторной активации.</span><span class="sxs-lookup"><span data-stu-id="d40aa-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="d40aa-123">Пример</span><span class="sxs-lookup"><span data-stu-id="d40aa-123">Example</span></span>

<span data-ttu-id="d40aa-124">Файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C`и пример реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="d40aa-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d40aa-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d40aa-125">See also</span></span>



[<span data-ttu-id="d40aa-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="d40aa-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="d40aa-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="d40aa-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="d40aa-128">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="d40aa-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

