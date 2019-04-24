---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Сообщает о ходе перечислений и перепланировании встреч.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326455"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="61f65-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="61f65-103">RebaseTaskProgress</span></span>

<span data-ttu-id="61f65-104">Сообщает о ходе перечислений и перепланировании встреч.</span><span class="sxs-lookup"><span data-stu-id="61f65-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61f65-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="61f65-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61f65-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="61f65-106">Header file:</span></span>  <br/> |<span data-ttu-id="61f65-107">тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="61f65-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="61f65-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="61f65-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="61f65-109">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="61f65-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="61f65-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="61f65-110">Called by:</span></span>  <br/> |<span data-ttu-id="61f65-111">Объект перебазового объекта Outlook</span><span class="sxs-lookup"><span data-stu-id="61f65-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="61f65-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="61f65-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="61f65-113">**Пфнребасетаскпрогресс** в соответствии с определением в тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="61f65-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="61f65-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="61f65-114">Parameters</span></span>

<span data-ttu-id="61f65-115">_Улмин_</span><span class="sxs-lookup"><span data-stu-id="61f65-115">_ulMin_</span></span>
  
> <span data-ttu-id="61f65-116">возврата Нижний конец диапазона обрабатываемых встреч.</span><span class="sxs-lookup"><span data-stu-id="61f65-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="61f65-117">Обычно это ноль.</span><span class="sxs-lookup"><span data-stu-id="61f65-117">It is usually zero.</span></span>
    
<span data-ttu-id="61f65-118">_Улмакс_</span><span class="sxs-lookup"><span data-stu-id="61f65-118">_ulMax_</span></span>
  
> <span data-ttu-id="61f65-119">возврата Максимальный конец диапазона обрабатываемых встреч.</span><span class="sxs-lookup"><span data-stu-id="61f65-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="61f65-120">Обычно это количество обрабатываемых элементов в папке календаря.</span><span class="sxs-lookup"><span data-stu-id="61f65-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="61f65-121">_Улкур_</span><span class="sxs-lookup"><span data-stu-id="61f65-121">_ulCur_</span></span>
  
> <span data-ttu-id="61f65-122">возврата Обрабатываемый текущий элемент.</span><span class="sxs-lookup"><span data-stu-id="61f65-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="61f65-123">_State_</span><span class="sxs-lookup"><span data-stu-id="61f65-123">_State_</span></span>
  
> <span data-ttu-id="61f65-124">возврата Значение, указывающее состояние обрабатываемого элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="61f65-125">Перечисление **ребасе_аппт_стате** определено в тзмовелиб. h.</span><span class="sxs-lookup"><span data-stu-id="61f65-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="61f65-126">_State_  одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="61f65-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="61f65-127">**Ребасе_аппт_стате_сканнинг_ексамининг** — сканирование и исследование элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="61f65-128">**Ребасе_аппт_стате_сканнинг_фаунд** — сканирование и поиск элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="61f65-129">**Ребасе_аппт_стате_бегин** — исправление и запуск элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="61f65-130">**Ребасе_аппт_стате_ребасинг** — исправление и корректировка элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="61f65-131">**Ребасе_аппт_стате_сендинг** — исправление и отправка обновления собрания.</span><span class="sxs-lookup"><span data-stu-id="61f65-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="61f65-132">**Ребасе_аппт_стате_доне** — восстановление и выполнение элемента.</span><span class="sxs-lookup"><span data-stu-id="61f65-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="61f65-133">_Провкур_</span><span class="sxs-lookup"><span data-stu-id="61f65-133">_pRowCur_</span></span>
  
> <span data-ttu-id="61f65-134">возврата Указатель на структуру **[сров](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , которая описывает проверяемый или фиксированный элемент.</span><span class="sxs-lookup"><span data-stu-id="61f65-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="61f65-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="61f65-135">Return values</span></span>

<span data-ttu-id="61f65-136">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="61f65-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61f65-137">Замечания</span><span class="sxs-lookup"><span data-stu-id="61f65-137">Remarks</span></span>

<span data-ttu-id="61f65-138">Клиентские приложения MAPI, использующие интерфейс [иолкапптребасер](iolkapptrebaser.md) , реализуют эту функцию для отслеживания обработки элементов.</span><span class="sxs-lookup"><span data-stu-id="61f65-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61f65-139">См. также</span><span class="sxs-lookup"><span data-stu-id="61f65-139">See also</span></span>

- [<span data-ttu-id="61f65-140">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="61f65-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

