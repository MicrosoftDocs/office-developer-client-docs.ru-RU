---
title: Многопоточность и управление памятью
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414468"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="6a3e7-103">Многопоточность и управление памятью</span><span class="sxs-lookup"><span data-stu-id="6a3e7-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="6a3e7-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a3e7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6a3e7-105">Правильная обработка памяти крайне важна для создания надежных надстроек XLL для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="6a3e7-106">Не удается выделить соответствующие буферы памяти и освободить их, когда они больше не нужны, уменьшает производительность, создает состязание за ресурсы и дестабилизации Excel.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="6a3e7-107">Начиная с Microsoft Office Excel 2007, вы можете настроить Excel для использования до 1 024 параллельных потоков при пересчете.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="6a3e7-108">В некоторых случаях, особенно при наличии нескольких процессоров или с пользовательскими функциями, работающими на кластерных серверах, многопоточность может увеличить производительность.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="6a3e7-109">В следующих разделах описано, как управлять памятью и потоками в XLL:</span><span class="sxs-lookup"><span data-stu-id="6a3e7-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="6a3e7-110">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="6a3e7-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="6a3e7-111">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="6a3e7-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="6a3e7-112">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="6a3e7-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="6a3e7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6a3e7-113">See also</span></span>



[<span data-ttu-id="6a3e7-114">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="6a3e7-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

