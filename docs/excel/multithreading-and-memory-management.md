---
title: Многопоточность и управление памятью
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807308"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="ef9c5-103">Многопоточность и управление памятью</span><span class="sxs-lookup"><span data-stu-id="ef9c5-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="ef9c5-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ef9c5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ef9c5-105">Правильность обработки памяти является важной создание надежных надстроек XLL для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="ef9c5-106">Сбой, связанный с выделения буферов памяти соответствующие и освободить их, если они больше не требуются снижает производительность, создает вероятность конфликта ресурсов и нестабильно работает Excel.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="ef9c5-107">Приступая к работе с Microsoft Office Excel 2007, вы можете настроить Excel для использования до 1024 параллельных потоков при перерасчете.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="ef9c5-108">В некоторых случаях особенно в том случае, когда доступно множество процессоров или с помощью пользовательских функций, работающим на серверах кластера Многопоточность может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="ef9c5-109">В следующих разделах рассматриваются способы управления памяти и потоков в XLL-модулей:</span><span class="sxs-lookup"><span data-stu-id="ef9c5-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="ef9c5-110">���������� ������� � Excel</span><span class="sxs-lookup"><span data-stu-id="ef9c5-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="ef9c5-111">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="ef9c5-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="ef9c5-112">�������������� �������� � Excel</span><span class="sxs-lookup"><span data-stu-id="ef9c5-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="ef9c5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ef9c5-113">See also</span></span>



[<span data-ttu-id="ef9c5-114">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="ef9c5-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

