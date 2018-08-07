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
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809924"
---
# <a name="mapstoragescode"></a><span data-ttu-id="b7d37-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="b7d37-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="b7d37-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7d37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7d37-105">Карты SCODE возвращать значение из объекта хранилища OLE к типу HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b7d37-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7d37-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b7d37-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7d37-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="b7d37-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="b7d37-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b7d37-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7d37-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7d37-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7d37-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b7d37-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7d37-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b7d37-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="b7d37-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7d37-112">Parameters</span></span>

 <span data-ttu-id="b7d37-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="b7d37-113">_StgSCode_</span></span>
  
> <span data-ttu-id="b7d37-114">[in] Возвращаемое значение MAPI SCODE из объекта хранения для сопоставления с значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b7d37-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7d37-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b7d37-115">Return value</span></span>

<span data-ttu-id="b7d37-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b7d37-116">S_OK</span></span> 
  
> <span data-ttu-id="b7d37-117">Вызов успешно и возвращается ожидаемым значением.</span><span class="sxs-lookup"><span data-stu-id="b7d37-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="b7d37-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b7d37-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b7d37-119">Невозможно найти соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="b7d37-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7d37-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7d37-120">Remarks</span></span>

<span data-ttu-id="b7d37-121">MAPI предоставляет функцию **MapStorageSCode** для внутреннего использования компоненты MAPI, базовый реализаций сообщений в окне сообщения DLL-Библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b7d37-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="b7d37-122">Так как эти компоненты хранилище OLE сами, они должны иметь возможность сопоставления значений ошибок, возвращаемых для решения проблем с использованием хранилища OLE значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b7d37-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="b7d37-123">Для получения дополнительных сведений см [Структурированного хранилища](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b7d37-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

