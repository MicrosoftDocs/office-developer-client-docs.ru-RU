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
# <a name="mapstoragescode"></a><span data-ttu-id="80606-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="80606-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="80606-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80606-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80606-105">Карты возвращаемого значения SCODE из объекта хранения OLE в тип HRESULT.</span><span class="sxs-lookup"><span data-stu-id="80606-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80606-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="80606-106">Header file:</span></span>  <br/> |<span data-ttu-id="80606-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="80606-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="80606-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="80606-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="80606-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="80606-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="80606-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="80606-110">Called by:</span></span>  <br/> |<span data-ttu-id="80606-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="80606-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="80606-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="80606-112">Parameters</span></span>

 <span data-ttu-id="80606-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="80606-113">_StgSCode_</span></span>
  
> <span data-ttu-id="80606-114">[in] Возвращаемая стоимость SCODE MAPI с объекта хранения OLE, который должен быть соизмелен со значением HRESULT.</span><span class="sxs-lookup"><span data-stu-id="80606-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80606-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80606-115">Return value</span></span>

<span data-ttu-id="80606-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="80606-116">S_OK</span></span> 
  
> <span data-ttu-id="80606-117">Вызов удался и возвращает ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="80606-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="80606-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="80606-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="80606-119">Функция не может найти совпадающие значения.</span><span class="sxs-lookup"><span data-stu-id="80606-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80606-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="80606-120">Remarks</span></span>

<span data-ttu-id="80606-121">MAPI предоставляет **функцию MapStorageSCode** для внутреннего использования компонентов MAPI, которые базируют реализацию сообщений на DLL сообщения.</span><span class="sxs-lookup"><span data-stu-id="80606-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="80606-122">Поскольку эти компоненты сами открывают хранилище OLE, они должны иметь возможность составить карту значений ошибок, возвращающихся из-за проблем с хранилищем OLE, к значению HRESULT.</span><span class="sxs-lookup"><span data-stu-id="80606-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="80606-123">Дополнительные сведения см. в [служба хранилища.](structured-storage-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="80606-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

