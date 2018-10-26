---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594294"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="04552-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="04552-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="04552-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04552-105">Возвращает сведения о, последнюю ошибку в объекте таблицы.</span><span class="sxs-lookup"><span data-stu-id="04552-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="04552-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04552-106">Parameters</span></span>

 <span data-ttu-id="04552-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="04552-107">_hResult_</span></span>
  
> <span data-ttu-id="04552-108">[in] Значение, возвращаемое методом, который не удалось.</span><span class="sxs-lookup"><span data-stu-id="04552-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="04552-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04552-109">_ulFlags_</span></span>
  
> <span data-ttu-id="04552-110">[in] Не используется, задайте значение нуль (0).</span><span class="sxs-lookup"><span data-stu-id="04552-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="04552-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="04552-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="04552-112">[out] Указывает на MAPI [MAPIERROR](mapierror.md) структура, содержащая сведения о последней ошибки, которые произошли для объекта в таблице.</span><span class="sxs-lookup"><span data-stu-id="04552-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="04552-113">См. также</span><span class="sxs-lookup"><span data-stu-id="04552-113">See also</span></span>



[<span data-ttu-id="04552-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04552-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="04552-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="04552-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="04552-116">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="04552-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

