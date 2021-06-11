---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Отчеты о ходе переомирия и повторного выполнения встреч.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326455"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="2e34a-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="2e34a-103">RebaseTaskProgress</span></span>

<span data-ttu-id="2e34a-104">Отчеты о ходе переомирия и повторного выполнения встреч.</span><span class="sxs-lookup"><span data-stu-id="2e34a-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2e34a-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2e34a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e34a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2e34a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e34a-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="2e34a-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="2e34a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2e34a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e34a-109">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="2e34a-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="2e34a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2e34a-110">Called by:</span></span>  <br/> |<span data-ttu-id="2e34a-111">Outlook повторного повторного</span><span class="sxs-lookup"><span data-stu-id="2e34a-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="2e34a-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2e34a-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="2e34a-113">**PFNREBASETASKPROGRESS,** как определено в tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="2e34a-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="2e34a-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="2e34a-114">Parameters</span></span>

<span data-ttu-id="2e34a-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="2e34a-115">_ulMin_</span></span>
  
> <span data-ttu-id="2e34a-116">[in] Низкий конец диапазона обрабатываемых назначений.</span><span class="sxs-lookup"><span data-stu-id="2e34a-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="2e34a-117">Обычно это ноль.</span><span class="sxs-lookup"><span data-stu-id="2e34a-117">It is usually zero.</span></span>
    
<span data-ttu-id="2e34a-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="2e34a-118">_ulMax_</span></span>
  
> <span data-ttu-id="2e34a-119">[in] Высокий конец диапазона обрабатываемых назначений.</span><span class="sxs-lookup"><span data-stu-id="2e34a-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="2e34a-120">Обычно это число элементов в обрабатываемой папке календаря.</span><span class="sxs-lookup"><span data-stu-id="2e34a-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="2e34a-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="2e34a-121">_ulCur_</span></span>
  
> <span data-ttu-id="2e34a-122">[in] Текущий обрабатываемый элемент.</span><span class="sxs-lookup"><span data-stu-id="2e34a-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="2e34a-123">_Состояние_</span><span class="sxs-lookup"><span data-stu-id="2e34a-123">_State_</span></span>
  
> <span data-ttu-id="2e34a-124">[in] Значение, которое указывает состояние обрабатываемого элемента.</span><span class="sxs-lookup"><span data-stu-id="2e34a-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="2e34a-125">Код REBASE_APPT_STATE **определяется** в tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="2e34a-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="2e34a-126">_State_  одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2e34a-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="2e34a-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** — сканирование и изучение элемента.</span><span class="sxs-lookup"><span data-stu-id="2e34a-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="2e34a-128">**REBASE_APPT_STATE_SCANNING_FOUND** — сканирование и найти элемент.</span><span class="sxs-lookup"><span data-stu-id="2e34a-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="2e34a-129">**REBASE_APPT_STATE_BEGIN** — исправление и запуск элемента.</span><span class="sxs-lookup"><span data-stu-id="2e34a-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="2e34a-130">**REBASE_APPT_STATE_REBASING** — исправление и настройка элемента.</span><span class="sxs-lookup"><span data-stu-id="2e34a-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="2e34a-131">**REBASE_APPT_STATE_SENDING** — исправление и отправка обновления собрания.</span><span class="sxs-lookup"><span data-stu-id="2e34a-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="2e34a-132">**REBASE_APPT_STATE_DONE** — исправление и исправление элемента.</span><span class="sxs-lookup"><span data-stu-id="2e34a-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="2e34a-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="2e34a-133">_pRowCur_</span></span>
  
> <span data-ttu-id="2e34a-134">[in] Указатель на структуру **[SRow,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** которая описывает отсканированный или исправленный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e34a-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2e34a-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2e34a-135">Return values</span></span>

<span data-ttu-id="2e34a-136">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="2e34a-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e34a-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e34a-137">Remarks</span></span>

<span data-ttu-id="2e34a-138">Клиентские приложения MAPI, которые используют [интерфейс IOlkApptRebaser,](iolkapptrebaser.md) реализуют эту функцию для отслеживания обработки элементов.</span><span class="sxs-lookup"><span data-stu-id="2e34a-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e34a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="2e34a-139">See also</span></span>

- [<span data-ttu-id="2e34a-140">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="2e34a-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

