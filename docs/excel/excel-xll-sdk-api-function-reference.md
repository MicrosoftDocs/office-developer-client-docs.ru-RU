---
title: Справочник по функциям API SDK XLL для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Справочник по функциям API [Excel 2007], функции [Excel 2007], справочник [Excel 2007], пакет средств разработки XLL для Excel 2007, справочник
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304125"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="a57c0-104">Справочник по функциям API SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="a57c0-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="a57c0-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a57c0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a57c0-106">Пакет SDK XLL для Microsoft Excel 2013 содержит исходные файлы для библиотеки платформы, предназначенной для ускорения записи библиотек XLL, а также два примера проектов (Example и Generic).</span><span class="sxs-lookup"><span data-stu-id="a57c0-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="a57c0-107">В этом разделе приведены справочные сведения по следующим функциям:</span><span class="sxs-lookup"><span data-stu-id="a57c0-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="a57c0-108">обратные вызовы Excel, доступные для XLL;</span><span class="sxs-lookup"><span data-stu-id="a57c0-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="a57c0-109">обратные вызовы XLL, поиск которых выполняется в Microsoft Excel;</span><span class="sxs-lookup"><span data-stu-id="a57c0-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="a57c0-110">ключевые функции в примерах проектов и платформ.</span><span class="sxs-lookup"><span data-stu-id="a57c0-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="a57c0-111">Примеры проектов</span><span class="sxs-lookup"><span data-stu-id="a57c0-111">Sample projects</span></span>

<span data-ttu-id="a57c0-112">Пакет SDK XLL для Excel 2013 содержит исходные файлы и файлы проектов Microsoft Visual Studio для следующих примеров проектов:</span><span class="sxs-lookup"><span data-stu-id="a57c0-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="a57c0-113">Проект **Framework** (`SAMPLES\FRAMEWRK\`) содержит проект, который можно встроить в библиотеку FRAMEWRK.lib для последующего связывания с другими проектами XLL.</span><span class="sxs-lookup"><span data-stu-id="a57c0-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="a57c0-114">Эта библиотека включает множество функций и инструментов, которые упрощают написание библиотек XLL.</span><span class="sxs-lookup"><span data-stu-id="a57c0-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="a57c0-115">Данная библиотека используется в каждом из других проектов в сочетании с файлом заголовка FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="a57c0-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="a57c0-116">Проект **Example** (`SAMPLES\EXAMPLE\`) содержит проект EXAMPLE.xll, который можно встроить в библиотеку XLL.</span><span class="sxs-lookup"><span data-stu-id="a57c0-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="a57c0-117">Библиотека XLL включает ряд примеров использования библиотеки платформы, а также пример реализации функций интерфейса надстройки XLL, таких как **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="a57c0-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="a57c0-118">Проект **Generic** (`SAMPLES\GENERIC\`) содержит проект GENERIC.xll, который можно встроить в библиотеку XLL.</span><span class="sxs-lookup"><span data-stu-id="a57c0-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="a57c0-119">Эта библиотека XLL демонстрирует несколько примеров функций и команд. Ее можно использовать в качестве отправной точки при написании собственных библиотек XLL.</span><span class="sxs-lookup"><span data-stu-id="a57c0-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="a57c0-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a57c0-120">In this section</span></span>

- [<span data-ttu-id="a57c0-121">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="a57c0-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="a57c0-122">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="a57c0-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="a57c0-123">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="a57c0-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="a57c0-124">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="a57c0-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="a57c0-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="a57c0-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="a57c0-126">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="a57c0-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="a57c0-127">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="a57c0-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="a57c0-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a57c0-128">See also</span></span>

- [<span data-ttu-id="a57c0-129">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="a57c0-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="a57c0-130">Разработка библиотек XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="a57c0-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

