---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407062"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="a9789-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a9789-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="a9789-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9789-105">Приостанавливать обработку до завершения одной или более асинхронных операций в таблице.</span><span class="sxs-lookup"><span data-stu-id="a9789-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="a9789-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9789-106">Parameters</span></span>

 <span data-ttu-id="a9789-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9789-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a9789-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="a9789-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a9789-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="a9789-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="a9789-110">[in] Максимальное количество миллисекунд для ожидания завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="a9789-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="a9789-111">Чтобы неопределенное время ждать завершения, установите  _для ulTimeout_ 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a9789-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="a9789-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="a9789-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="a9789-113">[in, out] При вводе допустимый указатель или NULL.</span><span class="sxs-lookup"><span data-stu-id="a9789-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="a9789-114">При выходе, если  _lpulTableStatus_ является допустимым указателем, он указывает на последнее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="a9789-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="a9789-115">Если  _lpulTableStatus_ имеет NULL, сведения о состоянии не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="a9789-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="a9789-116">Если **WaitForCompletion** возвращает неудачное значение HRESULT,  _содержимое lpulTableStatus_ будет неопределенным.</span><span class="sxs-lookup"><span data-stu-id="a9789-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a9789-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9789-117">Return value</span></span>

<span data-ttu-id="a9789-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9789-118">S_OK</span></span> 
  
> <span data-ttu-id="a9789-119">Операция ожидания прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a9789-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="a9789-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a9789-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a9789-121">Таблица не поддерживает ожидание завершения асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="a9789-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="a9789-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a9789-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="a9789-123">Асинхронная операция или операции не были завершены в указанное время.</span><span class="sxs-lookup"><span data-stu-id="a9789-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9789-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9789-124">Remarks</span></span>

<span data-ttu-id="a9789-125">Метод **IMAPITable::WaitForCompletion** приостанавливать обработку до завершения всех асинхронных операций, которые в настоящее время проводятся для таблицы.</span><span class="sxs-lookup"><span data-stu-id="a9789-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="a9789-126">**WaitForCompletion** позволяет выполнить асинхронные операции полностью или в течение определенного количества миллисекунд, как указано  _в ulTimeout,_ перед прерыванием.</span><span class="sxs-lookup"><span data-stu-id="a9789-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="a9789-127">Чтобы обнаружить асинхронные операции, вызовите метод [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="a9789-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9789-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a9789-128">See also</span></span>



[<span data-ttu-id="a9789-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="a9789-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="a9789-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="a9789-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="a9789-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="a9789-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="a9789-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a9789-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a9789-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a9789-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="a9789-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9789-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

