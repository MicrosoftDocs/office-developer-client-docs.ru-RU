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
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592593"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="b3ba1-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b3ba1-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="b3ba1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3ba1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3ba1-105">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="b3ba1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3ba1-106">Parameters</span></span>

 <span data-ttu-id="b3ba1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b3ba1-107">_hResult_</span></span>
  
>  <span data-ttu-id="b3ba1-108">[in] Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="b3ba1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3ba1-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="b3ba1-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="b3ba1-111">Это должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-111">This must be 0.</span></span> 
    
 <span data-ttu-id="b3ba1-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b3ba1-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="b3ba1-113">[out] Указатель на структуру **MAPIERROR** , который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="b3ba1-114">В разделе mapidefs.h для определения типа **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b3ba1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b3ba1-115">See also</span></span>



[<span data-ttu-id="b3ba1-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="b3ba1-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="b3ba1-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="b3ba1-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

