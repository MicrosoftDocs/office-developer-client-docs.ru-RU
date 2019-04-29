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
# <a name="calludf"></a><span data-ttu-id="58c77-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="58c77-103">CallUDF</span></span>

<span data-ttu-id="58c77-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58c77-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58c77-105">Вызывает пользовательскую функцию в высокопроизводительной вычислительной среде.</span><span class="sxs-lookup"><span data-stu-id="58c77-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="58c77-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58c77-106">Parameters</span></span>

<span data-ttu-id="58c77-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="58c77-107">_SessionId_</span></span>
  
> <span data-ttu-id="58c77-108">Идентификатор сеанса, в котором необходимо совершить вызов.</span><span class="sxs-lookup"><span data-stu-id="58c77-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="58c77-109">_Ксллнаме_</span><span class="sxs-lookup"><span data-stu-id="58c77-109">_XLLName_</span></span>
  
> <span data-ttu-id="58c77-110">Имя XLL, которое содержит определяемую пользователем функцию.</span><span class="sxs-lookup"><span data-stu-id="58c77-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="58c77-111">_Удфнаме_</span><span class="sxs-lookup"><span data-stu-id="58c77-111">_UDFName_</span></span>
  
> <span data-ttu-id="58c77-112">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="58c77-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="58c77-113">_Каллбаккаддр_</span><span class="sxs-lookup"><span data-stu-id="58c77-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="58c77-114">Функция, которая должна вызываться соединителем при завершении пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="58c77-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="58c77-115">_Пксасинчандле_</span><span class="sxs-lookup"><span data-stu-id="58c77-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="58c77-116">Асинхронный дескриптор, используемый Excel и соединителем для отслеживания незавершенного вызова пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="58c77-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="58c77-117">Соединитель использует его позже, когда вызов завершается, при обратном вызове в Excel с помощью указателя на функцию, переданного в аргументе _каллбаккаддр_ .</span><span class="sxs-lookup"><span data-stu-id="58c77-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="58c77-118">_Аргкаунт_</span><span class="sxs-lookup"><span data-stu-id="58c77-118">_ArgCount_</span></span>
  
> <span data-ttu-id="58c77-119">Число аргументов, передаваемых в определенную пользователем функцию.</span><span class="sxs-lookup"><span data-stu-id="58c77-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="58c77-120">Максимально допустимое значение — 255.</span><span class="sxs-lookup"><span data-stu-id="58c77-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="58c77-121">_Параметр1_</span><span class="sxs-lookup"><span data-stu-id="58c77-121">_Parameter1_</span></span>
  
> <span data-ttu-id="58c77-122">Значение, передаваемое пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="58c77-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="58c77-123">Повторите этот аргумент для каждого параметра, указанного с помощью _аргкаунт_.</span><span class="sxs-lookup"><span data-stu-id="58c77-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58c77-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58c77-124">Return value</span></span>

<span data-ttu-id="58c77-125">**кслхпкретсукцесс** при успешной инициации вызова UDF; **кслхпкретинвалидсессионид** , если аргумент _SessionID_ является недопустимым; **кслхпкреткаллфаилед** для других сбоев, включая время ожидания. Если вызов возвращает код ошибки (все, кроме **кслхпкретсукцесс**), Excel считает, что не удалось выполнить вызов UDF, делает недействительным _пксасинчандле_и не ожидает выполнения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="58c77-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58c77-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="58c77-126">Remarks</span></span>

<span data-ttu-id="58c77-127">Эта функция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="58c77-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58c77-128">См. также</span><span class="sxs-lookup"><span data-stu-id="58c77-128">See also</span></span>

- [<span data-ttu-id="58c77-129">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="58c77-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

