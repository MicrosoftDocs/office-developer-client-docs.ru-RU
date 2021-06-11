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
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414979"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="8b8dd-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8b8dd-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="8b8dd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b8dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b8dd-105">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="8b8dd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8b8dd-106">Parameters</span></span>

 <span data-ttu-id="8b8dd-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="8b8dd-107">_hResult_</span></span>
  
>  <span data-ttu-id="8b8dd-108">[in] Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="8b8dd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b8dd-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="8b8dd-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="8b8dd-111">Это должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-111">This must be 0.</span></span> 
    
 <span data-ttu-id="8b8dd-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="8b8dd-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="8b8dd-113">[вышел] Указатель на **структуру MAPIERROR,** которая содержит расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="8b8dd-114">См. mapidefs.h для определения типа **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="8b8dd-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8b8dd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8b8dd-115">See also</span></span>



[<span data-ttu-id="8b8dd-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="8b8dd-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="8b8dd-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="8b8dd-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

