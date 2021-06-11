---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406152"
---
# <a name="imapitableabort"></a><span data-ttu-id="8bc33-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="8bc33-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="8bc33-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bc33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bc33-105">Останавливает любые асинхронные операции, которые в настоящее время ведутся для таблицы.</span><span class="sxs-lookup"><span data-stu-id="8bc33-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="8bc33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bc33-106">Parameters</span></span>

<span data-ttu-id="8bc33-107">Нет</span><span class="sxs-lookup"><span data-stu-id="8bc33-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8bc33-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bc33-108">Return value</span></span>

<span data-ttu-id="8bc33-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bc33-109">S_OK</span></span> 
  
> <span data-ttu-id="8bc33-110">Одна или несколько асинхронных операций остановлены.</span><span class="sxs-lookup"><span data-stu-id="8bc33-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="8bc33-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="8bc33-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="8bc33-112">Асинхронная операция продолжается и не может быть остановлена или уже завершена.</span><span class="sxs-lookup"><span data-stu-id="8bc33-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bc33-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bc33-113">Remarks</span></span>

<span data-ttu-id="8bc33-114">Метод **IMAPITable::Abort** останавливает любую асинхронную операцию, которая в настоящее время продолжается.</span><span class="sxs-lookup"><span data-stu-id="8bc33-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bc33-115">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8bc33-115">Notes to callers</span></span>

<span data-ttu-id="8bc33-116">Чтобы узнать, продолжается ли асинхронная операция, позвоните по методу [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="8bc33-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="8bc33-117">Если **прекращена** обработка вызова метода [IMAPITable:::Restrict,](imapitable-restrict.md) состояние таблицы будет таким, как было на момент обработки вызова **Abort.**</span><span class="sxs-lookup"><span data-stu-id="8bc33-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="8bc33-118">Если **прекращена** обработка вызова метода [IMAPITable::SortTable,](imapitable-sorttable.md) порядок сортировки таблицы не влияет и остается таким, как до вызова **SortTable.**</span><span class="sxs-lookup"><span data-stu-id="8bc33-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bc33-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8bc33-119">See also</span></span>



[<span data-ttu-id="8bc33-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="8bc33-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="8bc33-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8bc33-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="8bc33-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8bc33-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8bc33-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bc33-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

