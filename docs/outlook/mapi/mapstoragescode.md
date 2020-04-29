---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416526"
---
# <a name="mapstoragescode"></a><span data-ttu-id="62128-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="62128-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="62128-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62128-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62128-105">Сопоставляет возвращаемое значение SCODE из объекта OLE Storage с типом HRESULT.</span><span class="sxs-lookup"><span data-stu-id="62128-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62128-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="62128-106">Header file:</span></span>  <br/> |<span data-ttu-id="62128-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="62128-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="62128-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="62128-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="62128-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="62128-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="62128-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="62128-110">Called by:</span></span>  <br/> |<span data-ttu-id="62128-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="62128-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="62128-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="62128-112">Parameters</span></span>

 <span data-ttu-id="62128-113">_стгскоде_</span><span class="sxs-lookup"><span data-stu-id="62128-113">_StgSCode_</span></span>
  
> <span data-ttu-id="62128-114">возврата SCODE MAPI возвращает значение из объекта OLE Storage, которое должно быть сопоставлено со значением HRESULT.</span><span class="sxs-lookup"><span data-stu-id="62128-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62128-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62128-115">Return value</span></span>

<span data-ttu-id="62128-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="62128-116">S_OK</span></span> 
  
> <span data-ttu-id="62128-117">Вызов выполнен успешно и возвращено ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="62128-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="62128-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="62128-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="62128-119">Функции не удается найти совпадающее значение.</span><span class="sxs-lookup"><span data-stu-id="62128-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62128-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="62128-120">Remarks</span></span>

<span data-ttu-id="62128-121">MAPI предоставляет функцию **мапсторажескоде** для внутреннего использования компонентами MAPI, которые основаны на их реализациях сообщений в DLL сообщений.</span><span class="sxs-lookup"><span data-stu-id="62128-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="62128-122">Так как эти компоненты самостоятельно открывают хранилище OLE, они должны иметь возможность сопоставлять значения ошибок, возвращаемые для проблем с хранилищем OLE, со значением HRESULT.</span><span class="sxs-lookup"><span data-stu-id="62128-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="62128-123">Более подробную информацию можно узнать в разделе [структурированное хранилище](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="62128-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

