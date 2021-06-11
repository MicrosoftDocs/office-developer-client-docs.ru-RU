---
title: Управление многочитаниями и памятью
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
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="2ad16-103">Управление многочитаниями и памятью</span><span class="sxs-lookup"><span data-stu-id="2ad16-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="2ad16-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2ad16-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2ad16-105">Правильная обработка памяти имеет жизненно важное значение для создания надежных надстройок XLL для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2ad16-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="2ad16-106">Неспособность выделить соответствующие буферы памяти и освободить их, когда они больше не нужны, снижает производительность, создает раздор ресурсов и Excel.</span><span class="sxs-lookup"><span data-stu-id="2ad16-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="2ad16-107">Начиная с Microsoft Office Excel 2007 г. можно настроить Excel для использования до 1024 одновременно потоков при пересчете.</span><span class="sxs-lookup"><span data-stu-id="2ad16-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="2ad16-108">В некоторых случаях, особенно при наличии нескольких процессоров или с пользовательскими функциями, работающими на кластерных серверах, многочитание может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="2ad16-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="2ad16-109">Ниже описаны вопросы управления памятью и потоками в XLLs:</span><span class="sxs-lookup"><span data-stu-id="2ad16-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="2ad16-110">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="2ad16-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="2ad16-111">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="2ad16-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="2ad16-112">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="2ad16-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="2ad16-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2ad16-113">See also</span></span>



[<span data-ttu-id="2ad16-114">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="2ad16-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

