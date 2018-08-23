---
title: О таблице асинхронной операции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569423"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="1a5af-103">О таблице асинхронной операции</span><span class="sxs-lookup"><span data-stu-id="1a5af-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="1a5af-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a5af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a5af-105">Интерфейс **IMAPITable** включает в себя три метода, которые используются асинхронно и три методы для управления асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="1a5af-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="1a5af-106">В следующей таблице приведены следующие методы:</span><span class="sxs-lookup"><span data-stu-id="1a5af-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="1a5af-107">**Асинхронной операции**</span><span class="sxs-lookup"><span data-stu-id="1a5af-107">**Asynchronous operation**</span></span>|<span data-ttu-id="1a5af-108">**Метод асинхронного управления**</span><span class="sxs-lookup"><span data-stu-id="1a5af-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a5af-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1a5af-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="1a5af-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="1a5af-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="1a5af-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1a5af-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="1a5af-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1a5af-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="1a5af-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1a5af-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="1a5af-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1a5af-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="1a5af-115">**Для получения сведений о типе и текущей операции таблицы**</span><span class="sxs-lookup"><span data-stu-id="1a5af-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="1a5af-116">Вызов [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a5af-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="1a5af-117">**GetStatus**пользователя в таблице определить ли таблицы статических или динамических, если находится в стадии разработки или завершения операции, и если произошла ошибка завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1a5af-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="1a5af-118">Например если это клиент должен отменить операцию сортировки, так как она выполняется слишком много времени, клиента можно вызвать **GetStatus** , чтобы определить, на самом деле операции сортировки в настоящее время обрабатывает ли.</span><span class="sxs-lookup"><span data-stu-id="1a5af-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="1a5af-119">Затем клиент может вызывать [IMAPITable::Abort](imapitable-abort.md) , чтобы остановить его.</span><span class="sxs-lookup"><span data-stu-id="1a5af-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="1a5af-120">**Для приостановки действия до завершения асинхронной задачи**</span><span class="sxs-lookup"><span data-stu-id="1a5af-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="1a5af-121">Вызов [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="1a5af-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="1a5af-122">Вызов **WaitForCompletion** позволяет завершение без прерывания задачи.</span><span class="sxs-lookup"><span data-stu-id="1a5af-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1a5af-123">См. также</span><span class="sxs-lookup"><span data-stu-id="1a5af-123">See also</span></span>

- [<span data-ttu-id="1a5af-124">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="1a5af-124">MAPI Tables</span></span>](mapi-tables.md)

