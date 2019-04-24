---
title: Имапитаблеваитфоркомплетион
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328814"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="8323a-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8323a-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="8323a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8323a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8323a-105">ПриОстанавливает обработку, пока не завершится одна или несколько асинхронных операций, выполняемых над таблицей.</span><span class="sxs-lookup"><span data-stu-id="8323a-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8323a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8323a-106">Parameters</span></span>

 <span data-ttu-id="8323a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8323a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8323a-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8323a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8323a-109">_Ултимеаут_</span><span class="sxs-lookup"><span data-stu-id="8323a-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="8323a-110">возврата Максимальное время ожидания завершения асинхронной операции или операций (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="8323a-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="8323a-111">Чтобы подождать неопределенное время до завершения, задайте для параметра _ултимеаут_ значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8323a-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="8323a-112">_Лпултаблестатус_</span><span class="sxs-lookup"><span data-stu-id="8323a-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="8323a-113">[вход, выход] Для входных данных — допустимый указатель или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8323a-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="8323a-114">В выходных данных, если _лпултаблестатус_ является допустимым указателем, он указывает на Последнее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="8323a-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="8323a-115">Если _лпултаблестатус_ имеет значение null, сведения о состоянии не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="8323a-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="8323a-116">Если **ваитфоркомплетион** возвращает неудачное значение HRESULT, то содержимое _лпултаблестатус_ не определено.</span><span class="sxs-lookup"><span data-stu-id="8323a-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8323a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8323a-117">Return value</span></span>

<span data-ttu-id="8323a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8323a-118">S_OK</span></span> 
  
> <span data-ttu-id="8323a-119">Операция ожидания выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8323a-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="8323a-120">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="8323a-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8323a-121">Таблица не поддерживает ожидание завершения асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="8323a-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="8323a-122">МАПИ_Е_ТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="8323a-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="8323a-123">Асинхронная операция или операции не завершились в указанное время.</span><span class="sxs-lookup"><span data-stu-id="8323a-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8323a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8323a-124">Remarks</span></span>

<span data-ttu-id="8323a-125">Метод **IMAPITable:: ваитфоркомплетион** приостанавливает обработку до тех пор, пока не завершится выполнение всех асинхронных операций, выполняемых в данный момент для таблицы.</span><span class="sxs-lookup"><span data-stu-id="8323a-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="8323a-126">**Ваитфоркомплетион** позволяет выполнять асинхронные операции как полностью полностью, так и в течение определенного числа миллисекунд, как указано в _ултимеаут_, до прерывания.</span><span class="sxs-lookup"><span data-stu-id="8323a-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="8323a-127">Чтобы определить выполняемые асинхронные операции, вызовите метод [IMAPITable::/Status](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="8323a-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8323a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8323a-128">See also</span></span>



[<span data-ttu-id="8323a-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="8323a-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="8323a-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="8323a-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="8323a-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8323a-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="8323a-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8323a-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8323a-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8323a-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8323a-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8323a-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

