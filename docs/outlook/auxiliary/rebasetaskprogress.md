---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Отчеты о ходе выполнения для перечисления и повторного размещения en встреч.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807962"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="bebe7-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="bebe7-103">RebaseTaskProgress</span></span>

<span data-ttu-id="bebe7-104">Отчеты о ходе выполнения для перечисления и повторного размещения en встреч.</span><span class="sxs-lookup"><span data-stu-id="bebe7-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bebe7-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bebe7-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bebe7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bebe7-106">Header file:</span></span>  <br/> |<span data-ttu-id="bebe7-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="bebe7-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="bebe7-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="bebe7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bebe7-109">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="bebe7-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="bebe7-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="bebe7-110">Called by:</span></span>  <br/> |<span data-ttu-id="bebe7-111">Объект сдвига Outlook</span><span class="sxs-lookup"><span data-stu-id="bebe7-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="bebe7-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="bebe7-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="bebe7-113">**PFNREBASETASKPROGRESS** , определенных в tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="bebe7-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="bebe7-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="bebe7-114">Parameters</span></span>

<span data-ttu-id="bebe7-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="bebe7-115">_ulMin_</span></span>
  
> <span data-ttu-id="bebe7-116">[in] Низкая конец диапазона, обрабатываемых встреч.</span><span class="sxs-lookup"><span data-stu-id="bebe7-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="bebe7-117">Обычно равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bebe7-117">It is usually zero.</span></span>
    
<span data-ttu-id="bebe7-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="bebe7-118">_ulMax_</span></span>
  
> <span data-ttu-id="bebe7-119">[in] Высокая конец диапазона, обрабатываемых встреч.</span><span class="sxs-lookup"><span data-stu-id="bebe7-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="bebe7-120">Обычно это количество элементов в папке календаря, обрабатываемых.</span><span class="sxs-lookup"><span data-stu-id="bebe7-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="bebe7-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="bebe7-121">_ulCur_</span></span>
  
> <span data-ttu-id="bebe7-122">[in] Текущий элемент, обрабатываемых.</span><span class="sxs-lookup"><span data-stu-id="bebe7-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="bebe7-123">_State_</span><span class="sxs-lookup"><span data-stu-id="bebe7-123">_State_</span></span>
  
> <span data-ttu-id="bebe7-124">[in] Значение, указывающее состояние обрабатываемый элемент.</span><span class="sxs-lookup"><span data-stu-id="bebe7-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="bebe7-125">Перечисление **REBASE_APPT_STATE** определен в tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="bebe7-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="bebe7-126">_Состояние_ — это один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bebe7-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="bebe7-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** — сканирования и проверки элемента.</span><span class="sxs-lookup"><span data-stu-id="bebe7-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="bebe7-128">**REBASE_APPT_STATE_SCANNING_FOUND** — сканирование и найти элемент.</span><span class="sxs-lookup"><span data-stu-id="bebe7-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="bebe7-129">**REBASE_APPT_STATE_BEGIN** — устранению и запуск элемента.</span><span class="sxs-lookup"><span data-stu-id="bebe7-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="bebe7-130">**REBASE_APPT_STATE_REBASING** — устранению и изменяет значения элемента.</span><span class="sxs-lookup"><span data-stu-id="bebe7-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="bebe7-131">**REBASE_APPT_STATE_SENDING** — устранению и отправка обновления собрания.</span><span class="sxs-lookup"><span data-stu-id="bebe7-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="bebe7-132">**REBASE_APPT_STATE_DONE** — исправление и Готово с элементом.</span><span class="sxs-lookup"><span data-stu-id="bebe7-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="bebe7-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="bebe7-133">_pRowCur_</span></span>
  
> <span data-ttu-id="bebe7-134">[in] Указатель на структуру **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** с описанием элемента выполняется поиск вирусов или фиксированной.</span><span class="sxs-lookup"><span data-stu-id="bebe7-134">[in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bebe7-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bebe7-135">Return values</span></span>

<span data-ttu-id="bebe7-136">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="bebe7-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bebe7-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="bebe7-137">Remarks</span></span>

<span data-ttu-id="bebe7-138">Клиентские приложения MAPI, использующие интерфейс [IOlkApptRebaser](iolkapptrebaser.md) реализовать эту функцию для отслеживания обработки элементов.</span><span class="sxs-lookup"><span data-stu-id="bebe7-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bebe7-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bebe7-139">See also</span></span>

- [<span data-ttu-id="bebe7-140">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="bebe7-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

