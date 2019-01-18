---
title: Знакомство с пакетом средств разработки программного обеспечения для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 365aea48cd520cd368c2a118c832aa705280a308
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708314"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="43451-104">Знакомство с пакетом средств разработки программного обеспечения для Excel</span><span class="sxs-lookup"><span data-stu-id="43451-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="43451-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43451-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43451-p101">Добро пожаловать в документацию по пакету средств разработки (SDK) XLL для Excel 2013. Этот справочник включает концептуальные обзоры, задачи программирования и примеры, которые помогут вам разрабатывать XLL для Microsoft Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="43451-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="43451-108">Последняя редакция: ноябрь 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43451-108">Revised: November 2012</span></span>
  
<span data-ttu-id="43451-109">Скачайте [пакет SDK XLL для Excel 2013](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="43451-109">Download the [Excel 2013 XLL SDK](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span></span>
  
<span data-ttu-id="43451-110">Пакет SDK XLL для Excel 2013 включает следующее:</span><span class="sxs-lookup"><span data-stu-id="43451-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="43451-111">**Программный интерфейс (API) C** включает файлы заголовков и исходные файлы, которые позволяют библиотекам DLL получать доступ к функциям Excel 2013, и описание интерфейса, который библиотека DLL должна предоставлять для работы с диспетчером надстроек Excel.</span><span class="sxs-lookup"><span data-stu-id="43451-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="43451-p102">**Проекты Microsoft Visual Studio** включают исходный код на C/C++ и демонстрируют использование API C. Эти примеры проектов включают примеры кода и служат отправной точкой для разработки собственных надстроек.</span><span class="sxs-lookup"><span data-stu-id="43451-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="43451-114">Документация по SDK включает следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="43451-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="43451-115">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="43451-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="43451-116">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="43451-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="43451-117">Разработка соединителей кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="43451-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="43451-118">Справочник по функциям API SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="43451-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="43451-119">Не рассмотренные функции</span><span class="sxs-lookup"><span data-stu-id="43451-119">Functionality Not Covered</span></span>

<span data-ttu-id="43451-120">Не рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="43451-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="43451-121">Разработка определенных пользователем функций и команд в листах макросов Excel (XLM).</span><span class="sxs-lookup"><span data-stu-id="43451-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="43451-122">Создание определенных пользователем функций в библиотеках DLL, которые управляют потоком выполнения макроса XLM.</span><span class="sxs-lookup"><span data-stu-id="43451-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="43451-123">Такие функции работают, возвращая специальный тип данных элемента управления потоком, который также не описываются в данной документации.</span><span class="sxs-lookup"><span data-stu-id="43451-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="43451-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="43451-124">Related Links</span></span>

[<span data-ttu-id="43451-125">Центр разработчиков Excel</span><span class="sxs-lookup"><span data-stu-id="43451-125">Excel Developer Center</span></span>](https://msdn.microsoft.com/office/aa905411.aspx)
  
[<span data-ttu-id="43451-126">Центр разработчика Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="43451-126">Microsoft Office Developer Center</span></span>](https://msdn.microsoft.com/office/default.aspx)
  
[<span data-ttu-id="43451-127">Пакет SDK для Excel 2010: пакет средств разработки XLL для Excel 2010</span><span class="sxs-lookup"><span data-stu-id="43451-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](https://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

