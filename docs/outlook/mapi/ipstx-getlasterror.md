---
title: Ипстксжетластеррор
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315101"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="6ac08-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6ac08-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="6ac08-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ac08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ac08-105">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="6ac08-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="6ac08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ac08-106">Parameters</span></span>

 <span data-ttu-id="6ac08-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="6ac08-107">_hResult_</span></span>
  
>  <span data-ttu-id="6ac08-108">возврата Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6ac08-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="6ac08-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ac08-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="6ac08-110">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="6ac08-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="6ac08-111">Значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6ac08-111">This must be 0.</span></span> 
    
 <span data-ttu-id="6ac08-112">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="6ac08-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="6ac08-113">вышли Указатель на структуру **мапиеррор** , которая содержит расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6ac08-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="6ac08-114">Определение типа **лпмапиеррор**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="6ac08-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6ac08-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6ac08-115">See also</span></span>



[<span data-ttu-id="6ac08-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="6ac08-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="6ac08-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="6ac08-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

