---
title: Безопасные функции кластера
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409302"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="43192-103">Безопасные функции кластера</span><span class="sxs-lookup"><span data-stu-id="43192-103">Cluster safe functions</span></span>

<span data-ttu-id="43192-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43192-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43192-105">В Excel 2013 Excel может разгружать вызовы функции User-Defined (UDF) в высокоскоростной вычислительный кластер с помощью выделенного интерфейса соединителю кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-105">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface.</span></span> <span data-ttu-id="43192-106">Поставщики вычислительных кластеров предоставляют соединители кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-106">Compute cluster vendors provide Cluster Connectors.</span></span> <span data-ttu-id="43192-107">Авторы UDF могут объявлять свои UDF как безопасные кластеры, а затем, когда соединитель кластера присутствует, Excel отправляет вызовы этим UDF соединителю кластера для разгрузки.</span><span class="sxs-lookup"><span data-stu-id="43192-107">UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="43192-108">Когда Excel обнаруживает кластерную безопасную UDF во время пересчета, он передает имя запущенной ВТБ XLL, имя безопасной для кластера UDF и любые параметры соединителю кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-108">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector.</span></span> <span data-ttu-id="43192-109">Соединитель выполняет вызов UDF удаленно и возвращает результаты в Excel.</span><span class="sxs-lookup"><span data-stu-id="43192-109">The connector runs the UDF call remotely and returns the results to Excel.</span></span> <span data-ttu-id="43192-110">Независимые вычисления продолжаются, и когда соединитель кластера завершит работу UDF, он передает результаты в Excel, и зависимые вычисления продолжаются.</span><span class="sxs-lookup"><span data-stu-id="43192-110">Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue.</span></span> <span data-ttu-id="43192-111">Механизм для этого асинхронного поведения имитирует механизм, используемый асинхронными UDF, за исключением того, что соединителю кластера управляют асинхронные аспекты, а не автор UDF.</span><span class="sxs-lookup"><span data-stu-id="43192-111">The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author.</span></span> <span data-ttu-id="43192-112">Как правило, соединитель кластера реализует shim XLL для загрузки XLL и запуска UDF на узлах вычислительного кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-112">Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="43192-113">Механизмы объявления UDF как кластеробезопасные похожи на механизмы объявления UDF как безопасных для многопотокового пересчета.</span><span class="sxs-lookup"><span data-stu-id="43192-113">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation.</span></span> <span data-ttu-id="43192-114">Однако поскольку UDF не обязательно работает на том же компьютере, что и другие UDF из того же сеанса Excel, при написании безопасных для кластера UDF есть другие факторы.</span><span class="sxs-lookup"><span data-stu-id="43192-114">However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="43192-115">Чтобы зарегистрировать UDF как кластеробезопасную, необходимо вызвать функцию вызова [xlfRegister (форма 1)](xlfregister-form-1.md) через интерфейс **Excel12** или **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="43192-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface.</span></span> <span data-ttu-id="43192-116">Дополнительные сведения об этих интерфейсах см. в [excel4/Excel12](excel4-excel12.md) и [Excel4v/Excel12v.](excel4v-excel12v.md)</span><span class="sxs-lookup"><span data-stu-id="43192-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="43192-117">Регистрация UDF в качестве кластерной с помощью интерфейса **Excel4** или **Excel4v** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="43192-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="43192-118">Если вы регистрируете функцию как кластеробезопасную, необходимо убедиться, что она работает безопасным образом кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-118">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way.</span></span> <span data-ttu-id="43192-119">Хотя точное поведение соединителю кластера зависит от реализации, необходимо разработать UDF для работы в распределенной компьютерной системе и иметь следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="43192-119">Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="43192-120">UDF не должен зависеть от состояния памяти.</span><span class="sxs-lookup"><span data-stu-id="43192-120">A UDF should not rely on any memory state.</span></span> <span data-ttu-id="43192-121">Например, UDF не должен полагаться на существующий кэш в памяти.</span><span class="sxs-lookup"><span data-stu-id="43192-121">For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="43192-122">UDF не должна выполнять вызовы Excel, которые поставщик соединителю кластера не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="43192-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="43192-123">В дополнение к безопасному для кластера поведению существуют следующие технические ограничения для безопасных кластерных УДО:</span><span class="sxs-lookup"><span data-stu-id="43192-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="43192-124">Нет аргументов XLOPER (типы P, R).</span><span class="sxs-lookup"><span data-stu-id="43192-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="43192-125">Нет аргументов XLOPER12, которые поддерживают ссылки на диапазоны (тип U).</span><span class="sxs-lookup"><span data-stu-id="43192-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="43192-126">Не может быть эквивалентной функцией листа макроса ('#' и &amp; ' не может быть объединено).</span><span class="sxs-lookup"><span data-stu-id="43192-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="43192-127">Для UDF с более коротким временем выполнения нагрузка на разгрузку может быть больше времени, необходимого для выполнения UDF, что не дает большого количества преимуществ использования этой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="43192-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="43192-128">Невозможно объявить Асинхронную UDF, безопасную для кластера.</span><span class="sxs-lookup"><span data-stu-id="43192-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="43192-129">Функция UDF может определить, будет ли она запускаться с помощью соединителя кластера, вызывая функцию вызова [xlRunningOnCluster.](xlrunningoncluster.md)</span><span class="sxs-lookup"><span data-stu-id="43192-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

