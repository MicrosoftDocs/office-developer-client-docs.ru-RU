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
# <a name="ixpprovidershutdown"></a><span data-ttu-id="8db60-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="8db60-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="8db60-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8db60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8db60-105">Упорядоченно закрывает поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8db60-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8db60-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8db60-106">Parameters</span></span>

 <span data-ttu-id="8db60-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8db60-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8db60-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8db60-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8db60-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8db60-109">Return value</span></span>

<span data-ttu-id="8db60-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8db60-110">S_OK</span></span> 
  
> <span data-ttu-id="8db60-111">Вызову удалось отключить поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8db60-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8db60-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8db60-112">Remarks</span></span>

<span data-ttu-id="8db60-113">Spooler MAPI вызывает **метод IXPProvider::Shutdown** незадолго до выпуска объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8db60-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="8db60-114">Перед **вызовом shutdown** MAPI выпускает все объекты с логотипом для поставщика.</span><span class="sxs-lookup"><span data-stu-id="8db60-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8db60-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8db60-115">See also</span></span>



[<span data-ttu-id="8db60-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="8db60-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="8db60-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8db60-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

