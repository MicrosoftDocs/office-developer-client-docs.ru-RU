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
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809197"
---
# <a name="imapitableabort"></a><span data-ttu-id="b6433-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="b6433-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="b6433-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6433-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6433-105">Останавливает асинхронной операции в данный момент для таблицы.</span><span class="sxs-lookup"><span data-stu-id="b6433-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="b6433-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6433-106">Parameters</span></span>

<span data-ttu-id="b6433-107">Нет</span><span class="sxs-lookup"><span data-stu-id="b6433-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b6433-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b6433-108">Return value</span></span>

<span data-ttu-id="b6433-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b6433-109">S_OK</span></span> 
  
> <span data-ttu-id="b6433-110">Один или несколько асинхронной операции остановлены.</span><span class="sxs-lookup"><span data-stu-id="b6433-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="b6433-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="b6433-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="b6433-112">Асинхронной операции находится в стадии разработки и не может быть остановлена или уже выполнена.</span><span class="sxs-lookup"><span data-stu-id="b6433-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6433-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6433-113">Remarks</span></span>

<span data-ttu-id="b6433-114">Метод **IMAPITable::Abort** останавливает асинхронной операции, который в данный момент находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="b6433-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6433-115">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b6433-115">Notes to callers</span></span>

<span data-ttu-id="b6433-116">Чтобы проверить, является ли в процессе выполнения асинхронной операции, вызовите метод [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b6433-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="b6433-117">Если **Прервать** останавливает обработку вызов метода [IMAPITable::Restrict](imapitable-restrict.md) , состояние таблицы будет во время обработки **Прервать** вызов.</span><span class="sxs-lookup"><span data-stu-id="b6433-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="b6433-118">Если **Прервать** останавливает обработку вызов метода [IMAPITable::SortTable](imapitable-sorttable.md) , порядок сортировки таблицы не зависит от и остается, которая была до вызова **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="b6433-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6433-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b6433-119">See also</span></span>



[<span data-ttu-id="b6433-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="b6433-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="b6433-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b6433-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="b6433-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b6433-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="b6433-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6433-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

