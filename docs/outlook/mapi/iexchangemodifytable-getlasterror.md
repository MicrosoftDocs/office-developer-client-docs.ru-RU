---
title: Иексчанжемодифитаблежетластеррор
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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424513"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="e4c10-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e4c10-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="e4c10-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4c10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4c10-105">Возвращает сведения о последней ошибке, произошедшей в объекте Table.</span><span class="sxs-lookup"><span data-stu-id="e4c10-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="e4c10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4c10-106">Parameters</span></span>

 <span data-ttu-id="e4c10-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="e4c10-107">_hResult_</span></span>
  
> <span data-ttu-id="e4c10-108">возврата Возвращаемое значение из метода, который завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e4c10-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="e4c10-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4c10-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e4c10-110">возврата Не используется, установите значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e4c10-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="e4c10-111">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="e4c10-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e4c10-112">вышли Указывает на структуру MAPI [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта Table.</span><span class="sxs-lookup"><span data-stu-id="e4c10-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4c10-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e4c10-113">See also</span></span>



[<span data-ttu-id="e4c10-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4c10-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="e4c10-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e4c10-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="e4c10-116">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e4c10-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

