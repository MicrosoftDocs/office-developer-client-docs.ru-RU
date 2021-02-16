---
title: Сведения об асинхронных операциях с таблицами
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439571"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="87e16-103">Сведения об асинхронных операциях с таблицами</span><span class="sxs-lookup"><span data-stu-id="87e16-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="87e16-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e16-105">Интерфейс **IMAPITable** включает три метода, которые работают асинхронно, и три метода управления асинхронной операцией.</span><span class="sxs-lookup"><span data-stu-id="87e16-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="87e16-106">В следующей таблице перечислены следующие методы:</span><span class="sxs-lookup"><span data-stu-id="87e16-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="87e16-107">**Асинхронная операция**</span><span class="sxs-lookup"><span data-stu-id="87e16-107">**Asynchronous operation**</span></span>|<span data-ttu-id="87e16-108">**Метод асинхронного управления**</span><span class="sxs-lookup"><span data-stu-id="87e16-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87e16-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="87e16-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="87e16-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="87e16-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="87e16-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="87e16-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="87e16-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="87e16-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="87e16-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="87e16-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="87e16-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="87e16-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="87e16-115">**Извлечение сведений о состоянии типа таблицы и текущей операции**</span><span class="sxs-lookup"><span data-stu-id="87e16-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="87e16-116">Вызов [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="87e16-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="87e16-117">С **помощью GetStatus** пользователь таблицы может определить, является ли таблица статической или динамической, находится ли операция в процессе выполнения или завершена, а также произошла ли ошибка в результате выполненной операции.</span><span class="sxs-lookup"><span data-stu-id="87e16-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="87e16-118">Например, если клиенту необходимо отменить операцию сортировки, так как она требует слишком много времени, клиент может сначала вызвать **GetStatus,** чтобы определить, действительно ли операция сортировки в настоящее время обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="87e16-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="87e16-119">Затем клиент может вызвать [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить его.</span><span class="sxs-lookup"><span data-stu-id="87e16-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="87e16-120">**Приостановка действия до завершения асинхронной задачи**</span><span class="sxs-lookup"><span data-stu-id="87e16-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="87e16-121">Вызов [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="87e16-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="87e16-122">Вызов **WaitForCompletion** позволяет выполнить задачу без прерывания.</span><span class="sxs-lookup"><span data-stu-id="87e16-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="87e16-123">См. также</span><span class="sxs-lookup"><span data-stu-id="87e16-123">See also</span></span>

- [<span data-ttu-id="87e16-124">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="87e16-124">MAPI Tables</span></span>](mapi-tables.md)

