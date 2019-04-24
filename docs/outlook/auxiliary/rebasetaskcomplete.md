---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Создает отчет о завершении для ребазового использования встреч.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328324"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="66da8-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="66da8-103">RebaseTaskComplete</span></span>

<span data-ttu-id="66da8-104">Создает отчет о завершении для ребазового использования встреч.</span><span class="sxs-lookup"><span data-stu-id="66da8-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="66da8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="66da8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66da8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="66da8-106">Header file:</span></span>  <br/> |<span data-ttu-id="66da8-107">тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="66da8-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="66da8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="66da8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="66da8-109">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="66da8-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="66da8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="66da8-110">Called by:</span></span>  <br/> |<span data-ttu-id="66da8-111">Объект перебазового объекта Outlook</span><span class="sxs-lookup"><span data-stu-id="66da8-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="66da8-112">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="66da8-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="66da8-113">**Пфнребасетасккомплете** в соответствии с определением в тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="66da8-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="66da8-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="66da8-114">Parameters</span></span>

<span data-ttu-id="66da8-115">_Улровиндекс_</span><span class="sxs-lookup"><span data-stu-id="66da8-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="66da8-116">возврата Строка, которая была обработана.</span><span class="sxs-lookup"><span data-stu-id="66da8-116">[in] The row that was processed.</span></span> <span data-ttu-id="66da8-117">Этот индекс ссылается на структуру **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** , переданную в [Иолкапптребасер:: бегинребасеаппоинтментс](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="66da8-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="66da8-118">_Провкур_</span><span class="sxs-lookup"><span data-stu-id="66da8-118">_pRowCur_</span></span>
  
> <span data-ttu-id="66da8-119">in] указатель на структуру **[сров](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , описывающий обработанный элемент.</span><span class="sxs-lookup"><span data-stu-id="66da8-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="66da8-120">_Хрресулт_</span><span class="sxs-lookup"><span data-stu-id="66da8-120">_hrResult_</span></span>
  
> <span data-ttu-id="66da8-121">возврата **Значение HRESULT** , указывающее результат операции перезаписи.</span><span class="sxs-lookup"><span data-stu-id="66da8-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="66da8-122">_Фмодифиед_</span><span class="sxs-lookup"><span data-stu-id="66da8-122">_fModified_</span></span>
  
> <span data-ttu-id="66da8-123">возврата Указывает, был ли изменен элемент.</span><span class="sxs-lookup"><span data-stu-id="66da8-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="66da8-124">_Фсентупдате_</span><span class="sxs-lookup"><span data-stu-id="66da8-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="66da8-125">возврата Указывает, было ли отправлено сообщение обновления собрания.</span><span class="sxs-lookup"><span data-stu-id="66da8-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="66da8-126">_Перрор_</span><span class="sxs-lookup"><span data-stu-id="66da8-126">_pError_</span></span>
  
> <span data-ttu-id="66da8-127">возврата Указатель на структуру **мапиеррор** с расширенными сведениями об ошибке.</span><span class="sxs-lookup"><span data-stu-id="66da8-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="66da8-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="66da8-128">Return values</span></span>

<span data-ttu-id="66da8-129">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="66da8-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66da8-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66da8-130">Remarks</span></span>

<span data-ttu-id="66da8-131">Клиентские приложения MAPI, использующие интерфейс [иолкапптребасер](iolkapptrebaser.md) , реализуют эту функцию для отслеживания завершения обновления элемента.</span><span class="sxs-lookup"><span data-stu-id="66da8-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66da8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="66da8-132">See also</span></span>

- [<span data-ttu-id="66da8-133">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="66da8-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

