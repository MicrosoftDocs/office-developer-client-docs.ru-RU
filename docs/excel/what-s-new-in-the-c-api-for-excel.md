---
title: Новые возможности API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c API [Excel 2007], новые возможности
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439690"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="5e16f-104">Новые возможности API C для Excel</span><span class="sxs-lookup"><span data-stu-id="5e16f-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="5e16f-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5e16f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5e16f-106">В сочетании с Microsoft Excel 2013 пакет средств разработки программного обеспечения (SDK) Microsoft Excel 2013 XLL включает поддержку следующих функций.</span><span class="sxs-lookup"><span data-stu-id="5e16f-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="5e16f-107">**Новые функции**</span><span class="sxs-lookup"><span data-stu-id="5e16f-107">**New Functions**</span></span>
    
    <span data-ttu-id="5e16f-108">ПАКЕТ SDK XLL для Microsoft Excel 2013 поддерживает обратное обращение ко всем новым функциям листа в Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="5e16f-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="5e16f-109">Дополнительные сведения о вызове функций Excel 2013 см. в статье [вызов Excel из библиотеки DLL или XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="5e16f-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="5e16f-110">**Асинхронные пользовательские функции**</span><span class="sxs-lookup"><span data-stu-id="5e16f-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="5e16f-111">Excel 2013 поддерживает асинхронный вызов пользовательских функций (UDF), что может увеличить производительность, одновременно разрешив выполнение нескольких вычислений.</span><span class="sxs-lookup"><span data-stu-id="5e16f-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="5e16f-112">Дополнительные сведения об асинхронных пользовательских функциях можно найти в статье [асинхронНые пользовательские функции](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5e16f-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="5e16f-113">**Соединители кластера**</span><span class="sxs-lookup"><span data-stu-id="5e16f-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="5e16f-114">Соединители кластера позволяют выполнять функции UDF на высокопроизводительных вычислительных кластерах.</span><span class="sxs-lookup"><span data-stu-id="5e16f-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="5e16f-115">Дополнительные сведения о создании соединителей кластера содержатся в разделе [Разработка кластерНых соединителЕй Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="5e16f-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5e16f-116">Надстройки XLL, которые вы планируете запускать в вычислительных кластерах, должны вызывать только функции, безопасные кластером.</span><span class="sxs-lookup"><span data-stu-id="5e16f-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="5e16f-117">Для получения дополнительных сведений о функциях, которые можно использовать, ознакомьтесь со статьей [Справка по функциям API пакета SDK для Office XLL](excel-xll-sdk-api-function-reference.md) и [безопасные функции кластера](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5e16f-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="5e16f-118">**Поддержка 64 бит**</span><span class="sxs-lookup"><span data-stu-id="5e16f-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="5e16f-119">Теперь вы можете скомпилировать и связать как 32, так и 64 – битовые XLL.</span><span class="sxs-lookup"><span data-stu-id="5e16f-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="5e16f-120">Дополнительную информацию можно узнать в статье [Создание XLL](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="5e16f-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e16f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5e16f-121">See also</span></span>



[<span data-ttu-id="5e16f-122">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="5e16f-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="5e16f-123">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="5e16f-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="5e16f-124">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="5e16f-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="5e16f-125">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="5e16f-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

