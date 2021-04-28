---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Монитор инициализации MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062055"
---
# <a name="createmapiinitializationmonitor"></a><span data-ttu-id="27d20-103">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="27d20-103">CreateMAPIInitializationMonitor</span></span>

<span data-ttu-id="27d20-104">**Применяется к**: Outlook 2016 | Outlook 2019 г.</span><span class="sxs-lookup"><span data-stu-id="27d20-104">**Applies to**: Outlook 2016 | Outlook 2019</span></span>
  
## <a name="mapi-initialization-monitor"></a><span data-ttu-id="27d20-105">Монитор инициализации MAPI</span><span class="sxs-lookup"><span data-stu-id="27d20-105">MAPI Initialization Monitor</span></span>

<span data-ttu-id="27d20-106">Иногда приложение, которое потребляет MAPI, может потребовать знать, когда инициализация будет завершена.</span><span class="sxs-lookup"><span data-stu-id="27d20-106">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="27d20-107">Например, он имеет несколько потоков, которые могли бы инициализировать MAPI, или в ответ на инициализацию MAPI приложение хотело бы выполнить некоторую работу, но не хочет всегда вращать стек MAPI.</span><span class="sxs-lookup"><span data-stu-id="27d20-107">For example, it have multiple threads which could initialize MAPI, or in response to MAPI being initialize the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="27d20-108">Монитор инициализации предоставляет эту функцию с помощью функции (экспортируемой из OLMAPI32.DLL) и нескольких простых интерфейсов, описанных ниже.</span><span class="sxs-lookup"><span data-stu-id="27d20-108">The initialization monitor provides this functionality through a function (exported from OLMAPI32.DLL) and a couple of simple interfaces described below.</span></span>

<span data-ttu-id="27d20-109">Это точка входа, экспортируемая из OLMAPI32.DLL это позволяет звонячему получить интерфейс для запроса текущего состояния инициализации, установки вызова для завершения инициализации или блокировки текущего потока до завершения.</span><span class="sxs-lookup"><span data-stu-id="27d20-109">This is entry point exported from OLMAPI32.DLL this allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="27d20-110">Объект, возвращаемый из этого API, является многоразовым и безопасным для потока и может вызываться из любого потока, а не только из потока, который его извлек.</span><span class="sxs-lookup"><span data-stu-id="27d20-110">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="27d20-111">Кроме того, в отличие от других объектов, открытых в MAPI, этот объект действителен до тех пор, пока DLL загружен, его можно повторно использовать в сеансах инициализации и можно потреблять до или после того, как была вызвана MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="27d20-111">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="27d20-112">Возвращает успех или сбой с помощью стандартного HRESULT com и назначает параметр out экземпляру IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="27d20-112">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a><span data-ttu-id="27d20-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor (IMAPIInitMonitor ppInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="27d20-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span></span>

<span data-ttu-id="27d20-114">Эта точка входа, экспортируемая из OLMAPI32.DLL, позволяет вызываемой записи получить интерфейс для запроса текущего состояния инициализации, установки вызова для завершения инициализации или блокировки текущего потока до завершения.</span><span class="sxs-lookup"><span data-stu-id="27d20-114">This entry point exported from OLMAPI32.DLL allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="27d20-115">Объект, возвращаемый из этого API, является многоразовым и безопасным для потока и может вызываться из любого потока, а не только из потока, который его извлек.</span><span class="sxs-lookup"><span data-stu-id="27d20-115">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="27d20-116">Кроме того, в отличие от других объектов, открытых в MAPI, этот объект действителен до тех пор, пока DLL загружен, его можно повторно использовать в сеансах инициализации и можно потреблять до или после того, как была вызвана MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="27d20-116">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="27d20-117">Возвращает успех или сбой с помощью стандартного HRESULT com и назначает параметр out экземпляру IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="27d20-117">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="27d20-118">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="27d20-118">Quick info</span></span>

| <span data-ttu-id="27d20-119">идентификатор</span><span class="sxs-lookup"><span data-stu-id="27d20-119">identifier</span></span> | <span data-ttu-id="27d20-120">result</span><span class="sxs-lookup"><span data-stu-id="27d20-120">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="27d20-121">Экспортируемая по:</span><span class="sxs-lookup"><span data-stu-id="27d20-121">Exported by:</span></span>  <br/> |<span data-ttu-id="27d20-122">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="27d20-122">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="27d20-123">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="27d20-123">Called by:</span></span>  <br/> |<span data-ttu-id="27d20-124">Клиент</span><span class="sxs-lookup"><span data-stu-id="27d20-124">Client</span></span>  <br/> |
|<span data-ttu-id="27d20-125">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="27d20-125">Implemented by:</span></span>  <br/> |<span data-ttu-id="27d20-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="27d20-126">Outlook</span></span>  <br/> |

## <a name="parameters"></a><span data-ttu-id="27d20-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="27d20-127">Parameters</span></span>
  
 <span data-ttu-id="27d20-128">_ppInitMonitor_</span><span class="sxs-lookup"><span data-stu-id="27d20-128">_ppInitMonitor_</span></span>
> <span data-ttu-id="27d20-129">[вышел] Указатель для получения вновь созданного экземпляра монитора инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="27d20-129">[out] A pointer to receive the newly created instance of the MAPI initialization monitor.</span></span>
  
## <a name="return-values"></a><span data-ttu-id="27d20-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="27d20-130">Return values</span></span>

<span data-ttu-id="27d20-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="27d20-131">S_OK</span></span>
> <span data-ttu-id="27d20-132">Успешно создан новый экземпляр монитора инициализации.</span><span class="sxs-lookup"><span data-stu-id="27d20-132">A new instance of the initialization monitor was created successfully.</span></span>

<span data-ttu-id="27d20-133">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="27d20-133">E_OUTOFMEMORY</span></span>
> <span data-ttu-id="27d20-134">Не хватило памяти, чтобы обустраить новый объект.</span><span class="sxs-lookup"><span data-stu-id="27d20-134">There was not enough memory to crate a new object.</span></span>

## <a name="see-also"></a><span data-ttu-id="27d20-135">См. также</span><span class="sxs-lookup"><span data-stu-id="27d20-135">See also</span></span>
[<span data-ttu-id="27d20-136">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="27d20-136">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="27d20-137">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="27d20-137">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
