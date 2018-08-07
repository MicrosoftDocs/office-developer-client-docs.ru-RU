---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809576"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="7cc4d-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7cc4d-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="7cc4d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cc4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cc4d-105">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="7cc4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cc4d-106">Parameters</span></span>

 <span data-ttu-id="7cc4d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="7cc4d-107">_hResult_</span></span>
  
>  <span data-ttu-id="7cc4d-108">[in] Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="7cc4d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cc4d-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="7cc4d-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="7cc4d-111">Это должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-111">This must be 0.</span></span> 
    
 <span data-ttu-id="7cc4d-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7cc4d-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="7cc4d-113">[out] Указатель на структуру **MAPIERROR** , который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="7cc4d-114">В разделе mapidefs.h для определения типа **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7cc4d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7cc4d-115">See also</span></span>



[<span data-ttu-id="7cc4d-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="7cc4d-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="7cc4d-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="7cc4d-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

