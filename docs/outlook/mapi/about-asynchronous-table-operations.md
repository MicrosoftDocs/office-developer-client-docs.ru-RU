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
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807972"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="26191-103">О таблице асинхронной операции</span><span class="sxs-lookup"><span data-stu-id="26191-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="26191-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26191-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26191-105">Интерфейс **IMAPITable** включает в себя три метода, которые используются асинхронно и три методы для управления асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="26191-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="26191-106">В следующей таблице приведены следующие методы:</span><span class="sxs-lookup"><span data-stu-id="26191-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="26191-107">**Асинхронной операции**</span><span class="sxs-lookup"><span data-stu-id="26191-107">**Asynchronous operation**</span></span>|<span data-ttu-id="26191-108">**Метод асинхронного управления**</span><span class="sxs-lookup"><span data-stu-id="26191-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26191-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="26191-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="26191-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="26191-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="26191-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="26191-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="26191-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="26191-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="26191-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="26191-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="26191-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="26191-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="26191-115">**Для получения сведений о типе и текущей операции таблицы**</span><span class="sxs-lookup"><span data-stu-id="26191-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="26191-116">Вызов [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="26191-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="26191-117">**GetStatus**пользователя в таблице определить ли таблицы статических или динамических, если находится в стадии разработки или завершения операции, и если произошла ошибка завершения операции.</span><span class="sxs-lookup"><span data-stu-id="26191-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="26191-118">Например если это клиент должен отменить операцию сортировки, так как она выполняется слишком много времени, клиента можно вызвать **GetStatus** , чтобы определить, на самом деле операции сортировки в настоящее время обрабатывает ли.</span><span class="sxs-lookup"><span data-stu-id="26191-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="26191-119">Затем клиент может вызывать [IMAPITable::Abort](imapitable-abort.md) , чтобы остановить его.</span><span class="sxs-lookup"><span data-stu-id="26191-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="26191-120">**Для приостановки действия до завершения асинхронной задачи**</span><span class="sxs-lookup"><span data-stu-id="26191-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="26191-121">Вызов [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="26191-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="26191-122">Вызов **WaitForCompletion** позволяет завершение без прерывания задачи.</span><span class="sxs-lookup"><span data-stu-id="26191-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="26191-123">См. также</span><span class="sxs-lookup"><span data-stu-id="26191-123">See also</span></span>

- [<span data-ttu-id="26191-124">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="26191-124">MAPI Tables</span></span>](mapi-tables.md)

