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
# <a name="cluster-safe-functions"></a><span data-ttu-id="8c516-103">Безопасные функции кластера</span><span class="sxs-lookup"><span data-stu-id="8c516-103">Cluster safe functions</span></span>

<span data-ttu-id="8c516-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8c516-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8c516-105">В Excel 2013 Excel может разгрузить вызовы User-Defined Function (UDF) в высокоскоростной вычислительный кластер через выделенный интерфейс соединителю кластера.</span><span class="sxs-lookup"><span data-stu-id="8c516-105">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface.</span></span> <span data-ttu-id="8c516-106">Поставщики кластеров вычислений предоставляют соединители кластера.</span><span class="sxs-lookup"><span data-stu-id="8c516-106">Compute cluster vendors provide Cluster Connectors.</span></span> <span data-ttu-id="8c516-107">Авторы UDF могут объявить свои UDF как кластерные безопасные, а затем, когда соединители кластера присутствуют, Excel отправляет вызовы этим UDFs в соединители кластера для разгрузки.</span><span class="sxs-lookup"><span data-stu-id="8c516-107">UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="8c516-108">Когда Excel обнаруживает кластерную UDF во время пересчета, она передает имя запущенного XLL, имя безопасного кластера UDF и любые параметры соединителю кластера.</span><span class="sxs-lookup"><span data-stu-id="8c516-108">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector.</span></span> <span data-ttu-id="8c516-109">Соединителю выполняется вызов UDF удаленно и возвращает результаты Excel.</span><span class="sxs-lookup"><span data-stu-id="8c516-109">The connector runs the UDF call remotely and returns the results to Excel.</span></span> <span data-ttu-id="8c516-110">Не зависящие вычисления продолжаются, и когда соединителю кластера завершится запуск UDF, результаты будут Excel и зависящие вычисления будут продолжаться.</span><span class="sxs-lookup"><span data-stu-id="8c516-110">Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue.</span></span> <span data-ttu-id="8c516-111">Механизм этого асинхронного поведения имитирует механизм, используемый асинхронными UDF, за исключением того, что соединителю кластера управляют асинхронные аспекты вместо автора UDF.</span><span class="sxs-lookup"><span data-stu-id="8c516-111">The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author.</span></span> <span data-ttu-id="8c516-112">Как правило, соединитель кластера реализует shim XLL для загрузки XLLs и запуска UDF на вычислительных узлах кластера.</span><span class="sxs-lookup"><span data-stu-id="8c516-112">Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="8c516-113">Механика объявления UDF как кластерной безопасности похожа на механизмы объявления UDF безопасными для многопоточной пересчета.</span><span class="sxs-lookup"><span data-stu-id="8c516-113">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation.</span></span> <span data-ttu-id="8c516-114">Однако, поскольку UDF не обязательно работает на том же компьютере, что и другие UDF из того же сеанса Excel, при написании UDF с безопасностью кластера существуют различные соображения.</span><span class="sxs-lookup"><span data-stu-id="8c516-114">However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="8c516-115">Чтобы зарегистрировать UDF как кластерную безопасность, необходимо вызвать функцию [вызова xlfRegister (Form 1)](xlfregister-form-1.md) с помощью интерфейса **Excel12** или **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="8c516-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface.</span></span> <span data-ttu-id="8c516-116">Дополнительные сведения об этих интерфейсах см. в [таблицах Excel4/Excel12](excel4-excel12.md) и [Excel4v/Excel12v.](excel4v-excel12v.md)</span><span class="sxs-lookup"><span data-stu-id="8c516-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="8c516-117">Регистрация UDF в качестве кластерного безопасного интерфейса **Excel4** или **Excel4v** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8c516-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="8c516-118">Если вы регистрируете функцию в качестве кластерной, необходимо убедиться, что она будет вести себя безопасно кластерно.</span><span class="sxs-lookup"><span data-stu-id="8c516-118">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way.</span></span> <span data-ttu-id="8c516-119">Хотя точное поведение соединиттеля кластера зависит от реализации, необходимо разработать UDF для работы с распределенной компьютерной системой и иметь следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="8c516-119">Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="8c516-120">UDF не должен полагаться на состояние памяти.</span><span class="sxs-lookup"><span data-stu-id="8c516-120">A UDF should not rely on any memory state.</span></span> <span data-ttu-id="8c516-121">Например, UDF не должен полагаться на существующий кэш в памяти.</span><span class="sxs-lookup"><span data-stu-id="8c516-121">For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="8c516-122">UDF не должен выполнять Excel вызовов, которые поставщик соединителю кластера не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="8c516-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="8c516-123">В дополнение к безопасному для кластера поведению существуют следующие технические ограничения для UDF с безопасностью кластера:</span><span class="sxs-lookup"><span data-stu-id="8c516-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="8c516-124">Нет аргументов XLOPER (типы "P", "R").</span><span class="sxs-lookup"><span data-stu-id="8c516-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="8c516-125">Нет аргументов XLOPER12, которые поддерживают ссылки на диапазон (тип "U").</span><span class="sxs-lookup"><span data-stu-id="8c516-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="8c516-126">Не может быть эквивалентной функции макроса ('#' и &amp; ' не может быть совмещена).</span><span class="sxs-lookup"><span data-stu-id="8c516-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="8c516-127">Для UDF с более коротким временем выполнения накладная часть разгрузки может быть больше времени, необходимого для выполнения UDF, что отрицает многие преимущества использования этой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="8c516-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8c516-128">Нельзя объявить групповую UDF асинхронной UDF.</span><span class="sxs-lookup"><span data-stu-id="8c516-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="8c516-129">UDF может определить, запускается ли он с помощью соединителя кластера, позвонив в [функцию вызова xlRunningOnCluster.](xlrunningoncluster.md)</span><span class="sxs-lookup"><span data-stu-id="8c516-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

