---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409694"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="e8656-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="e8656-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="e8656-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8656-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8656-105">Закрывает поставщика транспорта упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="e8656-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e8656-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8656-106">Parameters</span></span>

 <span data-ttu-id="e8656-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8656-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e8656-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="e8656-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8656-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8656-109">Return value</span></span>

<span data-ttu-id="e8656-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8656-110">S_OK</span></span> 
  
> <span data-ttu-id="e8656-111">Вызов успешно завершение работы поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e8656-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8656-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8656-112">Remarks</span></span>

<span data-ttu-id="e8656-113">Пулер MAPI вызывает метод **IXPProvider::Shutdown** перед освобождением объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e8656-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="e8656-114">Перед **вызовом shutdown** MAPI освобождает все объекты для работы поставщика.</span><span class="sxs-lookup"><span data-stu-id="e8656-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8656-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e8656-115">See also</span></span>



[<span data-ttu-id="e8656-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="e8656-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="e8656-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8656-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

