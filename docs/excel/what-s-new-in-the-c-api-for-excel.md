---
title: Новые возможности в API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], новые возможности
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19807325"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="4898b-104">Новые возможности в API C для Excel</span><span class="sxs-lookup"><span data-stu-id="4898b-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="4898b-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4898b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4898b-106">В сочетании с Microsoft Excel 2013 Microsoft Excel 2013 XLL Software Development Kit (SDK) поддерживает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="4898b-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="4898b-107">**Новые функции**</span><span class="sxs-lookup"><span data-stu-id="4898b-107">**New Functions**</span></span>
    
    <span data-ttu-id="4898b-108">Пакет SDK XLL Microsoft Excel 2013 поддерживает обратного вызова для всех дополнительных функций листов в Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="4898b-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="4898b-109">Дополнительные сведения о вызове функции Excel 2013 [вызов в Excel из DLL или XLL](calling-into-excel-from-the-dll-or-xll.md)см.</span><span class="sxs-lookup"><span data-stu-id="4898b-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="4898b-110">**Асинхронные пользовательские функции**</span><span class="sxs-lookup"><span data-stu-id="4898b-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="4898b-111">Excel 2013 поддерживает вызов пользовательских функций (UDF) асинхронно, которой могут улучшить производительность, включив несколько вычислений для запуска в то же время.</span><span class="sxs-lookup"><span data-stu-id="4898b-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="4898b-112">Дополнительные сведения о асинхронных пользовательских функций [Asynchronous_User-Defined](asynchronous-user-defined-functions.md)см.</span><span class="sxs-lookup"><span data-stu-id="4898b-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="4898b-113">**Соединители кластера**</span><span class="sxs-lookup"><span data-stu-id="4898b-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="4898b-114">Соединителей кластеров для включения пользовательских функций для запуска на высокопроизводительные вычислительные кластеры.</span><span class="sxs-lookup"><span data-stu-id="4898b-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="4898b-115">Дополнительные сведения о создании соединителей кластеров можно [Разработка соединителей кластеров для Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="4898b-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4898b-116">Надстройки XLL, которые предполагается запускать на вычислительные кластеры должны вызывать только функции безопасно кластера.</span><span class="sxs-lookup"><span data-stu-id="4898b-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="4898b-117">Дополнительные сведения о функции можно использовать, [Справочник по функциям Excel XLL SDK API](excel-xll-sdk-api-function-reference.md) и [Безопасные для кластера функции](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4898b-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="4898b-118">**Поддержка 64-разрядная версия**</span><span class="sxs-lookup"><span data-stu-id="4898b-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="4898b-119">Теперь можно скомпилировать и связать 32- и 64-разрядная версия XLL-модулей.</span><span class="sxs-lookup"><span data-stu-id="4898b-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="4898b-120">Дополнительные сведения содержатся в разделе [Создание XLL-модулей](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="4898b-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4898b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4898b-121">See also</span></span>



[<span data-ttu-id="4898b-122">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="4898b-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="4898b-123">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="4898b-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="4898b-124">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="4898b-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="4898b-125">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="4898b-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

