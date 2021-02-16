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
# <a name="imapitableabort"></a><span data-ttu-id="ac5b3-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="ac5b3-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="ac5b3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac5b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac5b3-105">Останавливает все асинхронные операции, которые в настоящее время ведутся для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ac5b3-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="ac5b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac5b3-106">Parameters</span></span>

<span data-ttu-id="ac5b3-107">Нет</span><span class="sxs-lookup"><span data-stu-id="ac5b3-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ac5b3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac5b3-108">Return value</span></span>

<span data-ttu-id="ac5b3-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac5b3-109">S_OK</span></span> 
  
> <span data-ttu-id="ac5b3-110">Одна или несколько асинхронных операций были остановлены.</span><span class="sxs-lookup"><span data-stu-id="ac5b3-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="ac5b3-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="ac5b3-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="ac5b3-112">Асинхронная операция находится в процессе выполнения и не может быть остановлена или уже завершена.</span><span class="sxs-lookup"><span data-stu-id="ac5b3-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac5b3-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac5b3-113">Remarks</span></span>

<span data-ttu-id="ac5b3-114">Метод **IMAPITable::Abort** останавливает все асинхронные операции, которые в настоящее время находятся в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="ac5b3-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac5b3-115">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ac5b3-115">Notes to callers</span></span>

<span data-ttu-id="ac5b3-116">Чтобы узнать, идет ли асинхронная операция, вызовите метод [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="ac5b3-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="ac5b3-117">Если **прекратить** обработку вызова метода [IMAPITable::Restrict,](imapitable-restrict.md) состояние таблицы будет таким, как было на момент обработки вызова **Abort.**</span><span class="sxs-lookup"><span data-stu-id="ac5b3-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="ac5b3-118">Если **при** остановке обработки вызова метода [IMAPITable::SortTable](imapitable-sorttable.md) порядок сортировки таблицы остается таким же, как и до вызова **SortTable.**</span><span class="sxs-lookup"><span data-stu-id="ac5b3-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac5b3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ac5b3-119">See also</span></span>



[<span data-ttu-id="ac5b3-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="ac5b3-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="ac5b3-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="ac5b3-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="ac5b3-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="ac5b3-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ac5b3-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac5b3-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

