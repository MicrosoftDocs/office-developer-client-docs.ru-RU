---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433013"
---
# <a name="calludf"></a><span data-ttu-id="e0ca9-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="e0ca9-103">CallUDF</span></span>

<span data-ttu-id="e0ca9-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0ca9-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e0ca9-105">Вызывает функцию, определяемую пользователем, в высокой производительности вычислительной среды.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="e0ca9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0ca9-106">Parameters</span></span>

<span data-ttu-id="e0ca9-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-107">_SessionId_</span></span>
  
> <span data-ttu-id="e0ca9-108">ID сеанса, в котором необходимо сделать вызов.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="e0ca9-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-109">_XLLName_</span></span>
  
> <span data-ttu-id="e0ca9-110">Имя XLL, которое содержит функцию, определяемую пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="e0ca9-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-111">_UDFName_</span></span>
  
> <span data-ttu-id="e0ca9-112">Имя функции, определяемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="e0ca9-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="e0ca9-114">Функция, которую соединитатель должен вызывать после завершения функции, определенной пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="e0ca9-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="e0ca9-116">Асинхронная ручка, используемая Excel и соединитетелем для отслеживания ожидающих вызовов функций, определенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="e0ca9-117">Соединиттель использует его позже, когда вызов будет завершен, когда он возвращается в Excel с помощью указателя функции, переданного в _аргументе CallBackAddr._</span><span class="sxs-lookup"><span data-stu-id="e0ca9-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="e0ca9-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-118">_ArgCount_</span></span>
  
> <span data-ttu-id="e0ca9-119">Количество аргументов, которые необходимо передать в функцию, определяемую пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="e0ca9-120">Максимальное допустимые значения — 255.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="e0ca9-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="e0ca9-121">_Parameter1_</span></span>
  
> <span data-ttu-id="e0ca9-122">Значение, передав его в функцию, определяемую пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="e0ca9-123">Повторите этот аргумент для каждого параметра, показанного  _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0ca9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0ca9-124">Return value</span></span>

<span data-ttu-id="e0ca9-125">**xlHpcRetSuccess,** если вызов UDF успешно инициировался; **xlHpcRetInvalidSessionId,** если аргумент _SessionId_ недействителен; **xlHpcRetCallFailed на** других сбоях, включая время. Если вызов возвращает код ошибки (все, кроме **xlHpcRetSuccess),** Excel считает вызов UDF недействительным, недействителен _pxAsyncHandle_ и не ожидает обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0ca9-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0ca9-126">Remarks</span></span>

<span data-ttu-id="e0ca9-127">Эта функция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0ca9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e0ca9-128">See also</span></span>

- [<span data-ttu-id="e0ca9-129">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="e0ca9-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

