---
title: Справочник по функции API пакет SDK XLL для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Справочник по функциям API [excel 2007], [Excel 2007] функции, ссылки [Excel 2007, Excel 2007 XLL пакет средств разработки, ссылка
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807251"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="87461-104">Справочник по функции API пакет SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="87461-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="87461-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="87461-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="87461-106">Пакет SDK Microsoft Excel 2013 XLL содержит исходные файлы для библиотеки Framework, предназначенный для ускорения записи XLL-модулей и два примера проекта, пример и универсальный.</span><span class="sxs-lookup"><span data-stu-id="87461-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="87461-107">В этом разделе представлены ссылки на функцию для следующих:</span><span class="sxs-lookup"><span data-stu-id="87461-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="87461-108">Обратные вызовы для Excel, которые могут вызывать XLL.</span><span class="sxs-lookup"><span data-stu-id="87461-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="87461-109">XLL обратных вызовов, которые ищет Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="87461-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="87461-110">Ключевые функции в проектах образец и framework.</span><span class="sxs-lookup"><span data-stu-id="87461-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="87461-111">Примеры проектов</span><span class="sxs-lookup"><span data-stu-id="87461-111">Sample projects</span></span>

<span data-ttu-id="87461-112">Пакет SDK Excel XLL 2013 предоставляет исходные файлы и файлы проекта Microsoft Visual Studio для следующие примеры проектов:</span><span class="sxs-lookup"><span data-stu-id="87461-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="87461-113">Проект **Framework** (`SAMPLES\FRAMEWRK\`) содержит проекта, который можно создать в библиотеке FRAMEWRK.lib, который затем могут быть связаны в другие проекты XLL.</span><span class="sxs-lookup"><span data-stu-id="87461-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="87461-114">Библиотека содержит множество функций и средств, которые делают создание XLL-модулей для удобства.</span><span class="sxs-lookup"><span data-stu-id="87461-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="87461-115">Эта библиотека используется в обоих других проектов в сочетании с файл заголовка FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="87461-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="87461-116">**Пример** проекта (`SAMPLES\EXAMPLE\`) содержит проекта, который можно создать в надстройке XLL EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="87461-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="87461-117">Многие примеры использования библиотеки Framework и примеры реализации функции интерфейса надстройки XLL, такие как **xlAutoOpen**XLL.</span><span class="sxs-lookup"><span data-stu-id="87461-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="87461-118">**Универсальный** проекта (`SAMPLES\GENERIC\`) содержит проекта, который можно создать в надстройке XLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="87461-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="87461-119">XLL демонстрирует несколько пример функции и команды и является хорошей отправной точкой для написания собственного XLL-модулей.</span><span class="sxs-lookup"><span data-stu-id="87461-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="87461-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="87461-120">In this section</span></span>

- [<span data-ttu-id="87461-121">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="87461-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="87461-122">������� ��������� ������ API C Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="87461-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="87461-123">Функции API XLM важные и полезные C</span><span class="sxs-lookup"><span data-stu-id="87461-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="87461-124">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="87461-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="87461-125">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="87461-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="87461-126">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="87461-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="87461-127">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="87461-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="87461-128">См. также</span><span class="sxs-lookup"><span data-stu-id="87461-128">See also</span></span>

- [<span data-ttu-id="87461-129">���������������� � �������������� C API � Excel</span><span class="sxs-lookup"><span data-stu-id="87461-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="87461-130">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="87461-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

