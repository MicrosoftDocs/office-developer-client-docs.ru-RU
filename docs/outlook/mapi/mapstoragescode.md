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
# <a name="mapstoragescode"></a><span data-ttu-id="db6bb-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="db6bb-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="db6bb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db6bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db6bb-105">Сопоирует возвращаемого значения SCODE из объекта хранилища OLE с типом HRESULT.</span><span class="sxs-lookup"><span data-stu-id="db6bb-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db6bb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="db6bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="db6bb-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="db6bb-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="db6bb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="db6bb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="db6bb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="db6bb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="db6bb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="db6bb-110">Called by:</span></span>  <br/> |<span data-ttu-id="db6bb-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="db6bb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="db6bb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="db6bb-112">Parameters</span></span>

 <span data-ttu-id="db6bb-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="db6bb-113">_StgSCode_</span></span>
  
> <span data-ttu-id="db6bb-114">[in] MapI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span><span class="sxs-lookup"><span data-stu-id="db6bb-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db6bb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db6bb-115">Return value</span></span>

<span data-ttu-id="db6bb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="db6bb-116">S_OK</span></span> 
  
> <span data-ttu-id="db6bb-117">Вызов был успешным и возвращен ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="db6bb-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="db6bb-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="db6bb-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="db6bb-119">Функция не может найти совпадающие значения.</span><span class="sxs-lookup"><span data-stu-id="db6bb-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db6bb-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="db6bb-120">Remarks</span></span>

<span data-ttu-id="db6bb-121">MAPI предоставляет **функцию MapStorageSCode** для внутреннего использования компонентов MAPI, которые базируют свои реализации сообщений на DLL сообщения.</span><span class="sxs-lookup"><span data-stu-id="db6bb-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="db6bb-122">Так как эти компоненты открывают хранилище OLE самостоятельно, они должны иметь возможность соедооставить значения ошибок, возвращенные при проблемах с хранилищем OLE, со значением HRESULT.</span><span class="sxs-lookup"><span data-stu-id="db6bb-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="db6bb-123">Дополнительные сведения см. в [подстройки "Структурированное хранилище".](structured-storage-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="db6bb-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

