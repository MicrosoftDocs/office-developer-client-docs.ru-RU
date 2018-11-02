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
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586951"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="0b403-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0b403-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="0b403-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b403-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b403-105">Приостанавливает работу до завершения одного или нескольких асинхронной операции выполняется в таблице.</span><span class="sxs-lookup"><span data-stu-id="0b403-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="0b403-106">���������</span><span class="sxs-lookup"><span data-stu-id="0b403-106">Parameters</span></span>

 <span data-ttu-id="0b403-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b403-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0b403-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0b403-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0b403-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="0b403-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="0b403-110">[in] Максимальное число миллисекундах время ожидания для асинхронной операции или операции для выполнения.</span><span class="sxs-lookup"><span data-stu-id="0b403-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="0b403-111">До начала неопределенное время до завершения, значение _ulTimeout_ 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0b403-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="0b403-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="0b403-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="0b403-113">[in, out] На выходе — допустимый указатель или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0b403-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="0b403-114">В выходных данных Если _lpulTableStatus_ является допустимым указателем, он указывает самое последнее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="0b403-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="0b403-115">Если _lpulTableStatus_ имеет значение NULL, возвращаются сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="0b403-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="0b403-116">Если **WaitForCompletion** возвращает значение HRESULT неудачно, содержимое _lpulTableStatus_ не определено.</span><span class="sxs-lookup"><span data-stu-id="0b403-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0b403-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b403-117">Return value</span></span>

<span data-ttu-id="0b403-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b403-118">S_OK</span></span> 
  
> <span data-ttu-id="0b403-119">Операция ожидания прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0b403-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="0b403-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0b403-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0b403-121">Таблицы не поддерживает ожидание завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="0b403-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="0b403-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0b403-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="0b403-123">Асинхронной операции или операции не завершена в указанное время.</span><span class="sxs-lookup"><span data-stu-id="0b403-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b403-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b403-124">Remarks</span></span>

<span data-ttu-id="0b403-125">Метод **IMAPITable::WaitForCompletion** приостанавливает работу до завершения любой асинхронной операции в настоящее время на правильном пути для таблицы.</span><span class="sxs-lookup"><span data-stu-id="0b403-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="0b403-126">**WaitForCompletion** можно разрешить асинхронной операции, либо полностью полный или для запуска некоторых количество миллисекунд, как указано в _ulTimeout_, прежде чем прерывания.</span><span class="sxs-lookup"><span data-stu-id="0b403-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="0b403-127">Для обнаружения в процессе выполнения асинхронной операции, вызовите метод [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="0b403-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b403-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0b403-128">See also</span></span>



[<span data-ttu-id="0b403-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="0b403-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="0b403-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0b403-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="0b403-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="0b403-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="0b403-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0b403-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="0b403-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0b403-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0b403-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b403-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

