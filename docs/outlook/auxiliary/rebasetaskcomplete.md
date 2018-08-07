---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Отчеты о выполнении для повторного размещения en встреч.
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807966"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="d9cd8-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="d9cd8-103">RebaseTaskComplete</span></span>

<span data-ttu-id="d9cd8-104">Отчеты о выполнении для повторного размещения en встреч.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9cd8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d9cd8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9cd8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d9cd8-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9cd8-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="d9cd8-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="d9cd8-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d9cd8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9cd8-109">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="d9cd8-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="d9cd8-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d9cd8-110">Called by:</span></span>  <br/> |<span data-ttu-id="d9cd8-111">Объект сдвига Outlook</span><span class="sxs-lookup"><span data-stu-id="d9cd8-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="d9cd8-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="d9cd8-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="d9cd8-113">**PFNREBASETASKCOMPLETE** , определенных в tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="d9cd8-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="d9cd8-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9cd8-114">Parameters</span></span>

<span data-ttu-id="d9cd8-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="d9cd8-116">[in] Строку, в которой было обработано.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-116">[in] The row that was processed.</span></span> <span data-ttu-id="d9cd8-117">В этом индекс относится к **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** структуры, переданной в [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="d9cd8-117">This index refers to the **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="d9cd8-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-118">_pRowCur_</span></span>
  
> <span data-ttu-id="d9cd8-119">входной параметр] указатель на структуру **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , описывающий элемент, который был обработан.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-119">in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="d9cd8-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-120">_hrResult_</span></span>
  
> <span data-ttu-id="d9cd8-121">[in] Значение **HRESULT** , указывающее, результат операции сдвига.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="d9cd8-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-122">_fModified_</span></span>
  
> <span data-ttu-id="d9cd8-123">[in] Указывает, будет ли изменения элемента.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="d9cd8-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="d9cd8-125">[in] Указывает, было отправлено ли сообщение об обновлении собрания.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="d9cd8-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="d9cd8-126">_pError_</span></span>
  
> <span data-ttu-id="d9cd8-127">[in] Указатель на структуру **MAPIERROR** с расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d9cd8-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d9cd8-128">Return values</span></span>

<span data-ttu-id="d9cd8-129">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9cd8-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="d9cd8-130">Remarks</span></span>

<span data-ttu-id="d9cd8-131">Клиентские приложения MAPI, использующие интерфейс [IOlkApptRebaser](iolkapptrebaser.md) реализовать эту функцию, чтобы отслеживать выполнение обновления элементов.</span><span class="sxs-lookup"><span data-stu-id="d9cd8-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9cd8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d9cd8-132">See also</span></span>

- [<span data-ttu-id="d9cd8-133">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="d9cd8-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

