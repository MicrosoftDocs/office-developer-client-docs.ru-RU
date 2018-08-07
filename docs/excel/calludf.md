---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807138"
---
# <a name="calludf"></a><span data-ttu-id="5746b-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="5746b-103">CallUDF</span></span>

<span data-ttu-id="5746b-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5746b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5746b-105">Вызывает пользовательскую функцию в вычислительной среде высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="5746b-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="5746b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5746b-106">Parameters</span></span>

<span data-ttu-id="5746b-107">_Код сеанса_</span><span class="sxs-lookup"><span data-stu-id="5746b-107">_SessionId_</span></span>
  
> <span data-ttu-id="5746b-108">Идентификатор сеанса, в котором для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="5746b-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="5746b-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="5746b-109">_XLLName_</span></span>
  
> <span data-ttu-id="5746b-110">Имя XLL, содержащий пользовательскую функцию.</span><span class="sxs-lookup"><span data-stu-id="5746b-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="5746b-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="5746b-111">_UDFName_</span></span>
  
> <span data-ttu-id="5746b-112">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="5746b-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="5746b-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="5746b-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="5746b-114">Функция, которая соединитель должен вызывать после завершения пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5746b-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="5746b-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="5746b-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="5746b-116">Асинхронный дескриптор, используемых в Excel и соединитель для отслеживания вызовов ожидающих пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5746b-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="5746b-117">Соединитель использует его более поздняя версия после завершения вызова, когда он вызывает Excel с помощью указатель функции передается в аргументе _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="5746b-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="5746b-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="5746b-118">_ArgCount_</span></span>
  
> <span data-ttu-id="5746b-119">Число аргументов, передаваемых в пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="5746b-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="5746b-120">Максимально допустимое значение — 255.</span><span class="sxs-lookup"><span data-stu-id="5746b-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="5746b-121">_Параметр1_</span><span class="sxs-lookup"><span data-stu-id="5746b-121">_Parameter1_</span></span>
  
> <span data-ttu-id="5746b-122">Значение для передачи пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="5746b-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="5746b-123">Повторите этот аргумент для каждого параметра, указанный в параметре _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="5746b-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5746b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="5746b-125">**xlHpcRetSuccess** Если UDF успешно звонок; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на другие сбои, включая время ожидания. Если звонок возвращает код ошибки (все, кроме **xlHpcRetSuccess**), затем Excel считает вызов пользовательских Функций, не были выполнены, признает недействительным _pxAsyncHandle_и не ожидает обратного вызова будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="5746b-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5746b-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="5746b-126">Remarks</span></span>

<span data-ttu-id="5746b-127">Эта функция выполняет асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5746b-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5746b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5746b-128">See also</span></span>

- [<span data-ttu-id="5746b-129">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="5746b-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

